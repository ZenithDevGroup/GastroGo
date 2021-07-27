<template>
  <div class="HeaderContainer">
    <div class="innerContainer">
      <div class="logoContainer">
        <NuxtLink to="/"><span>GastroGo</span></NuxtLink>
      </div>
      <ul class="NavEntries">
        <NuxtLink to="/">HOME</NuxtLink>
        <NuxtLink to="/">ABOUT US</NuxtLink>
        <NuxtLink to="/">PARTNERS</NuxtLink>
        <NuxtLink to="/">FAQ</NuxtLink>
        <NuxtLink to="/">CONTACT US</NuxtLink>
      </ul>
      <!-- <div id="navToggleIcon">
          <font-awesome-icon
            :icon="['fas', 'bars']"
            class="icon"
            size="lg"
            @click="toggleMenu()"
          />
        </div> -->
    </div>
  </div>
</template>
<style lang="scss" scoped>
.HeaderContainer {
  .innerContainer {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    
  }
  .logoContainer{
  
    justify-content: center;
    padding:30px 100px;
    img{
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
    padding: 0 100px ;
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
</style>