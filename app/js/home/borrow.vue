<template>
  <Panel title="理财精选" :class="$style.panel">
    <section :class="$style.content">
      <router-link to="/home">
        <img src="https://img12.360buyimg.com/jrpmobile/jfs/t1/24958/23/5984/66824/5c466c74Eefe11794/234f78a6487d9130.jpg" alt="">
      </router-link>
    </section>
  </Panel>
</template>

<script>
  import Panel from '../core/panel'

  export default {
    name: "borrow",
    components: {
      Panel
    }
  }
</script>

<style lang="scss" module>
  @import "../../css/element";

  .panel {
    @include panel;
    .content {
      padding-bottom: 40px;
      img {
        display: block;
        width: 100%;
      }
    }
  }
</style>
