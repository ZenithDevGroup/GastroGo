<template>
    <div class="title">
        <h3>{{ title }}</h3>
        <p>{{ description }}</p>
      </div>
</template>
<script>
export default {
  props:[ 'title', 'description']
}
</script>
<style lang="scss"scoped>
  .title{
   display: grid;
   justify-content: center;
          padding-top: 60px;
          padding-bottom: 80px;
          text-align: center;
      
      h3{
        padding-bottom: 10px;

      }
      p{
        text-align: center;
        font-size: 14px;
        color: grey;
        max-width: 560px;
        word-wrap:break-word;
      }
      }
</style>