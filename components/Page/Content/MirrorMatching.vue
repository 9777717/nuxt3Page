<script lang="ts" setup>
import { html } from 'property-information'

const slider = [
  {
    img: 'https://static.cmereye.com/imgs/2023/04/fe71351b6af68252.png',
    kind: '漸進鏡',
    suitable: '適合人士',
    presbyterians: '大多數老花人士',
    effect: '達致效果',
    daily: '照顧日常基本需要',
    advantage: '優點',
    des: ['價錢實惠', '可看清遠、中、近距離的物件'],
  },
  {
    img: 'https://static.cmereye.com/imgs/2023/04/fe71351b6af68252.png',
    kind: '漸進鏡',
    suitable: '適合人士',
    presbyterians: '大多數老花人士',
    effect: '達致效果',
    daily: '照顧日常基本需要',
    advantage: '優點',
    des: ['價錢實惠', '可看清遠、中、近距離的物件'],
  },
  {
    img: 'https://static.cmereye.com/imgs/2023/04/fe71351b6af68252.png',
    kind: '漸進鏡',
    suitable: '適合人士',
    presbyterians: '大多數老花人士',
    effect: '達致效果',
    daily: '照顧日常基本需要',
    advantage: '優點',
    des: ['價錢實惠', '可看清遠、中、近距離的物件'],
  },
]
</script>

<template>
  <PageTitle :text_l="'配鏡'" :text_r="'服務'" />
  <div class="MirrorMatching">
    <div class="flex flex-row">
      <div v-for="slide in slider" :key="slide.img" class="slider">
        <div class="imgSlide">
          <img :src="slide.img" alt="MirrorMatching" />
        </div>
        <div class="textSlide">
          <div>{{ slide.kind }}</div>
          <div></div>
          <div>
            <div>
              <div>{{ slide.suitable }}</div>
              <div>{{ slide.effect }}</div>
              <div>{{ slide.advantage }}</div>
            </div>
            <div>
              <div>{{ slide.presbyterians }}</div>
              <div>{{ slide.daily }}</div>
              <div>
                <p v-for="nav in slide.des" :key="nav[0]">·&nbsp;{{ nav }}</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped lang="scss">
.slider {
  width: 320px;
  height: 400px;
  display: flex;
  flex-direction: column;
  margin-right: 22px;
}

.imgSlide {
  width: 300px;
  height: 195px;

  & > img {
    height: 100%;
    width: 100%;
  }
}

.textSlide {
  width: 320px;
  & > div:nth-child(1) {
    font-family: 'Noto Sans CJK TC';
    font-style: normal;
    font-weight: 700;
    font-size: 20px;
    line-height: 40px;
    /* or 200% */

    display: flex;
    align-items: center;

    /* Turquoise */

    color: #00a4ce;
  }

  & > div:nth-child(2) {
    border-bottom: 1px solid #aad4e5;
    margin: 4px 0 0 0;
  }

  & > div:nth-child(3) {
    display: flex;
    & > div:nth-child(1) {
      width: 78px;
      margin-right: 10px;
      display: flex;
      flex-direction: column;
      align-items: flex-end;
      & > div {
        margin-top: 12px;
        padding: 5px 7px;
        font-family: 'Noto Sans CJK TC';
        font-style: normal;
        font-weight: 700;
        font-size: 16px;
        line-height: 24px;
        /* identical to box height, or 150% */

        display: flex;
        align-items: center;

        /* 白色 */

        color: #ffffff;

        background: #00a4ce;
      }
    }
    & > div:nth-child(2) {
      display: flex;
      flex-direction: column;
      align-items: flex-start;
      & > div {
        padding: 5px 0;
        margin-top: 12px;
        font-family: 'Noto Sans CJK TC';
        font-style: normal;
        font-weight: 700;
        font-size: 16px;
        line-height: 24px;
        /* or 150% */

        display: flex;
        align-items: center;

        /* Dark Grey */

        color: #3e5270;
      }
      & > div:nth-child(3) {
        display: flex;
        flex-direction: column;
        align-items: flex-start;
      }
    }
  }
}
</style>
<style lang="scss" scoped>
@media (max-width: 767px) {
  .MirrorMatching {
    margin-top: 26px;
    margin-bottom: 66px;
  }
}
</style>
