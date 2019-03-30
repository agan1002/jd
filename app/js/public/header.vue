<template>
  <div :class="$style.header">
    <span :class="$style.left">
      <em>登录</em>&nbsp;|&nbsp;<em>注册</em>
    </span>
    <btn :class="$style.btnDownload">App下载</btn>
  </div>
</template>

<script>
  import btn from '../core/btn'
  export default {
    components: {
      btn
    }
  }
</script>

<style lang="scss" module>
.header {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  height: 100px;
  line-height: 100px;
  font-size: 32px;
  color: #666;
  z-index: 100;
  background-color: #fff;
  .left {
    line-height: 30px;
    height: 30px;
    font-size: 28px;
    margin: 17px 0 0 18px;
  }
  .btnDownload {
    float: right;
    font-size: 24px;
    border-width: 0;
    height: 56px;
    line-height: 56px;
    min-width: 120px;
    margin: 28px 24px 0 0;
    border-radius: 4px;
    padding: 0;
  }
}
</style>
