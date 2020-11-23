<template>
  <div class="home">
    <Swiper class="swiper-banner" :options="bannerSwiperOptions">
      <SwiperItem v-for="(item, index) in bannerImgs" :key="index" :style="{ background: 'url('+ item +') no-repeat center center' }"></SwiperItem>
    </Swiper>

    <div class="sub-wrap">
      <div class="emphasis-product">
        <h1>重点产品</h1>
        <div class="product">
          <div class="item">
            <div class="title">微服务应用平台</div>
            <div class="content">领先的Microservices应用平台微服务治理、集中式架构转型、轻松上云、业务快速创新</div>
            <div class="more"><span>了解更多</span></div>
          </div>
          <div class="item">
            <div class="title">大数据平台</div>
            <div class="content">可实时响应的集成架构 海量存储、高效计算的存储架构</div>
            <div class="more"><span>了解更多</span></div>
          </div>
          <div class="item">
            <div class="title">云应用平台</div>
            <div class="content">众多客户信赖的企业云应用平台 支持大型电信企业应用的开发与运行 支持企业客户提供开放能力</div>
            <div class="more"><span>了解更多</span></div>
          </div>
        </div>
      </div>
    </div>

    <div class="solution">
      <div class="sub-wrap">
        <h1>解决方案</h1>
        <div class="tabs">
          <div class="item" :class="[index === solutionTabsCur ? 'cur' : '']" v-for="(item, index) in solutionTabs" :key="index" @click="toSolutionIndex(index)">{{item}}</div>
        </div>
      </div>
    </div>
    <Swiper class="swiper-solution" :options="solutionSwiperOptions" ref="solutionSwiper">
      <SwiperItem v-for="(item, index) in solutionImgs" :key="index" :style="{ background: 'url('+ item +') no-repeat center center' }"></SwiperItem>
    </Swiper>

    <div class="binary">
      <div class="sub-wrap">
        <div class="number">
          <div class="item">
            <h2>41项</h2>
            <p>核心技术</p>
          </div>
          <div class="item">
            <h2>58项</h2>
            <p>发明专利</p>
          </div>
          <div class="item">
            <h2>11项</h2>
            <p>标准规范</p>
          </div>
          <div class="item">
            <h2>183项</h2>
            <p>软件著作权</p>
          </div>
        </div>
        <div class="content">
          <h2>为什么Hot是行业领导者</h2>
          <p>国产化核心技术能力</p>
        </div>
      </div>
    </div>

    <div class="sub-wrap">
      <div class="news-wrap">
        <h1>新闻动态</h1>
        <div class="news">
          <div class="item">
            <div class="title">
              <img src="http://www.shuhaosoft.com/images/pros1.png">
            </div>
            <div class="content">领先的Microservices应用平台微服务治理、集中式架构转型、轻松上云、业务快速创新</div>
          </div>
          <div class="item">
            <div class="title">
              <img src="http://www.shuhaosoft.com/images/pros2.png">
            </div>
            <div class="content">可实时响应的集成架构 海量存储、高效计算的存储架构</div>
          </div>
          <div class="item">
            <div class="title">
              <img src="http://www.shuhaosoft.com/images/pros3.png">
            </div>
            <div class="content">众多客户信赖的企业云应用平台 支持大型电信企业应用的开发与运行 支持企业客户提供开放能力</div>
          </div>
        </div>
      </div>
    </div>

  </div>
</template>

<script>
import { ref, reactive, onMounted } from 'vue'
import Swiper from '@/components/Swiper.vue'
import SwiperItem from '@/components/SwiperItem.vue'

export default {
  name: 'Home',
  components: {
    Swiper,
    SwiperItem
  },
  setup () {
    const bannerImgs = reactive([
      'http://www.primeton.com/images/banner2_0414.png',
      'http://www.primeton.com/images/banner2_0414.png',
      'http://www.primeton.com/images/banner2_0414.png'
    ])

    const bannerSwiperOptions = reactive({
      height: 360,
      swiperOptions: {
        autoplay: true,
        loop: true,
        pagination: {
          el: '.swiper-pagination'
        },
        navigation: {
          nextEl: '.swiper-button-next',
          prevEl: '.swiper-button-prev'
        }
      }
    })

    const solutionImgs = reactive([
      'http://www.primeton.com/images/in_tabpic1.png',
      'http://www.primeton.com/images/in_tabpic1.png',
      'http://www.primeton.com/images/in_tabpic1.png',
      'http://www.primeton.com/images/in_tabpic1.png',
      'http://www.primeton.com/images/in_tabpic1.png',
      'http://www.primeton.com/images/in_tabpic1.png'
    ])

    const solutionTabs = reactive([
      '金融', '政府', '运营商', '教育', '发电', '广电'
    ])

    const solutionTabsCur = ref(0)
    const solutionSwiperOptions = reactive({
      height: 400,
      hideNavButton: true,
      isDisableDrag: true
    })

    const solutionSwiper = ref(null)

    onMounted(() => {

    })

    const toSolutionIndex = (index) => {
      solutionTabsCur.value = index
      const solutionSwiperObj = solutionSwiper.value.swiper
      solutionSwiperObj.slideTo(index)
    }

    return {
      bannerImgs,
      bannerSwiperOptions,
      solutionImgs,
      solutionSwiperOptions,
      solutionTabs,
      solutionTabsCur,
      solutionSwiper,
      toSolutionIndex
    }
  }
}
</script>

