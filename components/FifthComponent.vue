<template>
  <div class="MainContainer">
    <div></div>
    <div class="content">
      <TitleComponent
        :title="titleContent[0].title"
        :description="titleContent[0].description"
      />

    
      <div class="teamProfile" v-for="(item, i) in teamInfo" :key="i">  
        <hr>
        <TeamProfile
          :name="item.name"
          :description="item.description"
          :position="item.position"
          :isLeft="item.isLeft"
          :src="require(`~/assets/images/${item.src}.jpg`)"
        />
      </div>
    </div>
    <div></div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      titleContent: [
        {
          title: "The Team",
          description:
            " Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed doeiusmod tempor",
        },
      ],
      teamInfo: [
        {
          name: "Johann Notail",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmodtempor incididunt ut labore et dolore magna aliqua.Ut enim ad minimveniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex eacommodo consequat. Duis aute irure dolor in reprehenderit in voluptatevelit esse cillum dolore eu fugiat nulla pariatur.",
          isLeft: false,
          position: "CEO",
          src: "austin-wade-X6Uj51n5CE8-unsplash",
        },
        {
          name: "Ana Notail",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmodtempor incididunt ut labore et dolore magna aliqua.Ut enim ad minimveniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex eacommodo consequat. Duis aute irure dolor in reprehenderit in voluptatevelit esse cillum dolore eu fugiat nulla pariatur.",
          isLeft: true,
          position: "CEO",
          src: "austin-wade-X6Uj51n5CE8-unsplash",
        },
        {
          name: "Ceb Notail",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmodtempor incididunt ut labore et dolore magna aliqua.Ut enim ad minimveniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex eacommodo consequat. Duis aute irure dolor in reprehenderit in voluptatevelit esse cillum dolore eu fugiat nulla pariatur.",
          isLeft: false,
          position: "CEO",
          src: "austin-wade-X6Uj51n5CE8-unsplash",
        },
      ],
    };
  },
};
</script>
<style lang="scss" scoped>
.MainContainer {
  display: grid;
  grid-template-columns: 1fr 4fr 1fr;
  text-align: center;
  background-color: white;

  .teamProfile {
    display: grid;
    grid-gap: 40px;
    margin-bottom: 60px;
    justify-content: center;
    div {
      justify-self: center;
    }

    hr{
      border: 1px solid #FAFAFA;
    }
  }
}


</style>