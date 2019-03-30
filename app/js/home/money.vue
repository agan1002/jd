<template>
  <Panel title="理财精选" :class="$style.panel">
    <section :class="$style.content">
      <dl v-for="item in items" :key="item.title" :class="$style.item">
        <dt>{{item.title}}<span>{{item.sub}}</span></dt>
        <dd :class="$style.red">{{item.rate}}</dd>
        <dd :class="$style.gray">{{item.text}}</dd>
      </dl>
    </section>
  </Panel>
</template>

<script>
  import Panel from '../core/panel'
  export default {
    name: "money",
    components: {
      Panel
    },
    data () {
      return {
        items: [
          {
            title: '长乐盈',
            sub: '180天可质押',
            rate: '5.80%',
            text: '近1年历史年化回报率'
          },
          {
            title: '京智0号',
            sub: '大数据赋能',
            rate: '6.00%',
            text: '近1月历史年化投资回报率'
          },
          {
            title: '建信养老飞益鑫',
            sub: '1000起投',
            rate: '4.57%',
            text: '近7日年化收益率'
          },
          {
            title: '小白基金',
            sub: '超短期',
            rate: '4.50%',
            text: '近7日年化收益率'
          }
        ]
      }
    }
  }
</script>

<style lang="scss" module>
@import "../../css/element";
  .panel {
    @include panel;
    .content {
      @include list(row);
      width: 100%;
      .item {
        width: 50%;
        height: 218px;
        padding-left: 32px;
        box-sizing: border-box;
        dt {
          font-size: 30px;
          color: #333;
          font-weight: 700;
          height: 42px;
          line-height: 42px;
          span {
            color: #ff5155;
            height: 34px;
            line-height: 34px;
            padding: 0 4px;
            font-size: 22px;
            border: 1px solid #ff5155;
            position: relative;
            left: 8px;
            top: -2px;
          }
        }
        .red {
          font-size: 44px;
          color: #ff5155;
          height: 58px;
          line-height: 58px;
        }
        .gray {
          font-size: 24px;
          color: #999;
          height: 34px;
          line-height: 34px;
        }
      }
    }
  }
</style>
