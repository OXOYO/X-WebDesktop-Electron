/**
* Created by OXOYO on 2018/5/4.
*
*/

<style scoped lang="less" rel="stylesheet/less">
  .title-btn {
    display: none;
    width: 20px;
    height: 20px;
    text-align: center;
    vertical-align: top;
    color: #ffffff;
    -webkit-app-region: no-drag;

    &:hover {
      color: #2d8cf0;
    }
  }
</style>

<template>
  <div class="title-btn" :style="style" @click.stop.prevent="handleTrigger">
    <Icon :type="iconMap[action]"></Icon>
  </div>
</template>

<script>
  import { remote } from 'electron'

  export default {
    name: 'TitleBtn',
    props: {
      action: {
        type: String,
        required: true
      }
    },
    data () {
      return {
        iconMap: {
          min: 'minus',
          max: 'android-checkbox-outline-blank',
          rest: 'ios-browsers-outline',
          close: 'close'
        },
        styleMap: {
          min: {
            backgroundColor: 'green',
            right: '100px'
          },
          max: {
            backgroundColor: 'yellow',
            right: '60px'
          },
          close: {
            backgroundColor: 'black',
            right: '20px'
          }
        }
      }
    },
    computed: {
      style: function () {
        let _t = this
        return _t.styleMap[_t.type]
      }
    },
    methods: {
      handleTrigger: function () {
        let _t = this
        // 获取当前窗口
        let win = remote.getCurrentWindow()
        switch (_t.action) {
          case 'min':
            win.minimize()
            break
          case 'max':
            if (win.isMaximized()) {
              win.unmaximize()
            } else {
              win.maximize()
            }
            break
          case 'close':
            win.close()
            break
        }
      }
    }
  }
</script>
