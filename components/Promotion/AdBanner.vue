<template>
  <div class="adBanner">
    <div>
      <img
        src="https://static.cmereye.com/imgs/2023/04/eb53f7fcfe6ea309.png"
        alt=""
      />
    </div>
    <div></div>
    <div>最新推廣</div>
    <div></div>
  </div>
</template>

<style scoped lang="scss">
@media (min-width: 768px) {
  .adBanner {
    position: relative;
    width: 100%;
    margin-top: 84px;

    & > div:nth-child(3) {
      position: absolute;
      top: 110px;
      left: 275px;
      font-family: 'Noto Sans CJK TC';
      font-style: normal;
      font-weight: 700;
      font-size: 150px;
      line-height: 222px;
      text-align: center;
      letter-spacing: 0.1em;

      /* 白色 */

      color: #ffffff;

      /* Soft Shadow */

      text-shadow: 4px 4px 4px rgba(0, 0, 0, 0.1);
    }

    & > div:nth-child(2) {
      position: absolute;
      bottom: 330px;
      left: 0;
      width: 1020px;
      height: 82px;
      background: #00a4ce;
      opacity: 0.7;
    }

    & > div:nth-child(4) {
      position: absolute;
      bottom: 0;
      width: 0;
      height: 0;
      border-color: #00a4ce33 transparent;
      border-width: 0 1920px 150px 0;
      border-style: solid;
    }
  }
}
</style>
