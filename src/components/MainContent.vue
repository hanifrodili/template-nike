<template lang="pug">
.MainContent.mb-14
  content-section.top
    template( v-slot:content )
        v-card.product-cta.full
          img.card-bg-image(:src="require('../assets/images/nike-0.webp')")
          .card-content
            v-card-text.pa-0
              p(style="font-weight: 500;font-size: 16px;line-height: 1.5;") Nike Free Metcon 4
              p.nike-font(style="") For Your <br>Every Move
            v-card-actions.pa-0
              v-btn.btn-cta(
                color="white"
                rounded
                x-large
              ) Shop the Feeling

  content-section.featured
    template( v-slot:title )
      | Featured
    template( v-slot:content )
      //- v-img( src="https://picsum.photos/900/1600" )
      div.d-flex.flex-row.overflow-auto(style="gap:12px")
        v-card.product-cta.half
          img.card-bg-image(:src="require('../assets/images/nike-1.webp')")
          .card-content
            v-card-text.pa-0
              p.mb-0(style="font-weight: 500;font-size: 16px;line-height: 1.5;") Effortless Everyday Wear
              h2(style="font-weight: 500;font-size: 20px;line-height: 1.2;") Varsity Vintage Styles
            v-card-actions.pa-0
              v-btn.btn-cta(
                color="white"
                rounded
                x-large
              ) Shop
        v-card.product-cta.half
          img.card-bg-image(:src="require('../assets/images/nike-2.jpeg')")
          .card-content
            v-card-text.pa-0
              //- p(style="font-weight: 500;font-size: 16px;line-height: 1.5;") Effortless Everyday Wear
              h2(style="font-weight: 500;font-size: 20px;line-height: 1.2;") Nike React Infinity 3
            v-card-actions.pa-0
              v-btn.btn-cta(
                color="white"
                rounded
                x-large
              ) Shop

  content-section.shop
    template( v-slot:title )
      | Shop Nike Shoes
    template( v-slot:content ) 
      card-slider
  
  content-section.latest
    template( v-slot:title )
      p The Latest
    template( v-slot:content ) 
      div.overflow-hidden(style="aspect-ratio:2/1")
        video(autoplay muted style="width:100%;")
          source(:src="require('../assets/videos/fall.mp4')" type="video/mp4")
      
      div.text-center.mt-12
        p.mb-1(style="font-size: 16px; line-height: 1.5; font-weight: 500;") The all new Phantom GX
        p.mb-2.text-uppercase.nike-font(style="" ) More Grip.<br>More Precision.
        p.mt-6(style="font-size: 16px; line-height:24px") Phantom GX's precision, powered by Gripknit™
        v-btn.btn-cta.mt-6(
          color="black"
          rounded
          x-large
          style="height: 39px; color: white"
        ) Shop

  content-section.gear-up
    template( v-slot:title )
      | Gear Up
    template( v-slot:content ) 
      div.overflow-hidden(style="aspect-ratio:2/1")
        v-img( :src="require('../assets/images/nike-4.webp')" width="100%" )
      
      div.text-center.mt-12
        p.mb-1(style="font-size: 16px; line-height: 1.5; font-weight: 500;") Nike Yoga
        p.mb-2.text-uppercase.nike-font(style="" ) Stay Present in<br>Every Pose
        p.mt-6(style="font-size: 16px; line-height:24px") Focus on your practice, not your clothes thanks to yoga essentials<br>with soft, breathable fabrics and free-flowing fits.
        v-btn.btn-cta.mt-6(
          color="black"
          rounded
          x-large
          style="height: 39px; color: white"
        ) Shop

  content-section.more
    template( v-slot:title )
      | More Nike
    template( v-slot:content )
      div.d-flex.flex-row.overflow-x-auto(style="gap:12px")
        category-card(:img-src="require('../assets/images/nike-1.webp')" button-text="Men's")
        category-card(:img-src="require('../assets/images/nike-1.webp')" button-text="Women's")
        category-card(:img-src="require('../assets/images/nike-1.webp')" button-text="Kids'")
</template>

<script>
import ContentSection from "@/components/ContentSection.vue";
import CardSlider from "@/components/Slider.vue";
import CategoryCard from "@/components/CategoryCard.vue";


export default {
  name: 'MainContent',
  components: {
    ContentSection,
    CardSlider,
    CategoryCard
  },
}
</script>

<style lang="scss" scoped>
.product-cta{
  position: relative;
  overflow: hidden;
  box-shadow: none !important;
  border-radius: 0;
  min-width: 300px;
  width: 50%;

  h2,p{
    color: #fff;
  }

  .card-bg-image{
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    height: 100%;
    z-index: 0;
  }

  .card-content{
    display: flex;
    flex-direction: column;
    gap: 24px;
    position: absolute;
    z-index: 1;
    width: 100%;
    padding: 35px;
    bottom: 0;
    background: linear-gradient(0deg, rgba(0, 0, 0, 0.8) 0%, rgba(0, 212, 255, 0) 100%);
  }
}

.product-cta.full {
  aspect-ratio: 16/9;
  width: 100%;
}

.product-cta.half {
  aspect-ratio: 3/4;
  width: 50%;
}

.btn-cta{
  text-transform: capitalize;
  box-shadow: none !important;
  height: 39px !important;
  font-weight: 400;
  letter-spacing: 0em;
  font-weight: 500;
  padding: 6px 20px !important;
}

.btn-cta:hover {
  background-color: #b2b2b2 !important;
}

.nike-font {
  font-weight: 500;
  font-size: 72px;
  line-height: 60px;
  font-family: 'Nike Futura', 'Helvetica Neue', Helvetica, Arial, sans-serif;
}

@media (max-width: 959px){
  .nike-font{
    font-size: 48px;
    line-height: 40px;
  }

  .product-cta.full {
    aspect-ratio: 3/4;

    .card-bg-image{
      transform: translate(-25%, -50%);
    }
  }
}
</style>
