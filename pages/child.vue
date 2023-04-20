<template>
  <div class="child">
    <PageNavbar class="navbar" />
    <ChildDetaild />
    <PageFooter />
    <PageSmfooter />
  </div>
</template>

<script setup lang="ts"></script>

<style lang="scss" scoped>
@media (min-width: 768px) {
  .navbar {
    z-index: 999;
    position: fixed;
    top: 0;
    width: 100%;
    height: 84px;
  }

  .child {
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
