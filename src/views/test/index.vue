<template>
  <el-container class="container">
    <el-header class="container-header">
      <div class="page-title">
        标题
      </div>
    </el-header>
    <el-main class="container-main">主体内容</el-main>
    <el-footer class="container-footer">
      <el-button type="success" class="desk-button">测试按钮</el-button>
    </el-footer>
  </el-container>
</template>

<script>
export default {
}
</script>

<style scoped lang="scss">
@import "~@/styles/element-variables.scss";
.container{
  height: 100%;
  background-color:$--color-primary;
  color: #fff;
  padding: 30px;
  .container-header{
    height: 10% !important;
    padding: 0;
    //margin: 30px;
    .page-title{
      color: #fff;
      font-size: 30px;
      font-weight:bold;
    }
  }
  .container-main{
    height: 80%;
    padding: 0;
    background-color: #fff;
    //margin: 30px;
  }
  .container-footer{
    height: 10% !important;
    display: flex;
    justify-content: flex-end;
    align-items: center;
  }
  .desk-button{
    padding: 20px 50px;
    font-size: 24px;
  }
}
</style>
