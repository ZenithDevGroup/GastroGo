<template>
  <div class="MainContainer">
    <div class="content">
      <div class="title">
        <h3>{{ $t("everything") }}</h3>
        <p>{{ $t("partner-love") }}</p>
      </div>
      <div class="customCol">
        <div v-for="(item, i) in $t('rowComponent')" :key="i">
          <CustomRowComponent
            :title="item.title"
            :description="item.description"
            :imageUrl="images[i].src"
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
      images: [
        { 
          src: "order"
        },
        { 
          src: "chain"
        },
        { 
          src: "payment-terminal"
        },
        { 
          src: "booking"
        },
        { 
          src: "delivery-box"
        },
        { 
          src: "accounting"
        }
      ]
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