<template>
  <section>
    <div class="container">
      <TitleComp position="center" theme="light" data-aos="fade-up">OUR INGRADIENTS</TitleComp>

      <p data-aos="fade-up">
        Cras quis nulla commodo, aliquam lectus sed, blandit augue. Cras ullamcorper bibendum
        bibendum. Duis tincidunt urna non pretium porta. Nam condimentum vitae ligula vel ornare.
        Phasellus at semper turpis. Nunc eu tellus tortor. Etiam at condimentum nisl, vitae sagittis
        orci. Donec id dignissim nunc. Donec elit ante, eleifend a dolor et, venenatis facilisis
        dolor. In feugiat orci odio, sed lacinia sem elementum quis. Aliquam consectetur, eros et
        vulputate euismod, nunc leo tempor lacus, ac rhoncus neque eros nec lacus. Cras lobortis
        molestie faucibus.
      </p>
      <h1>OUR SERVICES</h1>
      <div class="ingredient-group">
        <div
          v-for="(item, index) in ingredients"
          :key="`ingredient-${index}`"
          class="ingredient-item"
          data-aos="fade-up"
          :data-aos-delay="(index % 3) * 200"
        >
          <img :src="getImageUrl(item.file)" :alt="item.title" />

          <h3>
            {{ item.title }}
          </h3>
          <p>
            {{ item.intro }}
          </p>

          <ButtonRoundComp>{{ item.button }}</ButtonRoundComp>
        </div>
      </div>
      <div class="h5">
        <a href="#!" class="btn-link" data-aos="fade-up"> VIEW MORE DIGISALAD’S INGRADIENTS </a>
      </div>
    </div>
  </section>
</template>

<script setup>
import TitleComp from '@/components/TitleComp.vue'
import ButtonRoundComp from '@/components/ButtonRoundComp.vue'

const getImageUrl = (fileName) => {
  // console.log('object', `@/assets/images/ingredient/${fileName}`)
  return `/images/ingredient/${fileName}`
  // return `@/assets/images/ingredient/${fileName}`
}
const ingredients = [
  {
    file: 'ingre-01.svg',
    title: 'ux design',
    intro:
      'Cras quis nulla commodo, aliquam lectus sed, blandit augue. Cras ullamcorper bibendum bibendum. Duis tincidunt urna non pretium porta. Nam condimentum vitae ligula vel ornare.',
    button: 'VIEW MORE'
  },
  {
    file: 'ingre-02.svg',
    title: 'ui design',
    intro:
      'Cras quis nulla commodo, aliquam lectus sed, blandit augue. Cras ullamcorper bibendum bibendum. Duis tincidunt urna non pretium porta. Nam condimentum vitae ligula vel ornare.',
    button: 'VIEW MORE'
  },
  {
    file: 'ingre-03.svg',
    title: 'website\ndevelopment',
    intro:
      'Cras quis nulla commodo, aliquam lectus sed, blandit augue. Cras ullamcorper bibendum bibendum. Duis tincidunt urna non pretium porta. Nam condimentum vitae ligula vel ornare.',
    button: 'VIEW MORE'
  },
  {
    file: 'ingre-04.svg',
    title: 'mobile app\ndevelopment',
    intro:
      'Cras quis nulla commodo, aliquam lectus sed, blandit augue. Cras ullamcorper bibendum bibendum. Duis tincidunt urna non pretium porta. Nam condimentum vitae ligula vel ornare.',
    button: 'VIEW MORE'
  },
  {
    file: 'ingre-05.svg',
    title: 'ecommerce',
    intro:
      'Cras quis nulla commodo, aliquam lectus sed, blandit augue. Cras ullamcorper bibendum bibendum. Duis tincidunt urna non pretium porta. Nam condimentum vitae ligula vel ornare.',
    button: 'VIEW MORE'
  },
  {
    file: 'ingre-06.svg',
    title: 'customer loyalty',
    intro:
      'Cras quis nulla commodo, aliquam lectus sed, blandit augue. Cras ullamcorper bibendum bibendum. Duis tincidunt urna non pretium porta. Nam condimentum vitae ligula vel ornare.',
    button: 'VIEW MORE'
  },
  {
    file: 'ingre-07.svg',
    title: 'digital\ntransformation',
    intro:
      'Cras quis nulla commodo, aliquam lectus sed, blandit augue. Cras ullamcorper bibendum bibendum. Duis tincidunt urna non pretium porta. Nam condimentum vitae ligula vel ornare.',
    button: 'VIEW MORE'
  },
  {
    file: 'ingre-08.svg',
    title: 'digital\nmarketing',
    intro:
      'Cras quis nulla commodo, aliquam lectus sed, blandit augue. Cras ullamcorper bibendum bibendum. Duis tincidunt urna non pretium porta. Nam condimentum vitae ligula vel ornare.',
    button: 'VIEW MORE'
  },
  {
    file: 'ingre-09.svg',
    title: 'branding',
    intro:
      'Cras quis nulla commodo, aliquam lectus sed, blandit augue. Cras ullamcorper bibendum bibendum. Duis tincidunt urna non pretium porta. Nam condimentum vitae ligula vel ornare.',
    button: 'BRANDING'
  }
]
</script>

