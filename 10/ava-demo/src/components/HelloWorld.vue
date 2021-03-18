<template>
  <div id="container"></div>
</template>

<script>
import { autoChart } from "@antv/chart-advisor";
// data:[
//   {field1: "2021-01", field2: 100 },
//   {field1: "2021-02", field2: 300 },
//   {field1: "2021-03", field2: 500 },
// ]
// data: [
//         { field1: "apple", field2: 100 },
//         { field1: "banana", field2: 300 },
//         { field1: "pear", field2: 800 },
//       ],
export default {
  name: "HelloWorld",
  data: function () {
    return {
      data: [
        { field1: "2021-01", field2: 100 },
        { field1: "2021-02", field2: 300 },
        { field1: "2021-03", field2: 800 },
      ],
    };
  },
  mounted() {
    const container = document.getElementById("container");
    autoChart(container, this.data, { toolbar: true, development: true });
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#container {
  width: 600px;
  height: 600px;
}
</style>
