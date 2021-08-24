<template>
  <div class="MainContainer">
    <div></div>
    <div class="content">
      <div class="description">
        <h1>Freedom and Flexibility</h1>
        <p>
          With our Android app, you can easily manage your restaurants presence
          on the user-focused GastroGo application. In this app, you can change
          the opening hours of your restaurant, manage your menu and your
          pricing, hide menu items for sold out dishes, control what images the
          users sees, and much more.
        </p>
      </div>
      <div class="carousel">
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
  
  display: flex;
  overflow: hidden !important;
  justify-content: center;
  align-content: center;
  // height: 100vh;
  .content {
    width: 80%;
    display: grid;
    justify-content: space-around;
    grid-template-columns: 1fr 1fr;
    // grid-gap: 60px;

    .description {
      text-align: left;
      display: flex;
      flex-direction: column;
      justify-content: center;
      order: 1;
      h1 {
        padding-bottom: 30px;
        font-size: calc((1.1 - 1) * 1.2vw + 2.5rem);
        color: rgb(202, 11, 53) !important;
      }
      p {
        line-height: 1.3;
        font-size: calc((1.1 - 1) * 1.2vw + 1rem);
        color: grey;
        word-wrap: break-word;
        max-width: 50ch;
      }
    }
    .carousel {
      order: 2;
      display: flex;
      align-items: center;
      margin-bottom: 60px;
      div {
        width: 100%;
      }
    }
  }
}

@media only screen and (max-width: 1000px) {
  .MainContainer {
    // height: 100vh !important;
    display: flex !important;
    justify-content: center;

  }
  .content {
    justify-content: center;
    align-items: center;
    display: flex !important;
    flex-direction: column !important;
    padding: 60px 0;



    .description {
      padding-bottom: 30px;
      order: 2;
      text-align: center !important;

          p {
        line-height: 1.5;
        font-size: calc((1.1 - 1) * 1.5vw + 1.2rem) !important;
        color: grey;
        word-wrap: break-word;
        max-width: 50ch;
      }
    }
  }
}
</style>