<style lang="scss" scoped>
@import '@/assets/sass/utils/variables';
@import '@/assets/sass/mixins/breakpoint';

section {
  padding-top: 105px;
  padding-bottom: 135px;
  background-color: $primary;
}
.container {
  margin: auto;
  max-width: 1175px;
  border-top-left-radius: 30px;
  border-bottom-left-radius: 30px;
  @include media-breakpoint-up(sm) {
    border-top-left-radius: 50px;
    border-bottom-left-radius: 50px;
  }
}
p {
  max-width: 1010px;
  margin-top: 40px;
  margin-bottom: 40px;
  margin-left: auto;
  margin-right: auto;
  color: $white;
  letter-spacing: 0.0625em;
  line-height: 1.75;
  text-align: center;
}
.ingredient-group {
  display: grid;
  gap: 60px 50px;
  padding-top: 85px;
  @include media-breakpoint-up(sm) {
    grid-template-columns: repeat(3, 1fr);
  }
  .ingredient-item {
    position: relative;
    display: flex;
    flex-wrap: wrap;
    padding-left: 100px;
    @include media-breakpoint-up(sm) {
      flex-direction: column;
      padding-left: 0;
    }
  }
  img {
    display: block;
    margin-left: auto;
    margin-right: auto;
    @include media-breakpoint-down(sm) {
      position: absolute;
      top: 0;
      left: 0;
      width: 80px;
    }
    @include media-breakpoint-up(sm) {
      width: 108px;
    }
  }
  h3 {
    display: flex;
    align-items: center;
    justify-content: center;
    margin-top: 0;
    margin-bottom: 15px;

    color: $white;
    text-align: center;
    font-feature-settings:
      'clig' off,
      'liga' off;
    font-size: 20px;
    font-style: normal;
    font-weight: 700;
    line-height: normal;
    letter-spacing: 2px;
    text-transform: uppercase;

    @include media-breakpoint-up(sm) {
      height: 3em;
      margin-top: 20px;
      text-align: center;
      white-space: break-spaces;
    }
  }
  p {
    margin-top: 0;
    margin-bottom: 30px;
    letter-spacing: 0.0625em;
    @include media-breakpoint-down(sm) {
      line-height: 1.75;
      text-align: left;
    }
  }
  button {
    margin-top: auto;
    @include media-breakpoint-down(sm) {
      margin-left: 0;
    }
  }
}
.h5 {
  margin-top: 102px;
  text-align: center;
  .btn-link {
    width: 400px;
    height: 22px;
    padding-left: 0.1em;
    color: $white;
    font-weight: $font-weight-bold;
    letter-spacing: 0.1em;
    background: linear-gradient(
      180deg,
      rgba($white, 0) 65%,
      $highlight 65%,
      $highlight 90%,
      rgba($white, 0) 90%
    );
    &:hover {
      background: linear-gradient(
        180deg,
        rgba($white, 0) 65%,
        $surface 65%,
        $surface 90%,
        rgba($white, 0) 90%
      );
    }
  }
}
</style>
