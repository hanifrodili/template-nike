<template lang="pug">
.CTABanner
  .banner-wrapper
    .cta-text
      p.mb-6(style="font-size: 24px") 09 Jan - 24 Jan
      p.text-uppercase.mb-2(style="font-size: 72px; line-height: 60px; font-weight: 800; font-family: 'Nike Futura','Helvetica Neue',Helvetica,Arial,sans-serif;" ) Lunar New Year
      p.mt-6(style="font-size: 16px; line-height:24px") Spend RM450 or more to enjoy 18% off sitewide on your next order.<br>Shop now and receive limited edition Nike Red Packets with every purchase, while stocks last.
    .cta-button
      v-btn(
        color="white"
        rounded
        x-large
      ) Shop
      v-btn(
        color="white"
        rounded
        x-large
      ) Download the Nike App
        
</template>

<script>
export default {
  name: 'CTABanner'
}
</script>

<style lang="scss" scoped>
.CTABanner{
  background-image: url('../assets/images/bg.png');
  background-position: center;
  background-size: cover;
  color: white;
  min-height: 300px;
}
.banner-wrapper{
  padding: 40px 120px;

  .cta-text{
    display: flex;
    flex-direction: column;
    justify-content: center;
    text-align: center;
    margin-bottom: 25px;

    p{
      margin-bottom: 0;
    }
  }

  .cta-button{
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    gap: 6px;

    button{
      text-transform: capitalize;
      box-shadow: none !important;
      height: 39px;
      font-weight: 400;
      letter-spacing: 0em;
    }
  }
}

@media(max-width: 959px){
  .banner-wrapper{
    padding: 40px;
  }
}
</style>
