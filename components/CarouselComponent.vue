<template>
  <carousel :perPage="1" :autoplay="true" :loop=true>
  <slide v-for="(item, i) in items" :key="i">
    <div class="slideContainer">
        <img :src="require(`~/assets/images/${item.src}.png`)" alt="" />
      </div> 
  </slide>

</carousel>
</template>
<script>
import aosMixin from "~/mixins/aos";
import { Carousel, Slide } from 'vue-carousel';
export default {
    components: {
    Carousel,
    Slide
  },
  data() {
    return {
      items: [
        {
          src: "islide4",
        },
        {
          src: "islide5",
        },
        { src: "islide6" },
      ],
    };
  },
  mixins: [aosMixin],
};
</script>
<style lang="scss" scoped>

.slideContainer {
  overflow: hidden;
  display: flex;
  justify-content: center;
  img {
    // padding: 60px 0;
    width: 100%;
    height: 100%;
  }

}

@media only screen and (max-width: 991px){
  img {
    // padding: 60px 0;
    max-width: 500px;
    width: 100%;
    height: 100%;
  }
  
}
</style>