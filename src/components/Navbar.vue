<template lang="pug">
header.top-header
  .header-wrapper
    .header-brand-logo
      v-img( :src="require('@/assets/images/nike.svg')" )  
    .header-nav  
      ul.top-menu-list
        li.top-menu-text Men
        li.top-menu-text Women
        li.top-menu-text Kids
    .header-button
      v-btn.pa-2(icon)
        v-img.button-icon( :src="require('@/assets/images/favourites.svg')" )
      v-btn.pa-2(icon)
        v-img.button-icon( :src="require('@/assets/images/bag.svg')" )
      v-btn.pa-2.nav-mobile-btn(icon @click="openNav()")
        v-img.button-icon( :src="require('@/assets/images/hamburger.svg')" )  

  .mobile-nav
    .mobile-nav-panel
      v-btn.pa-2.button-icon.close-nav-btn(icon @click="closeNav()")
        svg(aria-hidden="true" class="pre-close-icon" focusable="false" viewBox="0 0 24 24" role="img" width="24px" height="24px" fill="none")
          path(stroke="#111" stroke-width="1.5" d="M18.973 5.027L5.028 18.972M5.027 5.027l13.945 13.945")
      .main-menu
        ul.mobile-menu-list
          li.mobile-menu-text(@click="openSubmenu('men')")
            |Men
            svg(width="8" height="15" viewBox="0 0 28 50" fill="none" xmlns="http://www.w3.org/2000/svg")
              path(d="M1 49L26 25.0017L1 1" stroke="black" stroke-width="5")

          li.mobile-menu-text(@click="openSubmenu('women')")
            |Women
            svg(width="8" height="15" viewBox="0 0 28 50" fill="none" xmlns="http://www.w3.org/2000/svg")
              path(d="M1 49L26 25.0017L1 1" stroke="black" stroke-width="5")

          li.mobile-menu-text(@click="openSubmenu('kids')")
            |Kids
            svg(width="8" height="15" viewBox="0 0 28 50" fill="none" xmlns="http://www.w3.org/2000/svg")
              path(d="M1 49L26 25.0017L1 1" stroke="black" stroke-width="5")
      
      .second-menu
        v-btn.pa-2.button-icon.back-nav-btn(icon @click="backMainMenu()")
          svg(width="8" height="15" viewBox="0 0 28 50" fill="none" xmlns="http://www.w3.org/2000/svg" style="transform: rotateZ(180deg)")
            path(d="M1 49L26 25.0017L1 1" stroke="black" stroke-width="5")
          .pl-4(style="font-size:16px; color: #111") Back
        ul.mobile-submenu-list(id="men")
          li.mb-4.submenu-title Men
          li.mobile-submenu-text(href="#" )
            |New & Feature
          li.mobile-submenu-text(href="#" )
            |Shoes
          li.mobile-submenu-text(href="#" )
            |Clothing
        
        ul.mobile-submenu-list(id="women")
          li.mb-4.submenu-title Women
          li.mobile-submenu-text(href="#" )
            |New & Feature
          li.mobile-submenu-text(href="#" )
            |Shoes
          li.mobile-submenu-text(href="#" )
            |Clothing

        ul.mobile-submenu-list(id="kids")
          li.mb-4.submenu-title Kids
          li.mobile-submenu-text(href="#" )
            |New & Feature
          li.mobile-submenu-text(href="#" )
            |Shoes
          li.mobile-submenu-text(href="#" )
            |Clothing
</template>

<script>
export default {
  name: 'TopHeader',
  methods: {
    openNav() {
      document.querySelector("body").classList.add("mobile-nav-open")
    },
    closeNav() {
      document.querySelector("body").classList.remove("mobile-nav-open")
    },
    openSubmenu(id) {
      document.querySelector(".second-menu").style.transform = "translateX(0px)"
      document.querySelector(`#${id}`).style.display = "block"
      document.querySelector(`#${id}`).style.pointerEvents = "all"
    },
    backMainMenu() {
      document.querySelector(".second-menu").style.transform = "translateX(320px)"
      document.querySelectorAll(".mobile-submenu-list").forEach(element => {
        element.style.display = "none"
        element.style.pointerEvents = "none"
      });
    }
  } 
}
</script>

