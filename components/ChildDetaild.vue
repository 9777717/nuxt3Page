<script setup lang="ts">
const childOrAdult = ref(true)
</script>
<template>
  <div class="ChildDetaild">
    <div>
      <el-switch v-model="childOrAdult" />
      <ChildBannerChild v-if="childOrAdult" />
      <AdultBannerAdult v-else />
    </div>
    <div class="ChildDetaild-w">
      <PageContentMyopia />
      <PageContentInfluenceCheck />
      <PageContentImageAd />
      <PageContentForm />
    </div>
  </div>
</template>

<style scoped lang="scss">
@media (min-width: 768px) {
  .ChildDetaild {
    margin-top: 150px;
    overflow: hidden;
    width: 100%;
    position: relative;
  }

  .ChildDetaild-w {
    z-index: 100;
    width: 884px;
    margin: auto;
  }

  .iconHeader {
    margin-top: 0;
  }
}
</style>
