<template>
  <div class="nav-page">
    <div class="container">
      <div class="link platform-center">
        <p>CIM 基础平台</p>
      </div>

      <div class="link middle-side data-center">
        <svg class="link-icon" aria-hidden="true">
          <use xlink:href="#icon-cim-pcm"></use>
        </svg>
        <span>数据中台</span>
      </div>
      <div class="link middle-side service-center">
        <svg class="link-icon" aria-hidden="true">
          <use xlink:href="#icon-cim-export-service"></use>
        </svg>
        <span>服务中台</span>
      </div>
      <div class="link middle-side share-center">
        <svg class="link-icon" aria-hidden="true">
          <use xlink:href="#icon-cim-link"></use>
        </svg>
        <span>共享门户</span>
      </div>

      <div class="link right-side maintenance-basic">
        <svg class="link-icon" aria-hidden="true">
          <use xlink:href="#icon-cim-sales-center"></use>
        </svg>
        <span>基础运维</span>
      </div>
      <div class="link right-side project-management">
        <svg class="link-icon" aria-hidden="true">
          <use xlink:href="#icon-cim-product-filter"></use>
        </svg>
        <span>项目管理</span>
      </div>
      <div class="link right-side configuration-center">
        <svg class="link-icon" aria-hidden="true">
          <use xlink:href="#icon-cim-settings"></use>
        </svg>
        <span>配置中心</span>
      </div>
      <div class="link right-side monitoring-com">
        <svg class="link-icon" aria-hidden="true">
          <use xlink:href="#icon-cim-video"></use>
        </svg>
        <span>运行监控</span>
      </div>
    </div>
  </div>
</template>
<script></script>
<style lang="scss" scoped>
.nav-page {
  height: 100%;
  padding: 10px;
  background-size: cover;
  background-position-y: -350px;
}

.container {
  height: 400px;
  display: grid;
  grid-template-columns: repeat(14, 1fr);
  grid-template-rows: repeat(6, 1fr);
  grid-gap: 10px 10px;
  grid-template-areas:
    "pc pc pc pc pc dc dc dc mb mb mb cc cc cc"
    "pc pc pc pc pc dc dc dc mb mb mb cc cc cc"
    "pc pc pc pc pc sc sc sc mb mb mb cc cc cc"
    "pc pc pc pc pc sc sc sc pm pm pm mc mc mc"
    "pc pc pc pc pc cs cs cs pm pm pm mc mc mc"
    "pc pc pc pc pc cs cs cs pm pm pm mc mc mc";
}

.container > .link {
  border-radius: 5px;
  font-weight: bolder;
  cursor: pointer;
  & > .link-icon {
    width: 3em; height: 3em;
    vertical-align: -0.15em;
    fill: currentColor;
    overflow: hidden;
    padding: 10px;
    background-color: rgba($color: #000, $alpha: 0.2);
    // border: 1px solid rgba($color: #fff, $alpha: 0.4);
    border-radius: 50%;
  }
  & > span {
    text-shadow: 2px -2px 2px #000000;
  }
}

.platform-center {
  position: relative;
  grid-area: pc;
  background-color: #2a3a5b;
  background-image: url(@/assets/images/cim-bg.png);
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center;

  & > p {
    font-size: 30px;
    font-weight: bold;
    color: #2ce7d3;
    background-color: rgba($color: #000, $alpha: 0.2);
    margin: 0;
    line-height: 2;
    text-align: center;
    position: absolute;
    width: 100%;
    bottom: 0;
  }
}

.data-center {
  grid-area: dc;
}

.service-center {
  grid-area: sc;
}

.share-center {
  grid-area: cs;
}

.maintenance-basic {
  grid-area: mb;
}

.configuration-center {
  grid-area: cc;
}

.project-management {
  grid-area: pm;
}

.monitoring-com {
  grid-area: mc;
}

.middle-side {
  display: flex;
  justify-content: space-around;
  align-items: center;
  font-size: 20px;
  color: #fff;
  background-color: #3ea7d7;
}

.right-side {
  display: flex;
  justify-content: space-around;
  align-items: center;
  font-size: 20px;
  color: #fff;
  background-color: #26a595;
}
</style>
