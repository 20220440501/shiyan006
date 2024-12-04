<!-- src/components/BarChart.vue -->
<template>
  <div ref="chart" class="chart-container"></div>
</template>

<script>
import { ref, onMounted } from 'vue';
import * as echarts from 'echarts';

export default {
  setup() {
    const chart = ref(null);

    onMounted(() => {
      // 初始化 ECharts 实例
      const myChart = echarts.init(chart.value);

      // 配置图表选项
      const option = {
        title: {
          text: '示例柱状图'
        },
        tooltip: {},
        xAxis: {
          data: ['衬衫', '羊毛衫', '雪纺衫', '裤子', '高跟鞋', '袜子']
        },
        yAxis: {},
        series: [
          {
            name: '销量',
            type: 'bar',
            data: [5, 20, 36, 10, 10, 20]
          }
        ]
      };

      // 使用配置项显示图表
      myChart.setOption(option);
    });

    return {
      chart
    };
  }
};
</script>

<style>
.chart-container {
  width: 100%;
  height: 400px;
}
</style>