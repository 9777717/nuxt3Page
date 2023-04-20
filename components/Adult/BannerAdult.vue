<template>
  <div class="BannerAdult">
    <div>
      <div>
        <img
          src="https://static.cmereye.com/imgs/2023/04/49b0b6b695dade91.png"
          alt=""
        />
      </div>
    </div>
    <div>
      <div>成人視力需求</div>
    </div>
  </div>
</template>

<style scoped lang="scss">
@media (min-width: 768px) {
  .BannerAdult {
    position: relative;
    & > div:nth-child(2) {
      position: absolute;
      top: 220px;
      right: 183px;
      font-family: 'Noto Sans CJK TC';
      font-style: normal;
      font-weight: 700;
      font-size: 120px;
      line-height: 178px;
      display: flex;
      align-items: center;
      letter-spacing: 0.1em;

      /* Turquoise */

      color: #00a4ce;
    }
  }
}
</style>
