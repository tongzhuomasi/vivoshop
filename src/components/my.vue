<template>
  <div class="my">
    <!--标题-->
    <div class="myHeader">{{my}}</div>
    <!--头像-->
    <div class="myMain">
      <div class="Main">
        <img src="/static/img/tou.jpg" alt="头像">
        <p>{{myName}}</p>
      </div>
    </div>
    <div class="MyBox">
      <!--我的订单-->
      <div class="myOrder" @click="order">
        <div class="Order">
          <i class="iconfont icon-74wodedingdan"></i>
          <p>我的订单</p>
        </div>
      </div>
      <!--联系我-->
      <div class="myCollection" @click="author">
        <div class="Order">
          <i class="iconfont icon-zuozhe"></i>
          <p>联系我</p>
        </div>
      </div>
    </div>

  </div>
</template>

<script>
  import {mapState} from 'vuex';

  export default {
    name: "my",
    data() {
      return {
        // lists:[]
        my: "我的",
        myName: "姜先生"
      }
    },
    methods: {
      order: function () {
        this.$router.push('/order')
      },
      author: function () {
        this.$router.push('/author')
      }
    }
  }
</script>


<style>
  .myHeader {
    height: 1.3rem;
    line-height: 1.3rem;
    font-size: 0.35rem;
    padding-left: 0.3rem;
    background: white;
    font-size: 0.41rem;
    display: flex;
    flex-flow: row nowrap;
    justify-content: center;
    align-items: center;
  }

  .myMain {
    height: 100%;
    background: white;
    margin-top: 10px;
    width: 100%;

  }

  .MyBox {
    width: 100%;
    height: 110px;
    background: white;
  }

  .myOrder, .myCollection {
    height: 50%;
  }

  .Main, .Order {
    height: 100%;
    /* background: red; */
    margin-left: 10px;
    border-bottom: 1px solid #cccccc;
    display: flex;
    flex-flow: row nowrap;
    justify-content: flex-start;
    align-items: center;
  }

  .myMain img {
    display: block;
    width: 60px;
    height: 60px;
    padding: 7px;
    float: left;
  }

  .myMain p {
    line-height: 75px;
  }

  .Order i, .Order p {
    display: block;
    line-height: 55px;
    float: left;
    padding-left: 10px;
  }
</style>
