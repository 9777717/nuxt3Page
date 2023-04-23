<script lang="ts" setup>
defineProps({
  text_l: {
    type: String,
    default: '',
  },
  text_r: {
    type: String,
    default: '',
  },
})
</script>

<template>
  <!-- <div class="text-4xl font-bold">
    <slot>{{ text }}</slot>
  </div> -->
  <div class="iconHeader">
    <div>
      <span>{{ text_l }}</span>
    </div>
    <div>{{ text_r }}</div>
  </div>
</template>
<style scoped>
@media (min-width: 768px) {
  .iconHeader {
    margin: 83px auto 43px auto;
    /* PC-Title */

    font-family: 'Noto Sans';
    font-style: normal;
    font-weight: 700;
    font-size: 40px;
    line-height: 54px;
    display: flex;
    align-items: center;
    justify-content: center;
    text-align: center;
    letter-spacing: 0.1em;

    /* 白色 */

    color: #3e5270;
  }

  .iconHeader > div:nth-child(1) {
    position: relative;
    width: 91px;
    height: 48px;
    background: #00a4ce;
    box-sizing: border-box;
    margin-top: 5px;
  }

  .iconHeader > div:nth-child(1) > span {
    color: #ffffff;
    position: absolute;
    left: 2px;
    bottom: 0px;
  }
}
</style>
<style lang="scss" scoped>
@media (max-width: 767px) {
  .iconHeader {
    margin: 0;
    font-family: 'Noto Sans CJK TC';
    font-style: normal;
    font-weight: 700;
    font-size: 24px;
    line-height: 36px;
    display: flex;
    align-items: center;
    text-align: center;
    letter-spacing: 0.1em;

    /* 白色 */

    color: #3e5270;
  }

  .iconHeader > div:nth-child(1) {
    position: relative;
    width: 56px;
    height: 34px;
    background: #00a4ce;
    box-sizing: border-box;
    margin-top: 0;
  }

  .iconHeader > div:nth-child(1) > span {
    color: #ffffff;
  }

  .iconHeader > div:nth-child(2) {
    margin-left: 2px;
  }
}
</style>
