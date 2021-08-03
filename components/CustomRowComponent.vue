<template>
  <div
    class="customCard"
    
  >
    <div class="imgContainer">
      <img src="https://cdn.vuetifyjs.com/images/cards/cooking.png" alt="" />
    </div>
    <div>
      <div class="textContainer">
        <h3 class="headline pink--text text--accent-2 text-center">Superdry</h3>
        <p>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed doeiusmod
          tempor incididunt ut labore et dolore magna aliqua.
        </p>
      </div>
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
    vertical-align: middle;
    width: 50px;
    height: 50px;
    border-radius: 50%;
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