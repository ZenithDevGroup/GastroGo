<template>
  <div class="IconContainer" >
    <v-icon>mdi-check</v-icon>
    <p>{{ iconDescription}}</p>
  </div>
</template>
<script>
export default {
    props:['title', 'iconDescription']
}
</script>
<style lang="scss" scoped>
  .IconContainer {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
      p {
        padding: 8px 4px;
      }
    }
</style>