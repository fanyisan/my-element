<template>
  <div class="theme-wrapper">
    <h2>官方主题</h2>
    <div class="preview">
      <div class="line">
        <div class="line-item" style="background: rgb(64, 158, 255)"></div>
        <div class="line-item" style="background: rgb(48, 49, 51)"></div>
      </div>
      <div class="line">
        <div class="line-item" style="background: rgb(160, 207, 255)"></div>
        <div class="line-item" style="background: rgb(217, 236, 255)"></div>
        <div class="line-item" style="background: rgb(220, 223, 230)"></div>
        <div class="line-item" style="background: rgb(144, 147, 153)"></div>
      </div>
      <div class="action">
        <div class="mask"></div>
        <div class="action-block">
          <div class="action-item">
            <img src="/eye.png" />
            <span>查看</span>
          </div>
          <div class="action-item">
            <img src="/copy.png" />
            <span>复制</span>
          </div>
        </div>
      </div>
      <div class="info">
        <div class="title">
          <strong>Element</strong>
          <span>by Element</span>
        </div>
        <div class="desc">默认主题</div>
      </div>
    </div>
    <h2>我的主题 (0/8)</h2>
    <div class="upload">
      <i class="el-icon-upload2"></i>
      <span>点击上传主题</span>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.theme-wrapper {
  width: 1140px;
  margin: 55px auto;

  h2 {
    font-size: 28px;
    color: #1f2f3d;
    font-weight: 400;
    margin-bottom: 24px;
    line-height: 1;
  }

  .preview {
    position: relative;
    overflow: hidden;
    width: 273px;
    height: 185px;
    border: solid 1px #ccc;
    border-radius: 4px;
    margin-bottom: 50px;

    &:hover {
      box-shadow: 1px 1px 10px #aaa;

      .action {
        opacity: 1;
      }
    }

    .line {
      display: flex;
      height: 65px;

      .line-item {
        flex: 1;
      }
    }

    .action {
      position: absolute;
      left: 0;
      top: 0;
      height: 130px;
      width: 100%;
      opacity: 0;
      transition: all 0.3s;

      .mask {
        position: absolute;
        top: 0;
        right: 0;
        bottom: 0;
        left: 0;
        background: #000;
        opacity: 0.4;
      }

      .action-block {
        position: absolute;
        display: flex;
        justify-content: space-between;
        align-items: center;
        height: 130px;
        width: 100%;
        padding: 0 60px;

        .action-item {
          text-align: center;
          font-size: 14px;
          cursor: pointer;

          img {
            width: 54px;
          }
          span {
            display: block;
            color: #fff;
          }
        }
      }
    }

    .info {
      padding: 0 12px;

      .title {
        display: flex;
        justify-content: space-between;
        line-height: 26px;

        strong {
          color: #303133;
          font-weight: 700;
        }

        span {
          color: #909399;
          font-size: 14px;
        }
      }

      .desc {
        font-size: 14px;
        color: #606266;
        margin-top: 5px;
      }
    }
  }

  .upload {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: 273px;
    height: 185px;
    border: dashed 1px #ccc;
    border-radius: 4px;
    background: #f5f7fa;
    color: #606266;
    font-size: 14px;
    cursor: pointer;

    i {
      font-size: 30px;
      color: #999;
      margin-bottom: 6px;
    }
  }
}
</style>
