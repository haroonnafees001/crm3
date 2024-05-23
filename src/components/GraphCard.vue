<template>
  <div class="container">
    <div class="col-6">
      <div class="card">
        <div class="card-header">
          <div class="card-title">
            <h1 class="title">Recent Workflow</h1>
          </div>
        </div>
        <div class="card-body">
          <pie-chart></pie-chart>
        </div>
        <div class="card-footer text-green font-size-12">
          <span class="mr-5 material-symbols-outlined ">trending_up</span>
          <span class="mr-5">12 %</span>
        </div>
      </div>
    </div>


    <div class="col-6">
      <div class="card">
        <div class="card-header">
          <div class="card-title">
            <h1 class="title">Recent Marketing</h1>
          </div>
        </div>
        <div class="card-body">
          <pie-chart></pie-chart>
        </div>
        <div class="card-footer text-green font-size-12">
          <span class="mr-5 material-symbols-outlined ">trending_up</span>
          <span class="mr-5"> 21 %</span>
        </div>
      </div>
    </div>


  </div>
</template>

<script setup>
import PieChart from "./PieChart.vue"
</script>

