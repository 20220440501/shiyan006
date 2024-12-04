<!-- src/components/MyForm.vue -->
<template>
  <div>
    <el-form :model="form" label-width="80px">
      <el-form-item label="用户名">
        <el-input v-model="form.username" placeholder="请输入用户名"></el-input>
      </el-form-item>
      <el-form-item label="密码">
        <el-input v-model="form.password" type="password" placeholder="请输入密码"></el-input>
      </el-form-item>
      <el-form-item>
        <el-button type="primary" @click="submitForm">提交</el-button>
        <el-button @click="resetForm">重置</el-button>
      </el-form-item>
    </el-form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      form: {
        username: '',
        password: ''
      }
    };
  },
  methods: {
    submitForm() {
      this.$message({
        message: `用户名: ${this.form.username}, 密码: ${this.form.password}`,
        type: 'success'
      });
    },
    resetForm() {
      this.form.username = '';
      this.form.password = '';
    }
    }
};
</script>

<style scoped>
.el-form {
  max-width: 400px;
  margin: 0 auto;
}
</style>