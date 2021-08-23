<template>
  <div class="title">
    <h3>{{ title }}</h3>
    <p>{{ description }}</p>
  </div>
</template>
<script>
export default {
  props: ["title", "description"],
};
</script>
<style lang="scss"scoped>
.title {
  display: grid;
  justify-content: center;
  padding-top: 60px;
  padding-bottom: 80px;

  h3 {
    padding-bottom: 10px;
    font-size:  calc((1.1 - 1) * 1.2vw + 2.5rem);
    color: rgb(202, 11, 53);
  }
  p {
    text-align: center;
    font-size:  calc((1.1 - 1) * 1.2vw + 1rem);
    color: grey;
    max-width: 560px;
    word-wrap: break-word;
  }
}
</style>