<template>
  <div :class="{ change_color: scrollPosition > 50 }" id="container-header">
    <div class="innerContainer">
      <div class="logoContainer">
        <NuxtLink to="/"
          ><img src="~/assets/images/logo.svg" alt="" />
          <span>astroGo</span></NuxtLink
        >
      </div>
      <div>
        <ul class="NavEntries">
          <NuxtLink to="/">Home</NuxtLink>
          <NuxtLink v-bind:to="section2">About</NuxtLink>
          <NuxtLink v-bind:to="section2" v-on:click.native="isActiveFunc"
            >Features
            <span v-if="isActive"
              ><img
                src="~/assets/images/arrow-down-sign-to-navigate.png"
                alt=""
            /></span>
            <span v-if="!isActive"
              ><img src="~/assets/images/up-arrow.png" alt="" /></span
          ></NuxtLink>
          <NuxtLink v-bind:to="section4">Team</NuxtLink>
          <NuxtLink v-bind:to="section5">Blog</NuxtLink>
        </ul>
      </div>
      <v-btn id="btn">GET IN TOUCH</v-btn>

      <div id="navToggleIcon">
        <v-icon v-if="!toggleNav" @click="toggleMenu()" light>mdi-menu</v-icon>
        <v-icon v-if="toggleNav" @click="toggleMenu()" light>mdi-close</v-icon>
      </div>
    </div>
    <div id="dropdown-menu" v-if="toggleNav">
      <DropdownMenuComponent @click.native="toggleMenu()" />
    </div>
    <!-- <div  >
      <ThirdComponent  />
    </div> -->
  </div>
</template>
<script>
export default {
  props: ["section1", "section2", "section3", "section4", "section5"],
  data: function () {
    return {
      toggleNav: false,
      scrollPosition: null,
      isActive: false,
    };
  },

  beforeMount() {
    window.addEventListener("scroll", this.handleScroll);
  },
  methods: {
    toggleMenu() {
      this.toggleNav = !this.toggleNav;
    },

    isActiveFunc() {
      this.isActive = !this.isActive;
    },
    handleScroll() {
      console.log(window.scrollY);
      this.scrollPosition = window.scrollY;
    },
  },
  mounted() {
    window.addEventListener("scroll", this.handleScroll);
  },
};
</script>
<style lang="scss" scoped>
#navToggleIcon {
  display: none;
}
.change_color {
  background-color: rgb(26, 25, 25) !important;
  
    a{
      color: white !important;
    }

    .NavEntries>span{
      color: white;
    }
}
#container-header {
  font-family: "Josefin Sans";
  background-color: transparent;
  position: fixed;
  z-index: 1;
  height: 100px;
  margin: 0;
  right: 0;
  left: 0;
  // box-shadow: 0 1px 2px rgba(102, 102, 102, 0.19), 0 2px 2px rgba(0, 0, 0, 0.23);
  width: 100%;

  #btn{
    background-color: rgb(211, 23, 79);
    color: white;
    letter-spacing: 2px;
    margin: 8px 0; 
  }
  .innerContainer {
    padding: 25px 6vw;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
  }
  .logoContainer {
    display: inline-block;
    vertical-align: middle;
    font-size: 22px;
    height: 100%;
    span {
      vertical-align: middle;
    }
    img {
      vertical-align: middle;
      width: 50px;
      height: 50px;
    }
  }
  .NavEntries {

    height: 100%;
    @media only screen and (min-width: 1100px) {
      display: grid;
    }
    @media only screen and (max-width: 1100px) {
      display: none;
    }
    padding: 15px 0;
    grid-auto-flow: column;
    grid-column-gap: 22px;
    align-items: center;
    li {
      list-style-type: none;
      display: inline;
      font-size: 14px;
      background-color: transparent !important;
    }

    img {
      padding-left: 10px;
      height: 10px;
    }
  }
  a {
    font-weight: bold;
    color: black;
    text-decoration: none;
    font-size: clamp(10px, 2.5vw, 14px);
    font-weight: 600;

    &.router-link-exact-active {
      color: #33c3c9;
    }
  }
  a:hover {
    opacity: 0.5;
  }
  a:active{
    font-weight: bold !important;
    color: blanchedalmond;
  }
}
@media only screen and (max-width: 1100px) {

  #btn{
    display: none;
  }
  #navToggleIcon {
    display: inline-block;
    padding: 10px ;
    margin: 0;
    height: 70px;
   
  }
}
</style>