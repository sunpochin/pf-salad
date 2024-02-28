<template>
  <section>
    <video
      class="video"
      poster="@/assets/images/bg.jpg"
      src="@/assets/video/DigiSaladVideo.mp4"
      muted
      loop
      autoplay
    ></video>

    <div class="container">
      <div class="logo" ref="refLogo">
        <LogoComp :style="logoTheme" width="199" height="88" />
      </div>

      <div class="subtitle h5">DIGITAL AGENCY</div>
      <div class="word-display">
        <span> We create </span> <br />
        <span> amazing </span> <br />
        <span> digital experiences </span>
      </div>
    </div>
  </section>
</template>

<script setup>
import LogoComp from '@/components/LogoComp.vue'
const logoTheme = 'light'
</script>

<style lang="scss" scoped>
@import '@/assets/sass/utils/variables';
@import '@/assets/sass/mixins/breakpoint';

section {
  position: relative;
  // todo
  height: 1024px;
}

// .pink_dot {
//   margin-top: -1.75rem;
//   margin-left: -0.5rem;

//   &::before {
//     content: ' ';
//     display: block;
//     width: 10px;
//     height: 10px;
//     background: #ee6c8a;
//     border-radius: 100%;
//     position: absolute;
//     bottom: 5px;
//     right: -15px;
//   }
// }

// .we-create {
//   display: inline-block;
//   position: relative;
//   margin-bottom: 36px;
// }
// .haha {
//   margin-left: 300px;
//   font-size: 24px;
//   font-weight: 700;
//   line-height: 1.25;
//   letter-spacing: 0.2412em;
//   color: $white;
//   @include media-breakpoint-up(sm) {
//     font-size: 3rem;
//   }
//   @include media-breakpoint-up(md) {
//     font-size: 4rem;
//   }
//   @include media-breakpoint-up(lg) {
//     font-size: 5rem;
//   }
//   @include media-breakpoint-up(xl) {
//     font-size: 3rem;
//   }
// }
.video {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  object-fit: cover;
  overflow: hidden;
}

picture,
img {
  display: none;
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  object-fit: cover;
  @media (pointer: none), (pointer: coarse) {
    display: block;
  }
}
.container {
  height: 100%;
  padding-top: 70px;
  @media screen and (min-width: 360px) {
    padding-top: 100px;
  }
  @include media-breakpoint-up(sm) {
    padding-top: 180px;
  }
  @include media-breakpoint-up(xl) {
    padding-left: 170px;
    padding-right: 170px;
  }
}

.logo {
  position: relative;
  top: 25px;
  left: 220px;
  transform-origin: top left;
  transition: all 0.1s;
  &.opacity-0 {
    opacity: 0;
  }
}

.word-display {
  margin: 20px 0 20px 226px;
  color: $white;
  font-size: $display * 0.7;
  font-weight: $font-weight-bold;
  line-height: 1.5;
  text-transform: uppercase;
  letter-spacing: 0.2412em;
  @include media-breakpoint-up(xs) {
    font-size: $display * 0.9;
    line-height: 1.85;
  }
  @include media-breakpoint-up(sm) {
    margin-top: 34px;
    font-size: $display;
  }
  span {
    position: relative;
    display: inline;
    padding-left: 0.2412em;
    z-index: 1;

    &:last-child {
      position: relative;
      display: inline;
      background: linear-gradient(
        180deg,
        rgba($white, 0) 60%,
        $primary 60%,
        $primary 85%,
        rgba($white, 0) 85%
      );
      z-index: 10;
      @include media-breakpoint-up(sm) {
        background: linear-gradient(
          180deg,
          rgba($white, 0) 68%,
          $primary 68%,
          $primary 87%,
          rgba($white, 0) 87%
        );
      }
      &::after {
        position: absolute;
        @include beforeafter;
        bottom: calc(0.5em + 3px);
        left: calc(100% + 10px);
        width: 10px;
        height: 10px;
        background-color: $surface;
        border-radius: 10px;
      }
    }
  }
}
.subtitle {
  position: absolute;
  top: 249px;
  left: 62.5px;
  // left: calc((100% - 1640px) / 2);
  display: flex;
  flex-direction: row;
  align-items: center;
  gap: 25px;
  color: $white;
  font-weight: $font-weight-bold;
  letter-spacing: 0.13875em;
  white-space: nowrap;
  writing-mode: vertical-lr;
  transform: rotate(180deg);
  &::before {
    @include beforeafter;
    width: 2px;
    height: 115px;
    background-color: currentColor;
  }
}
</style>
