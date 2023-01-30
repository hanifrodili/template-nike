<template lang="pug">
.CategoryCard
  v-card.product-cat()
    v-img.card-bg-image(:src="imgSrc")
    v-btn.btn-cta(
      color="white"
      rounded
      x-large
      style="position:absolute; bottom: 48px"
    ) {{ buttonText }}
      
</template>

<script>
export default {
  name: 'CategoryCard',
  props: {
    imgSrc: {
      type: String
    },
    buttonText: {
      type: String
    },
    url: {
      type: String
    }
  },
}
</script>

<style lang="scss" scoped>
.CategoryCard {
  flex-grow: 1;
}
.product-cat {
  position: relative;
  overflow: hidden;
  // width: calc(100%/3);
  min-width: 300px;
  min-height: 300px;
  aspect-ratio: 1;
  box-shadow: none !important;
  border-radius: 0;
  padding:48px;

  .card-bg-image {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    height: 100%;
    z-index: 0;
  }
}

.btn-cta {
  text-transform: capitalize;
  box-shadow: none !important;
  height: 39px !important;
  font-weight: 400;
  letter-spacing: 0em;
  font-weight: 500;
  padding: 6px 20px;
}

.btn-cta:hover {
  background-color: #b2b2b2 !important;
}
</style>
