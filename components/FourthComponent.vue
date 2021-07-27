<template>
  <div class="MainContainer">
    <div></div>
    <div class="content">
      <TitleComponent :title="title" :description="description" />
      <div class="carouselContainer">
        <div class="description">
          <h1>Title here</h1>
          <p>
            orem ipsum dolor sit amet, consectetur adipiscing elit, sed do
            eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim
            ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut
            aliquip ex ea commodo consequat. Duis aute irure dolor in
            reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla
            pariatur.
          </p>
        </div>
        <CarouselComponent />
      </div>
    </div>
    <div></div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      title: "Freedom and Flexibility",
      description:
        "  Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed doeiusmod tempor",
    };
  },
};
</script>
<style lang="scss" scoped>
.MainContainer {
  display: grid;
  grid-template-columns: 1fr 4fr 1fr;
  background-color: white;
  text-align: center;
  height: 100vh;

 

  .carouselContainer {
    display: grid;
    grid-template-columns: 1fr 1fr;

    .description {
      display: flex;
      flex-direction: column;
      justify-content: center;
      margin: 40px;

      p {
        padding-top: 20px;
        text-align: left;
      }
    }
  }
}
</style>