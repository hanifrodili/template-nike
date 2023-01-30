<template lang="pug">
.MiddleBanner
  .banner-wrapper
    v-carousel(
      cycle
      height="100%"
      hide-delimiter-background
      hide-delimiters
      :show-arrows="false"
    )
      v-carousel-item
        .slide-wrapper
          p Lunar New Year
          p Get 18% off sitewide* on your next order. 
            a Shop Promo Terms
      v-carousel-item
        .slide-wrapper
          p Lunar New Year
          p Receive limited edition Nike Red Packets with every purchase, while stocks last. 
            a Shop Promo Terms
      v-carousel-item
        .slide-wrapper
          p Free Standard Delivery & 30-Day Free Returns
          p
            a Join Now View Details
</template>

<script>
export default {
  name: 'CarouselBanner'
}
</script>

<style lang="scss" scoped>
a{
  color: black !important;
  font-weight: 500;
  text-decoration: underline;
}
.banner-wrapper{
    height: auto;
    min-height: 58px;
    transition: all .5s;
    box-shadow: inset 0 -1px 0 0 #e5e5e5;
    position: relative;
    background: #f5f5f5;
    overflow: hidden;
    padding: 0 20px;
    padding-top: 10px;
    padding-bottom: 8px;

    .slide-wrapper{
      display: flex;
      align-items: center;
      text-align: center;
      flex-direction: column;
      p{
        margin-bottom: 0
      }
      p:nth-child(1){
        font-size: 16px;
        font-weight: 500;
        line-height: 24px;
      }
      p:nth-child(2){
        font-size: 12px;
        line-height: 28px;
      }
    }
  }
</style>
