<template>
  <div class="bg flex justify-center">
    <div class="bg-w">
      <PageContentMyopia />
      <PageContentMirrorMatching />
      <PageContentInfluenceCheck />
      <PageContentInspectionItem />
      <PageContentImageAd />
      <PageContentForm />
    </div>
  </div>
</template>

<style lang="scss" scoped>
// .bg {
//   background: #f2fcff;
// }
.bg-w {
  width: 884px;
}
</style>

<style lang="scss" scoped>
@media (max-width: 766px) {
  .bg-w {
    width: 100vw;
  }
}
</style>
