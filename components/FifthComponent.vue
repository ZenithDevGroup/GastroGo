<template>
  <div class="MainContainer">
    <div></div>
    <div class="content">
      <TitleComponent :title="title" :description="description" />
      <div class="teamProfile">
        <TeamProfile />
        <TeamProfile />
        <TeamProfile />
      </div>
    </div>
    <div></div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      title: "Team",
      description:
        " Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed doeiusmod tempor",
    };
  },
};
</script>
<style lang="scss" scoped>
.MainContainer {
  display: grid;
  grid-template-columns: 1fr 4fr 1fr;
  text-align: center;



  .teamProfile {
    display: grid;
    margin: 40px 0;
    width: 100%;
    justify-content: center;
    grid-template-columns: repeat(3, 1fr);
    div {
      justify-self: center;
    }
  }
}
</style>