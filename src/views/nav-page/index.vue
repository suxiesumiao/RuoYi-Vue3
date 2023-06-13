<template>
  <div class="nav-page">
    <div class="container">
      <div class="link platform-center">
        <p>CIM 基础平台</p>
      </div>

      <div class="link middle-side data-center">
        <span>数据中台</span>
      </div>
      <div class="link middle-side service-center">
        <span>服务中台</span>
      </div>
      <div class="link middle-side share-center">
        <span>共享门户</span>
      </div>

      <div class="link right-side maintenance-basic">
        <span>基础运维</span>
      </div>
      <div class="link right-side project-management">
        <span>项目管理</span>
      </div>
      <div class="link right-side configuration-center">
        <span>配置中心</span>
      </div>
      <div class="link right-side monitoring-com">
        <span>运行监控</span>
      </div>
    </div>
  </div>
</template>
<script >
</script>
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

.container>.link {
  border-radius: 5px;
  cursor: pointer;
}

.platform-center {
  position: relative;
  grid-area: pc;
  background-color: #2a3a5b;

  &>p {
    font-size: 30px;
    font-weight: bold;
    color: #2ce7d3;
    background-color: rgba($color: #000000, $alpha: 0.2);
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
  background-color: tomato;
}

.service-center {
  grid-area: sc;
  background-color: steelblue;
}

.share-center {
  grid-area: cs;
  background-color: gold;
}

.maintenance-basic {
  grid-area: mb;
  background-color: aqua;
}

.configuration-center {
  grid-area: cc;
  background-color: aqua;
}

.project-management {
  grid-area: pm;
  background-color: aqua;
}

.monitoring-com {
  grid-area: mc;
  background-color: aqua;
}

.middle-side {
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 20px;
  color: #fff;
  background-color: #3ea7d7;
}

.right-side {
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 20px;
  color: #fff;
  background-color: #26a595;
}
</style>