<template>
  <div>
    <line-chart :chartData='chartData'/>
  </div>
</template>

<script>
// @ is an alias to /src
import LineChart from '../components/LineChart.vue'

export default {
  name: 'home',
  data () {
    return {
      chartData: [
        { 'task': 'Pilotaje',
          'data': [{ 'x': '2015-09-29', 'y': 0 },
            { 'x': '2015-11-07', 'y': 9 }]
        },
        { 'task': 'Cimentación Superficial',
          'data': [{ 'x': '2015-11-10', 'y': 0 },
            { 'x': '2015-12-19', 'y': 9 }]
        },
        { 'task': 'Estructura',
          'data': [{ 'x': '2015-12-19', 'y': 0 },
            { 'x': '2016-05-14', 'y': 9 }]
        },
        { 'task': 'Mamposteria',
          'data': [{ 'x': '2016-03-07', 'y': 0 },
            { 'x': '2016-07-15', 'y': 9 }]
        },
        { 'task': 'Friso Interno',
          'data': [{ 'x': '2016-04-05', 'y': 0 },
            { 'x': '2016-08-04', 'y': 9 }]
        },
        { 'task': 'Estuco y 1ra mano pintura',
          'data': [{ 'x': '2016-04-19', 'y': 0 },
            { 'x': '2016-08-11', 'y': 9 }]
        },
        { 'task': 'Prolong. electricas y sanitarias',
          'data': [{ 'x': '2016-03-28', 'y': 0 },
            { 'x': '2016-07-26', 'y': 9 }]
        },
        { 'task': 'Friso Fachada',
          'data': [{ 'x': '2016-07-29', 'y': 9 },
            { 'x': '2016-10-19', 'y': 0 }]
        },
        { 'task': 'Mortero',
          'data': [{ 'x': '2016-04-27', 'y': 0 },
            { 'x': '2016-08-18', 'y': 9 }]
        },
        { 'task': 'Puertas Provisionales',
          'data': [{ 'x': '2016-09-14', 'y': 9 },
            { 'x': '2016-12-10', 'y': 0 }]
        },
        { 'task': 'Pruebas hidraulicas y red refrigeración',
          'data': [{ 'x': '2016-08-18', 'y': 9 },
            { 'x': '2016-11-11', 'y': 0 }]
        },
        { 'task': 'Piso',
          'data': [{ 'x': '2016-08-25', 'y': 9 },
            { 'x': '2016-11-23', 'y': 0 }]
        },
        { 'task': 'Pruebas sanitarias',
          'data': [{ 'x': '2016-09-06', 'y': 9 },
            { 'x': '2016-12-06', 'y': 0 }]
        },
        { 'task': 'Estructura Drywall',
          'data': [{ 'x': '2016-09-21', 'y': 9 },
            { 'x': '2016-12-19', 'y': 0 }]
        },
        { 'task': 'Laminado Drywall',
          'data': [{ 'x': '2016-10-14', 'y': 9 },
            { 'x': '2017-01-12', 'y': 0 }]
        },
        { 'task': 'Cableado',
          'data': [{ 'x': '2016-10-05', 'y': 9 },
            { 'x': '2016-12-31', 'y': 0 }]
        },
        { 'task': 'Carpinteria Metálica',
          'data': [{ 'x': '2016-09-02', 'y': 9 },
            { 'x': '2016-11-29', 'y': 0 }]
        },
        { 'task': 'Carpinteria Aluminio',
          'data': [{ 'x': '2016-09-28', 'y': 9 },
            { 'x': '2016-12-26', 'y': 0 }]
        },
        { 'task': '2da Mano Pintura',
          'data': [{ 'x': '2016-10-27', 'y': 9 },
            { 'x': '2017-01-23', 'y': 0 }]
        },
        { 'task': 'Primera Lavada',
          'data': [{ 'x': '2016-11-08', 'y': 9 },
            { 'x': '2017-01-30', 'y': 0 }]
        },
        { 'task': 'Carpinteria Madera-Mesones',
          'data': [{ 'x': '2016-11-19', 'y': 9 },
            { 'x': '2017-02-09', 'y': 0 }]
        },
        { 'task': '3ra mano pintura',
          'data': [{ 'x': '2016-12-10', 'y': 9 },
            { 'x': '2017-02-21', 'y': 0 }]
        },
        { 'task': 'Aparatos elec-sanit',
          'data': [{ 'x': '2016-11-30', 'y': 9 },
            { 'x': '2017-02-13', 'y': 0 }]
        },
        { 'task': 'Segunda Lavada',
          'data': [{ 'x': '2016-12-21', 'y': 9 },
            { 'x': '2017-03-03', 'y': 0 }]
        },
        { 'task': 'Detalle y terminación',
          'data': [{ 'x': '2016-12-28', 'y': 9 },
            { 'x': '2017-03-09', 'y': 0 }]
        },
        { 'task': 'Tercera Lavada',
          'data': [{ 'x': '2017-01-03', 'y': 9 },
            { 'x': '2017-03-16', 'y': 0 }]
        },
        { 'task': 'Fin Proyecto',
          'data': [{ 'x': '2017-03-15', 'y': 0 },
            { 'x': '2017-03-15', 'y': 9 }] }
      ]
    }
  },
  components: {
    LineChart
  }
}
</script>
