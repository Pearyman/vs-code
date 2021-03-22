<template>
  <div id="container"></div>
</template>

<script>
import { autoChart } from "@antv/chart-advisor";
// data: [
//         { field1: "apple", field2: 100 },
//         { field1: "banana", field2: 300 },
//         { field1: "pear", field2: 800 },
//       ],
export default {
  name: "HelloWorld",
  data() {
    return {
      data: [
        { name: "London", 月份: "Jan.", 月均降雨量: 18.9 },
        { name: "London", 月份: "Feb.", 月均降雨量: 28.8 },
        { name: "London", 月份: "Mar.", 月均降雨量: 39.3 },
        { name: "London", 月份: "Apr.", 月均降雨量: 81.4 },
        { name: "London", 月份: "May", 月均降雨量: 47 },
        { name: "London", 月份: "Jun.", 月均降雨量: 20.3 },
        { name: "London", 月份: "Jul.", 月均降雨量: 24 },
        { name: "London", 月份: "Aug.", 月均降雨量: 35.6 },
        { name: "Berlin", 月份: "Jan.", 月均降雨量: 12.4 },
        { name: "Berlin", 月份: "Feb.", 月均降雨量: 23.2 },
        { name: "Berlin", 月份: "Mar.", 月均降雨量: 34.5 },
        { name: "Berlin", 月份: "Apr.", 月均降雨量: 99.7 },
        { name: "Berlin", 月份: "May", 月均降雨量: 52.6 },
        { name: "Berlin", 月份: "Jun.", 月均降雨量: 35.5 },
        { name: "Berlin", 月份: "Jul.", 月均降雨量: 37.4 },
        { name: "Berlin", 月份: "Aug.", 月均降雨量: 42.4 }
      ]
    };
  },
  mounted() {
    const container = document.getElementById("container");
    autoChart(container, this.data, {
      toolbar: true,
      development: true,
      title: "我们来测试一个图表例子",
      description: "是的，这是一个名副其实的副标题",
      config: {
        configs: {
          xAxis: { visible: true },
          columnWidthRatio: 1,
          tooltip: { visible: true },
          xField: "月份",
          yField: "月均降雨量",
          colorField: "name",
          seriesField: "name",
          isGroup: true,
          autoFit: true,
          legend: false,
          label: { visible: true }
        },
        type: "Column"
      }
    });
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#container {
  width: 600px;
  height: 600px;
}
</style>
