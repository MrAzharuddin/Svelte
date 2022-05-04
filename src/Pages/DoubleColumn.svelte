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
            height: 'auto',
            stacked: true,
            toolbar:{
              show:false
            }
        },
        colors: ['#04d9ff', '#baeb17'],
        plotOptions: {
          bar: {
            horizontal: false,
            barHeight: '80%',
            columnWidth:'60%',
          },
        },
        dataLabels: {
          enabled: false,
        },
        fill:{
          type:'gradient',
          opacity:[0.85,0.25,1],
          gradient: {
            type:'vertical',
            inverseColors:false,
            shadeIntensity: 0.4,
            opacityFrom: 0.8,
            opacityTo: 1,
            stops: [0, 90, 100]
          }
        }, 
        grid: {
          show:false,
          //       xaxis: {
          //     lines: {
          //         show: true
          //     }
          // },   
          // yaxis: {
          //     lines: {
          //         show: true
          //     }
          // },  
          padding:{
            top:0,
            left:0,
            right:0,
            bottom:0

          }
        },
        xaxis:{
          axisBorder: {
              show: false,
              color: '#04d9ff',
              offsetX: 0,
              offsetY: -510,
          },
          // tooltip: {
          //   enabled: false,
          //   offsetX: 0,
          // },
          labels:{
            // show:false,
            formatter: function (value){
              return ""
            }
          }
        },
        yaxis:{
          // // axisBorder:{
          // //   show:'true',
          // //   color:'#04d9ff'
          // // },
          // showForNullSeries: false,
          // seriesName: undefined,
          labels:{
            // show:false,
            formatter: function (value){
              return ""
            }
          }
        },
        legend:{
          show:false
        }
  };

  let chart1;

  function renderCharts1(node) {
      chart1 = new ApexCharts(node, options);
      chart1.render();
  }


// options help
// series: for data
// chart: for which type and all - toolbar helps for navbar way, disable to hide options


</script>

<main>
 <div use:renderCharts1 class="rounded-lg max-w-[33.33%] border-1 border-black" />
</main>