<template>
  <div id="c1"></div>
</template>

<script>
import G2 from '@antv/g2'

export default {
  mounted () {
    const data = [
      { step: 'Seeing it first time', framework: 'Vue.js', value: 0 },
      { step: 'Seeing it first time', framework: 'React', value: 0 },
      { step: 'Seeing it first time', framework: 'Angular', value: 0 },
      { step: 'First steps', framework: 'Vue.js', value: 2 },
      { step: 'First steps', framework: 'React', value: 4 },
      { step: 'First steps', framework: 'Angular', value: 5 },
      { step: 'Diving deeper', framework: 'Vue.js', value: 5 },
      { step: 'Diving deeper', framework: 'React', value: 7 },
      { step: 'Diving deeper', framework: 'Angular', value: 9 },
      { step: 'Building apps', framework: 'Vue.js', value: 6 },
      { step: 'Building apps', framework: 'React', value: 9 },
      { step: 'Building apps', framework: 'Angular', value: 10 },
      { step: 'Deployment', framework: 'Vue.js', value: 7 },
      { step: 'Deployment', framework: 'React', value: 10 },
      { step: 'Deployment', framework: 'Angular', value: 12 }
    ]
    const chart = new G2.Chart({
      container: 'c1',
      padding: ['auto', 75, 'auto', 75],
      height: 425,
      width: 1000
    })
    chart.scale('value', {
      min: 0
    })
    chart.scale('step', {
      range: [0, 1]
    })
    chart.axis('value', {
      label: null
    })
    chart.axis('step', {
      label: {
        textStyle: {
          fontSize: '18'
        }
      }
    })
    chart.guide().dataMarker({
      position: ['First steps', 2],
      content: 'ES5, control DOM',
      style: {
        text: {
          fontSize: '16'
        }
      }
    }).dataMarker({
      position: ['First steps', 4],
      content: 'ES6, JSX',
      style: {
        text: {
          fontSize: '16'
        }
      }
    }).dataMarker({
      position: ['First steps', 5],
      content: 'TypeScript, workflow',
      style: {
        text: {
          fontSize: '16'
        }
      }
    }).dataMarker({
      position: ['Diving deeper', 5],
      content: 'ES6, .vue files',
      style: {
        text: {
          fontSize: '16'
        }
      }
    }).dataMarker({
      position: ['Diving deeper', 7],
      content: 'Everything is JavaScript',
      style: {
        text: {
          fontSize: '16'
        }
      }
    }).dataMarker({
      position: ['Diving deeper', 9],
      content: 'Components, modules, syntax',
      style: {
        text: {
          fontSize: '16'
        }
      }
    }).dataMarker({
      position: ['Building apps', 6],
      content: 'Component orchestration, communication, routing',
      style: {
        text: {
          fontSize: '16'
        }
      }
    }).dataMarker({
      position: ['Building apps', 9],
      content: 'State management',
      style: {
        text: {
          fontSize: '16'
        }
      }
    }).dataMarker({
      position: ['Building apps', 10],
      content: 'Dependency injection, putting it all together',
      style: {
        text: {
          fontSize: '16'
        }
      }
    })
    chart.legend('framework', {
      textStyle: {
        fontSize: '16'
      }
    })
    chart.tooltip(false)
    chart.source(data)
    chart.line().position('step*value').color('framework')
    chart.render()
  }
}
</script>
