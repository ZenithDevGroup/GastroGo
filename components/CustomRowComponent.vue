<template>
  <div
    class="customCard"
    
  >
    <div class="imgContainer">
      <img :src="require('~/assets/feature-icons/'+ imageUrl + '.png')" alt="" />
    </div>
    <div>
      <div class="textContainer">
        <h3 class="headline pink--text text--accent-2 text-center">{{ title }}</h3>
        <p>
          {{ description}}
        </p>
      </div>
    </div>
  </div>
</template>
<script>
import aosMixin from "~/mixins/aos";
export default {
  props: ['title', 'description', 'imageUrl'],
  mixins: [aosMixin],


};
</script>
<style lang="scss" scoped>
.customCard {
  display: flex;
  height: 100%;
  flex-direction: column;
  text-align: center;
  justify-content: center;
  border-radius: 12px;
  .textContainer {
    h3 {
      padding: 10px;
    }
    p {
      color: rgb(68, 68, 68);
      padding: 10px 30px;
      flex-wrap: wrap;
    }
  }
}
.imgContainer {
  text-align: center;
  padding: 20px;
  
  img {
    background-image: url("~/assets/hero-images/cookie.png");
    vertical-align: middle;
    // background-color: rgb(250, 189, 133);
    width: 50px;
    height: 50px;
    color: white;
    border-radius: 10%;
    padding: 4px;
  }
}

.customCard:hover{
  img {
    border-radius: 50%;
    transition: all 1s;
  }
}

@media only screen and (max-width: 1360px) {
  .customCard {
    display: flex;
    flex-direction: row !important;
    justify-content: center;
    align-content: center;
    text-align: left !important;

    .textContainer {
      height: 100%;
      display: flex;
      flex-direction: column;
      justify-content: center;
    }

    h3 {
      padding: 0 10px !important;
    }
    p {
      padding: 0 10px !important;
    }
  }
}
</style>