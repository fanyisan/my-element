<template>
  <div class="the-header-wrapper">
    <img :src="src" class="logo" />
    <div class="nav">
      <span
        v-for="(item, index) of navItems"
        :key="item"
        @click="activeIndex = index"
        :class="activeIndex === index ? 'active' : ''"
        class="nav-item"
      >
        <span class="item-content">{{ item }}</span>
      </span>
      <el-dropdown trigger="click" class="lang-drop">
        <span>中文<i class="el-icon-arrow-down"></i></span>
        <el-dropdown-menu slot="dropdown">
          <el-dropdown-item>中文</el-dropdown-item>
          <el-dropdown-item>English</el-dropdown-item>
        </el-dropdown-menu>
      </el-dropdown>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      src: '/logo.svg',
      navItems: ['指南', '组件', '主题', '资源'],
      activeIndex: -1
    }
  }
}
</script>

<style lang="scss" scoped>
.the-header-wrapper {
  display: flex;
  align-items: center;
  justify-content: space-between;
  max-width: 1140px;
  height: 80px;
  margin: 0 auto;
  border-bottom: 1px solid #dcdfe6;

  .logo {
    width: 146px;
    height: 38px;
  }

  .nav {
    display: flex;
    align-self: stretch;
    color: #409eff;

    .nav-item {
      display: flex;
      flex-direction: column;
      padding: 0 22px;
      opacity: 0.5;
      cursor: pointer;

      &:hover {
        opacity: 1;
      }

      .item-content {
        flex: 1;
        line-height: 77px;
      }
    }

    .lang-drop {
      display: flex;
      align-items: center;
      margin-left: 40px;
      font-size: 16px;
      color: #888;
      opacity: 0.8;

      .el-icon-arrow-down {
        font-size: 12px;
        margin-left: 10px;
      }

      /deep/ .el-dropdown-selfdefine {
        display: flex;
        align-items: center;
        padding: 10px 0 10px 10px;
        cursor: pointer;
      }

      &:hover {
        color: #409eff;
      }
    }

    .active {
      opacity: 1;

      &::after {
        content: '';
        height: 2px;
        width: 100%;
        background: #409eff;
      }
    }
  }
}
</style>
