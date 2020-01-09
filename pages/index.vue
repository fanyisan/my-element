<template>
  <div>
    <div class="main">
      <h1 class="main-title">网站快速成型工具</h1>
      <p class="main-desc">
        Element, 一套为开发者、设计师和产品经理准备的基于Vue2.0的桌面端组件库
      </p>
      <div class="banner">
        <el-image
          src="https://element.eleme.cn/2.13/static/theme-index-blue.c38b733.png"
        ></el-image>
        <div :style="{ height: maskHeight + 'px' }" class="mask">
          <el-image
            src="https://element.eleme.cn/2.13/static/theme-index-red.c8e136e.png"
          ></el-image>
        </div>
      </div>
      <div class="sponsor">
        <img src="/sponsor/多会.svg" width="45px" />
        <div class="sponsor-desc">
          <p>Sponsored by 多会</p>
          <p>炫酷的新一代活动票务系统</p>
        </div>
      </div>
      <div class="cards">
        <div v-for="item of cards" :key="cards.title" class="card">
          <div class="card-body">
            <img :src="item.url" class="card-img" />
            <h3 class="card-title">{{ item.title }}</h3>
            <p class="card-desc">
              {{ item.desc }}
            </p>
          </div>
          <a href="#" class="card-action">查看详情</a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      maskHeight: 0,
      cards: [
        {
          url: 'https://element.eleme.cn/2.13/static/guide.0a8462c.png',
          title: '指南',
          desc:
            '了解设计指南，帮助产品设计人员搭建逻辑清晰、结构合理且高效易用的产品。'
        },
        {
          url: 'https://element.eleme.cn/2.13/static/component.bd3411b.png',
          title: '组件',
          desc:
            '使用组件 Demo 快速体验交互细节；使用前端框架封装的代码帮助工程师快速开发。'
        },
        {
          url: '/theme.svg',
          title: '主题',
          desc: '在线主题编辑器，可视化定制和管理站点主题、组件样式'
        },
        {
          url: 'https://element.eleme.cn/2.13/static/resource.a72b8f8.png',
          title: '资源',
          desc:
            '下载相关资源，用其快速搭建页面原型或高保真视觉稿，提升产品设计效率。'
        }
      ]
    }
  },
  mounted() {
    window.addEventListener('scroll', this.handleScroll)
  },
  beforeDestroy() {
    window.removeEventListener('scroll', this.handleScroll)
  },
  methods: {
    handleScroll(e) {
      const scrollTop =
        window.pageYOffset ||
        document.documentElement.scrollTop ||
        document.body.scrollTop
      this.maskHeight = scrollTop
    }
  }
}
</script>

<style lang="scss" scoped>
.main {
  text-align: center;

  .main-title {
    font-size: 34px;
    color: #555;
  }

  .main-desc {
    font-size: 18px;
    color: #888;
  }

  .banner {
    position: relative;
    margin: 30px auto;
    width: 890px;

    .el-image {
      width: 100%;
    }

    .mask {
      position: absolute;
      top: 0;
      overflow: hidden;
      max-height: 550px;
    }
  }

  .sponsor {
    display: flex;
    justify-content: center;
    align-items: center;
    color: #999;
    height: 100px;
    margin: 0 20px 50px;

    .sponsor-desc {
      text-align: left;
      font-size: 14px;
      margin-left: 20px;
      line-height: 24px;
    }
  }

  .cards {
    display: flex;
    margin: 0 60px 110px;

    .card {
      position: relative;
      overflow: hidden;
      flex: 1;
      height: 430px;
      border: solid 1px #eee;
      border-radius: 5px;
      margin: 0 19px;
      transition: all 0.3s;

      &:hover {
        transform: translateY(-5px);
        box-shadow: 1px 1px 10px 5px #f6f6f6;
      }

      .card-body {
        .card-img {
          margin: 66px 0;
          width: 160px;
        }

        .card-title {
          font-weight: 400;
          color: #1f2f3d;
        }

        .card-desc {
          color: #99a9bf;
          font-size: 14px;
          line-height: 20px;
          margin: 14px 25px;
        }
      }

      .card-action {
        position: absolute;
        left: 0;
        bottom: 0;
        height: 54px;
        width: 100%;
        line-height: 54px;
        color: #409eff;
        font-size: 14px;
        border-top: solid 1px #eee;
        transition: all 0.2s;

        &:hover {
          background: #409eff;
          color: #fff;
        }
      }
    }
  }
}
</style>
