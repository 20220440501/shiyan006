<!-- src/App.vue -->
<template>
  <div id="app">
    <el-container>
      <el-header>
        <h2>Vue 项目示例</h2>
      </el-header>
      <el-main>
        <el-row :gutter="20">
          <el-col :span="12">
            <MyForm />
          </el-col>
          <el-col :span="12">
            <BarChart />
          </el-col>
        </el-row>
      </el-main>
    </el-container>
  </div>
</template>

<script>
import MyForm from './components/MyForm.vue';
import BarChart from './components/BarChart.vue';

export default {
  components: {
    MyForm,
    BarChart
  }
};
</script>

<style>
.el-header {
  background-color: #409EFF;
  color: white;
  text-align: center;
  line-height: 60px;
}
</style>