<template>
   <a href="#section5"> <v-btn large >{{ $t('contact')}}</v-btn></a>
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

   
  } a{
      text-decoration: none !important;
      color: white;
    }
</style>