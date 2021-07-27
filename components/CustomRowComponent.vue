<template>
  <!-- <div class="customRow">
            <div class="imgContainer">
              <img
                src="~/assets/images/henry-perks-BJXAxQ1L7dI-unsplash.jpg"
                alt="Skytsunami"
              />
            </div>
            <div class="col">
              <h3>Push Notif</h3>
              <p>Some description</p>
            </div>
          </div> -->
  <v-card class="mx-auto my-12 customCard" max-width="374">
    <div class="imgContainer">
      <img src="https://cdn.vuetifyjs.com/images/cards/cooking.png" alt="" />
    </div>
    <v-card-text>
      <div class="textContainer">
        <h3
          class="headline pink--text text--accent-2 text-center"
          style="text-align: center"
        >
          Superdry
        </h3>
        Small plates, salads & sandwiches - an intimate setting with 12 indoor
        seats plus patio seating.
      </div>
    </v-card-text>
  </v-card>
</template>
<style lang="scss" scoped>
// .customRow {
//   margin-left: 20px;
//   display: grid;
//   justify-content: start;
//   text-align: left;
//   grid-template-columns: 1fr 3fr;
// }
.customCard {
  border-radius: 12px;
  .textContainer{
    padding: 20px;

    h3{
      padding: 10px 0;
    }
  }
  img {
    margin-top: 30px;
  }
}
.imgContainer {
  img {
    width: 20% !important;
    height: auto;
    border-radius: 50%;
  }
}
</style>