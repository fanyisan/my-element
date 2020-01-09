<template>
  <div>
    <div class="container">
      <div class="sidebar">
        <div class="sponsor">
          <p>赞助商</p>
          <img src="/sponsor/多会.svg" width="42px" />
        </div>
        <ul class="menu">
          <li class="menu-item">设计原则</li>
          <li class="menu-item">导航</li>
        </ul>
      </div>
      <nuxt-child class="content" />
    </div>
  </div>
</template>

<style lang="scss" scoped>
.container {
  display: flex;
  width: 1140px;
  margin: 0 auto;
  padding-top: 55px;

  .sidebar {
    width: 200px;
    color: #777;
    font-size: 14px;
    line-height: 40px;
    font-weight: 300;

    .menu {
      list-style: none;
      padding-left: 0;
      font-size: 16px;
      font-weight: 700;
      margin-top: 15px;
    }
  }

  .content {
    flex: 1;
  }
}
</style>
