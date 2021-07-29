<template>
  <div class="MainContainer">
    <div></div>

    <div class="content" data-aos="fade-right">
      <div class="title">
        <h3>Features</h3>
        <p>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed doeiusmod
          tempor incididunt ut labore et.
        </p>
      </div>

      <div class="customCol">
        <div v-for="i in 3" :key="i">
          <CustomRowComponent />
        </div>
      </div>
    </div>
    <div></div>
  </div>
</template>
<script>
import aosMixin from "~/mixins/aos";
export default {
  data() {
    return {
      title: "Features",
      description:
        "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed doeiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enimad minim veniam, quis nostrud exercitation ullamco laboris nisi utaliquip ex ea commodo consequat.",
    };
  },
  mixins: [aosMixin],
};
</script>
<style lang="scss" scoped>
.MainContainer {
  display: grid;
  grid-template-columns: 1fr 4fr 1fr;
  .title {
    display: grid;
    justify-content: start;
    text-align: left;

    h3 {
      padding-bottom: 10px;
      color: rgb(202, 11, 53);
    }
    p {
      font-size: clamp(1rem, 5vw, 2rem);
      color: rgb(68, 68, 68);
      max-width: 500px;
      word-wrap: break-word;
    }
  }
  .content {
    display: grid;
    grid-template-columns: auto 1fr;
    justify-content: center;
    text-align: left;
    padding: 60px 0;

    .imgContainer {
      display: flex;
      justify-content: center;
      text-align: center;
      background-size: cover;
      background-image: url("~/assets/images/henry-perks-BJXAxQ1L7dI-unsplash.jpg");
    }

    .customCol {
      
      display: flex;
      flex-direction: row;
      justify-content: center;
      row-gap: 60px;

      div {
        justify-self: center;
      }
    }
  }
}

@media only screen and (max-width: 1366px) {
  .MainContainer {
    .content {
      display: flex !important;
      flex-direction: column;

      .title {
        // padding-top: ;
        justify-content: center !important;
        text-align: center !important;
        padding-bottom: 20px;

        // p {
        //   max-width: 100% !important;
        // }
      }
      .customCol {
        padding-top: 20px;
        display: grid;
        grid-template-columns: repeat(2, 1fr);
        justify-content: flex-start;
        text-align: left;
        div {
          justify-self: flex-start;
        }
      }
    }
  }
}
@media only screen and (max-width: 1100px) {
    .MainContainer {
    .content {
      display: flex !important;
      flex-direction: column;

      .title {
        // padding-top: ;
        justify-content: center !important;
        text-align: center !important;
        padding-bottom: 20px;

        // p {
        //   max-width: 100% !important;
        // }
      }
      .customCol {
        padding-top: 20px;
        display: flex;
        flex-direction: column;
        justify-content: flex-start;
        text-align: left;
        div {
          justify-self: flex-start;
        }
      }
    }
  }
}
</style>