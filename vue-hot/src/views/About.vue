<template>
  <div class="about">
    <div class="banner"></div>

    <div class="sub-wrap">
      <div class="introduction">
        <h1>武汉霍特科技有限公司</h1>
        <p>北京数浩科技有限公司（简称数浩科技）为国家级高新技术企业，成立于2008年1月，是一家以技术为核心竞争力的金融科技公司，致力于为金融机构提供平民化的数据应用软件。公司目前以DVLINK（数浩金融业监管合规应用套件）为基础，专注于为金融机构提供监管合规类软件产品和技术服务，公司总部位于北京，在重庆设有研发中心。</p>
        <p>自成立以来，数浩科技一直专注于金融行业和数据应用领域，以“让数据应用平民化”为使命，坚持技术为本和自主研发，与大型金融机构、股份制银行、农村商业银行和城市商业银行等行业标杆企业建立了长期和深入的合作关系，积累了丰富的数据应用类软件解决方案和实施经验，形成了完备的金融数据模型和品类齐全的数据管理和应用软件。</p>
        <p>为了全面聚焦监管合规应用，数浩科技研发团队对公司产品进行了大规模的整合、升级和转型，正式发布DVLINK（数浩金融业监管合规应用套件）。DVLINK为新一代监管合规应用套件，打通监管数据、监管报表、数据分析、数据质量、风险监测等监管合规业务的方方面面，全面提升金融机构监管合规业务的弹性和敏捷性。</p>
        <p>面向未来，数浩科技将始终坚持技术为本、专业专注和持续创新，踏踏实实，不走捷径，厚积薄发，做实、做精、做强产品和服务，为客户创造真正价值，为员工提供广阔舞台。</p>
      </div>

      <div class="culture">
        <h1>企业文化</h1>
        <div class="content">
          <div class="item">
            <div class="icon">
              <img src="http://www.shuhaosoft.com/images/about1.png">
            </div>
            <div class="title">公司使命</div>
            <div class="description">让数据应用平民化</div>
          </div>
          <div class="item">
            <div class="icon">
              <img src="http://www.shuhaosoft.com/images/about2.png">
            </div>
            <div class="title">公司愿景</div>
            <div class="description">数据应用软件领导品牌</div>
          </div>
          <div class="item">
            <div class="icon">
              <img src="http://www.shuhaosoft.com/images/about3.png">
            </div>
            <div class="title">价值观</div>
            <div class="description">诚信、求实、创新、共赢</div>
          </div>
          <div class="item">
            <div class="icon">
              <img src="http://www.shuhaosoft.com/images/about4.png">
            </div>
            <div class="title">经营理念</div>
            <div class="description">技术为本、专业专注</div>
          </div>
          <div class="item">
            <div class="icon">
              <img src="http://www.shuhaosoft.com/images/about5.png">
            </div>
            <div class="title">管理理念</div>
            <div class="description">无为而治、极简敏捷</div>
          </div>
        </div>
      </div>

    </div>
  </div>
</template>

<style lang="scss" scoped>
.banner {
  height: 500px;
  background: url("http://www.shuhaosoft.com/images/about_banner.png") no-repeat
    center center;
}

.sub-wrap {
  margin-top: -80px;

  .introduction {
    background-color: #4466ff;
    color: #fff;
    padding: 50px;

    h1 {
      text-align: center;
      font-size: 24px;
      margin-bottom: 30px;
      font-weight: bold;
    }

    p {
      line-height: 30px;
      text-indent: 2em;
      margin-top: 20px;
    }
  }

  .culture {
    margin-bottom: 50px;
    h1 {
      height: 120px;
      line-height: 120px;
      text-align: center;
      font-weight: bold;
      margin-top: 30px;
    }

    .content {
      -webkit-display: flex;
      display: flex;

      .item {
        -webkit-flex: 1;
        flex: 1;
        -webkit-display: flex;
        display: flex;
        align-items: center;
        justify-content: center;
        flex-direction: column;

        .title {
          margin-top: 10px;
          font-weight: bold;
        }

        .description {
          margin-top: 10px;
          font-size: 14px;
        }
      }
    }
  }
}
</style>
