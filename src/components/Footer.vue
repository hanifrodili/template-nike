<template lang="pug">
.Footer
  v-row
    v-col.col-12.col-md-8()
      v-row
        v-col.footer-col.col-12.col-md-3()
          a.footer-title(href="#") Find a store
          a.footer-title(href="#") Become a member
          a.footer-title(href="#") Sign up for email
          a.footer-title(href="#") Student discounts
          a.footer-title(href="#") Send us feedback

        v-col.footer-col.col-12.col-md-3()
          div.d-flex.flex-row.justify-space-between.align-center(v-if="$vuetify.breakpoint.width < 960" @click="toggleCollapse()")
            p.footer-title Get help
            v-icon.collapsible-icon(color="white" small) mdi-plus
          a.footer-title(href="#" v-else) Get help
          a.footer-item(href="#") Order status
          a.footer-item(href="#") Delivery
          a.footer-item(href="#") Returns
          a.footer-item(href="#") Payments options
          a.footer-item(href="#") Contact us

        v-col.footer-col.col-12.col-md-3()
          div.d-flex.flex-row.justify-space-between.align-center(v-if="$vuetify.breakpoint.width < 960" @click="toggleCollapse()")
            p.footer-title About Nike
            v-icon.collapsible-icon(color="white" small) mdi-plus
          a.footer-title(href="#" v-else) About Nike
          a.footer-item(href="#") News
          a.footer-item(href="#") Careers
          a.footer-item(href="#") Investors
          a.footer-item(href="#") Sustainability
              
    v-col.col-12.col-md-4()
      div.social-media
        a(href="#")
          svg.social-media-item(width="32" height="32" viewBox="0 0 48 48" fill="currentColor" xmlns="http://www.w3.org/2000/svg")
            path(d="M24 0C19.626 0 15.6 1.066 11.92 3.2C8.29145 5.28191 5.28191 8.29145 3.2 11.92C1.066 15.6 0 19.626 0 24C0 28.374 1.066 32.4 3.2 36.08C5.28191 39.7086 8.29145 42.7181 11.92 44.8C15.6 46.934 19.626 48 24 48C28.374 48 32.4 46.934 36.08 44.8C39.7086 42.7181 42.7181 39.7086 44.8 36.08C46.934 32.4 48 28.374 48 24C48 19.626 46.934 15.6 44.8 11.92C42.7181 8.29145 39.7086 5.28191 36.08 3.2C32.4 1.066 28.374 0 24 0ZM36 18.56V19.36C36 22.134 35.334 24.8 34 27.36C32.6844 29.9006 30.726 32.052 28.32 33.6C25.654 35.306 22.666 36.16 19.36 36.16C16.1394 36.1841 12.9776 35.2966 10.24 33.6H11.68C14.454 33.6 16.906 32.746 19.04 31.04C17.76 31.04 16.614 30.64 15.6 29.84C14.586 29.04 13.866 28 13.44 26.72L14.56 27.04C15.306 27.04 15.84 26.934 16.16 26.72C14.7985 26.5214 13.5662 25.8049 12.72 24.72C11.8373 23.6663 11.3556 22.3345 11.36 20.96C12.214 21.494 13.12 21.76 14.08 21.76C12.266 20.694 11.36 19.04 11.36 16.8C11.36 15.734 11.626 14.72 12.16 13.76C13.76 15.68 15.6 17.174 17.68 18.24C19.7914 19.3149 22.1122 19.9156 24.48 20C24.266 19.68 24.16 19.2 24.16 18.56C24.16 16.96 24.746 15.574 25.92 14.4C27.094 13.226 28.48 12.64 30.08 12.64C31.68 12.64 33.174 13.226 34.56 14.4C35.52 14.186 36.8 13.706 38.4 12.96C37.974 14.454 37.12 15.52 35.84 16.16H36C37.494 15.84 38.56 15.52 39.2 15.2C38.134 16.586 37.066 17.706 36 18.56Z" fill="currentColor")

        a(href="#")  
          svg.social-media-item(width="32" height="32" viewBox="0 0 48 48" fill="currentColor" id="icon" xmlns="http://www.w3.org/2000/svg")
            path(d="M24 0C19.626 0 15.6 1.066 11.92 3.2C8.29145 5.28191 5.28191 8.29145 3.2 11.92C1.066 15.6 0 19.626 0 24C0 28.374 1.066 32.4 3.2 36.08C5.28191 39.7086 8.29145 42.7181 11.92 44.8C15.6 46.934 19.626 48 24 48C28.374 48 32.4 46.934 36.08 44.8C39.7086 42.7181 42.7181 39.7086 44.8 36.08C46.934 32.4 48 28.374 48 24C48 19.626 46.934 15.6 44.8 11.92C42.7181 8.29145 39.7086 5.28191 36.08 3.2C32.4 1.066 28.374 0 24 0ZM30.24 24H26.24V38.4H20.8V24H17.28V19.04H20.8V16C20.8 13.76 21.174 12.16 21.92 11.2C22.774 10.026 24.32 9.44 26.56 9.44H30.56V14.4H28.16C27.306 14.4 26.774 14.534 26.56 14.8C26.346 15.066 26.24 15.574 26.24 16.32V18.72H30.56L30.24 24Z" fill="currentColor")

        a(href="#")  
          svg.social-media-item(width="32" height="32" viewBox="0 0 48 48" fill="currentColor" xmlns="http://www.w3.org/2000/svg")
            path(d="M22.56 35.2C22.4711 35.3923 22.3331 35.5578 22.16 35.68C22.0197 35.7803 21.8524 35.836 21.68 35.84C21.52 35.84 21.414 35.786 21.36 35.68C21.2983 35.5279 21.271 35.3639 21.28 35.2V29.28H19.84V35.84C19.8243 36.202 19.9073 36.5615 20.08 36.88C20.24 37.146 20.48 37.28 20.8 37.28C21.12 37.28 21.414 37.174 21.68 36.96C21.946 36.746 22.24 36.48 22.56 36.16V37.12H24V29.28H22.56V35.2ZM13.92 28V26.4H19.2V28H17.44V37.12H15.68V28H13.92ZM23.84 18.56C23.626 18.56 23.44 18.48 23.28 18.32C23.2039 18.248 23.1434 18.1611 23.1021 18.0648C23.0608 17.9685 23.0397 17.8648 23.04 17.76V12.96C23.04 12.854 23.094 12.746 23.2 12.64C23.306 12.534 23.494 12.48 23.76 12.48C24.026 12.48 24.24 12.534 24.4 12.64C24.4784 12.6921 24.5418 12.7639 24.5838 12.8481C24.6259 12.9323 24.6453 13.026 24.64 13.12V17.76C24.64 17.974 24.56 18.16 24.4 18.32C24.328 18.3961 24.2411 18.4566 24.1448 18.4979C24.0485 18.5392 23.9448 18.5603 23.84 18.56ZM27.84 35.2C27.84 33.92 27.894 32.586 28 31.2C28 30.986 27.92 30.8 27.76 30.64C27.6 30.48 27.44 30.4 27.28 30.4H27.04L26.56 30.72V35.52L27.04 35.84L27.36 36C27.574 36 27.706 35.946 27.76 35.84C27.814 35.734 27.84 35.52 27.84 35.2ZM28 29.12C28.426 29.12 28.774 29.28 29.04 29.6C29.306 29.92 29.44 30.4 29.44 31.04V35.52C29.44 36.054 29.334 36.48 29.12 36.8C29.0319 36.9488 28.9003 37.0669 28.7429 37.1385C28.5856 37.21 28.41 37.2315 28.24 37.2C27.9117 37.1581 27.5894 37.0775 27.28 36.96C27.0396 36.8761 26.8396 36.7047 26.72 36.48V37.12H25.12V26.4H26.72V29.92C26.934 29.706 27.146 29.52 27.36 29.36C27.5411 29.2118 27.7661 29.1274 28 29.12ZM35.84 39.36C36.374 38.934 36.694 37.546 36.8 35.2C36.906 34.026 37.014 32.906 37.12 31.84C37.12 30.88 37.014 29.814 36.8 28.64C36.586 26.294 36.24 24.854 35.76 24.32C35.28 23.786 33.226 23.414 29.6 23.2L24.32 23.04L18.88 23.2C15.254 23.414 13.2 23.786 12.72 24.32C12.24 24.854 11.894 26.294 11.68 28.64C11.5735 29.7033 11.5201 30.7713 11.52 31.84C11.52 32.906 11.574 34.026 11.68 35.2C11.894 37.546 12.24 38.96 12.72 39.44C13.2 39.92 15.254 40.32 18.88 40.64L24.32 40.8L29.6 40.64C33.226 40.32 35.306 39.946 35.84 39.52V39.36ZM16.8 8H14.88L17.12 15.2V19.68H19.04V14.88L21.28 8H19.36L18.24 12.64H18.08L16.8 8ZM21.44 13.12V17.6C21.44 18.346 21.654 18.934 22.08 19.36C22.506 19.786 23.094 20 23.84 20C24.586 20 25.174 19.786 25.6 19.36C26.026 18.934 26.24 18.346 26.24 17.6V13.12C26.24 12.48 26.026 11.946 25.6 11.52C25.174 11.094 24.586 10.88 23.84 10.88C23.094 10.88 22.506 11.094 22.08 11.52C21.654 11.946 21.44 12.48 21.44 13.12ZM27.68 11.2V18.4C27.6643 18.762 27.7473 19.1215 27.92 19.44C28.08 19.706 28.346 19.84 28.72 19.84C29.094 19.84 29.44 19.76 29.76 19.6C30.08 19.44 30.4 19.2 30.72 18.88V19.84H32.48V11.2H30.72V17.6C30.6178 17.8089 30.4489 17.9778 30.24 18.08C30.068 18.1753 29.8764 18.2301 29.68 18.24C29.52 18.24 29.414 18.214 29.36 18.16C29.306 18.106 29.28 17.974 29.28 17.76V11.04H27.68V11.2ZM24 0C28.374 0 32.4 1.066 36.08 3.2C39.7086 5.28191 42.7181 8.29145 44.8 11.92C46.934 15.6 48 19.626 48 24C48 28.374 46.934 32.4 44.8 36.08C42.7181 39.7086 39.7086 42.7181 36.08 44.8C32.4 46.934 28.374 48 24 48C19.626 48 15.6 46.934 11.92 44.8C8.29145 42.7181 5.28191 39.7086 3.2 36.08C1.066 32.4 0 28.374 0 24C0 19.626 1.066 15.6 3.2 11.92C5.28191 8.29145 8.29145 5.28191 11.92 3.2C15.6 1.066 19.626 0 24 0ZM33.12 32.16L32.96 31.36C32.96 31.04 32.906 30.8 32.8 30.64C32.7479 30.5616 32.6761 30.4983 32.5919 30.4562C32.5077 30.4141 32.414 30.3947 32.32 30.4C32.226 30.3947 32.1323 30.4141 32.0481 30.4562C31.9639 30.4983 31.8921 30.5616 31.84 30.64C31.734 30.8 31.68 31.04 31.68 31.36V32.16H33.12ZM32.48 29.12C33.12 29.12 33.626 29.306 34 29.68C34.374 30.054 34.56 30.614 34.56 31.36V33.28H31.68V34.88C31.68 35.2 31.734 35.44 31.84 35.6C31.946 35.76 32.134 35.84 32.4 35.84C32.666 35.84 32.854 35.76 32.96 35.6C33.066 35.44 33.12 35.146 33.12 34.72V34.4H34.56V34.88C34.56 35.626 34.374 36.214 34 36.64C33.626 37.066 33.094 37.28 32.4 37.28C31.706 37.28 31.174 37.066 30.8 36.64C30.426 36.214 30.24 35.626 30.24 34.88V31.36C30.24 30.72 30.454 30.186 30.88 29.76C31.306 29.334 31.84 29.12 32.48 29.12Z")
        a(href="#")  
          svg.social-media-item(width="32" height="32" viewBox="0 0 48 48" fill="currentColor" xmlns="http://www.w3.org/2000/svg")
            path(d="M32 24.96C31.7958 26.0026 31.4171 27.0033 30.88 27.92C30.3484 28.8244 29.6412 29.6132 28.8 30.24C27.6874 31.0719 26.3482 31.5462 24.96 31.6C23.5888 31.6571 22.2296 31.3243 21.04 30.64C19.8272 29.9613 18.8503 28.9286 18.24 27.68C17.28 25.76 17.066 23.734 17.6 21.6H15.36L15.52 32.64C15.52 32.854 15.6 33.066 15.76 33.28C15.92 33.494 16.106 33.6 16.32 33.6H32.96C33.174 33.6 33.386 33.494 33.6 33.28C33.814 33.066 33.92 32.854 33.92 32.64V21.6H31.68C32 22.666 32.106 23.786 32 24.96ZM24.64 28.96C25.92 28.96 27.04 28.48 28 27.52C28.96 26.56 29.44 25.414 29.44 24.08C29.4514 22.7763 28.965 21.5174 28.08 20.56C27.174 19.546 26.054 19.04 24.72 19.04C23.386 19.04 22.24 19.52 21.28 20.48C20.32 21.44 19.84 22.586 19.84 23.92C19.84 25.254 20.294 26.426 21.2 27.44C22.106 28.454 23.2 28.96 24.48 28.96H24.64ZM32.96 13.76H30.72C30.506 13.76 30.294 13.866 30.08 14.08C29.866 14.294 29.76 14.506 29.76 14.72V17.44C29.974 17.866 30.294 18.08 30.72 18.08H32.96C33.28 18.08 33.52 17.974 33.68 17.76C33.8282 17.5789 33.9126 17.3539 33.92 17.12V14.72C33.92 14.506 33.814 14.294 33.6 14.08C33.386 13.866 33.174 13.76 32.96 13.76ZM24 0C19.626 0 15.6 1.066 11.92 3.2C8.29145 5.28191 5.28191 8.29145 3.2 11.92C1.066 15.6 0 19.626 0 24C0 28.374 1.066 32.4 3.2 36.08C5.28191 39.7086 8.29145 42.7181 11.92 44.8C15.6 46.934 19.626 48 24 48C28.374 48 32.4 46.934 36.08 44.8C39.7086 42.7181 42.7181 39.7086 44.8 36.08C46.934 32.4 48 28.374 48 24C48 19.626 46.934 15.6 44.8 11.92C42.7181 8.29145 39.7086 5.28191 36.08 3.2C32.4 1.066 28.374 0 24 0ZM36.48 33.76L36.32 33.92V34.08C36.3245 34.3329 36.2771 34.5841 36.1808 34.818C36.0845 35.0519 35.9413 35.2636 35.76 35.44C35.3897 35.8117 34.9156 36.0627 34.4 36.16H15.04C14.7799 36.1616 14.5228 36.105 14.2874 35.9942C14.0521 35.8835 13.8445 35.7214 13.68 35.52C13.3163 35.1125 13.0677 34.6155 12.96 34.08L12.8 33.76L12.96 14.08C12.96 13.546 13.146 13.066 13.52 12.64C13.894 12.214 14.346 11.946 14.88 11.84H34.24C34.7556 11.9373 35.2297 12.1883 35.6 12.56C35.9717 12.9303 36.2227 13.4044 36.32 13.92L36.48 33.76Z" fill="currentColor")
  .sub-footer.mt-4.pt-6
    v-row
      v-col.d-flex.col-12.col-md-6(:class="$vuetify.breakpoint.width < 960 ? 'flex-column' : 'flex-row align-center'" style="gap:10px")
        div.d-flex.flex-row.mr-5(style="gap:10px")
          img(:src="require('../assets/images/pin.svg')" height="15")
          p.mb-0(style="font-size: 12px; color: white") {{ location }}
        div
          p.mb-0(style="font-size: 12px; color: #7e7e7e") © 2023 Nike, Inc. All Rights Reserved
      v-col.col-12.col-md-6
        div.d-flex.justify-end(style="gap:12px" :class="$vuetify.breakpoint.width < 960 ? 'flex-column justify-space-between' : 'flex-row'")
          a.footer-item.pa-2(href="#") Guides
          a.footer-item.pa-2(href="#") Terms of sale
          a.footer-item.pa-2(href="#") Terms of use
          a.footer-item.pa-2(href="#") Nike Privacy Policy
