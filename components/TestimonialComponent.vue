<template>
  <div class="MainComponent">
    <div class="content">
      <div>
        <TitleComponent :title="$t('think')" />
      </div>
      <carousel perPage="1" :autoplay="true" :loop="true">
        <slide v-for="(item, i) in $t('comments')" :key="i">
          <div class="slideContainer" >
            <CommentComponent :comment="item" :name="owners.name" :src="owners[i].src" />
          </div>
        </slide>
      </carousel>
    </div>
  </div>
</template>
<script>
import { Carousel, Slide } from "vue-carousel";
export default {
  components: {
    Carousel,
    Slide,
  },
  data() {
    return {
      owners: [
        {
          name: "Mads Damgaard",
          src: "mads",
        },
        {
          name: "Johnny Andersen",
          src: "johnny2",
        },
        {
          name: "Alexander Olesen",
          src: "lateP",
        },
        {
          name: "David Blom",
          src: "david2",
        },
      ],
      // owners: [
      //   {
      //     name: "Mads Damgaard",
      //     position: "Restaurant owner at Pitstop",
      //     src: "mads",
      //   },
      //   {
      //     name: "Johnny Andersen",
      //     position: "Restaurant owner at Café Banegården",
      //     src: "johnny2",
      //   },
      //   {
      //     name: "Alexander Olesen",
      //     position: "Restaurant owner at Olesen’s Smørrebrød",
      //     src: "lateP",
      //   },
      //   {
      //     name: "David Blom",
      //     position: "Restaurant owner at Restaurant Passebækgård",
      //     src: "david2",
      //   },
      // ],
    };
  },
};
</script>
<style lang="scss" scoped>
.MainComponent {
  overflow: hidden !important;
  display: flex;
  justify-content: center;
  .content {
    text-align: center;
    width: 80%;
  }
}
</style>