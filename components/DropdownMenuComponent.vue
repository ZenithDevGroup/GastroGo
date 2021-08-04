<template>
  <div class="dropdown-content">
    <div>
      <ul class="NavEntries">
        <NuxtLink to="/">Home</NuxtLink>
        <NuxtLink to="#section2">About</NuxtLink>
        <NuxtLink to="#section3">Features</NuxtLink>
         <NuxtLink to="#section3">Partners</NuxtLink>
        <NuxtLink to="#section4">Pricing</NuxtLink>
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
  background-color: rgb(8, 8, 8) !important;
  width: 100%;
  height: auto;
  left: 0;
  right: 0;
  // box-shadow: 0px 8px 16px 0px rgba(0, 0, 0, 0.2);
  padding: 12px 16px;
  z-index: 999;
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