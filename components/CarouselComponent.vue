<template>
  <v-carousel
    
    dark
    :show-arrows="false"
    cycle
    hide-delimiters
    data-aos="fade-left"
  >
    <v-carousel-item v-for="(item, i) in items" :key="i">
      <div class="questionContainer">
        <h3>{{ item.question }}</h3>
      </div>
    </v-carousel-item>
  </v-carousel>
</template>
<script>
import aosMixin from "~/mixins/aos";

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
  mixins: [aosMixin],
};
</script>
<style lang="scss" scoped>
.questionContainer {
  height: 100%;
  width: 100%;
  max-width: 475px;
  max-height: 475px;
  background-color: #fafafa;
  display: flex;
  flex-wrap: wrap;

  h3 {
    font-weight: 700;
    font-family: "Helvetica Neue";
    font-size: clamp(1rem, 5vw, 2rem);
    margin: auto;
    padding: 0 20px;
  }
}
@media only screen and (max-width: 641px) {
  .questionContainer{
    max-height: 375px;
  }
}


</style>