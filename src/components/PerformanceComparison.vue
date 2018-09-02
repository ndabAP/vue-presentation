<template>
  <div id="c1"></div>
</template>

<script>
import G2 from '@antv/g2'

export default {
  mounted () {
    const data = [
      { x: 'After 1,000 rows', framework: 'Vue.js', y: 7.2 },
      { x: 'Clicking create 1.000 rows', framework: 'Vue.js', y: 7.3 },
      { x: 'Creating and clearing 1.000 rows', framework: 'Vue.js', y: 3.8 },
      { x: 'After 1,000 rows', framework: 'React', y: 7.6 },
      { x: 'Clicking create 1.000 rows', framework: 'React', y: 9 },
      { x: 'Creating and clearing 1.000 rows', framework: 'React', y: 4.7 },
      { x: 'After 1,000 rows', framework: 'Angular', y: 10.5 },
      { x: 'Clicking create 1.000 rows', framework: 'Angular', y: 10.8 },
      { x: 'Creating and clearing 1.000 rows', framework: 'Angular', y: 7.1 }
    ]
    const chart = new G2.Chart({
      container: 'c1',
      height: 425,
      width: 1000
    })
    chart.scale('y', {
      min: 0
    })
    chart.axis('x', {
      label: {
        textStyle: {
          fontSize: '18'
        }
      }
    })
    chart.axis('y', {
      label: null
    })
    chart.tooltip(false)
    chart.source(data)
    chart.legend('framework', {
      textStyle: {
        fontSize: '16'
      }
    })
    chart.interval().position('x*y').color('framework').adjust([
      {
        type: 'dodge',
        marginRatio: 0.075
      }])
    chart.render()
  }
}
</script>
