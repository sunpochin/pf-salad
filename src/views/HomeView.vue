<script setup>
// import HeaderComp from '@/components/HeaderComp.vue'
import TasteComp from '@/components/TasteComp.vue'
import AboutComp from '@/components/AboutComp.vue'
import AwardsComp from '@/components/AwardsComp.vue'
import Ingradients from '@/components/IngradientsComp.vue'
import FounderComp from '@/components/FounderComp.vue'
import BrandComp from '@/components/BrandComp.vue'
import ShowCase from '@/components/ShowCase.vue'
</script>

<template>
  <div class="home">
    <!-- <HeaderComp /> -->
    <TasteComp />
    <AboutComp />
    <AwardsComp />
    <Ingradients />
    <FounderComp />
    <BrandComp />
    <!-- <ShowCase /> -->
  </div>
</template>

<style lang="scss" scoped>
@import '@/assets/sass/mixins/breakpoint';
.home {
  width: 100%;
  max-width: 100%;
  margin: auto;
}

.container {
  position: relative;

  @include media-breakpoint-up(md) {
    max-width: 540px;
  }

  @include media-breakpoint-up(xl) {
    max-width: 1272px;
    flex: 1 1 0;
  }
}
</style>
