<template>
  <div class="dropdown-content">
    <div>
      <ul class="NavEntries">
        <NuxtLink to="/">HOME</NuxtLink>
        <NuxtLink to="#section2">ABOUT US</NuxtLink>
        <NuxtLink to="#section3">PARTNERS</NuxtLink>
        <NuxtLink to="#section4">FAQ</NuxtLink>
        <NuxtLink to="#section5">CONTACT US</NuxtLink>
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
  position: absolute;
  text-align: center;
  background-color: rgb(236, 236, 236) !important;
  width: 100%;
  height: auto;
  // box-shadow: 0px 8px 16px 0px rgba(0, 0, 0, 0.2);
  padding: 12px 16px;
  z-index: 1;
}
.NavEntries {
  padding: 60px 0;
  display: grid;
  margin: 0;
  grid-auto-flow: row;
  grid-row-gap: 60px;
  align-items: center;
  li {
    list-style-type: none;
  }
}
a {
  font-weight: bold;
  color: #535252;
  text-decoration: none;
  font-family: "Helvetica Neue";
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