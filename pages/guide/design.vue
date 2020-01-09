<template>
  <div class="design-wrapper">
    <h2>设计原则</h2>
    <div class="cards">
      <div v-for="item of cards" :key="item.title" class="card">
        <img :src="item.url" class="card-img" />
        <h4>{{ item.title }}</h4>
        <span>{{ item.desc }}</span>
      </div>
    </div>
    <div class="detail">
      <h3>一致性 Consistency</h3>
      <ul>
        <li>
          <strong>与现实生活一致: </strong>
          <span
            >与现实生活的流程、逻辑保持一致，遵循用户习惯的语言和概念；</span
          >
        </li>
        <li>
          <strong>在界面中一致: </strong>
          <span
            >所有的元素和结构需保持一致，比如：设计样式、图标和文本、元素的位置等。</span
          >
        </li>
      </ul>
      <h3>反馈 Feedback</h3>
      <ul>
        <li>
          <strong>控制反馈: </strong>
          <span>通过界面样式和交互动效让用户可以清晰的感知自己的操作；</span>
        </li>
        <li>
          <strong>页面反馈: </strong>
          <span>操作后，通过页面元素的变化清晰地展现当前状态。</span>
        </li>
      </ul>

      <h3>效率 Efficiency</h3>
      <ul>
        <li>
          <strong>简化流程：</strong>
          <span>设计简洁直观的操作流程；</span>
        </li>
        <li>
          <strong>清晰明确: </strong>
          <span>语言表达清晰且表意明确，让用户快速理解进而作出决策；</span>
        </li>
        <li>
          <strong>帮助用户识别: </strong>
          <span>界面简单直白，让用户快速识别而非回忆，减少用户记忆负担。</span>
        </li>
      </ul>
      <h3>可控 Controllability</h3>
      <ul>
        <li>
          <strong>用户决策: </strong>
          <span
            >根据场景可给予用户操作建议或安全提示，但不能代替用户进行决策；</span
          >
        </li>
        <li>
          <strong>结果可控: </strong>
          <span>用户可以自由的进行操作，包括撤销、回退和终止当前操作等。</span>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      cards: [
        {
          url: '/Consistency.png',
          title: '一致',
          desc: 'Consistency'
        },
        {
          url: '/Feedback.png',
          title: '反馈',
          desc: 'Feedback'
        },
        {
          url: '/Efficiency.png',
          title: '效率',
          desc: 'Efficiency'
        },
        {
          url: '/Controllability.png',
          title: '可控',
          desc: 'Controllability'
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.design-wrapper {
  padding-left: 60px;

  h2 {
    font-size: 28px;
    font-weight: 400;
    color: #1f2f3d;
  }

  .cards {
    display: flex;
    margin: 30px -7px 70px;

    .card {
      flex: 1;
      text-align: center;
      height: 210px;
      background: #fbfcfd;
      margin: 0 7px;

      .card-img {
        width: 80px;
        margin: 40px 0 25px;
      }

      h4 {
        font-size: 18px;
        color: #1f2f3d;
        font-weight: 400;
      }

      span {
        font-size: 14px;
        color: #99a9bf;
      }
    }
  }

  .detail {
    h3 {
      color: #1f2d3d;
      font-size: 22px;
      font-weight: 400;
      margin-bottom: 30px;
    }

    ul {
      padding-left: 0;
      margin-bottom: 50px;

      li {
        color: #99a9bf;
        font-size: 14px;
        margin-bottom: 10px;

        &::before {
          content: '';
          display: inline-block;
          width: 4px;
          height: 4px;
          border-radius: 50%;
          vertical-align: middle;
          background-color: #5e6d82;
          margin-right: 5px;
        }

        strong {
          color: #5e6d82;
          font-weight: 400;
        }
      }
    }
  }
}
</style>
