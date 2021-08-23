<template>
  <div class="MainContainer">
    <div class="content">
      <div class="title">
        <h3> Everything you need</h3>
        <p>
         Our partners love us due to all our features included in one system.
        </p>
      </div>
      <div class="customCol">
        <div v-for="(item, i) in rowComponent" :key="i">
          <CustomRowComponent
            :title="item.title"
            :description="item.description"
            :imageUrl="item.src"
          />
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
      title: "Features",
      description:
        "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed doeiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enimad minim veniam, quis nostrud exercitation ullamco laboris nisi utaliquip ex ea commodo consequat.",
      rowComponent: [
        {
          title: "Online Ordering",
          description:
            "Let your customers order from your restaurant directly from their smartphone.",
          src: "order",
        },
        {
          title: "Free Flexibility",
          description:
            "Change your menu daliy and much more without any extra cost.",
          src: "chain",
        },
        {
          title: "POS",
          description:
            "We offer a smart POS system where you can easily change and add items in the system. ",
          src: "payment-terminal",
        },
        {
          title: "Table Booking",
          description:
            "Let your customers book at table from your restaurant directly from their smartphone.",
          src: "booking",
        },
        {
          title: "Companion app",
          description: "Accept orders directly on your smartphone.",
          src: "delivery-box",
        },
        {
          title: "Accounting overview",
          description:
            "Download your data directly from the app",
          src: "accounting",
        },
      ],
    };
  },
  mixins: [aosMixin],
};
</script>
<style lang="scss" scoped>
.MainContainer {
  scroll-behavior: smooth;
  display: flex;
  justify-content: center;
  .title {
    display: grid;
    justify-content: center;
    text-align: center;

    h3 {
      position: relative;
      max-width: 30ch;
      padding-bottom: 10px;
      font-size: calc((1.1 - 1) * 1.2vw + 2.5rem);
      color: rgb(202, 11, 53);
    }
    p {
         position: relative;
      font-size: calc((1.1 - 1) * 1.2vw + 1rem);
      color: rgb(68, 68, 68);
    }
  }
  .content {
    width: 80%;
    height: 100%;
    display: grid;
    grid-template-rows: auto 1fr;
    justify-content: center;
    text-align: left;
    padding: 60px 0;
    margin-top: 60px;

    .customCol {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      justify-content: center;
      grid-gap: 60px;
      margin: 60px 0;
      div {
        justify-self: center;
      }
    }
  }
}

// @media only screen and (max-width: 1366px) {
//   .MainContainer {
//     .content {
//       display: flex !important;
//       flex-direction: column;

//       .title {
//         justify-content: center !important;
//         text-align: center !important;
//         padding-bottom: 20px;
//       }
//       .customCol {
//         padding-top: 20px;
//         display: grid;
//         grid-template-columns: repeat(2, 1fr);
//         justify-content: flex-start;
//         text-align: left;
//         div {
//           justify-self: flex-start;
//         }
//       }
//     }
//   }
// }
@media only screen and (max-width: 1100px) {
  .MainContainer {
    grid-template-columns: auto 1fr auto;
    .content {
      display: flex !important;
      flex-direction: column;

      .title {
        justify-content: center !important;
        text-align: center !important;
        padding-bottom: 20px;
      }
      .customCol {
        padding-top: 20px;
        display: flex;
        flex-direction: column;
        text-align: left;

        div {
          display: flex;
          justify-content: flex-start;
        }
      }
    }
  }
}
</style>