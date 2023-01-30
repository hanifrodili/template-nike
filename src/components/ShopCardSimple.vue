<template lang="pug">
.ShopCardSimple
  v-card.product-card
    v-img( :src="imgSrc" width="100%" )
    div.d-flex.flex-row.justify-space-between.mt-3.mr-4
      div(style="width:80%")
        h2.card-title {{ title }}
        v-card-subtitle.card-subtitle {{ description }}
      div
        h3.card-title RM {{ price }}
    
</template>

<script>
export default {
  name: 'ShopCardSimple',
  props: {
    imgSrc:{
      type: String
    },
    title: {
      type: String
    },
    description: {
      type: String
    },
    price: {
      type: String
    }
  },
  data: ()=>({
  })
}
</script>

<style lang="scss" scoped>
.ShopCardSimple{
  --column-offset: 18px;
  -ms-flex: 0 0 calc(33% - var(--column-offset));
  flex: 0 0 calc(33% - var(--column-offset));
}
.product-card{
  position: relative;
  width: 30vw;
  min-width: 300px;
  min-height: 300px;
  aspect-ratio: 3/4;
  box-shadow: none !important;
  border-radius: 0;

  .card-title{
    font-size: 16px;
    line-height: 24px;
    font-style: normal;
    text-transform: none;
    color: #111111;
    font-weight: 500;
    padding: 0;
    align-items: flex-start;
  }

  .card-subtitle {
    color: #757575;
    font-size: 16px;
    line-height: 24px;
    font-style: normal;
    text-transform: none;
    font-weight: 400;
    padding: 0;
    align-items: flex-start;
  }
}
</style>
