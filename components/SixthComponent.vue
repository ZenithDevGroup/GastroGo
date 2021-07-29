<template>
  <div class="MainContainer">
    <div></div>
    <div class="content">
      <TitleComponent
        :title="titleContent[0].title"
        :description="titleContent[0].description"
      />
      <div class="sheetContainer">
        <div
          v-for="(item, i) in items"
          :key="i"
          data-aos="flip-left"
          data-aos-easing="ease-out-cubic"
          data-aos-duration="2000"
        >
          <img :src="require(`~/assets/partners/${item.src}.png`)" alt="" />
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
          title: "Our Amazing Partners",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed doeiusmod tempor incididunt ut labore et dolore magna aliqua.",
        },
      ],
    };
  },
  mixins: [aosMixin],
};
</script>
<style lang="scss" scoped>
.sheetContainer {
  display: grid;
  grid-template-columns: repeat(5, 1fr);
  grid-gap: 10px;
  justify-content: center;
  margin-bottom: 60px;

  div {
    justify-self: center;
  }
}
.MainContainer {
  display: grid;
  grid-template-columns: 1fr 4fr 1fr;
  justify-content: center;
  text-align: center;
  width: 100%;

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

@media only screen and (max-width: 1100px) {
  .sheetContainer {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    grid-gap: 10px;
    justify-content: center;
    margin-bottom: 60px;

    div {
      justify-self: center;
    }
  }
}
@media only screen and (max-width: 641px) {
  .sheetContainer {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-gap: 10px;
    justify-content: center;
    margin-bottom: 60px;

    div {
      justify-self: center;
    }
  }
}
</style>