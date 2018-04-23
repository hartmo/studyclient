<template>
    <div id="app">
        <div class="header">
            <el-menu :default-active="activeIndex" class="el-menu-demo" mode="horizontal" @select="handleSelect">
                <el-menu-item index="1">首页</el-menu-item>
                <el-submenu index="2">
                    <template slot="title">自考方向</template>
                    <el-menu-item index="2-1">计算机网络</el-menu-item>
                    <el-menu-item index="2-2">会计</el-menu-item>
                    <el-menu-item index="2-3">汉语</el-menu-item>
                    <el-submenu index="2-4">
                        <template slot="title">公共科目</template>
                        <el-menu-item index="2-4-1">计算机应用</el-menu-item>
                        <el-menu-item index="2-4-2">高等数学</el-menu-item>
                        <el-menu-item index="2-4-3">学位英语</el-menu-item>
                    </el-submenu>
                </el-submenu>
                <el-menu-item index="3" disabled>消息中心</el-menu-item>
                <el-menu-item index="4" class="f_r">
                    <template>
                        <ul class="login_ground">
                            <li><span class="b_r">登录</span></li>
                            <li><span>注册</span></li>
                            <li class="login_name"><span>hartmo</span></li>
                        </ul>
                    </template>
                </el-menu-item>
            </el-menu>
        </div>
        <div class="router_box">
            <router-view></router-view>
        </div>
    </div>
</template>

<script>
  export default {
    name: 'studyclient',
    data () {
      return {
        isCollapse: true,
        activeIndex: '1'
      }
    },
    methods: {
      handleSelect (data) {
        console.log(data)
      }
    }
  }
</script>
<style href="http://at.alicdn.com/t/font_634398_09n2oan16oueg66r.css"></style>
<style lang="scss">
    @import '~element-ui/lib/theme-chalk/index.css';
    @import "./sass/main.scss";
    @import "./app.scss";
    /* CSS */
</style>
