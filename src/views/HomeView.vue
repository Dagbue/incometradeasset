<template>
  <div class="home">
    <slider-section/>
    <home-section1/>
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
import HomeSection1 from "@/components/Home/HomeSection1.vue";
import HomeSection2 from "@/components/Home/HomeSection2.vue";
import HomeSection3 from "@/components/Home/HomeSection3.vue";
import FooterHome from "@/components/BaseComponents/footerHome.vue";
import ContactUs from "@/components/Home/ContactUs.vue";
import FaqSection1 from "@/components/Home/FaqSection1.vue";
import HomeSection4 from "@/components/Home/HomeSection4.vue";
import HomeSection5 from "@/components/Home/HomeSection5.vue";
import HomeSection6 from "@/components/Home/HomeSection6.vue";
import MarketView from "@/components/Home/MarketView.vue";

export default {
  name: 'HomeView',
  components: {
    MarketView,
    HomeSection6,
    HomeSection5,
    HomeSection4,
    FaqSection1,
    ContactUs,
    FooterHome,
    HomeSection3,
    HomeSection2,
    HomeSection1,
    SliderSection
  },
}
</script>
