<template>
  <div id="login">
    <base-form></base-form>
    <base-table v-bind:dataTable="dataTable"></base-table>
    <el-button  @click="changeData">数据更新</el-button>
  </div>
</template>




<script>
  import baseForm from './BaseForm'
  import baseTable from './BaseTable'
    export default {
        name: "Login",
      components:{
        baseForm,
        baseTable
      },
      data(){
          return{
            username:'',
            password:'',
            reslut:'',
            dataTable:[]
          }
      },
      methods:{
          login(){
            this.$axios.post('/vue/user/login',{name:this.name,password:this.password}).then(res=>{
              this.reslut=data.msg;
            })
          },
        changeData:function () {
          this.dataTable=[{'username':'小三','password':'23'},{'username':'小四','password':'26'},{'username':'小五','password':'25'}]
        alert( this.dataTable)
        }
      }

    }
</script>

<style scoped>

</style>
