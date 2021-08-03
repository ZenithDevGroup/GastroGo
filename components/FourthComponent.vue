<template>
  <div class="MainContainer">
    <div></div>
    <div class="content">
      <div class="carouselContainer">
        <div class="description" data-aos="fade-right">
          <TitleComponent :title="title" :description="description" />
          <!-- <h1>Title here</h1>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
            eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim
            ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut
            aliquip ex ea commodo consequat. Duis aute irure dolor in
            reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla
            pariatur.
          </p> -->
        </div>
        <CarouselComponent />
      </div>
    </div>
  </div>
</template>
<script>
import aosMixin from "~/mixins/aos";

export default {
  data() {
    return {
      title: "Freedom and Flexibility",
      description:
        "  Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.",
    };
  },
  mixins: [aosMixin],
};
</script>
<style lang="scss" scoped>
.MainContainer {
  display: grid;
  grid-template-columns: 1fr 4fr 1fr;
  background-color: white;
  text-align: center;
  height: 100%;

  .carouselContainer {
    padding: 60px 0;
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-gap: 100px;
    .description {
      display: flex;
      flex-direction: column;
      justify-content: center;

      p,
      h1 {
        padding-top: 20px;
        text-align: left;
      }
    }
  }
}

@media only screen and (max-width: 1360px) {
  .carouselContainer {
    display: flex !important;
    flex-direction: column;

    .description {
      padding-top: 0;
      order: 2;
    }
  }
}
</style>