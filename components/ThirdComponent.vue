<template>
  <div class="MainContainer">
    <div></div>

    <div class="content">
      <div class="title">
        <h3>Features</h3>
        <p>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed doeiusmod
          tempor incididunt ut labore et.
        </p>
      </div>

        <!-- <div class="imgContainer">
          <img src="~/assets/images/phone-logo.png" alt="" />
        </div> -->
        <div class="customCol">
          <div v-for="(item, i) in rowComponent" :key="i">
            <CustomRowComponent
              :title="item.title"
              :description="item.description"
            />
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
      rowComponent: [
        {
          title: "Send Push Notification",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed doeiusmod tempor",
        },
        {
          title: "Loyalty Programs",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed doeiusmod tempor",
        },
        {
          title: "Stamp Cards and Discount Coupons",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed doeiusmod tempor",
        },
        {
          title: "Restaurant Promotions",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed doeiusmod tempor",
        },
      ],
    };
  },
  mixins: [aosMixin],
};
</script>
<style lang="scss" scoped>
.MainContainer {
  display: flex;
  justify-content: center;
  // display: grid;
  // grid-template-columns: 1fr 4fr 1fr;
  text-align: center;
  .title {
    display: grid;
    justify-content: center;
    text-align: center;

    h3 {
      padding-bottom: 10px;
      font-size: calc((1.1 - 1) * 1.2vw + 2.5rem);
      color: rgb(202, 11, 53);
    }
    p {
      font-size: calc((1.1 - 1) * 1.2vw + 1rem);
      color: rgb(68, 68, 68);
    }
  }
  .content {
    max-width: 1270px;
    margin: auto;
    display: grid;
    grid-template-rows: auto 1fr;
    justify-content: center;
    text-align: left;
    padding: 60px 0;

    .customCol {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      justify-content: center;
      grid-gap: 60px;
      margin: 60px 0;
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

        // .imgContainer{
        //   display: none;
        // }
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