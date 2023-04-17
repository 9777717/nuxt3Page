<template>
  <div class="banner flex-1 w-full flex flex-col">
    <div class="min-h-full first_page">
      <div class="bg_peomi transform motion-safe:hover:scale-105">
        <img
          class="img transform motion-safe:hover:scale-105"
          src="https://static.cmereye.com/imgs/2023/04/949a53d691437ec7.png"
        />
        <text>兒童視光服務</text>
      </div>
      <div class="bg_peo transform motion-safe:hover:scale-105">
        <text>成人視光服務</text>
        <img
          class="img transform motion-safe:hover:scale-105"
          src="https://static.cmereye.com/imgs/2023/04/23a9931f7bb7b510.png"
        />
      </div>

      <div class="ba_bottom transform motion-safe:hover:scale-110">
        <img
          src="https://static.cmereye.com/imgs/2023/04/4f06d9a47c56800c.png"
        />
      </div>
    </div>
  </div>
  <div class="bannerSm">
    <div class="bannerSmBg">
      <div class="bgsm_peomi peomi transform motion-safe:hover:scale-105">
        <img
          class="img transform motion-safe:hover:scale-105"
          src="https://static.cmereye.com/imgs/2023/04/949a53d691437ec7.png"
        />
        <text>兒童視光服務</text>
      </div>
      <div class="bgsm_peo transform motion-safe:hover:scale-105">
        <text>成人視光服務</text>
        <img
          class="img transform motion-safe:hover:scale-105"
          src="https://static.cmereye.com/imgs/2023/04/23a9931f7bb7b510.png"
        />
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.banner {
  height: 1080px;
  background: url('https://static.cmereye.com/imgs/2023/04/3bbca41eecbd1883.png');
}
.first_page {
  display: flex;
  flex-direction: row;
  flex-wrap: nowrap;
  justify-content: space-around;
}

.bg_peomi,
.bg_peo {
  width: 260px;
  height: 70px;
  font-family: 'Noto Sans CJK TC';
  font-style: normal;
  font-weight: 700;
  font-size: 28px;
  line-height: 41px;
  box-sizing: border-box;

  display: flex;
  align-items: center;
}

.bg_peomi {
  background: #ffee54;
  border: 1.71498px solid #ffffff;
  border-radius: 46px;
  text-align: right;
  color: #00a4ce;

  position: absolute;
  top: 460px;
  left: 200px;
}

.bg_peo {
  background: #ffffff;
  opacity: 0.9;
  border: 1.58937px solid #00a4ce;
  border-radius: 52px;
  color: #00a4ce;

  position: absolute;
  top: 460px;
  right: 200px;
}

.bg_peo > text,
.bg_peomi > img {
  padding: 0 25px;
}

.img {
  display: inline-block;
}

.ba_bottom {
  position: absolute;
  left: 50.83%;
  right: 47.77%;
  bottom: 14.11%;
  top: 1000px;
}
</style>
<style lang="scss" scoped>
@media (max-width: 767px) {
  .banner,
  .ba_bottom {
    display: none;
  }
  .bannerSm {
    margin-top: 64px;
    .bannerSmBg {
      display: flex;
      flex-direction: column-reverse;
      justify-content: space-around;
      align-items: center;
      margin-top: -50px;

      position: relative;
      width: 100vw;
      height: 754px;
      background: url('https://static.cmereye.com/imgs/2023/04/4601b13acb1c62d5.png')
          top left no-repeat,
        url('https://static.cmereye.com/imgs/2023/04/03b378f4a8cc28b8.png')
          bottom left no-repeat;
      .bgsm_peomi,
      .bgsm_peo {
        background: #ffffff;
        opacity: 0.9;
        width: 168.11px;
        height: 44.6px;
        /* Turquoise */

        border: 1.01268px solid #00a4ce;
        border-radius: 33.1323px;

        font-family: 'Noto Sans CJK TC';
        font-style: normal;
        font-weight: 700;
        font-size: 17.8404px;
        line-height: 26px;
        // display: flex;
        // align-items: center;

        /* Turquoise */

        color: #00a4ce;

        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: space-evenly;
      }
      .bgsm_peomi {
        opacity: 1;
        background: #ffee54;
        /* 白色 */
        border: 1.09271px solid #ffffff;
      }
      .bgsm_peo {
        margin-left: 175px;
        margin-top: 115px;
      }
      .peomi {
        margin-right: 175px;
        margin-top: 15px;
      }
    }
  }
}
@media (min-width: 768px) {
  .bannerSm {
    display: none;
  }
}
</style>
