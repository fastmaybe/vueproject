<template>
    <div id="baseTable">
        <el-table :data="dataTable">
          <el-table-column type="index" label="序号"></el-table-column>
          <el-table-column prop="username" label="用户名"></el-table-column>
          <el-table-column prop="password" label="密码"></el-table-column>
        </el-table>
    </div>
</template>

<script>
    export default {
        name: "BaseTable",
      props:{
        dataTable:Array
      },
      created:{

      }
      ,
      data(){
        return{
           // dataTable:[{'username':'小三','password':'23'},{'username':'小四','password':'26'},{'username':'小五','password':'25'}]
        }
      }

    }
</script>

<style scoped>

</style>
