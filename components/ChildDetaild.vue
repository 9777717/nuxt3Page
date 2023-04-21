<script setup lang="ts">
const childOrAdult = ref(true)
</script>
<template>
  <div class="ChildDetaild">
    <div class="bnDetail">
      <div>
        <el-switch
          v-model="childOrAdult"
          inline-prompt
          active-icon=""
          inactive-icon=""
        />
      </div>
      <div
        v-if="childOrAdult"
        :class="
          childOrAdult === true
            ? 'animate__animated animate__fadeInBottomRight'
            : 'animate__animated animate__fadeOutTopLeft'
        "
      >
        <ChildBannerChild />
      </div>
      <div
        v-else
        :class="
          childOrAdult === false
            ? 'animate__animated animate__fadeInBottomLeft'
            : 'animate__animated animate__fadeInLeftBig'
        "
      >
        <AdultBannerAdult />
      </div>
    </div>
    <div class="liveModel">
      <PageContentMyopia v-if="childOrAdult" />
      <PageContentMirrorMatching v-else />
    </div>
    <div class="ChildDetaild-w">
      <PageContentInfluenceCheck />
      <PageContentImageAd />
      <PageContentForm />
    </div>
  </div>
</template>

<style scoped lang="scss">
@media (min-width: 768px) {
  .ChildDetaild {
    overflow: hidden;
    width: 100%;
    position: relative;

    & > div {
      position: relative;
    }

    .bnDetail > div:nth-child(1) {
      position: absolute;
      top: 146px;
      z-index: 10;
      left: 47%;
    }
  }

  :deep(.el-switch__core) {
    background: #00a4ce;
    border: 14px solid #f6f6f6;
    box-shadow: inset 0px 0px 2.23138px 2.23138px rgba(0, 0, 0, 0.1),
      inset 0px 2.23138px 5.57846px 1.11569px rgba(0, 0, 0, 0.25);
    border-radius: 44.6277px;
    width: 162px;
    height: 83px;
    border-radius: 58px;
  }

  :deep(.el-switch.is-checked .el-switch__core) {
    background: #ffee54;
    box-shadow: inset 0px 0px 2.23138px 2.23138px rgba(0, 0, 0, 0.1),
      inset 0px 2.23138px 5.57846px 1.11569px rgba(0, 0, 0, 0.25);
    border-radius: 44.6277px;
    transform: matrix(-1, 0, 0, 1, 0, 0);
    border: 14px solid #f6f6f6;
  }
  :deep(.el-switch__core::before) {
    content: '';
    width: 40px;
    height: 40px;
    background: url('https://static.cmereye.com/imgs/2023/04/bbd64119a071aecd.png')
      no-repeat no-repeat;
    position: absolute;
    right: 80px;
    top: 12px;
  }
  :deep(.el-switch__core::after) {
    content: '';
    width: 40px;
    height: 40px;
    background: url('https://static.cmereye.com/imgs/2023/04/56577123ca0c1773.png')
      no-repeat no-repeat;
  }
  :deep(.el-switch__core .el-switch__action) {
    width: 58px;
    height: 58px;
    left: calc(100% - 58px);
  }
  :deep(.el-switch.is-checked .el-switch__core .el-switch__action) {
    transition: all 1s;
    left: calc(100% - 58px);
  }
  .ChildDetaild-w {
    z-index: 100;
    width: 884px;
    margin: auto;
    margin-top: 75px;
  }

  .liveModel {
    position: relative;
    z-index: 100;
    width: 884px;
    margin: auto;
    margin-top: -162px;
  }
}
</style>
