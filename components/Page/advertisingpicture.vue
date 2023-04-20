<template>
  <PromotionAdBanner />
  <div class="advertisingpicture">
    <div>
      <div>
        <img
          src="https://static.cmereye.com/imgs/2023/04/914e7c42584aaec5.png"
          alt=""
        />
      </div>
      <div>
        <img
          src="https://static.cmereye.com/imgs/2023/04/16e5723f02a2f2c9.png"
          alt=""
        />
      </div>
      <div>
        <img
          src="https://static.cmereye.com/imgs/2023/04/8dbd275cc2d99efc.png"
          alt=""
        />
      </div>
      <div>
        <img
          src="https://static.cmereye.com/imgs/2023/04/118269efd0044af0.png"
          alt=""
        />
      </div>
    </div>
  </div>
</template>
<style scoped lang="scss">
@media (min-width: 768px) {
  .advertisingpicture {
    & > div {
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      flex-direction: row;
      align-content: space-between;
      box-sizing: border-box;
      margin: 60px 492px;
      margin-bottom: 40px;
      & > div {
        width: 400px;
        height: 420px;
        margin: 26px 30px;
        & > img {
          width: 100%;
          height: 100%;
        }
      }
    }
  }
}
</style>
