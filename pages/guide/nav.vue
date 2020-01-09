<template>
  <div class="nav-wrapper">
    <h2>导航</h2>
    <p>
      导航可以解决用户在访问页面时：在哪里，去哪里，怎样去的问题。一般导航会有「侧栏导航」和「顶部导航」2
      种类型。
    </p>
    <h3>选择合适的导航</h3>
    <p>
      选择合适的导航可以让用户在产品的使用过程中非常流畅，相反若是不合适就会引起用户操作不适（方向不明确），以下是「侧栏导航」和
      「顶部导航」的区别。
    </p>
    <h3>侧栏导航</h3>
    <el-row :gutter="20">
      <el-col :span="9">
        <p>
          可将导航栏固定在左侧，提高导航可见性，方便页面之间切换；顶部可放置常用工具，如搜索条、帮助按钮、通知按钮等。适用于中后台的管理型、工具型网站。
        </p>
      </el-col>
      <el-col :span="15">
        <img src="https://element.eleme.cn/2.13/static/navbar_1.499e088.png" />
        <h5>一级类目</h5>
        <p>适用于结构简单的网站：只有一级页面时，不需要使用面包屑。</p>
        <img src="https://element.eleme.cn/2.13/static/navbar_2.59ecae2.png" />
        <h5>二级类目</h5>
        <p>
          侧栏中最多可显示两级导航；当使用二级导航时，我们建议搭配使用面包屑，方便用户定位自己的位置和快速返回。
        </p>
        <img src="https://element.eleme.cn/2.13/static/navbar_3.8dcec92.png" />
        <h5>三级类目</h5>
        <p>
          适用于较复杂的工具型后台，左侧栏为一级导航，中间栏可显示其对应的二级导航，也可放置其他的工具型选项。
        </p>
      </el-col>
    </el-row>
    <h3>顶部导航</h3>
    <el-row :gutter="20">
      <el-col :span="10">
        <p>
          顺应了从上至下的正常浏览顺序，方便浏览信息；顶部宽度限制了导航的数量和文本长度。
        </p>
      </el-col>
      <el-col :span="14">
        <img src="https://element.eleme.cn/2.13/static/navbar_0.b608f86.png" />
        <p>适用于导航较少，页面篇幅较长的网站。</p>
      </el-col>
    </el-row>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.nav-wrapper {
  padding-left: 55px;

  h2 {
    font-size: 28px;
    color: #1f2f3d;
    margin-bottom: 10px;
    font-weight: 400;
  }

  h3 {
    font-size: 22px;
    color: #1f2f3d;
    margin-bottom: 30px;
    font-weight: 400;
  }

  h5 {
    font-weight: 400;
  }

  p {
    color: #5e6d82;
    font-size: 14px;
    margin-bottom: 55px;
    line-height: 1.6;
  }

  .el-row {
    img {
      width: 100%;
      border: solid 15px #f9fcfa;
      margin-bottom: 15px;
    }
  }
}
</style>
