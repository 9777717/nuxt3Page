<script lang="ts" setup>
/**
 *  注意：使用该组件父级需要 相对定位position: relative; 且父级宽度合适
 *    top: '520px', // 到父级的高度
 *    height: '342px', // 平行四边形的高度
 *    transform: 'skewY(348deg)', // 旋转角度
 *    background: '#fff', // 平行四边形颜色
 *  注意看层级
 * **/
defineProps({
  styleRhom: {
    type: Object,
    default() {
      return {}
    },
  },
})
</script>
<template>
  <div class="rhomboidTop">
    <div class="blackdrop-rhomboidTop" :style="{ ...styleRhom }"></div>
  </div>
</template>

<style scoped lang="scss">
@media (min-width: 767px) {
  .blackdrop-rhomboidTop {
    position: absolute;
    left: 0;
    width: 100%;
    z-index: 10;
    top: 520px;
    height: 342px;
    transform: skewY(348deg);
    background: #fff;
  }
}
</style>
<style scoped lang="scss">
@media (max-width: 767px) {
  .rhomboidTop {
    display: none;
  }
}
</style>
