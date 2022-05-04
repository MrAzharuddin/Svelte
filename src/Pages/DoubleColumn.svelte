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
        },
        stroke: {
          width: 1,
          colors: ["#fff"]
        },
        fill:{
          type:'gradient',
          opacity:[0.85,0.25,1],
          gradient: {
          type:'vertical',
          inverseColors:true,
          shadeIntensity: 0.4,
          opacityFrom: 0.8,
          opacityTo: 1,
          stops: [0, 90, 100]
        }
        }, 
        grid: {
          show:false,
        }
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