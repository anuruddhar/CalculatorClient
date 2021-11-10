<template>
  <div class="card text-center m-3">
    <div class="card-body">Add: 5, 2, 3, 5, 3 = {{ add }}</div>
    <div class="card-body">Subtract: 25, 2, 3, 5, 3 = {{ subtract }}</div>
    <div class="card-body">Multiply: 2, 4, 3, 5 = {{ multiply }}</div>
     <div class="card-body">Divide: 16, 4 = {{ divide }}</div>
      <div class="card-body">SplitEq: 120, 4 = {{ splitEq }}</div>
       <div class="card-body">SplitNum: 140, 45, 35, 20 = {{ splitNum }}</div>
  </div>
</template>

<script>
import axios from "axios";

export default {
  name: "get-request",
  data() {
    return {
      add: null,
      subtract: null,
      multiply: null,
      divide: null,
      splitEq: null,
      splitNum: null,
    };
  },
  created() {
    axios
      .get(
        "http://localhost:51844/api/calculator/add?param1=5&param2=2&param3=3&param4=5&param5=3"
      )
      .then((response) => (this.add = response.data));

    axios
      .get(
        "http://localhost:51844/api/calculator/subtract?param1=25&param2=2&param3=3&param4=5&param5=3"
      )
      .then((response) => (this.subtract = response.data));

    axios
      .get(
        "http://localhost:51844/api/calculator/multiply?param1=2&param2=4&param3=3&param4=5"
      )
      .then((response) => (this.multiply = response.data));

    axios
      .get(
        "http://localhost:51844/api/calculator/divide/16/4"
      )
      .then((response) => (this.divide = response.data));

    axios
      .get(
        "http://localhost:51844/api/calculator/splitEq/120/4"
      )
      .then((response) => (this.splitEq = response.data));

    axios
      .get(
        "http://localhost:51844/api/calculator/splitNum?param1=140&param2=45&param3=35&param4=20"
      )
      .then((response) => (this.splitNum = response.data));
  },
};
</script>
