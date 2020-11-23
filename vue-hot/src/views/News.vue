<template>
  <div class="about">
    <div class="banner"></div>

    <div class="sub-wrap">
      <div class="news">
        <div class="item">
          <div class="img">
            <img src="http://www.shuhaosoft.com/images/dynamic1.png">
          </div>
          <div class="info">
            <div class="title">
              <h1>DVLink（数浩金融业监管合规应用套件）--打通监管合规业务方方面面</h1>
              <span>2020/05/31</span>
            </div>
            <div class="content">
              DVLink是数浩科技推出的新一代监管合规应用套件，打通监管数据、监管报表、数据分析、数据质量、风险监测等监管合规业务的方方面面，全面提升金融机构监管合规业务的弹性和敏捷性。 与传统监管合规应用软件相比，DVLink在监管报表数样分离、监管数据可视化分析、监管数据质量监测、合规风险监测等诸多领域实现技术突破和创新，打破数据、指标、报表、报文、分析、监测等之间的耦合和藩篱，赋能金融机构更加快速地编报监管报表，更加充分地发挥监管数据价值，更加敏捷和准确地检查监管数据质量，更加及时和深入地预警合规风险，更加高效地生产高数据质量的监管指标。
            </div>
            <div class="btn">
              <span @click="toNewsDetail">了解详情</span>
            </div>
          </div>
        </div>
        <div class="item">
          <div class="img">
            <img src="http://www.shuhaosoft.com/images/dynamic1.png">
          </div>
          <div class="info">
            <div class="title">
              <h1>DVLink（数浩金融业监管合规应用套件）--打通监管合规业务方方面面</h1>
              <span>2020/05/31</span>
            </div>
            <div class="content">
              DVLink是数浩科技推出的新一代监管合规应用套件，打通监管数据、监管报表、数据分析、数据质量、风险监测等监管合规业务的方方面面，全面提升金融机构监管合规业务的弹性和敏捷性。 与传统监管合规应用软件相比，DVLink在监管报表数样分离、监管数据可视化分析、监管数据质量监测、合规风险监测等诸多领域实现技术突破和创新，打破数据、指标、报表、报文、分析、监测等之间的耦合和藩篱，赋能金融机构更加快速地编报监管报表，更加充分地发挥监管数据价值，更加敏捷和准确地检查监管数据质量，更加及时和深入地预警合规风险，更加高效地生产高数据质量的监管指标。
            </div>
            <div class="btn">
              <span @click="toNewsDetail">了解详情</span>
            </div>
          </div>
        </div>
        <div class="item">
          <div class="img">
            <img src="http://www.shuhaosoft.com/images/dynamic1.png">
          </div>
          <div class="info">
            <div class="title">
              <h1>DVLink（数浩金融业监管合规应用套件）--打通监管合规业务方方面面</h1>
              <span>2020/05/31</span>
            </div>
            <div class="content">
              DVLink是数浩科技推出的新一代监管合规应用套件，打通监管数据、监管报表、数据分析、数据质量、风险监测等监管合规业务的方方面面，全面提升金融机构监管合规业务的弹性和敏捷性。 与传统监管合规应用软件相比，DVLink在监管报表数样分离、监管数据可视化分析、监管数据质量监测、合规风险监测等诸多领域实现技术突破和创新，打破数据、指标、报表、报文、分析、监测等之间的耦合和藩篱，赋能金融机构更加快速地编报监管报表，更加充分地发挥监管数据价值，更加敏捷和准确地检查监管数据质量，更加及时和深入地预警合规风险，更加高效地生产高数据质量的监管指标。
            </div>
            <div class="btn">
              <span @click="toNewsDetail">了解详情</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { useRouter } from 'vue-router'
export default {
  name: 'Header',
  setup () {
    const router = useRouter()
    const toNewsDetail = () => {
      let toUrl = router.resolve({
        name: 'NewsDetail',
        params: { id: 1 }
      })

      window.open(toUrl.href, '_blank');
    }

    return {
      toNewsDetail
    }
  }
}
</script>

<style lang="scss" scoped>
.banner {
  height: 410px;
  background: url("http://www.shuhaosoft.com/images/dynamic_banner.png")
    no-repeat center center;
}

.news {
  margin: 30px 0;
  .item {
    -webkit-display: flex;
    display: flex;
    padding: 30px 0;
    border-bottom: #ddd 1px solid;

    &:last-child {
      border: none;
    }

    .img {
      width: 330px;
      height: 210px;
    }

    .info {
      margin-left: 30px;
      -webkit-flex: 1;
      flex: 1;

      .title {
        -webkit-display: flex;
        display: flex;
        -webkit-align-items: center;
        align-items: center;

        h1 {
          font-size: 20px;
          -webkit-flex: 1;
          flex: 1;
          font-weight: bold;
        }

        span {
          font-size: 14px;
        }
      }

      .content {
        font-size: 16px;
        margin-top: 10px;
        height: 126px;
      }

      .btn {
        margin-top: 10px;
        text-align: right;

        span {
          display: inline-block;
          background-color: #4466ff;
          color: #fff;
          font-size: 16px;
          width: 84px;
          height: 36px;
          line-height: 36px;
          text-align: center;
          border-radius: 2px;
          cursor: pointer;
        }
      }
    }
  }
}
</style>
