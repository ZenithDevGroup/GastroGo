<template>
  <div :class="{ change_color: scrollPosition > 50 }" id="container-header">
    <div class="innerContainer">
      <div class="logoContainer">
        <NuxtLink to="/"
          ><img src="~/assets/images/logo.svg" alt="" />
          <p>GastroGo</p></NuxtLink
        >
      </div>
      <div>
        <ul class="NavEntries">
          <NuxtLink to="/">{{$t('home')}}</NuxtLink>
          <NuxtLink v-bind:to="section2" v-on:click.native="isActiveFunc"
            >Features
          </NuxtLink>
          <NuxtLink v-bind:to="section3" >{{$t('pricing')}}</NuxtLink>
        </ul>
      </div>
      <div class="buttonContainer">  
        <ButtonComponent id="btn" />
        <LocaleSwitcher />
        <!-- <div class="v2dropdown">
          <v-icon class="dropicon">mdi-google-earth</v-icon>
          <div class="v2dropdown-content">
            <a @click="selectLang('en')">English</a>
            <a @click="selectLang('dk')">Dansk</a>
          </div>
        </div> -->
      
        <div id="navToggleIcon">
          <v-icon
            v-if="!toggleNav && isDark == 'white'"
            @click="toggleMenu()"
            dark
            large
            >mdi-menu</v-icon
          >
          <v-icon
            v-if="!toggleNav && isDark == 'black'"
            @click="toggleMenu()"
            light
            large
            >mdi-menu</v-icon
          >
          <v-icon
            v-if="toggleNav && isDark == 'black'"
            @click="toggleMenu()"
            dark
            >mdi-close</v-icon
          >
          <v-icon
            v-if="toggleNav && isDark == 'white'"
            @click="toggleMenu()"
            light
            >mdi-close</v-icon
          >
        </div>
      </div>
    </div>
    <div id="dropdown-menu" v-if="toggleNav">
      <DropdownMenuComponent @click.native="toggleMenu()" />
    </div>
  </div>
</template>
<script>
import CountryFlag from "vue-country-flag";
export default {
  components: {
    CountryFlag,
  },
  props: ["section1", "section2", "section3", "section4", "section5"],
  data: function () {
    return {
      toggleNav: false,
      scrollPosition: null,
      isActive: false,
      isDark: null,
    };
  },
  beforeMount() {
    window.addEventListener("scroll", this.handleScroll);
  },
  methods: {
    selectLang(lang){
      if(lang == 'en'){
        return en;
      }
      return dk;
    },

    toggleMenu() {
      this.toggleNav = !this.toggleNav;
    },

    isActiveFunc() {
      this.isActive = !this.isActive;
    },
    handleScroll() {
      this.scrollPosition = window.scrollY;
      if (this.scrollPosition >= 50) {
        this.isDark = "white";
      } else this.isDark = "black";
    },
  },
  mounted() {
    window.addEventListener("scroll", this.handleScroll);
  },
};
</script>
<style lang="scss" scoped>
#dropdown-menu {
  position: absolute;
  top: 0;
}
.v2dropdown {
  position: relative;
  display: inline-block;
}
.v2dropdown:hover {
  cursor: pointer;
}

.v2dropdown-content {
  border-radius: 10px;
  display: none;
  position: absolute;
  background-color: #f1f1f1;
  min-width: 160px;
  box-shadow: 0px 8px 16px 0px rgba(0, 0, 0, 0.2);
  z-index: 1;
}

.v2dropdown-content a {
  color: black;
  border-radius: 10px;
  padding: 12px 16px;
  text-decoration: none;
  display: block;
}

// .v2dropdown-content a:hover {background-color: #ddd;}

.v2dropdown:hover .v2dropdown-content {
  display: block;
}
@keyframes smoothScroll {
  0% {
    transform: translateY(-40px);
  }
  100% {
    transform: translateY(0px);
  }
}

.buttonContainer {
  display: flex;
  flex-direction: row;
  align-items: center;
  gap: 10px;
  justify-content: space-around;
}

#navToggleIcon {
  display: none;
}
.change_color {
  position: fixed !important;
  top: 0 !important;
  left: 0;
  animation: smoothScroll 1s forwards;
  background-color: rgb(26, 25, 25) !important;
  box-shadow: 0 1px 2px rgba(102, 102, 102, 0.19), 0 2px 2px rgba(0, 0, 0, 0.23);
  z-index: 1000;
  p {
    color: white !important;
  }

  .v-icon {
    color: white;
  }

  .NavEntries > span {
    color: white !important;
  }
  .NavEntries > a {
    color: white !important;
  }
}
#container-header {
  width: 100%;
  -webkit-transition: position 10s;
  -moz-transition: position 10s;
  -ms-transition: position 10s;
  -o-transition: position 10s;
  transition: position 10s;

  font-family: "Josefin Sans";
  background-color: transparent;
  position: fixed;
  z-index: 9;
  margin: 0;
  right: 0;
  left: 0;
  top: 0;
  display: flex;
  justify-content: center;
  // box-shadow: 0 1px 2px rgba(102, 102, 102, 0.19), 0 2px 2px rgba(0, 0, 0, 0.23);
  width: 100%;
  .innerContainer {
    // padding: 8px 6vw;
    width: 85%;
    display: flex;
    align-content: center;
    flex-direction: row;
    justify-content: space-between;
  }
  .logoContainer {
    display: flex;
    flex-direction: column;
    justify-content: center;
    // font-size: 22px;
    text-align: center;
    height: 100%;
    span {
      vertical-align: middle;
    }
    img {
      vertical-align: middle;
      width: 40px;
      height: 40px;
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
    // padding: 15px 0;
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
    // font-size: clamp(10px, 2.5vw, 14px);
    font-weight: 600;

    &.router-link-exact-active {
      color: #33c3c9;
    }
  }
  a:hover {
    opacity: 0.5;
  }
  a:active {
    font-weight: bold !important;
    color: blanchedalmond;
  }
}
@media only screen and (max-width: 1100px) {
  .logoContainer {
    span {
      display: none !important;
    }
  }
  #btn {
    display: none;
  }
  #dropdown-menu {
    overflow: hidden !important;
  }
  #navToggleIcon {
    display: inline-block;
    padding: 30px 20px;
    margin: 0;
  }
}
</style>