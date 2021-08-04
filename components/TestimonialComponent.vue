<template>
  <div class="MainComponent">
    <div></div>
    <div class="content">
      <div>
        <TitleComponent :title="title" :description="description" />
      </div>
      <div class="customRow">
        <CommentComponent />
        <CommentComponent />
        <CommentComponent />
      </div>

      <div class="carousel">
        <v-carousel
          light
          cycle
          :show-arrows="false"
          delimiter-icon="mdi-minus"
          height="300"
          hide-delimiter-background
       
        >
          <v-carousel-item v-for="i in 3" :key="i">
            <div class="questionContainer">
             <CommentComponent />
            </div>
          </v-carousel-item>
        </v-carousel>
      </div>
    </div>
    <div></div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      title: "What others think about us",
      description:
        " ",
    };
  },
};
</script>
<style lang="scss" scoped>
.carousel{
  display: none;
}
.MainComponent {
  height: 100%;
  display: grid;
  grid-template-columns: 1fr 4fr 1fr;

  .content {
    text-align: center;
  }

  .customRow {
    display: grid;
    grid-auto-flow: column;
    grid-gap: 20px;
    margin-bottom: 60px;
  }
}
@media only screen and(max-width:1100px) {
  .customRow {
    display: flex !important;
    flex-direction: column;
  }
}
@media only screen and (max-width:641px) {
 .customRow{
   display: none !important;
 }
 .carousel{
   margin-bottom: 30px ;
   display: block;
 }
}
</style>