<script setup lang="ts">
const childOrAdult = ref(true)
// const btnBarBg = () => {
// }
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
      <!-- <div class="box" @click="btnBarBg">
        <div :class="childOrAdult === true ? 'boxChild1' : 'boxChild2'">
          <div></div>
        </div>
        <div class="btnChild"></div>
        <div class="bgImghChild">
          <img
            :style="[{ opacity: childOrAdult === true ? '1' : '0.3' }]"
            src="https://static.cmereye.com/imgs/2023/04/f819f1f6ddb97db2.png"
            alt=""
          />
          <img
            :style="[{ opacity: childOrAdult === false ? '1' : '0.3' }]"
            src="https://static.cmereye.com/imgs/2023/04/ce0a52541ca1f2f9.png"
            alt=""
          />
        </div>
      </div> -->
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
    <PageRhomboidTop
      :style-rhom="{
        top: '650px',
        height: '342px',
        transform: 'skewY(348deg)',
        background: '#fff',
      }"
    />
    <PageRhomboidTop
      :style-rhom="{
        top: '2110px',
        height: '342px',
        transform: 'skewY(13deg)',
        background: childOrAdult === true ? '#FFF8B9' : '#C2EAF2',
      }"
    />
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
  .box {
    position: absolute;
    top: 240px;
    z-index: 10;
    left: 47%;

    width: 162px;
    height: 84px;
    background: linear-gradient(
      180deg,
      #e9e9e9 0%,
      #e9e9e9 0.01%,
      #ffffff 100%
    );
    box-shadow: inset 0px 0px 4.46277px rgba(0, 0, 0, 0.05);
    border-radius: 58.016px;
    transform: matrix(-1, 0, 0, 1, 0, 0);
  }
  .box:hover {
    cursor: pointer;
  }

  .boxChild1 {
    background: #ffee54;
    width: 135.36px;
    height: 56.22px;
    box-shadow: inset 0px 0px 2.23138px 2.23138px rgba(0, 0, 0, 0.1),
      inset 0px 2.23138px 5.57846px 1.11569px rgba(0, 0, 0, 0.25);
    border-radius: 44.6277px;
    transform: matrix(-1, 0, 0, 1, 0, 0);
    position: absolute;
    left: 13.4px;
    right: -121.97px;
    top: 13.39px;
    bottom: 13.39px;
  }
  .boxChild2 {
    background: #00a4ce;
    width: 135.36px;
    height: 56.22px;
    box-shadow: inset 0px 0px 2.23138px 2.23138px rgba(0, 0, 0, 0.1),
      inset 0px 2.23138px 5.57846px 1.11569px rgba(0, 0, 0, 0.25);
    border-radius: 44.6277px;
    transform: matrix(-1, 0, 0, 1, 0, 0);
    position: absolute;
    left: 13.4px;
    right: -121.97px;
    top: 13.39px;
    bottom: 13.39px;
  }
  .btnChild {
    position: relative;
    width: 58px;
    height: 58px;
    background: linear-gradient(180deg, #eaeaea 0%, #ffffff 100%);
    box-shadow: 0px 0px 4.46277px rgba(0, 0, 0, 0.1),
      0px 6.69415px 6.69415px -1.11569px rgba(0, 0, 0, 0.25);
    transform: matrix(-1, 0, 0, 1, 0, 0);
    border-radius: 44.6277px;
    position: absolute;
    top: 12px;
    left: 91px;
  }
  .bgImghChild {
    position: relative;
    top: 12px;
    left: 15px;
  }
  .bgImghChild > img:nth-child(1) {
    position: absolute;
    opacity: 0.3;
    width: 33px;
    height: 36px;
    top: 12px;
    left: 91px;
  }
  .bgImghChild > img:nth-child(2) {
    position: absolute;
    opacity: 0.3;
    width: 32px;
    height: 31px;
    top: 12px;
    left: 10px;
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
