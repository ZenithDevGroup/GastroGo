<template>
  <div class="MainContainer">
    <v-icon>{{ icon }}</v-icon>
    <p>{{ iconDescription}}</p>
  </div>
</template>
<script>
export default {
    props:['title', 'iconDescription']
}
</script>
<style lang="scss" scoped>
  div {
      display: flex;
      justify-content: center;

      p {
        padding: 8px 4px;
      }
    }
</style>