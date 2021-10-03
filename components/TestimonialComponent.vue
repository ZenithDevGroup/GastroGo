<template>
  <div class="MainComponent">
    <div class="content">
      <div>
        <TitleComponent :title="$t('think')" />
      </div>
      <carousel :perPage=1 :autoplay="true" :loop="true">
        <slide v-for="(item, i) of $t('comments')" :key="i">
          <div class="slideContainer">
            <CommentComponent
              :comment="item"
              :name="getOwnerName(i)"
              :imageUrl="require(`@/assets/images/${getOwnerImage(i)}`)"
            />
          </div>
        </slide>
      </carousel>
      <!-- <div v-for="(dataItem, b) of owners" :key="b">
        {{ getOwnerName(b) }}
        {{ getOwnerImage(b) }}
        <CommentComponent
          :comment="dataItem"
          :name="owners[b].name"
          :imageUrl="owners[b].src"
        />
      </div> -->
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
  data: () => {
    var owners = {
      "Mads Damgaard": {
        src: "mads.png",
      },
      "Johnny Andersen": {
        src: "johnny2.png",
      },
      "Alexander Olesen": {
        src: "lateP.png",
      },
      "David Blom": {
        src: "david2.png",
      },
    };
    var data = {
      owners,
      getOwnerName:(v)=>{
        //the key is the owners name so return v;
        return v;
      },
      getOwnerPosition: (v) => {
        return owners[v]?.position;
      },
      getOwnerImage: (v) => {
        return owners[v]?.src;
      },
    };
    return data;
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