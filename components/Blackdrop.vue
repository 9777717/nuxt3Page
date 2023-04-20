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
@media (min-width: 768px) {
  .bg {
    overflow: hidden;
  }
  .bg-w {
    width: 884px;
    margin: auto;
  }
}
</style>

<style lang="scss" scoped>
@media (max-width: 767px) {
  .bg-w {
    width: 100vw;
  }
}
</style>
