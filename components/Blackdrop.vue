import { PageRhomboidTop } from '~~/.nuxt/components';

<template>
  <div class="blackdrop flex justify-center">
    <PageRhomboidTop
      :style-rhom="{
        top: '520px',
        height: '342px',
        transform: 'skewY(348deg)',
        background: '#fff',
      }"
    />
    <PageRhomboidTop
      :style-rhom="{
        top: '2520px',
        height: '342px',
        transform: 'skewY(13deg)',
        background: '#c2eaf2',
      }"
    />
    <div class="blackdrop-w">
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
@media (min-width: 768px) {
  .blackdrop {
    overflow: hidden;
    width: 100%;
    position: relative;
  }

  .blackdrop-w {
    z-index: 100;
    width: 884px;
    margin: auto;
  }
}
</style>

<style lang="scss" scoped>
@media (max-width: 767px) {
  .blackdrop-w {
    width: 100vw;
  }
}
</style>
