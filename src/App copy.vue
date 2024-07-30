<script setup>
import { RouterLink, RouterView } from 'vue-router'




</script>

<template>
  <div class="abovenav">
    <el-row :gutter="24" style="height: 100%;">
    <el-col :span="2"><div class="logo" />
      <img style="width: 60px; height: 60px;border-radius: 30px;" src="../src/assets/img/logo.png" />
    </el-col>
    <el-col :span="15"></el-col>
    <el-col :span="5"><div class="nav" />
      <el-row class="row-bg" justify="start" :gutter="24">
        <el-col :span="6"><div class="grid-content"><RouterLink to="/">Home</RouterLink></div></el-col>
        <el-col :span="6"><div class="grid-content"><RouterLink to="/about">About</RouterLink></div></el-col>
        <el-col :span="6"><div class="grid-content">  <RouterLink to="/date">Date</RouterLink></div></el-col>
        <el-col :span="6"><div class="grid-content"><RouterLink to="/last">Last</RouterLink></div></el-col>
      </el-row>
    </el-col>
    <el-col class="user"  :span="2"><div/>
      <img  class="userimage" src="../src/assets/img/logoo.png" />
    </el-col>
  </el-row>
  </div>
  <div class="common-layout">
  </div>
  <RouterView />
</template>

<style scoped>



.abovenav{
  height: 61px;
  background-color: antiquewhite;
  text-align: center;
  float:none;
  vertical-align:middle;
  .img{
    position:absolute;
    width:100%;
    height:100vh;
    }
}

.row-bg{
height: 100%;
width: 300px;
}
.logo{
  /* background-image:url("../assets/img/logo.jpg"); */
  background-size: cover; /* 背景图片覆盖整个元素 */
  background-repeat: no-repeat; /* 背景图片不重复 */
  background-position: center; 
  }
.el-row:last-child {
  margin-bottom: 0;
}
.el-col {
  border-radius: 4px;
}
.grid-content {

  padding: 20px 40px 0px 0px;
  position: fixed;

  display: flex;
  border-radius: 4px;
  min-height: 36px;
}
.user{
  text-align: left;

}
.userimage{
  width: 50px; 
  height: 50px; 
  border-radius: 15px; 
  margin: 6px 0px 0px 18px ;
}


</style>
