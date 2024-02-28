<template>
  <NavbarComp :isShow="navbarStatus" />
  <RouterView />
</template>

<script setup>
import AOS from 'aos'
import 'aos/dist/aos.css'
import { ref, onMounted } from 'vue'
import { RouterView } from 'vue-router'
import NavbarComp from '@/components/NavbarComp.vue'

onMounted(() => {
  AOS.init()
  window.addEventListener('scroll', toggleNav)
})

const navbarStatus = ref(false)

const toggleNav = () => {
  const scrollTop = window.scrollY
  const position = window.innerHeight / 2

  if (scrollTop > position) {
    navbarStatus.value = true
  } else {
    navbarStatus.value = false
  }
  console.log('navbarStatus.value: ', navbarStatus.value)
}
</script>

<style scoped></style>