<style lang="scss" scoped>
.top-header{
  background: #fff;
  position: relative;
  height: 60px;
  width: 100%;
  transition: transform .15s ease;
  z-index: 2
}
.header-wrapper{
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  height: 100%;
  max-width: 1920px;
  padding: 0 14px 0 16px;
  opacity: 1;
}

.header-brand-logo{
  width: 79.8px;
  display: flex;
  place-content: center;
}

.header-nav{
  display: none;
  align-items: center;
  .top-menu-list{
    font-weight: 500;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    list-style: none;
    padding: 0;
  }
  .top-menu-text{
    padding: 16px 12px 18px 12px;
    border-bottom: 2px solid transparent;
    cursor: pointer;
  }

  .top-menu-text:hover {
    border-bottom: 2px solid black;
  }
}

.header-button{
  display: flex;
  align-items: center;
  gap: 12px;
  .button-icon{
    width: 20px;
  }
}

.mobile-nav {
  pointer-events: none;
  width: 100vw;
  height: 100vh;
  position: absolute;z-index: 9;
  backdrop-filter: blur(0);
  background-color: rgba(0,0,0,0);
  inset: 0;
  transition: background ease-in-out .25s;

  .mobile-nav-panel{
    position: absolute;
    overflow-x: hidden;
    inset: 0;
    height: 100vh;
    background-color: #fff;
    padding: 40px 0 0 0;
    width: 320px;
    transform: translateX(320px);
    transition: transform ease-in-out .25s;
    margin-left: auto;

    .main-menu {
      padding: 30px 30px 150px 36px;
      height: 100%;
      width: 320px;
      background-color: #fff;
      position: absolute;
      top: 45px;
      right: 0;
      left: 0;
      bottom: 0;
      
      .mobile-menu-list{
        list-style: none;
        padding-left: 0;

        .mobile-menu-text{
          padding: 10px 0;
          font-weight: 500;
          font-size: 24px;
          line-height: 1.6;
          display: flex;
          flex-direction: row;
          justify-content: space-between;
          align-items: center;
        }
      }
    }

    .second-menu {
      padding: 30px 30px 150px 36px;
      height: 100%;
      width: 320px;
      background-color: #fff;
      position: absolute;
      right: 0;
      left: 0;
      bottom: 0;
      transform: translateX(320px);
      transition: transform ease-in-out .25s;

      .mobile-submenu-list{
        margin-top: 58px;
        display: none;
        pointer-events: none;
        list-style: none;
        padding-left: 0;

        .mobile-submenu-text{
          padding: 4px 0;
          font-weight: 500;
          font-size: 16px;
          line-height: 1.5;
          color: #757575;
          display: flex;
          flex-direction: row;
          justify-content: space-between;
          align-items: center;
        }
      }

      .submenu-title{
        font-weight: 500;
        font-size: 24px;
        line-height: 28px;
      }
    }
  }

  .close-nav-btn{
    position: absolute;
    right: 14px;
    top: 14px;
    margin-right: 10px;
  }

  .back-nav-btn{
    position: absolute;
    left: 56px;
    top: 30px;
    // margin-left: 10px;
  }
}

@media(min-width: 960px) {
  .header-wrapper{
    padding: 0 38px 0 36px;
  }
  .header-nav {
    display: flex;
  }
  .nav-mobile-btn {
    display: none;
  }
}
</style>

<style lang="scss">
body{
  overflow-x: hidden;
}
body.mobile-nav-open {
  overflow: hidden;
  position: fixed;
  top: 0;
  right: 0;
  left: 0;
  bottom: 0;

  .mobile-nav {
    pointer-events: all;
    backdrop-filter: blur(5px);
    background-color: rgba(0, 0, 0, 0.5);

    .mobile-nav-panel {
      transform: translateX(0);
    }
  }
}
</style>
