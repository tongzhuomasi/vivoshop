<template>
  <div class="Author">
      <div class="AuthorHeader">
        <router-link to="my">
          <i class="iconfont icon-552cc14536532"></i>
        </router-link>
          关于我
      </div>
      <div class="AuthorMain">
        <div class="AuthorText">
          <img class="AuthorIcon" src="../../static/img/icon.png" alt="作者">
          <p>作者：JT-姜涛</p>
          <p>我的QQ:609403518</p>
          <p>我的邮箱:tongzhuomasi@163.com</p>
        </div>
        <router-link :to="{name:'Home'}" >前往首页</router-link>
      </div>
  </div>
</template>

<script>
import { mapState } from 'vuex';
export default {
}
</script>

<style>
.Author{
  position: absolute;
  width: 100%;
  height: 100%;
  z-index: 999;
  background: white;
}
.AuthorHeader{
    position: fixed;
    top: 0;
    width: 100%;
    height: 1.3rem;
    line-height: 1.3rem;
    background: white;
    padding-left: 0.3rem;
    -webkit-box-shadow: 0 0 10px #cecece;
    box-shadow: 0 0 10px #cecece;
    z-index: 1;
    font-size: 0.41rem;
}
.AuthorMain{
    margin-top: 1.6rem;
    font-size: 0.4rem;
  display: flex;
  flex-flow: column nowrap;
  justify-content: flex-start;
  align-items: center;
}
.AuthorMain a{
    display: block;
    text-align: center;
    margin: 0.8rem auto;
    width: 110px;
    height: 37px;
    line-height: 37px;
    border-radius: 4px;
    text-align: center;
    background: #e0524b;
    color: white;
    font-weight: 800;
    font-size: 0.5rem;
}
.AuthorHeader i{
    display: block;
    float: left;
    height: 50px;
    font-size: 0.71rem;
    color: black;
    width: 0.9rem;
}
.AuthorIcon {
  margin: 0.5rem auto;
  width: 150px;
  border-radius: 50%;
}
.AuthorText {
  font-size: 0.5rem
}

</style>
