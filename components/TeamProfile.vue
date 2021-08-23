<template>
  <div class="profile">
    <div v-if="!isLeft" class="imgContainer" data-aos="fade-zoom-in">
      <img :src="src" alt="" />
    </div>
    <div
      :class="isLeft ? 'alignRight' : 'alignLeft'"
      class="profileInfo"
      data-aos="fade-ri"
    >
      <h4>{{ name }}</h4>
      <p
        style="font-size: 12px; padding: 10px 0; font-weight: bold; color: grey"
      >
        {{ position }}
      </p>
      <p id="description">
        {{ description }}
      </p>
    </div>
    <div
      v-if="isLeft"
      class="imgContainer"
      data-aos="fade-zoom-in"
      data-aos-easing="ease-in-back"
      data-aos-delay="300"
      data-aos-offset="0"
    >
      <img :src="src" alt="" />
    </div>
  </div>
</template>


<script>
import aosMixin from "~/mixins/aos";
export default {
  props: ["src", "name", "position", "description", "isLeft"],
  mixins: [aosMixin],
};
</script>
<style lang="scss"scoped>
.profile {
  height: 350px;
  text-align: left;
  display: grid;
  grid-template-columns: 1fr 1fr;
  justify-content: center;
  align-content: center;
  grid-gap: 40px;
  .imgContainer {
    text-align: center;
  }

  .profileInfo {
    display: flex;
    flex-direction: column;
    justify-content: center;
  }
  .alignLeft {
    text-align: left;
  }
  .alignRight {
    text-align: right;
  }
  #description {
    align-content: center;
    padding: 10px 0;
    max-width: 600px;
    font-size: 0.9rem;
    flex-wrap: wrap;
    color: #707070;
  }
}
.col {
  width: 60%;
}

img {
  vertical-align: middle;
  width: 200px;
  height: 200px;
  border-radius: 50%;
}

@media only screen and (max-width: 1100px) {
  .profile {
    height: auto;
    grid-template-columns: 1fr;

    .profileInfo {
      grid-row: 2;
      text-align: center;
    }
  }
}
</style>