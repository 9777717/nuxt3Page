<template>
  <div class="bgPopularize">
    <PageNavbar class="navbar" />
    <Latestpromotion />
    <PageFooter />
    <PageSmfooter />
  </div>
</template>

<style lang="scss" scoped>
@media (min-width: 768px) {
  .navbar {
    z-index: 999;
    position: fixed;
    top: 0;
    width: 100%;
    height: 84px;
  }

  .bgPopularize {
    background: #f2fcff;
    overflow: hidden;
  }
}
</style>
<style lang="scss" scoped>
@media (max-width: 767px) {
  .navbar {
    z-index: 999;
    position: fixed;
    top: 0;
    width: 100vw;
    height: 64px;
  }
}
</style>
