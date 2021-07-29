<template>
  <div class="MainContainer">
    <!-- <Header
      :section1="section1"
      :section2="section2"
      :section3="section3"
      :section4="section4"
      :section5="section5"
    /> -->
    <div class="content">
      <FirstComponent id="section1" ref="section1" />
      <SecondComponent id="section2" ref="section2" />
      <ThirdComponent id="section3" ref="section3" />
      <FourthComponent id="section4" ref="section4" />
      <div data-aos="fade-up" id="section5" ref="section5">
        <TestimonialComponent />
      </div>
      <FifthComponent />
      <div id="contact"></div>
      <SixthComponent />
    </div>
  </div>
</template>
<script>
import aosMixin from "~/mixins/aos";
export default {
  mixins: [aosMixin],

};
</script>

<style lang="scss" scoped>
.MainContainer {
  content: "";
  background-color: #fafafa;
  margin: 0;

  
}
// #section2,#section3, #section4, #section5{
//   padding: 60px;
// }
</style>
