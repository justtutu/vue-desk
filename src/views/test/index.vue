<template>
  <el-container class="container">
    <el-header class="container-header">
      <div class="page-title">
        标题
      </div>
    </el-header>
    <el-main class="container-main">
      <el-carousel arrow="always" :autoplay="false" height="500px">
        <el-carousel-item>
          <div class="left">
            111123213123123123
            111123213123123123
            111123213123123123
            111123213123123123
            111123213123123123
            111123213123123123
            111123213123123123
            111123213123123123
            111123213123123123
            111123213123123123
            111123213123123123
            111123213123123123
            111123213123123123
          </div>
          <div class="right">
            <ul class="menu-list">
              <router-link class="menu" to="/">
                <div class="icon" />
                <div class="title">当日挂号</div>
              </router-link>
              <router-link class="menu" to="/">
                <div class="icon" />
                <div class="title">现场预约</div>
              </router-link>
              <router-link class="menu" to="/">
                <div class="icon" />
                <div class="title">预约取号</div>
              </router-link>
            </ul>
          </div>
        </el-carousel-item>
        <el-carousel-item>
          <div>
            2222
          </div>
        </el-carousel-item>
      </el-carousel>
    </el-main>
    <el-footer class="container-footer">
      <el-button type="warning" class="desk-button">测试按钮</el-button>
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
    color: #000;
    .left{
      width: 20%;
      height: 100%;
      float: left;
    }
    .right{
      width: 80%;
      height: 100%;
      float: left;
      .menu-list{
        list-style: none;
        color: #fff;
        height: 100%;
        display: flex;
        justify-content: space-evenly;
        .menu{
          width: 30%;
          height: 30%;
          background-color: #26b562;
          display: flex;
          flex-direction: column;
          .title{
            font-size: 20px;
          }
        }
      }
    }
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
