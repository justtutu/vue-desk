<template>
  <el-container class="container">
    <el-header class="container-header">
      <div class="page-title">
        标题
      </div>
    </el-header>
    <el-main class="container-main">
      <el-carousel arrow="always" :autoplay="false">
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
              <router-link
                v-for="(item,index) in menuList"
                :key="item.path
                "
                class="menu"
                :class="'bg'+index"
                :to="item.path"
              >
                <svg class="icon" aria-hidden="true">
                  <use :xlink:href="'#icon-'+item.path" />
                </svg>
                <div class="title">{{ item.name }}</div>
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
  data() {
    return {
      menuList: [{
        name: '当日挂号',
        path: 'todayRegister'
      }, { name: '现场预约', path: 'liveOrder' }, { name: '预约取号', path: 'takeNumber' },
      { name: '门诊缴费', path: 'opcPay' }, { name: '门诊预交查询', path: 'opcOrderQuery' },
      { name: '门诊清单查询', path: 'opcListQuery' }, { name: '物价查询', path: 'priceQuery' }, { name: '满意度调查', path: 'satisfactionResearch' }, { name: '医院介绍', path: 'hospitalIntroduce' }]
    }
  }
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
        flex-wrap: wrap;
        .menu{
          width: 27%;
          height: 27%;
          background-color: #26b562;
          display: flex;
          flex-direction: column;
          align-items: center;
          justify-content: space-evenly;
          .title{
            font-size: 20px;
            color: #ecf0f1;
          }
          &.bg1{
            background-color: #1abc9c;
          }
          &.bg2{
            background-color: #2ecc71;
          }
          &.bg3{
            background-color: #3498db;
          }
          &.bg4{
            background-color: #9b59b6;
          }
          &.bg5{
            background-color: #f1c40f;
          }
          &.bg6{
            background-color: #e67e22;
          }
          &.bg7{
            background-color: #e74c3c;
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
.el-carousel{
  height: 100%;

}
::v-deep  .el-carousel__container{
  height: 100% !important;
}
</style>
