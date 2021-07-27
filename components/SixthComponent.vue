<template>
  <div class="MainContainer">
    <div></div>
    <div class="content">
      <TitleComponent :title="titleContent[0].title" :description="titleContent[0].description"/>
      <div class="sheetContainer">
        <div v-for="(item, i) in items" :key="i">
          <img :src="require(`~/assets/partners/${item.src}.png`)" alt="" />
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      items: [
        {
          src: "billiejean",
        },
        {
          src: "cityrock-logo",
        },
        // {
        //   src: "factory-lodge-logo.jpg",
        // },
        {
          src: "gonzalez-nakskov",
        },
        {
          src: "gronneverden",
        },
        {
          src: "hoffman_logo",
        },
        {
          src: "logo-liva",
        },
        {
          src: "mindbjergs",
        },
        {
          src: "olsens",
        },

        {
          src: "Pitstop-logo",
        },
        {
          src: "surt_og_soedt",
        },
        {
          src: "tempus",
        },
        {
          src: "yaki_marienlyst",
        },
        {
          src: "yaki_nykoebingF",
        },
        {
          src: "zangenberg",
        },
      ],
      titleContent: [
        {
          title: "Samarbejdspartnere",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed doeiusmod tempor incididunt ut labore et dolore magna aliqua.",
        },
      ],
    };
  },
};
</script>
<style lang="scss" scoped>
.sheetContainer {
  display: grid;
  grid-template-columns: repeat(5, 1fr);
  grid-gap: 10px;
  justify-content: center;

  div {
    justify-self: center;
  }
}
.MainContainer {
  display: grid;
  background-color: white;
  grid-template-columns: 1fr 4fr 1fr;
  justify-content: center;
  text-align: center;
  width: 100%;
  margin: 40px 0;
  height: 560px;

  .title {
    padding-top: 60px;
    padding-bottom: 80px;

    h2 {
      padding-bottom: 10px;
    }
    p {
      font-size: 12px;
      color: grey;
    }
  }

  img {
    width: 100px;
    height: auto;
  }
}
</style>