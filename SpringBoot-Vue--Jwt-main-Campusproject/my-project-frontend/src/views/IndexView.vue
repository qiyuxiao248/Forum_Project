<template>
    <div class="main-content">
      <el-container style="height: 100%">
        <el-header class ="main-content-header">
          <el-image class="logo" src="https://element-plus.org/images/element-plus-logo.svg"></el-image>
          <div style="flex: 1" class="user-info">
            <div class="profile">

            </div>
            <el-avatar></el-avatar>
          </div>
        </el-header>
        <el-container>
          <el-aside width="200px">Aside</el-aside>
          <el-main>Main</el-main>
        </el-container>
      </el-container>
    </div>

</template>

<script setup>
import { logout } from '@/net'
import router from "@/router";

function userLogout() {
  logout(() => router.push("/"))
}
</script>

<style lang="less" scoped>
.main-content{
  height: 100vh;
  width: 100vw;
}
.main-content-header{
  border-bottom: solid 1px var(--el-border-color);
  height: 55px;
  display: flex;
  align-items: center;
  box-sizing: border-box;
}
.logo{
  height: 32px;
}
.user-info{

}

</style>
