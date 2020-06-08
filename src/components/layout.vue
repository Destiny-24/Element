<template>
  <div class="page-wrapper">
    <Sider class="page-sider">Sider</Sider>
    <div class="page-mainer">
      <Header class="page-header">Header</Header>
      <div class="page-body">
        <router-view></router-view>
      </div>
      <Footer class="page-footer">Footer</Footer>
    </div>
  </div>
</template>

<script>
import Header from "./layoutHeader.vue";
import Sider from "./layoutSider.vue";
import Footer from "./layoutFooter.vue";
export default {
  data() {
    return {};
  },
  components: {
    Header,
    Sider,
    Footer
  }
};
</script>

<style type="text/css" lang="less">
.page-wrapper {
  height: 100vh;
  background-color: #f0f2f5;
  display: flex;
}

.page-sider {
  position: relative;
  background-color: #fff;
  box-shadow: 2px 0 8px 0 rgba(29, 35, 41, 0.05);
  width: 240px;
}

.page-mainer {
  flex: 1;
  display: flex;
  flex-direction: column;
}

.page-header {
  background-color: #fff;
  box-shadow: 0 2px 8px #f0f1f2;
  position: relative;
  z-index: 10;
  height: 64px;
}

.page-body {
  flex: 1;
}

.page-footer {
  text-align: center;
  font-size: 12px;
  line-height: 40px;
  opacity: 0.4;
}
</style>
