<template>
  <div class="templateParent">
      <Header
      :section1="section1"
      :section2="section2"
      :section3="section3"
      :section4="section4"
      :section5="section5"
    />
    <div class="route">
      <Nuxt />
      
    </div>
    <div class="footer">
      <Footer
        :section1="section1"
        :section2="section2"
        :section3="section3"
        :section4="section4"
        :section5="section5"
      ></Footer>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      section1: "#section1",
      section2: "#section2",
      section3: "#section3",
      section4: "#section4",
      section5: "#section5",
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: "mdi-apps",
          title: "Welcome",
          to: "/",
        },
        {
          icon: "mdi-chart-bubble",
          title: "Inspire",
          to: "/inspire",
        },
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: "Vuetify.js",
    };
  },
};
</script>

<style lang="scss">
body {
  margin: 0;
  overflow-x: hidden;
  // display: flex;
  // flex-direction: column;
  // justify-content: space-between;

}
.spacer
{
    width: 100%;
    height: 95px;
}
</style>
