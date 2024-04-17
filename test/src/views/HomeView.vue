<script setup>
// import HelloWorld from './components/HelloWorld.vue'
import PreLoader from '../components/PreLoader.vue'
import BackToTop from '../components/BackToTop.vue'
import HeaderMenu from '../components/HeaderMenu.vue'
import SectionHero from '../section/SectionHero.vue'
import SectionServices from '../section/SectionServices.vue'
import SectionPorto from '../section/SectionPorto.vue'
import SectionResume from '../section/SectionResume.vue'
import SectionSkills from '../section/SectionSkills.vue'
import SectionBlog from '../section/SectionBlog.vue'
import SectionContact from '../section/SectionContact.vue'
import FooterArea from '../components/FooterArea.vue'
</script>

<template>
  <PreLoader />
  <BackToTop />

  <main class="site-content" id="content">
    <HeaderMenu />
    <SectionHero />
    <SectionServices />
    <SectionPorto />
    <SectionResume />
    <SectionSkills />
    <SectionBlog />
    <SectionContact />
  </main>
  <FooterArea />
</template>

<style scoped></style>
