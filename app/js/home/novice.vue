<template>
  <Panel title="新手特权" :class="$style.panel">
    <section :class="$style.content">
      <div :class="$style.item">
        <h4>下载Apps<span :class="$style.red">送888元礼包</span></h4>
        <p :class="$style.gray">新手专享</p>
        <img src="https://img12.360buyimg.com/jrpmobile/jfs/t27334/12/1829630702/5159/f8133cd6/5bee6bbdN8606cfbb.png">
      </div>
      <div :class="$style.item">
        <ul>
          <li>
            <img src="//img12.360buyimg.com/jrpmobile/jfs/t1/19965/4/1946/28370/5c18958aE9e8a930d/9810bed7979e6bd5.jpg">
            <h4 :class="$style.red">领128元新手礼包</h4>
            <p :class="$style.gray">立即开通</p>
          </li>
          <li>
            <img src="https://img12.360buyimg.com/jrpmobile/jfs/t1/27014/35/2022/24897/5c1895d9Ef095679a/c0918d244bbfb2e5.jpg">
            <h4>打白条<span :class="$style.red">享免息</span></h4>
            <p :class="$style.gray">立即开通享豪礼</p>
          </li>
        </ul>
      </div>
    </section>
  </Panel>
</template>

<script>
  import Panel from '../core/panel'
  export default {
    name: "Novice",
    components: {
      Panel
    }
  }
</script>

<style lang="scss" module>
@import "../../css/element";
  .panel {
    @include panel;
    >h4 {
      border-bottom: 1px solid #ddd;
    }
    .content {
      @include list(row);
      .item {
        width: 50%;
        box-sizing: border-box;
        &:first-child {
          padding: 32px 20px;
          text-align: center;
          border-right: 1px solid #ddd;
          img {
            width: 132px;
            height: 132px;
            margin: 20px auto 0;
          }
        }
        h4 {
          font-size: 24px;
          line-height: 40px;
        }
        .red {
          color: #ff0000;
        }
        .gray {
          color: #999;
          font-size: 24px;
        }
        ul {
          width: 100%;
          li {
            width: 100%;
            height: 144px;
            padding: 32px 28px;
            box-sizing: border-box;
            &:first-child {
              border-bottom: 1px solid #ddd;
            }
            h4 {
              overflow: hidden;
              text-overflow: ellipsis;
              white-space: nowrap;
            }
            img {
              float: right;
              height: 80px;
              width: 80px;
            }
          }
        }
      }
    }
  }
</style>
