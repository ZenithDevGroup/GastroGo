<template>
  <v-carousel dark :show-arrows="false" cycle hide-delimiters>
    <v-carousel-item v-for="(item, i) in items" :key="i">
      <div class="questionContainer">
        <h3>{{ item.question }}</h3>
      </div>
    </v-carousel-item>
  </v-carousel>
</template>
<script>
export default {
  data() {
    return {
      items: [
        {
          question: "What do they want?",
        },
        {
          question: "What do they need?",
        },
        { question: "Where are they from? " },
        { question: "How much do they spend?" },
      ],
    };
  },
};
</script>
<style lang="scss" scoped>
.questionContainer {
  height: 100%;
  background-size: cover;
  background-color: #fafafa;
  display: flex;

  h3 {
    font-weight: 700;
    font-family: "Helvetica Neue";
    font-size: 56px;
    margin: auto;
  }
}
img {
  width: 175px;
  height: 175px;
}
</style>