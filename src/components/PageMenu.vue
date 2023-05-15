<template>
  <div class="my-menu">
    <el-menu
      mode="horizontal"
      @select="RouteToOtherPage"
      background-color="rgb(220, 210, 234)"
      active-text-color="purple"
      :default-active="1"
    >
      <el-menu-item index="0">
        <el-image
          alt="Project logo"
          :src="require('@/assets/logo.png')"
          :fit="cover"
        />
      </el-menu-item>
      <div class="redirection">
        <el-menu-item index="1">
          <div class="menu-item-inside">
            纪念馆
            <el-icon><House /></el-icon>
          </div>
        </el-menu-item>
        <el-menu-item index="2">
          <div class="menu-item-inside">
            用户中心
            <el-icon><User /></el-icon>
          </div>
        </el-menu-item>
        <el-menu-item index="3">
          <div class="menu-item-inside">
            法律事务
            <el-icon><Reading /></el-icon>
          </div>
        </el-menu-item>
        <el-menu-item index="4">
          <div class="menu-item-inside">
            网站介绍
            <el-icon><MoreFilled /></el-icon>
          </div>
        </el-menu-item>
        <el-menu-item index="5">
          <div class="menu-item-inside">
            个性定制
            <el-icon><Pointer /></el-icon>
          </div>
        </el-menu-item>
      </div>
    </el-menu>
  </div>
</template>

<script>
import router from "../router/index";
import {
  House,
  User,
  Reading,
  MoreFilled,
  Pointer,
} from "@element-plus/icons-vue";

export default {
  name: "PageMenu",
  components: {
    House,
    User,
    Reading,
    MoreFilled,
    Pointer,
  },
  methods: {
    RouteToOtherPage(pageIndex) {
      switch (pageIndex) {
        case 0:
          router.push({ name: "home" });
          break;
        case 1:
          router.push({ name: "home" });
          break;
        case 2:
          //vuex user(param) not coded yet
          router.push({ name: "userPage", params: {} });
          break;
        case 3:
          router.push({ name: "lawAssistance" });
          break;
        case 4:
          router.push({ name: "introduction" });
          break;
      }
    },
  },
};
</script>

<style scoped>
.menu-item-inside {
  font-size: 20px;
}
.el-icon svg {
  height: 2em;
  width: 2em;
  margin-bottom: 5px;
}
.redirection {
  margin-left: 4.5em;
  display: inline-flex;
}
.el-menu-item {
  margin-right: 4em;
}
.my-menu {
  font-family: text;
  margin: 2em;
  --el-menu-hover-text-color: white;
}
</style>
