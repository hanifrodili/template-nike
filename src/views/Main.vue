<template lang="pug">
.main
  top-header
  carousel-banner
  cta-banner
  main-content
  quick-links
  bottom-footer
</template>

<script>
  import TopHeader from "@/components/Navbar.vue";
  import CarouselBanner from "@/components/CarouselBanner.vue";
  import CtaBanner from "@/components/CTABanner.vue";
  import MainContent from "@/components/MainContent.vue";
  import QuickLinks from "@/components/QuickLinks.vue";
  import BottomFooter from "@/components/Footer.vue";

  export default {
    name: 'MainPage',
    mounted() {
      document.title = 'Home - Nike MY'
    },
    components: {
      TopHeader,
      CarouselBanner,
      CtaBanner,
      MainContent,
      QuickLinks,
      BottomFooter
    },
  }
</script>
