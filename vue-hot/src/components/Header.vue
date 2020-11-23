<template>
  <div class="header-warp">
    <div class="header">
      <div class="sub-wrap">
        <div class="logo">
          <img src="http://www.primeton.com/images/logo.png">
        </div>
        <div class="nav">
          <ul>
            <li v-for="(item, index) in nav" :key="index" :class="[index === navCurrent ? 'cur' : '']" @click="toNext(item.linkTo)" @mouseenter="enter(index)" @mouseleave="leave()">{{item.text}}</li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { ref, reactive } from 'vue'
import { useRouter } from 'vue-router'
export default {
  name: 'Header',
  setup () {
    const nav = reactive([
      {
        linkTo: '/',
        text: '首页'
      },
      {
        linkTo: '/',
        text: '软件基础平台'
      },
      {
        linkTo: '/',
        text: '解决方案'
      },
      {
        linkTo: '/',
        text: '服务支持'
      },
      {
        linkTo: '/news',
        text: '新闻'
      },
      {
        linkTo: '/about',
        text: '关于霍特'
      }
    ])

    const navCurrent = ref(0)

    const router = useRouter()

    const enter = (index) => {
      navCurrent.value = index
    }

    const leave = () => {
      navCurrent.value = null
    }

    const toNext = (url) => {
      router.push(url)
    }

    return {
      nav,
      navCurrent,
      toNext,
      enter,
      leave
    }
  }
}
</script>

<style lang="scss">
.header-warp {
  width: 100%;
  height: 64px;

  .header {
    width: 100%;
    background-color: #fff;
    height: 64px;
    position: fixed;
    left: 0;
    top: 0;
    z-index: 99;

    .sub-wrap {
      -webkit-display: flex;
      display: flex;
      .logo {
        width: 200px;
        -webkit-display: flex;
        display: flex;
        align-items: center;
      }
      .nav {
        flex: 1;

        ul {
          -webkit-display: flex;
          display: flex;
          -webkit-justify-content: flex-end;
          justify-content: flex-end;

          li {
            height: 64px;
            line-height: 60px;
            padding: 0 20px;
            border-top: 4px #fff solid;
            cursor: pointer;

            &.cur {
              background-color: #f5f5f5;
              border-top: 4px #4466ff solid;
              color: #4466ff;
            }
          }
        }
      }
    }
  }
}
</style>
