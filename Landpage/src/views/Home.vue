<template>
  <div>
    <Header />
    <HeroSection />
    <AboutSection />
    <ActivitiesSection />
    <GallerySection />
    <ContactSection />
    <Footer />
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

import Header from "../components/Header.vue";
import HeroSection from "../components/HeroSection.vue";
import AboutSection from "../components/AboutSection.vue";
import ActivitiesSection from "../components/ActivitiesSection.vue";
import GallerySection from "../components/GallerySection.vue";
import ContactSection from "../components/ContactSection.vue";
import Footer from "../components/Footer.vue";

export default defineComponent({
  components: {
    Header,
    HeroSection,
    AboutSection,
    ActivitiesSection,
    GallerySection,
    ContactSection,
    Footer
  }
});
</script>

<style scoped>
</style>
