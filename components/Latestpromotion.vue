<template>
  <PageAdvertisingpicture />
  <div class="blackdrop flex justify-center">
    <PageRhomboidTop
      :style-rhom="{
        top: '220px',
        height: '342px',
        transform: 'skewY(348deg)',
        background: '#fff',
      }"
    />
    <div class="blackdrop-w">
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
  .iconHeader {
    margin-top: 0;
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
