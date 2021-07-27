<template>
  <div class="MainContainer">
    <div></div>
    <div class="content">
      <TitleComponent :title="title" :description="description" />
      <!-- 
      <div class="customRow">
        <div>
          <h3>What You Get With Your Content Marketing Startups</h3>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
            eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim
            ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut
            aliquip ex ea commodo consequat.
          </p>
        </div>
        <div>
          <v-btn>GET STARTED</v-btn> 
        </div>
      </div> -->
      <div class="feature">
        <div class="customCol">
          <div v-for="i in 3" :key="i">
            <CustomRowComponent />
          </div>
        </div>
      </div>
    </div>
    <div></div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      title: "Features",
      description:
        "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed doeiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enimad minim veniam, quis nostrud exercitation ullamco laboris nisi utaliquip ex ea commodo consequat.",
    };
  },
};
</script>
<style lang="scss" scoped>
.MainContainer {
  display: grid;
  grid-template-columns: 1fr 4fr 1fr;
  .content {
    display: grid;
    grid-template-rows: auto 1fr;
    justify-content: center;
    text-align: center;

    .customRow {
      margin-top: 60px;
      display: grid;
      grid-template-columns: 1fr 1fr;
      justify-content: space-between;

      div {
        text-align: left;
        justify-self: center;
        p {
          padding-top: 20px;
          color: grey;
          font-size: 12px;
        }
      }
    }

    .feature {
      display: grid;

      flex-direction: rows;
      gap: 100px;
      padding: 60px 0;
      justify-content: space-between;

      .imgContainer {
        display: flex;
        justify-content: center;
        text-align: center;
        background-size: cover;
        background-image: url("~/assets/images/henry-perks-BJXAxQ1L7dI-unsplash.jpg");
      }

      .customCol {
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        grid-gap: 10px;
        justify-content: space-between;

        div{
          justify-self: center;
        }
      }
    }
  }
  .title {
    padding-top: 60px;
  }
}
</style>