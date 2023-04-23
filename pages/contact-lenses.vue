<script setup lang="ts"></script>
<template>
  <div class="contactLenses">
    <PageNavbar class="navbar" />
    <div class="header">
      <!-- <LeneseMisightContact /> -->
      <LeneseOrthoKContact />
    </div>
    <PageFooter />
    <PageSmfooter />
  </div>
</template>

<style scoped lang="scss">
@media (min-width: 768px) {
  .navbar {
    z-index: 999;
    position: fixed;
    top: 0;
    width: 100%;
    height: 84px;
  }
  .contactLenses {
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
