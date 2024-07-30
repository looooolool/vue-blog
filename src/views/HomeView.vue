<script>
import {ref} from 'vue'

import * as echarts from "echarts";

export default {
  data() {
    return {
      myChart: {},
      xData: [], //横坐标
      yData: [100,98,91,81,70,57,43,31,20,11,4,0,5,14,24, 34, 45, 59, 72, 85, 94,99,], //体力数据23
      taskData: [100, 99, 94, 86, 78, 68, 59, 50, 41, 32, 23, 15, 9, 3, 0, 5, 14, 23, 32, 41, 50, 59, 68, 77, 86, 94, 99], //情绪数据28
      taskData111: [ 100, 95, 88, 80, 72, 64, 56, 49, 42, 36, 29, 22, 14, 6,0, 3, 6, 9, 12, 16, 20, 25, 30, 36, 42, 49, 56, 64, 72, 80, 88, 95,  ], //智力数据33
      myChartStyle: { float: "left", width: "100%", height: "400px" } //图表样式
      
    };
  },
  mounted() {
    this.initEcharts();
  },
  methods: {
    addNumberx(){
      var month=30;
      for(let i=1;i<=month;i++){
        this.xData.push(i);
        console.log(this.xData);
      }
    },
    initEcharts() {
      const option = {
        xAxis: {
          data: this.xData
        },
        legend: { // 图例
          data: ["体力", "情绪","智力"],
          bottom: "0%"
        },
        yAxis: {},
        series: [
          {
            name: "体力",
            data: this.yData,
            type: "line", // 类型设置为折线图
            smooth: true, //平滑曲线
            label: {
              show: true,
              position: "top",
              textStyle: {
                fontSize: 16
              }
            }
          },
          {
            name: "情绪",
            data: this.taskData,
            type: "line", // 类型设置为折线图
            smooth: true, //平滑曲线
            label: {
              show: true,
              position: "bottom",
              textStyle: {
                fontSize: 16
              }
            }
          },
          {
            name: "智力",
            data: this.taskData111,
            type: "line", // 类型设置为折线图
            smooth: true, //平滑曲线
            label: {
              show: true,
              position: "bottom",
              textStyle: {
                fontSize: 16
              }
            }
          },
        ]
      };
      this.myChart = echarts.init(document.getElementById("mychart"));
      this.myChart.setOption(option);
      //随着屏幕大小调节图表
      // window.addEventListener("resize", () => {
      //   this.myChart.resize();
      // });
    }
  }
};

</script>

<template>
  <div class="about">
    <!-- <h1>人体生物节律表</h1> -->
    <div class="echart" id="mychart" :style="myChartStyle"></div>
  <!-- 23 体力，28 情绪，33智力 -->
  {{ addNumberx() }}
  </div>
</template>
