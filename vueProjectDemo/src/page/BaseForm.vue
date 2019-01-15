<template>
  <div id="BaseForm">
    <el-form>
      <el-form-item>
        <el-input v-model="username" placeholder="用户名"></el-input>
      </el-form-item>
      <el-form-item>
        <el-input v-model="password" aria-placeholder="密码"></el-input>
      </el-form-item>
      <!--<el-form-item>-->
        <!--<bootstrap-date-input data-date-picker="activated"></bootstrap-date-input>-->
      <!--</el-form-item>-->
      <el-form-item>
        <el-button @click="toLogin">登录</el-button>
      </el-form-item>
    </el-form>
  </div>
</template>

<script>
    export default {
        name: "BaseForm",
      data:{
        username:'',
        password:''
      },
      methods:{
        toLogin:function () {
         alert(this.username+''+this.password)
        }
      }
    }

</script>

<style scoped>

</style>
