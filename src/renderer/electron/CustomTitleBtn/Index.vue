/**
* Created by OXOYO on 2018/5/4.
*
* 自定义标题栏按钮
*/

<style lang="less" rel="stylesheet/less">
  .custom-title-btn {
    position: absolute;
    width: 100%;
    height: 30px;
    line-height: 30px;
    background-color: transparent;
    margin-top: 2px;
    z-index: 1500;
    top: 0;
    left: 0;
    right: 0;
    writing-mode: horizontal-tb;
    -webkit-app-region: drag;

    .title-btn-block {
      position: absolute;
      top: 0;
      right: 0;
      min-width: 200px;
      height: 100%;
      line-height: 30px;
      padding: 0 15px;
      text-align: right;
      -webkit-app-region: no-drag;

      &:hover {
        .title-btn {
          display: inline-block;
        }
      }
    }
  }
</style>

<template>
  <div class="custom-title-btn" @contextmenu.stop.prevent>
    <div class="title-btn-block">
      <TitleBtn action="min"></TitleBtn>
      <TitleBtn action="max"></TitleBtn>
      <TitleBtn action="close"></TitleBtn>
    </div>
  </div>
</template>

<script>
  import TitleBtn from './components/TitleBtn.vue'

  export default {
    name: 'CustomTitleBtn',
    components: {
      TitleBtn
    }
  }
</script>
