<template>
  <div class="bg">
    <PageNavbar class="navbar" />
    <PageContent />
    <Blackdrop />
    <PageFooter />
  </div>
</template>

<style lang="scss" scoped>
.navbar {
  z-index: 999;
  position: fixed;
  top: 0;
  width: 100%;
  height: 84px;
}

.bg {
  background: #f2fcff;
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
