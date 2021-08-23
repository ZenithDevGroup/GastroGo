<template>
    <v-btn large ><a href="#section5">GET IN TOUCH</a></v-btn>
</template>
<script>
export default {
  props:['section5']
}
</script>
<style lang="scss"scoped>
  .v-btn{
    background-color: rgb(211, 23, 79) !important;
    color: white !important;
    letter-spacing: 2px;
    border-radius: 30px;
    margin: 20px 0; 

    a{
      text-decoration: none;
      color: white;
    }
  }
</style>