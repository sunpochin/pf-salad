<template>
  <button type="button">
    <slot></slot>
  </button>
</template>

<style lang="scss" scoped>
@import '@/assets/sass/utils/variables';
@import '@/assets/sass/mixins/functions';
button {
  width: 165px;
  height: 58px;
  position: relative;
  margin: auto;
  padding: 0;
  color: $white;
  font-size: $h6-font-size;
  font-size: 14px;
  font-style: normal;
  font-weight: $font-weight-bold;
  line-height: normal;
  letter-spacing: 2.222px;

  background-color: transparent;
  border: 2px solid $white;
  border-radius: 35px;
  overflow: hidden;
  z-index: 1;
  &::before {
    @include beforeafter;
    position: absolute;
    top: 0;
    right: 0;
    width: 0;
    height: 100%;
    background-color: $surface;
    transition: width 0.5s;
    z-index: -1;
  }
  &:hover {
    &::before {
      width: 100%;
    }
  }
}
</style>
