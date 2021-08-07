<template>
  <div class="MainContainer">
    <div></div>
    <div class="content">
      <div class="carouselContainer">
        <div class="description" data-aos="fade-right">
          <!-- <TitleComponent :title="title" :description="description" /> -->

          <h1>Freedom and Flexibility</h1>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
            eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim
            ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut
            aliquip ex ea commodo consequat. Duis aute irure dolor in
            reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla
            pariatur.
          </p>
        </div>
        <div class="carousel">
          <CarouselComponent />
        </div>
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
  display: flex;
  justify-content: center;
  height: 100%;
  .content {
    width: 80%;
    
    display: flex;
    text-align: center;
    justify-content: center;
    align-content: center;
    padding: 60px 0;
    .carouselContainer {
      display: grid;
      grid-template-columns: 1fr 1fr;
      grid-gap: 100px;
      .carousel {
        order: 2;
      }

      .description {
        text-align: left;
        display: flex;
        flex-direction: column;
        justify-content: center; 
        order: 1;
        h1 {
          padding-bottom: 10px;
          font-size: calc((1.1 - 1) * 1.2vw + 2.5rem);
          color: rgb(202, 11, 53) !important;
        }
        p {
          font-size: calc((1.1 - 1) * 1.2vw + 1rem);
          color: grey;
          word-wrap: break-word;
        }
      }
    }
  }
}

@media only screen and (max-width: 1100px) {
  .MainContainer {
    grid-template-columns: auto 1fr auto;
  }
  .carouselContainer {
    display: flex !important;
    flex-direction: column;

    .description {
      padding-top: 0;
      order: 2;
      text-align: center !important;
    }
  }
}
</style>