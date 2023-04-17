<script lang="ts" setup>
const { t } = useLang()
</script>
<template>
  <div class="IamgeAd">
    <div class="top"></div>
    <div>
      <span>{{ t('pages.content.title.titleDiscounts') }}</span>
    </div>
    <div>
      <img src="https://static.cmereye.com/imgs/2023/04/2edb5be2606f83b0.png" />
    </div>
  </div>
</template>

<style scoped lang="scss">
@media (min-width: 768px) {
  .IamgeAd {
    margin-top: 57px;
  }
  .IamgeAd > div:nth-child(1) {
    width: 100%;
    height: 8px;
    background: #00a4ce;
  }
  .IamgeAd > div:nth-child(2) {
    background-color: #ffee54;
    width: 100%;
    height: 67px;

    display: flex;
    align-items: center;
    justify-content: center;
  }
  .IamgeAd > div:nth-child(2) > span {
    font-family: 'Noto Sans';
    font-style: normal;
    font-weight: 700;
    font-size: 40px;
    line-height: 54px;
    text-align: center;
    letter-spacing: 0.1em;

    /* Turquoise */

    color: #00a4ce;
  }
}
</style>

<style lang="scss" scoped>
@media (max-width: 767px) {
  .IamgeAd {
    margin-top: 57px;
  }
  .IamgeAd > div:nth-child(1) {
    width: 100%;
    height: 6px;
    background: #00a4ce;
  }
  .IamgeAd > div:nth-child(2) {
    background-color: #ffee54;
    width: 100%;
    height: 36px;

    display: flex;
    align-items: center;
    justify-content: center;
  }
  .IamgeAd > div:nth-child(2) > span {
    font-family: 'Noto Sans CJK TC';
    font-style: normal;
    font-weight: 700;
    font-size: 24px;
    line-height: 36px;
    text-align: center;
    letter-spacing: 0.1em;

    /* Turquoise */

    color: #00a4ce;
  }
}
</style>
