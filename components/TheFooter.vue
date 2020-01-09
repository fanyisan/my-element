<template>
  <div class="the-footer-wrapper">
    <div class="footer-main">
      <h4>链接</h4>
      <a
        v-for="item of links[0]"
        :key="item"
        href="#"
        class="footer-main-link"
        >{{ item }}</a
      >
    </div>
    <div class="footer-main">
      <h4>社区</h4>
      <a
        v-for="item of links[1]"
        :key="item"
        href="#"
        class="footer-main-link"
        >{{ item }}</a
      >
    </div>
    <div class="footer-social">
      <h4>Element 2.1 Fullerene</h4>
      <a href="#"><i class="iconfont icon-weixin"></i></a>
      <a href="#"><i class="iconfont icon-github"></i></a>
      <a href="#"><i class="iconfont icon-gitter"></i></a>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      links: [
        [
          '代码仓库',
          '更新日志',
          '常见问题',
          '脚手架',
          '在线主题生成器',
          'Element-React',
          'Element-Angular'
        ],
        ['在线讨论', '反馈建议', '贡献指南', 'SegmentFault', 'Awesome Element']
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.the-footer-wrapper {
  display: flex;
  height: 340px;
  padding: 40px 150px;
  background: #f7fbfd;

  h4 {
    margin-bottom: 15px;
    font-size: 18px;
  }

  a {
    text-decoration: none;
    color: #666;
    font-size: 14px;

    &:hover {
      color: #333;
    }
  }

  .footer-main {
    margin-right: 110px;

    .footer-main-link {
      display: block;
      line-height: 28px;
    }
  }
  .footer-social {
    margin-left: auto;
    text-align: right;

    a {
      margin-left: 12px;
    }

    .iconfont {
      display: inline-block;
      transition: all 0.2s linear;
      font-size: 33px;
      color: #c8d6e8;

      &:hover {
        transform: scale(1.2);
        color: #999fff;
      }
    }
  }
}
</style>
