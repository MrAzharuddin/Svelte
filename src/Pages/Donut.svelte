<script>
import ApexCharts from 'apexcharts'
  var options = {
          series: [44, 55, 41, 17, 15],
          chart: {
          type: 'donut',
        },
        responsive: [{
          breakpoint: 480,
          options: {
            chart: {
              width: '300px'
            },
            legend: {
              position: 'bottom'
            }
          }
        }]
    };

  let chart1;

function renderCharts1(node) {
    chart1 = new ApexCharts(node, options);
    chart1.render();
}
</script>

<main class='flex w-full overflow-scroll scrollbar'>
 <div use:renderCharts1 class="z-[-1] my-2 bg-gray-100 p-2 rounded-lg shadow-inner" />
 <div use:renderCharts1 class="z-[-1] my-2 bg-gray-100 p-2 rounded-lg shadow-inner" />
</main>