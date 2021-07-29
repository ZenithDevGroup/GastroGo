<template>
  <div class="HeaderContainer">
    <div class="innerContainer">
      <div class="logoContainer">
        <NuxtLink to="/"><span>GastroGo</span></NuxtLink>
      </div>
      <div >
        <ul class="NavEntries">
        <NuxtLink to="/" >HOME</NuxtLink>
        <NuxtLink v-bind:to="section2">ABOUT US</NuxtLink>
        <NuxtLink v-bind:to="section3">OUR PARTNERS</NuxtLink>
        <NuxtLink v-bind:to="section4">FAQ</NuxtLink>
        <NuxtLink v-bind:to="section5">CONTACT US</NuxtLink>
      </ul>
      </div>
      <div id="navToggleIcon">
        <v-icon v-if="!toggleNav" @click="toggleMenu()">mdi-menu</v-icon>
         <v-icon v-if="toggleNav" @click="toggleMenu()">mdi-close</v-icon>
      </div>
    </div>
    <div  id="dropdown-menu" v-if="toggleNav">
      <DropdownMenuComponent @click.native="toggleMenu()"/>
    </div>
  </div>
</template>
<script>
export default {
  props:['section1', 'section2', 'section3','section4','section5'],
  data: function(){
    return {
      toggleNav:false,
    }
  },
  methods: {
     toggleMenu(){
       this.toggleNav =!this.toggleNav
    }, 
  }
}
</script>
<style lang="scss" scoped>
#navToggleIcon {
  display: none;
}
.HeaderContainer {
  background-color: rgb(236, 236, 236) !important;
  position: fixed;
  z-index: 999;
  box-shadow: 0 1px 2px rgba(102, 102, 102, 0.19), 0 2px 2px rgba(0, 0, 0, 0.23);
  width: 100%;
  .innerContainer {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
  }
  .logoContainer {
    justify-content: center;
    padding: 30px 10vw;
    img {
      width: 20px;
    }
  }
  .NavEntries {
    @media only screen and (min-width: 1100px) {
      display: grid;
    }
    @media only screen and (max-width: 1100px) {
      display: none;
    }
    padding: 0 10vw;
    margin: 0;
    height: 70px;
    grid-auto-flow: column;
    grid-column-gap: 22px;
    align-items: center;
    li {
      list-style-type: none;
      display: inline;
      font-size: 14px;
      background-color: transparent !important;
    }
  }
  a {
    font-weight: bold;
    color: #535252;
    text-decoration: none;
    font-family: "Helvetica Neue";
    font-size: clamp(10px, 2.5vw, 14px);
    font-weight: 600;

    &.router-link-exact-active {
      color: #33c3c9;
    }
  }
  a:hover {
    opacity: 0.5;
  }
}
@media only screen and (max-width: 1100px) {
  #navToggleIcon {
    display: block;
    padding: 30px 10vw;
    margin: 0;
    height: 70px;
  }
}
</style>