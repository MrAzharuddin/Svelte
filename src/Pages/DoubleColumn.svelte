<script>
import ApexCharts from 'apexcharts'
  var options = {
          series: [{
          name: 'Males',
          data: [1.2, 1.80, 3.2, 2.6, 3.9,0.8, 2.4 ]
        },
        {
          name: 'Females',
          data: [-2.8, -0.85, -4.06, -1.18, -2.4, -3.6, -2.2]
        }
        ],
          chart: {
          type: 'bar',
          height: 440,
          stacked: true
        },
        colors: ['#04d9ff', '#baeb17'],
        plotOptions: {
          bar: {
            horizontal: false,
            barHeight: '80%',
          },
        },
        dataLabels: {
          enabled: false,
          // style: {
          //   colors: ['#F44336', '#E91E63', '#9C27B0']
          // }
        },
        stroke: {
          width: 1,
          colors: ["#fff"]
        },
        markers: {
          colors: ['#F44336', '#E91E63', '#9C27B0']
        },
        fill:{
          type:'gradient',
          // opacity:[0.85,0.25,1],
          gradient: {
          type:'vertical',
          inverseColors:'true',
          shadeIntensity: 0.4,
          opacityFrom: 0.8,
          opacityTo: 1,
          stops: [0, 90, 100]
        }
        },
        
        grid: {
          // row: {
          //   colors: ['#F44336', '#E91E63', '#9C27B0']
          // },
          // column: {
          //   colors: ['#F44336', '#E91E63', '#9C27B0']
          // },
          show:false,
          // tooltip: {
          //   shared: false,
          //   x: {
          //     formatter: function (val) {
          //       return val
          //     }
          //   },
          //   y: {
          //     formatter: function (val) {
          //       return Math.abs(val) + "%"
          //     }
          //   }
          // },
          title: {
            text: 'Mauritius population pyramid 2011'
          },
          // xaxis: {
          //   categories: ['85+', '80-84', '75-79', '70-74', '65-69', '60-64', '55-59', '50-54',
          //     '45-49', '40-44', '35-39', '30-34', '25-29', '20-24', '15-19', '10-14', '5-9',
          //     '0-4'
          //   ],
          //   title: {
          //     text: 'Percent'
          //   },
          //   labels: {
          //     formatter: function (val) {
          //       return Math.abs(Math.round(val)) + "%"
          //     }
          //   }
          // },
  };

  let chart1;

function renderCharts1(node) {
    chart1 = new ApexCharts(node, options);
    chart1.render();
}
</script>

<main>
 <div use:renderCharts1 class="z-[-1] my-2 bg-gray-100 p-2 rounded-lg shadow-inner" />
</main>