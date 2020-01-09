<template>
  <div class="resource-wrapper">
    <h2>资源</h2>
    <p>设计资源正在整理和完善中.</p>
    <ul class="container">
      <li>
        <div class="card">
          <img src="/components.svg" />
          <h3>Axure Components</h3>
          <p>
            通过在Axure中导入Element组件库,
            可以在交互设计阶段方便地调用常用的组件
          </p>
          <a href="#">下载</a>
        </div>
      </li>
      <li>
        <div class="card">
          <img src="/template.svg" />
          <h3>Sketch Template</h3>
          <p>
            从 Element Template
            快速调用常用组件，在提升设计效率的同时，保证统一的视觉风格
          </p>
          <a href="#">下载</a>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.resource-wrapper {
  width: 1140px;
  min-height: 100vh;
  margin: -80px auto 0;
  padding-top: 135px;

  h2 {
    font-size: 28px;
    font-weight: 400;
    color: #1f2f3d;
  }

  p {
    color: #5e6d82;
    font-size: 14px;
    margin: 14px 0;
    line-height: 1.5;
  }

  .container {
    display: flex;
    text-align: center;
    margin: 35px -11px 110px;

    li {
      padding: 0 11px;
      width: 33.3333%;

      .card {
        border: solid 1px #eee;
        border-radius: 5px;
        height: 394px;

        img {
          margin: 75px 0 35px;
        }

        h3 {
          font-size: 18px;
          color: #1f2f3d;
          font-weight: 400;
          margin-bottom: 10px;
        }

        p {
          font-size: 14px;
          color: #99a9bf;
          padding: 0 30px;
          line-height: 1.8;
        }

        a {
          display: inline-block;
          width: 190px;
          height: 42px;
          line-height: 42px;
          background: #409eff;
          color: #fff;
          font-size: 14px;
          border-radius: 2px;
        }
      }
    }
  }
}
</style>
