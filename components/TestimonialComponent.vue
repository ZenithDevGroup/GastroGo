<template>
  <div class="MainComponent">
    <div class="content">
      <div>
        <TitleComponent :title="title" :description="description" />
      </div>
      <carousel perPage="1" autoplay="true" loop="true">
        <slide v-for="(item, i) in comments" :key="i">
          <div class="slideContainer">
            <CommentComponent
              :comment="item.comment"
              :name="item.name"
              :position="item.position"
              :src="require(`~/assets/images/${item.src}.png`)"
            />
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
      title: "What others think about us",
      description: " ",

      comments: [
        {
          comment:
            "For a restaurant like ours, GastroGo makes digital sales possible for a business like mine. Our produce expenses are simply too high to be profitable with the commissions that the other platforms charge. When the heat is on and the restaurant is full, a phonecall can tip the balance between a good service and a bad one. GastroGo is our digital secretary and allows us to stay open for take-away business, even with a full restaurant.",
          name: "Mads Damgaard",
          position: "Restaurant owner at Pitstop",
          src: "mads",
        },
        {
          comment:
            "When we had to choose between takeaway or no service at all, I started to look for good fits between the solutions and my restaurant, but I quickly discovered that the solutions were expensive and inflexible in general. That is why I am now using GastroGo. I really liked the principle of it being free while granting me the full control of my own menus and opening hours, etc. And GastroGo isn't just \"FREE\", if you buy 23 other products first and otherwise being super expensive like I've seen with some other similar product. It makes a lot of sense to me.",
          name: "Johnny Andersen",
          position: "Restaurant owner at Café Banegården",
          src: "johnny2",
        },
        {
          comment:
            "First, the vision of GastroGo is really sound. It's a way for us to become more effective in our business. We’re using so much time every day answering the phone and writing things down by hand, and my customers can see that it's stressful with the phone constantly calling. We sell a lot of food and this technology allows us to spend our time with our customers and our food. It’s also nice that GastroGo is local. Technology and apps are for the big cities and foreign countries, so it’s awesome that some locals have decided to create a better alternative.",
          name: "Alexander Olesen",
          position: "Restaurant owner at Olesen’s Smørrebrød",
          src: "lateP",
        },
        {
          comment:
            "Becoming a partner of GastroGo has made me happy, since their customer service is the best I have ever experienced. There are no problems, just solutions. Thank you GastroGo for an awesome and easy to use app for our restaurant.",
          name: "David Blom",
          position: "Restaurant owner at Restaurant Passebækgård",
          src: "david2",
        },
      ],
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