</template>

<script>
export default {
  name: 'FooterSection',
  mounted() {
    this.getLocation()
  },
  data: ()=>({
    location: ''
  }),
  methods: {
    getLocation() {
      fetch('https://get.geojs.io/v1/ip/country.json')
        .then((response) => response.json())
        .then((data) => this.location = data.name);
    },

    toggleCollapse() {
      if (this.$vuetify.breakpoint.width < 960) {
        var coll = document.getElementsByClassName("footer-col");
        var i;

        for (i = 0; i < coll.length; i++) {
          coll[i].addEventListener("click", function () {
            // console.log(this.children[0].scrollHeight);
            let colHeight = parseInt(window.getComputedStyle(this).height.replace('px', ''))
            const collapsedHeight = this.children[0].scrollHeight + parseInt(window.getComputedStyle(this.children[0]).marginBottom.replace('px', ''))
            const openHeight = this.scrollHeight

            if (colHeight > collapsedHeight) {
              colHeight = collapsedHeight + "px"
              this.classList.remove('open')
            } else {
              colHeight = openHeight + "px"
              this.classList.add('open')
            }

            this.style.height = colHeight
          });
        }
       
      }
    }
  }
}
</script>

<style lang="scss" scoped>
.Footer {
  padding: 40px;
  padding-bottom: 0;
  background-color: #111;
  height: auto;
  min-height: 300px;
  width: 100%;

  .footer-title {
    color: #fff;
    text-transform: uppercase;
    font-family: Nike TG,Helvetica Neue,Helvetica,Arial,sans-serif;
    font-size: 14px;
    font-weight: 400;
    line-height: 2;
    margin-bottom: 4px;
  }

  .footer-item {
    color: #7e7e7e;
    text-transform: capitalize;
    font-family: Helvetica Neue,Helvetica,Arial,sans-serif;
    font-size: 12px;
    font-weight: 400;
    line-height: 2;
    padding: 4px 0 !important;
  }

    .footer-item:hover {
      color: #fff;
    }

  .footer-col {
    display: flex;
    flex-direction: column;
    overflow: hidden;
    transition: height ease-in .3s;
    margin-bottom: 20px;
  }

  .social-media {
    display: flex;
    flex-direction: row;
    gap: 16px;
    justify-content: flex-end;

    .social-media-item{
      color: #7e7e7e;
    }
    .social-media-item:hover{
      color: #fff;
    }
  }
  @media(min-width: 959px) {
    .footer-col:not(:nth-child(1)) {
      height: auto !important;
      overflow: hidden;
    }
  }
  @media(max-width: 959px) {
    .footer-col:not(:nth-child(1)) {
      height: 32px;
      overflow: hidden;
    }

    .footer-item {
      font-size: 12px;
      line-height: 2.333333333333333;
    }

    .collapsible-icon {
      transition: transform ease-in .3s;
    }

    .footer-col.open {
      div{
        .collapsible-icon {
          transform: rotate(45deg);
        }
      }
    }
    .social-media {
      justify-content: flex-start;
    }
  }
}

@media(max-width: 959px) {
  .Footer {
    padding: 28px 20px;
  }
}
</style>
