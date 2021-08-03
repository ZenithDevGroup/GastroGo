
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
          <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit</p>
        </div>
        <div>
          <v-btn>Get Started</v-btn>
        </div>
      </div>


      <div class="imgContainer">
        <img src="~/assets/images/devices.png" alt="" />
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
  background-image: url("~/assets/images/bg.png");
  background-size: cover;
  grid-template-columns: 1fr 4fr 1fr;
  .content {
    line-height: 0.9;
    display: grid;
    grid-template-columns: 1fr 1fr;
    align-content: center;
    grid-gap: 60px;
    justify-content: space-between;
    position: relative;
    .imgContainer {
      img {
        width: 100%;
        height: auto;
      }
    }
    .textContainer {
      font-size: calc((1.1 - 1) * 1.2vw + 2rem);
      margin: auto;
      padding: 20px;
      text-align: left;
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
.MainContainer{
    .content {
    display: grid;
    grid-auto-flow: row;
    grid-template-columns: none;
    text-align: center;
    .imgContainer{
      grid-row: 2
    }
    .textContainer {
      text-align: center !important;
      button {
        width: 80% !important;
      }
    }
  }
}
}
</style>