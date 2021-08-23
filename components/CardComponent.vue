<template>
  <div class="MainContainer">
    <v-card :loading="loading" class="mainCard customCol" elevation="0">
      <template slot="progress">
        <v-progress-linear
          color="deep-purple"
          height="10"
          indeterminate
        ></v-progress-linear>
      </template>
      <div class="title">
        <h3>{{ title }}</h3>
        <p>{{ titleDescription }}</p>
      </div>
      <div class="priceCard">
        <h1 v-if="!isFree">{{ price }}</h1>
        <h1 v-if="isFree">FREE</h1>
        <p style="font-size: 10px" v-if="!isFree">
          /month <span v-if="!isFree">/restaurant</span>
        </p>
      </div>
      <v-divider class="mx-4"></v-divider>
      <div class="iconContainer">
        <IconComponent
          v-for="(item, i) in priceDescription"
          v-bind:key="i"
          :iconDescription="item"
          :num="num"
        />
      </div>
      <v-btn x-large elevation="0" text
        ><a href="#section5">GET IN TOUCH</a></v-btn
      >
    </v-card>
  </div>
</template>
<script>
export default {
  props: ["title", "titleDescription", "price", "priceDescription", "isFree"],
};
</script>
<style lang="scss" scoped>
.customCol {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}
.customRow {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}
button {
  background-color: white !important;
}
.MainContainer {
  width: 100%;
  height: auto;
  .v-btn {
    border-radius: 0 0 30px 30px;
    a {
      text-decoration: none;
      color: black;
    }
  }

  .v-btn:hover {
    background-color: black !important;

     a {
      text-decoration: none;
      color: white !important;
    }
  }
  .title {
    h3 {
      padding: 20px 0;
    }
    padding: 30px 0;
  }

  .priceCard {
    margin: 20px 10px;
    padding: 20px 0;
    h1 {
      padding: 20px 0;
    }

    background-color: transparent !important;
    //  background-color: rgba(255,255,255,0.5);
    display: flex !important;
    justify-content: center;
    flex-direction: column;
    height: 30% !important;
  }
  .mainCard {
    border-radius: 30px;
    // padding: 20px;
    background-position: top;
    background-size: cover;
    background-image: url("~/assets/images/pricingbg.png");
    width: 100%;
    height: 100%;
    max-width: 435px !important;
  }
  .iconContainer {
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    align-content: center;
    flex-direction: column;
    padding: 30px;
    div {
      display: flex;
      justify-content: center;

      p {
        padding: 8px 4px;
      }
    }
  }
}
.mainSmallScreenCard {
  display: none;
}
</style>