<style lang="scss" scoped>
.emphasis-product {
  h1 {
    font-size: 32px;
    height: 100px;
    line-height: 100px;
  }
  .product {
    -webkit-display: flex;
    display: flex;
    justify-content: space-between;

    .item {
      width: 390px;
      background-color: #fff;
      padding: 40px;
      border-radius: 4px;

      .title {
        font-size: 24px;
      }

      .content {
        font-size: 16px;
        color: #747474;
        margin-top: 20px;
        line-height: 24px;
        min-height: 72px;
      }

      .more {
        span {
          width: 140px;
          height: 48px;
          line-height: 48px;
          text-align: center;
          font-size: 16px;
          display: block;
          border-radius: 24px;
          border: 1px solid #8a939b;
          color: #8a939b;
          margin-top: 30px;
          cursor: pointer;

          &:hover {
            background-color: #4466ff;
            border: 1px solid #4466ff;
            color: #fff;
          }
        }
      }
    }
  }
}

.solution {
  background-color: #fff;
  margin-top: 50px;

  .sub-wrap {
    -webkit-display: flex;
    display: flex;
    -webkit-align-items: center;
    align-items: center;
    -webkit-justify-content: space-between;
    justify-content: space-between;

    h1 {
      font-size: 32px;
      height: 100px;
      line-height: 100px;
    }

    .tabs {
      -webkit-display: flex;
      display: flex;

      .item {
        font-size: 16px;
        margin-left: 40px;
        padding: 0 30px;
        height: 40px;
        line-height: 36px;
        text-align: center;
        border-radius: 20px;
        border: 1px solid #333;
        cursor: pointer;

        &.cur {
          background-color: #4466ff;
          border: 1px solid #4466ff;
          color: #fff;
        }
      }
    }
  }
}

.binary {
  background: #fff url("http://www.primeton.com/images/binary.png") no-repeat
    center center;
  height: 400px;

  .sub-wrap {
    -webkit-display: flex;
    display: flex;
    .number {
      width: 50%;
      margin-top: 50px;
      -webkit-display: flex;
      display: flex;
      -webkit-flex-wrap: wrap;
      flex-wrap: wrap;
      .item {
        width: 50%;
        height: 150px;
        -webkit-display: flex;
        display: flex;
        -webkit-align-items: center;
        align-items: center;
        -webkit-justify-content: center;
        justify-content: center;
        -webkit-flex-direction: column;
        flex-direction: column;

        h2 {
          font-size: 48px;
          font-weight: bold;
          color: #4466ff;
        }

        p {
          font-size: 16px;
          color: #666;
        }
      }
    }

    .content {
      width: 50%;
      -webkit-display: flex;
      display: flex;
      -webkit-align-items: center;
      align-items: center;
      -webkit-justify-content: center;
      justify-content: center;
      -webkit-flex-direction: column;
      flex-direction: column;

      h2 {
        font-size: 36px;
        font-weight: bold;
      }

      p {
        font-size: 18px;
        color: #666;
        margin-top: 20px;
      }
    }
  }
}

.news-wrap {
  margin-bottom: 40px;
  h1 {
    font-size: 32px;
    height: 100px;
    line-height: 100px;
  }
  .news {
    -webkit-display: flex;
    display: flex;
    justify-content: space-between;

    .item {
      width: 390px;
      background-color: #fff;
      padding: 20px;
      border-radius: 4px;

      .title {
        font-size: 24px;
      }

      .content {
        font-size: 16px;
        color: #333;
        margin-top: 10px;
        line-height: 24px;
        min-height: 48px;
      }

      .more {
        span {
          width: 140px;
          height: 48px;
          line-height: 48px;
          text-align: center;
          font-size: 16px;
          display: block;
          border-radius: 24px;
          border: 1px solid #8a939b;
          color: #8a939b;
          margin-top: 30px;
          cursor: pointer;

          &:hover {
            background-color: #4466ff;
            border: 1px solid #4466ff;
            color: #fff;
          }
        }
      }
    }
  }
}
</style>
