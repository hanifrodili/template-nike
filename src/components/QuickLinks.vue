<template lang="pug">
.QuickLinks.mx-auto.mb-14.px-5
  v-row.cat-row
    v-col.cat-col.col-12.col-md-3()
      h3.cat-title(@click="toggleCategory($event)") Icon
      a.cat-item(href="#") Air Force 1
      a.cat-item(href="#") Huarache
      a.cat-item(href="#") Air Max 90
      a.cat-item(href="#") Air Max 95
      a.cat-item(href="#") Air Max 95
      a.cat-item(href="#") Air Max 270
    
    v-col.cat-col.col-12.col-md-3()
      h3.cat-title(@click="toggleCategory($event)") Shoes
      a.cat-item(href="#") Air Force 1
      a.cat-item(href="#") Huarache
      a.cat-item(href="#") Air Max 90
      a.cat-item(href="#") Air Max 95
      a.cat-item(href="#") Air Max 95
      a.cat-item(href="#") Air Max 270
    
    v-col.cat-col.col-12.col-md-3()
      h3.cat-title(@click="toggleCategory($event)") Clothing
      a.cat-item(href="#") Air Force 1
      a.cat-item(href="#") Huarache
      a.cat-item(href="#") Air Max 90
      a.cat-item(href="#") Air Max 95
      a.cat-item(href="#") Air Max 95
      a.cat-item(href="#") Air Max 270
    
    v-col.cat-col.col-12.col-md-3()
      h3.cat-title(@click="toggleCategory($event)") Kids
      a.cat-item(href="#") Air Force 1
      a.cat-item(href="#") Huarache
      a.cat-item(href="#") Air Max 90
      a.cat-item(href="#") Air Max 95
      a.cat-item(href="#") Air Max 95
      a.cat-item(href="#") Air Max 270
</template>

<script>
export default {
  name: 'QuickLinks',
  data: ()=>({

  }),
  methods: {
    toggleCategory(event) {
      if (this.$vuetify.breakpoint.width < 960) {
        let colHeight = parseInt(window.getComputedStyle(event.target.parentNode).height.replace('px', ''))
        const collapsedHeight = event.target.scrollHeight + parseInt(window.getComputedStyle(event.target).marginBottom.replace('px', ''))
        const openHeight = event.target.parentNode.scrollHeight

        if (colHeight > collapsedHeight) {
          colHeight = collapsedHeight + "px"
        } else {
          colHeight = openHeight + "px"
        }

        event.target.parentNode.style.height = colHeight
      }
    }
  }
}
</script>

<style lang="scss" scoped>
.QuickLinks {
    max-width: 880px;
    width: 100%;

    // .cat-row {
    //   height: 100%;
    //   max-height: calc((36px * 4) + 48px);
    //   overflow: hidden;
    //   transition: max-height ease-in 0.5s;
    // }

    // .cat-row:has(.cat-col:hover) {
    //   height: auto;
    //   max-height: 100%;
    // }

    .cat-col {
      display: flex;
      flex-direction: column;
      transition: height ease-in .3s;

      .cat-title{
        font-size: 16px;
        line-height: 24px;
        margin-bottom: 24px;
        font-weight: 500;
        cursor: pointer;
      }

      .cat-item{
        font-size: 16px;
        line-height: 24px;
        margin-bottom: 12px;
        font-weight: 500;
        color: #757575;
      }

      .cat-item:hover {
        color: #111 !important;
      }
    }

    @media(max-width: 959px){
      .cat-col{
        height: 48px;
        overflow: hidden;
      }
    }
  }
</style>
