<template>
  <svg :width="width" :height="height" ref="svg">
    <g ref="chart">
      <g v-for="path in paths" :key="path.id">
        <path :d="path" stroke="black" strokeWidth="10" fill="none" />
      </g>
    </g>
    <g ref="axis"></g>
  </svg>
</template>

<script>
import * as d3 from 'd3'
export default {
  name: 'LineChart',
  props: ['chartData'],
  data () {
    return {
      paths: [],
      width: 1300,
      height: 470,
      margin: {
        top: 5,
        right: 10,
        bottom: 5,
        left: 10
      }
    }
  },
  mounted () {
    this.redraw()
  },
  methods: {
    redraw () {
      // Transform to dates
      this.chartData.forEach(d => {
        d.data[0].x = new Date(d.data[0].x)
        d.data[1].x = new Date(d.data[1].x)
      })

      // Create the Scale we will use for the x Axis
      const xScale = d3.scaleTime()
        .domain([
          d3.min(this.chartData, function (d) { return d.data[0].x }),
          d3.max(this.chartData, function (d) { return d.data[1].x })
        ])
        .nice(d3.timeWeek)
        .range([0, this.width])

      // Create the Scale we will use for the y-Axis
      const yScale = d3.scaleLinear()
        .domain([0, this.getLevels(this.chartData)])
        .range([this.height - 30, 30])

      // Path generator
      const path = d3
        .line()
        .x(d => xScale(d.x))
        .y(d => yScale(d.y))

      // Get Path string for each activity
      this.paths = this.chartData.map(act => path(act.data))
    },
    // Functions to get the maximun number of levels of the locations
    getLevels (activities) {
      let ymaxStart = d3.max(activities, function (d) { return d.data[0].y })
      let ymaxEnd = d3.max(activities, function (d) { return d.data[1].y })
      if (ymaxStart > ymaxEnd) {
        return ymaxStart
      }
      return ymaxEnd
    }
  },
  watch: {
    chartData: function () {
      this.redraw()
    }
  }
}
</script>
