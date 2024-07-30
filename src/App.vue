<script setup>
import { RouterLink, RouterView } from 'vue-router'
import { ref } from 'vue'





</script>
<template>






  <div class="header">
      <div class="l-content" >
      <img style="width: 60px; height: 60px;border-radius: 30px;display: flex;" src="../src/assets/img/logo.png" />
      </div>

      <nav class="r-content">

          
<el-menu  style="padding-right: 18px;"
    :default-active="activeIndex"
    class="el-menu"
    mode="horizontal"
     :ellipsis="false"
    @select="handleSelect"
  >
<el-menu-item class="el-menu-item" index="1">
      <RouterLink class="grid-content" to="/" >Home</RouterLink></el-menu-item>
      <el-menu-item index="2">
        <RouterLink class="grid-content" to="/about">About</RouterLink></el-menu-item>
      <el-menu-item index="3">
        <RouterLink class="grid-content" to="/date">Date</RouterLink></el-menu-item>
    <el-menu-item index="4">
      <RouterLink class="grid-content "  to="/last">Last</RouterLink></el-menu-item>
</el-menu > 



        

      <div>
        <!-- 下拉菜单 -->
        <el-dropdown>
            <span class="el-dropdown-link">
                <img  class="userimage" src="../src/assets/img/user.png" />
            </span>
            <template #dropdown>
                <el-dropdown-menu>
                    <el-dropdown-item>个人中心</el-dropdown-item>
                    <el-dropdown-item>退出登录</el-dropdown-item>                        
                </el-dropdown-menu>
            </template>
        </el-dropdown>
      </div>


      </nav>
  </div>
  <RouterView />
</template>

<style scoped>
@import '../src/output.css';
a{
  text-decoration: none;
}
.el-menu{
  border-right: none ;
}
.el-menu-item{
  border-right: none ;
}
.header{
    display: flex;
    justify-content: space-between;
    align-items: center;
    background-color:rgb(255, 255, 255);
}
.l-content{
    display:flex;
    align-items:center;
}

.nav{  
  display: flex;
  justify-content: space-between;
  align-items: center;
  list-style-type: none; /* 移除默认列表样式 */
}
.grid-content{
    padding: 10px 10px 10px 10px; /* 设置链接内的内边距 */

    .p{
      text-decoration: none; /* 移除下划线 */
    }
  }
.r-content{
  display: flex;        /*弹性布局*/
  .userimage{
    width: 50px; 
    height: 50px; 
    border-radius: 15px; 
    margin: 2px 6px 0px 6px ;
  }
}

nav a:hover{
  color: goldenrod;
}
nav a:active{

  color:chocolate;
}

:deep(.bread span){
    color: #fff !important;
    cursor:pointer !important;
}
</style>