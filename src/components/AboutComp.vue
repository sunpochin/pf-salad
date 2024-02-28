<template>
  <section>
    <div class="container">
      <TitleComp position="center" theme="primary" data-aos="fade-up">ABOUT DIGISALAD</TitleComp>

      <div class="ratio" data-aos="fade-up" :data-aos-delay="0" data-aos-duration="1000">
        <iframe
          src="https://www.youtube.com/embed/IeIRJ9jZ5Ro?vq=hd1080"
          title="youtube"
          frameborder="0"
          allow=""
          allowfullscreen
        ></iframe>
      </div>

      <p>
        Cras quis nulla commodo, aliquam lectus sed, blandit augue. Cras ullamcorper bibendum
        bibendum. Duis tincidunt urna non pretium porta. Nam condimentum vitae ligula vel ornare.
        Phasellus at semper turpis. Nunc eu tellus tortor. Etiam at condimentum nisl, vitae sagittis
        orci. Donec id dignissim nunc. Donec elit ante, eleifend a dolor et, venenatis facilisis
        dolor. In feugiat orci odio, sed lacinia sem elementum quis. Aliquam consectetur, eros et
        vulputate euismod, nunc leo tempor lacus, ac rhoncus neque eros nec lacus. Cras lobortis
        molestie faucibus.
      </p>
    </div>
  </section>
</template>

<script setup>
import TitleComp from '@/components/TitleComp.vue'
</script>

<style lang="scss" scoped>
@import '@/assets/sass/mixins/functions';

section {
  padding-top: 125px;
  padding-bottom: 70px;
}
.container {
  max-width: 1010px;
  margin: auto;
}

.ratio {
  max-width: 960px;
  margin-top: 70px;
  margin-bottom: 30px;
  margin-left: auto;
  margin-right: auto;

  position: relative;
  &::before {
    @include beforeafter;
    width: 100%;
    padding-top: calc(9 / 16) * 100%;
  }
  iframe {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
  }
}

p {
  margin-top: 30px;
  margin-bottom: 30px;
  color: #262626;
  letter-spacing: 1px;
  line-height: 1.75;
  text-align: center;
}
</style>
