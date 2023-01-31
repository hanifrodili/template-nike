<template lang="pug">
.Slider
  .slider-button
    a(href="#")
      v-btn(text)
        p.mb-0.text-capitalize(style="font-size:16px; font-weight:500; line-height: 24px;") Shop
    div.nav
      v-btn.pa-2.nav-button-left(icon @click="goPrev()")
        img.button-icon( :src="require('../assets/images/arrow.svg')" style="transform: rotateZ(180deg)")
      v-btn.pa-2.nav-button-right(icon @click="goNext()")
        img.button-icon( :src="require('../assets/images/arrow.svg')" )

  .slider-items#slides
    shop-card-simple(v-for="item in 12" :key="item" :img-src="require('../assets/images/nike-3.webp')" :title="`NikeCourt Air Zoom Vapor ${item}`" price="709" description="Women's Hard Court Tennis Shoes")
</template>

<script>
import ShopCardSimple from "@/components/ShopCardSimple.vue";

export default {
  name: 'CardSlider',
  components: {
    ShopCardSimple
  },
  mounted() {
    this.initSlides()
  },
  methods: {
    initSlides() {
  
      var slides = document.getElementById("slides")

      const checkScroll = (e) => {
        var horizontal = e.scrollLeft;
        // var vertical = e.currentTarget.scrollTop;
        var width = e.offsetWidth;
        var scrollWidth = e.scrollWidth;
        // console.log("left:" + horizontal, "right:" + (scrollWidth - horizontal), "width:" + width)
        var navLeft = document.querySelector(".nav-button-left")
        var navRight = document.querySelector(".nav-button-right")
        if (horizontal >= 0) {
          navLeft.style.opacity = '1'
          navLeft.style.pointerEvents = 'auto'
        }
        if (horizontal <= 0) {
          navLeft.style.opacity = '0.3'
          navLeft.style.pointerEvents = 'none'
        }

        if (scrollWidth - horizontal <= width) {
          navRight.style.opacity = '0.3'
          navRight.style.pointerEvents = 'none'
        }
        if (scrollWidth - horizontal > width) {
          navRight.style.opacity = '1'
          navRight.style.pointerEvents = 'auto'
        }
      }

      checkScroll(slides)

      slides.addEventListener("scroll", ()=>{
        checkScroll(slides)
      });
    },

    goNext() {
      var slides = document.getElementById("slides")
      slides.scrollLeft += (300+12)
    },

    goPrev() {
      var slides = document.getElementById("slides")
      slides.scrollLeft -= (300+12)
    },

    // isScrolledIntoViewHorizontal(el) {
    //   var rect = el.getBoundingClientRect();
    //   var elemLeft = rect.left;
    //   var elemRight = rect.right;

    //   // Only completely visible elements return true:
    //   var isVisible = (elemLeft >= 0) && (elemRight <= window.innerWidth);
    //   // Partially visible elements return true:
    //   //isVisible = elemTop < window.innerHeight && elemBottom >= 0;
    //   return isVisible;
    // }
  }
}
</script>

<style lang="scss" scoped>
.slider-button {
  display: flex;
  flex-direction: row;
  gap: 12px;
  align-items: center;
  justify-content: flex-end;
  margin-top: -60px;
  margin-bottom: 12px;

  p {
    margin-bottom: 0;
  }

  .nav {
    display: flex;
    flex-direction: row;
    gap: 12px;
    .v-btn {
      width: 48px;
      height: 48px;
      background-color: #e5e5e5;
    }
  }

  .button-icon {
    height: 14px;
    width: 14px;
  }
}
.slider-items {
  --carousel-padding: 24px;
  display: flex;
  flex-direction: row;
  gap: 12px;
  overflow-x: scroll;
  padding-right: var(--carousel-padding);
  scroll-snap-type: x mandatory;
  margin-left: calc(-1 * var(--carousel-padding));
  margin-right: calc(-1 * var(--carousel-padding));
  padding-inline-start: var(--carousel-padding);
  -webkit-scroll-padding: 0 var(--carousel-padding);
  -moz-scroll-padding: 0 var(--carousel-padding);
  -ms-scroll-padding: 0 var(--carousel-padding);
  scroll-padding: 0 var(--carousel-padding);
  scroll-behavior: smooth;

  * {
    scroll-snap-align: start;
  }
}

@media(max-width: 959px) {
  .slider-button {
    margin-top: -55px;
    margin-bottom: 25px;
    .nav{
      display: none;
    }
  }
}
</style>
