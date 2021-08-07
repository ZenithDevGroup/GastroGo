
<template>
  <div class="MainContainer">
    <div class="content">
      <div class="textContainer">
        <div>
          <p>
            FREEmium Restaurant <span style="font-weight: bold">Solution</span>,
            Where You <span style="font-weight: bold">Take The Control </span>
            <!-- <typical
              class="typicalWrapper"
              :steps="['TAKE', 1000, 'TAKE THE', 500, 'TAKE THE CONTROL', 1000]"
              :loop="10"
              :wrapper="'h3'"
            ></typical> -->
          </p>
          <!-- <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit</p> -->
        </div>
        <div class="btnContainer bigBtnContainer">
          <v-btn class="tryForFreeBtn">Try for free</v-btn>
          <v-btn class="viewPlansBtn" to="/pricing"> view plans</v-btn>
        </div>
      </div>
      <div class="btnContainer smallBtnContainer">
        <v-btn class="tryForFreeBtn">Try for free</v-btn>
        <v-btn class="viewPlansBtn" to="/pricing"> view plans</v-btn>
      </div>
      <div class="imgContainer">
        <img src="~/assets/images/devices.png" alt="" />
      </div>
    </div>
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
.typicalWrapper {
  color: palevioletred;
}
.typicalWrapper::after {
  color: pink;
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
  display: flex;
  justify-content: center;
  background-image: url("~/assets/images/bg.png");
  background-size: cover;
  .content {
    width: 80%;
    height: 100%;
    display: grid;
    grid-template-columns: 1fr 1fr;
    align-content: center;
    grid-gap: 60px;
    justify-content: space-between;
    position: relative;

    .smallBtnContainer {
      display: none;
    }
    .imgContainer {
      img {
        width: 100%;
        height: auto;
      }
    }
    .textContainer {
      font-size: clamp(1rem, 5vw, 3rem);
      line-height: 1.3;
      margin: auto;
      text-align: left;
      color: black;
    }
  }
}

.tryForFreeBtn {
  background-color: white !important;
}
.viewPlansBtn {
  background-color: rgb(247, 213, 207) !important;
  color: rgb(253, 92, 92);
}
button {
  border-radius: 50px;
  padding: 25px !important;
  margin-right: 10px;
  margin-top: 20px;
  font-weight: bold;
}
@media only screen and (max-width: 1100px) {
  .MainContainer {
    grid-template-columns: 1fr 5fr 1fr;
    .content {
      display: grid;
      grid-auto-flow: row;
      grid-template-columns: none;
      text-align: center;
      padding-top: 100px;

      .bigBtnContainer {
        display: none;
      }
      .smallBtnContainer {
        display: block;
      }
      .imgContainer {
        grid-row: 3;
      }
      .textContainer {
        text-align: center !important;
        font-size: calc((1.1 - 1) * 1.2vw + 2.2rem) !important;
      }
    }
  }
}
</style>