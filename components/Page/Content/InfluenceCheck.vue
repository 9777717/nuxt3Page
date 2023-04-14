<script setup lang="ts">
import { Navigation, Pagination } from 'swiper'
import 'swiper/css'

import 'swiper/css/navigation'
import 'swiper/css/pagination'

const swiperNav = [
  {
    imgLink: 'https://static.cmereye.com/imgs/2023/04/fe71351b6af68252.png',
    textHeadrt: '綜合檢查',
    textNav:
      '8歲以下一般視為兒童視力發展至關重要的時期。若眼睛的發育在這期間出現異常而沒有作出矯正，便可能造成難以挽救的視力損害。因此，家長應為兒童定期安排綜合眼睛檢查，掌握小孩的視覺發展需要。',
  },
  {
    imgLink: 'https://static.cmereye.com/imgs/2023/04/b62c1fcd806bdcbc.png',
    textHeadrt: '綜合檢查',
    textNav:
      '8歲以下一般視為兒童視力發展至關重要的時期。若眼睛的發育在這期間出現異常而沒有作出矯正，便可能造成難以挽救的視力損害。因此，家長應為兒童定期安排綜合眼睛檢查，掌握小孩的視覺發展需要。',
  },
]
const modules = [Navigation, Pagination]
</script>

<template>
  <PageTitle :text_l="'視光'" :text_r="'檢查'" />
  <div class="InfluenceCheck">
    <swiper
      :centered-slides="true"
      :modules="modules"
      :slides-per-view="1"
      :loop="true"
      :effect="'creative'"
      :autoplay="{
        delay: 8000,
        disableOnInteraction: true,
      }"
      :pagination="{
        clickable: true,
      }"
      :navigation="true"
    >
      <swiper-slide v-for="slide in swiperNav" :key="slide">
        <div class="swiperNav">
          <div class="swiperBox">
            <div class="imgLeft">
              <img :src="slide.imgLink" :alt="slide.textHeadrt" />
            </div>
            <div class="flex flex-col items-center">
              <div class="iconText">{{ slide.textHeadrt }}</div>
              <div class="swiperText">
                {{ slide.textNav }}
              </div>
            </div>
          </div>
        </div>
      </swiper-slide>
    </swiper>
    <div class="swiperbg"></div>
  </div>
</template>

<style lang="scss" scoped>
.InfluenceCheck {
  position: relative;
}
.swiperbg {
  height: 440px;
  width: 1286px;
  background: #fff8b9;
  margin-left: 108px;
  position: absolute;
  z-index: 0;
  top: 80px;
}
.swiperBox {
  width: 884px;
  height: 505px;
  display: flex;
  padding: 35px 33px;
  background: #fff;
}
.swiperNav {
  display: flex;
  text-align: center;
  background: #fff;
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
.swiper {
  width: 100%;
  height: 100%;
}

.swiper-slide {
  text-align: center;
  font-size: 18px;
  background: #fff;

  /* Center slide text vertically */
  display: flex;
  justify-content: center;
  align-items: center;
}

.swiper-slide img {
  display: block;
  width: 100%;
  height: 100%;
  object-fit: cover;
}
</style>
<!-- 
<style scoped lang="scss">
.InfluenceCheck {
  position: relative;
}
// .InfluenceCheck > div {
//   margin-right: -54px;
// }
.swiperBox {
  width: 884px;
  height: 505px;
  display: flex;
  padding: 35px 33px;
}
.mySwiper {
  width: 884px;
  height: 505px;
}
.swiperNav {
  display: flex;
  text-align: center;
  background: #fff;
}
// .swiperNav > div:last-child {
//   flex: 1;
// }
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

.swiperbg {
  height: 440px;
  width: 1286px;
  background: #fff8b9;
  margin-left: 108px;
  position: absolute;
  z-index: 0;
  top: 80px;
}
.triangle {
  width: 0;
  height: 0;
  border-left: 10px solid transparent;
  border-right: 10px solid transparent;
  border-bottom: 14px solid #ffffff;
  transform: matrix(0, -1, -1, 0, 0, 0);
}
</style> -->
