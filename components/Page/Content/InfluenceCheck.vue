<script lang="ts" setup>
import Title from '../Title'
</script>

<template>
  <div class="InfluenceCheck">
    <Title :text_l="'視光'" :text_r="'檢查'" />
    <div class="swiper">
      <div class="swiperBox">
        <div class="swiperNav flex">
          <div class="imgLeft">
            <img
              src="https://static.cmereye.com/imgs/2023/04/fe71351b6af68252.png"
              alt="視光檢查"
            />
          </div>
          <div class="flex flex-col items-center">
            <div class="iconText">綜合檢查</div>
            <div class="swiperText">
              8歲以下一般視為兒童視力發展至關重要的時期。若眼睛的發育在這期間出現異常而沒有作出矯正，便可能造成難以挽救的視力損害。因此，家長應為兒童定期安排綜合眼睛檢查，掌握小孩的視覺發展需要。
            </div>
          </div>
        </div>
      </div>
      <div class="swiperBg"></div>
    </div>
  </div>
</template>

<style scoped lang="scss">
.InfluenceCheck {
  // position: relative;
}
.swiper {
  position: relative;
}
.swiperBox {
  width: 884px;
  height: 505px;
  background: #fff;
  padding: 35px 33px;
  z-index: 10;
  position: relative;
}
.swiperNav {
  text-align: center;
}
.swiperNav > div:last-child {
  flex: 1;
}
.swiperText {
  width: 270px;
  margin-left: 44px;

  /* MB-Noto Mid */

  font-family: 'Noto Sans CJK TC';
  font-style: normal;
  font-weight: 500;
  font-size: 16px;
  line-height: 32px;
  /* or 200% */

  text-align: justify;

  /* Dark Grey */

  color: #3e5270;
}
.imgLeft {
  width: 436px !important;
  // height: 436px;
}
.imgLeft > img {
  width: 100%;
  // height: 100%;
}
.iconText {
  width: 142px;
  margin-top: 80px;
  margin-bottom: 21px;

  // position: relative;
  padding: 0 18px;

  font-family: 'Noto Sans CJK TC';
  font-style: normal;
  font-weight: 700;
  font-size: 24px;
  line-height: 12px;
  display: flex;
  align-items: center;
  text-align: center;
  letter-spacing: 0.1em;

  /* Turquoise */

  color: #00a4ce;
  border-bottom: 9px solid #ffee54;
}

.swiperBg {
  height: 440px;
  width: 1320px;
  background: #fff8b9;
  margin-left: 108px;
  position: absolute;
  top: 80px;
  z-index: 4;
}
</style>
