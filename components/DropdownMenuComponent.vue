<template>
  <div class="dropdown-content">
    <div>
      <ul class="NavEntries">
       <div style="width: 100%; text-align:right;padding-right: 10%;top:0">
          <v-icon dark large >mdi-close</v-icon>
       </div>
        <NuxtLink to="/">{{$t('home')}}</NuxtLink>
        <!-- <NuxtLink to="#section2">About</NuxtLink> -->
        <NuxtLink to="#section2">Features</NuxtLink>
        <NuxtLink to="#section3">{{$t('pricing')}}</NuxtLink>
        <NuxtLink to="#section5">{{$t('getintouch')}}</NuxtLink>
      </ul>
    </div>
  </div>
</template>
<style lang="scss" scoped>
.dropdown {
  position: relative;
  display: inline-block;
}

.dropdown-content {
  position: relative;
  text-align: center;
  background-color: rgb(8, 8, 8) !important;
  width: 100vw;
  height: 100vh;
  left: 0;
  top: 0;
  right: 0;
  // box-shadow: 0px 8px 16px 0px rgba(0, 0, 0, 0.2);
  padding: 12px 16px;
  z-index: 999;
}
.NavEntries {
  padding: 30px 0;
  display: grid;
  margin: 0;
  grid-auto-flow: rows;
  grid-row-gap: 60px;
  align-items: center;
  li {
    list-style-type: none;
  }

  #btn {
    button {
      width: 50%;
    }
  }
}
a {
  font-weight: bold;
  color: white;
  text-decoration: none;
  font-size: clamp(1rem, 2.5vw, 2rem);
  font-weight: 600;

  &.router-link-exact-active {
    color: #33c3c9;
  }
}
a:hover {
  opacity: 0.5;
}
</style>