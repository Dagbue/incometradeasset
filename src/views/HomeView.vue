<template>
  <div class="home">
    <slider-section/>
    <section1/>
    <core/>
    <market-view/>
    <home-section4/>
    <home-section2/>
    <home-section3/>
    <faq-section1/>
    <home-section5/>
    <home-section6/>
    <contact-us/>
    <footer-home/>
  </div>
</template>

<script>
// @ is an alias to /src
import SliderSection from "@/components/Home/SliderSection.vue";
import HomeSection2 from "@/components/Home/HomeSection2.vue";
import HomeSection3 from "@/components/Home/HomeSection3.vue";
import FooterHome from "@/components/BaseComponents/footerHome.vue";
import ContactUs from "@/components/Home/ContactUs.vue";
import FaqSection1 from "@/components/Home/FaqSection1.vue";
import HomeSection4 from "@/components/Home/HomeSection4.vue";
import HomeSection5 from "@/components/Home/HomeSection5.vue";
import HomeSection6 from "@/components/Home/HomeSection6.vue";
import MarketView from "@/components/Home/MarketView.vue";
import Section1 from "@/components/Home/Section1.vue";
import Core from "@/components/Home/core.vue";

export default {
  name: 'HomeView',
  components: {
    Core,
    Section1,
    MarketView,
    HomeSection6,
    HomeSection5,
    HomeSection4,
    FaqSection1,
    ContactUs,
    FooterHome,
    HomeSection3,
    HomeSection2,
    SliderSection
  },
}
</script>
