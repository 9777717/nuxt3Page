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
