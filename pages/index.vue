<template>
  <div class="MainContainer">
    <div class="content">
     
      <FirstComponent id="section1" ref="section1" />
     <ThirdComponent id="section2" ref="section2" />
      <FourthComponent />
      <SecondComponent />
      <div >
        <TestimonialComponent />
      </div>
      <PricingComponent id="section3" ref="section3"/>
      <GetInTouchComponent id="section5" ref="contactus"/> 
     
      <!-- <SixthComponent />-->
    </div>
  </div>
</template>
<script>
import aosMixin from "~/mixins/aos";
export default {
  mixins: [aosMixin],
};
</script>

<style lang="scss" >
@media not all and (min-resolution: 0.001dpcm) {
  @supports (-webkit-appearance: none) {
    html{
      scroll-behavior: smooth;
      animation: all 7s infinite;
    }
  }}

html{
  scroll-behavior: smooth;
  animation: all 7s infinite;
}
.MainContainer {
  scroll-behavior: smooth !important;
  content: "";
  background-color: white;
  margin: 0;
  overflow-wrap: break-word;
  font-family: "Josefin Sans" !important;

 

}
</style>
