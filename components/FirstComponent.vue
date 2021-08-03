
<template>
  <div class="MainContainer">
    <div></div>
    <div class="content">
      <div class="textContainer">
        <div>
          <h3>
            <typical
              class="typicalWrapper"
              :steps="['ONE', 1000, 'ONE PAGE', 500, 'ONE PAGE SITE', 1000]"
              :loop="3"
              :wrapper="'h3'"
            ></typical>
          </h3>
          <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit,</p>
        </div>
        <div>
          <v-btn>Get Started</v-btn>
        </div>
      </div>
      <div class="imgContainer">
        <!-- <img src="~/assets/images/phone.png" alt=""> -->
      </div>
    </div>
    <div></div>
  </div>
</template>
<script>
import typical from "vue-typical";
export default {
  components: {
    typical,
  },
};
</script>
<style lang="scss" scoped>
.typicalWrapper::after {
  content: "";
  animation: blink 1s infinite step-start;
}

@keyframes blink {
  50% {
    opacity: 0;
  }
}
.MainContainer {
  height: 100vh;
  position: relative;
  justify-content: center;
  display: grid;
  background-color: white;
  margin: 0;

  grid-template-columns: 1fr 4fr 1fr;
  &::before {
    content: "";
    background-image: url("~/assets/images/bg.png");
    background-size: cover;
    position: absolute;
    background-position: center;
    top: 0px;
    right: 0px;
    bottom: 0px;
    left: 0px;
    opacity: 0.9;
  }
  .content {
    line-height: 0.9;
    display: grid;
    grid-template-columns: auto 1fr;
    align-content: center;
    justify-content: center;
    position: relative;
    // .diagonal {
    //   height: 100vh;
    //   background-size: cover;
    //   background-color: black;
    //   background-image: url("~/assets/images/henry-perks-BJXAxQ1L7dI-unsplash.jpg");
    // }

    .imgContainer{
      // background-color: rosybrown;
      img{
        width: 20%;
        height: 50%;
      }
    }
    .textContainer {
      font-size: calc((1.1 - 1) * 1.2vw + 4rem);
      margin: auto;
      padding: 20px;
      text-align: center;
      color: black;

      p {
        font-size: 22px;
        padding-top: 20px;
      }

      button {
        letter-spacing: 2px;
        font-size: 1rem;
        border-radius: 50px;
        padding: 25px;
        color: black;
        font-weight: bold;
        margin: 40px 0;
        background-color: white;
      }
    }
  }
}

@media only screen and (max-width: 1100px) {
  .content {
    display: grid;
    grid-template-areas: 1fr;
    .textContainer {
      button {
        width: 80% !important;
      }
    }
  }
}
</style>