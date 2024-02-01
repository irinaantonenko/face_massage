<template>
  <div>
    <main-page/>
    <experience-page/>
    <projects-page/>
    <plus-page/>
    <!-- <about-me-page/>     -->
    <contact-page/>
    <!-- <test-city></test-city>
    <new-component></new-component> -->
  </div>
</template>

<script>
import MainPage from './components/MainPage.vue';
import ContactPage from './components/ContactPage.vue';
import ProjectsPage from './components/ProjectsPage.vue';
import PlusPage from './components/PlusPage.vue';
// import AboutMePage from './components/AboutMePage.vue';
import ExperiencePage from './components/ExperiencePage.vue';
// import TestCity from './components/TestCity.vue';
// import NewComponent from './components/NewComponent.vue'
export default {
  name: 'App',
  components: {
    // TestCity,
    MainPage,
    ContactPage,
    ProjectsPage,
    PlusPage,
    // AboutMePage,
    ExperiencePage
    // NewComponent
  },
 
}
</script>

<style>
</style>
