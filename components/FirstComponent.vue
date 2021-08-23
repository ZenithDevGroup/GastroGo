
<template>
  <div class="MainContainer">
    <div class="content">
      <div class="textContainer">
        <div>
          <h1>BE A PARTNER TODAY</h1>
          <p
            >Become a part of the best online order platform GastroGo within 24
            hours for FREE. Press the button below and fill out the form.</p
          >
        </div>
      </div>
      <div class="smallBtnContainer">
        <v-btn class="tryForFreeBtn" ><a href="#section5">Try for free</a></v-btn>
      </div>
      <div class="imgContainer">
        <img src="~/assets/hero-images/newdevices.png" alt="" />
      </div>
    </div>

    <div class="btnContainer bigBtnContainer">
      <v-btn class="tryForFreeBtn" ><a href="#section5">Try for free</a></v-btn>
    </div>
    <div class="hero-container">
      <img src="~/assets/hero-images/lemon.png" alt="" />
    </div>
    <img
      class="apple slide absolute"
      src="~/assets/hero-images/apple.png"
      alt=""
    />
    <img
      class="donutspin bigdonut absolute"
      src="~/assets/hero-images/Doughnut.png"
      alt=""
    />
    <img
      class="cherries slide absolute"
      src="~/assets/hero-images/cherries.png"
      alt=""
    />
    <img
      class="cupcake slide absolute"
      src="~/assets/hero-images/ice-cupcake.png"
      alt=""
    />
    <img
      class="cookie spin absolute"
      src="~/assets/hero-images/cookie.png"
      alt=""
    />
    <img
      class="pepper slide absolute"
      src="~/assets/hero-images/pepper.png"
      alt=""
    />
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
.spin {
  animation: spin 7s infinite;
}
.donutspin {
  // animation: spin 60000ms infinite;
  animation-name: spin;
  animation-duration: 120000ms;
  animation-timing-function: linear;
  animation-iteration-count: infinite;
}
.slide {
  animation: slide 4s infinite alternate-reverse;
}
.absolute {
  position: absolute;
  width: 50px;
}
.apple {
  top: 5%;
  right: 40%;
}
.pepper {
  top: 10%;
  left: 10%;
}
.cherries {
  bottom: 130px;
}
.cupcake {
  left: 20%;
  top: 30%;
}
.bigdonut {
  top: 8%;
  right: 8%;
  width: 40% !important;
  height: auto;
}
.cookie {
  bottom: 10%;
  left: 10%;
}
.MainContainer {
  display: flex;
  overflow: hidden;
  height: 100vh;
  justify-content: center;

  .content {
    width: 80%;
    display: grid;
    grid-gap: 60px;
    grid-template-columns: 1fr 1fr;
    align-content: center;
    justify-content: space-between;
    z-index: 2;

    .smallBtnContainer {
      display: none;
    }
    .imgContainer {
      position: relative;
      img {
        width: 95%;
        height: auto;
      }
    }
    .textContainer {
      line-height: 1.3;
      margin: auto;
      text-align: left;
      color: black;

      h1{
        font-size: calc((1.1 - 1) * 1.2vw + 3.3rem);
      }
      p{
        font-size: calc((1.1 - 1) * 1.2vw + 1.2rem);
        max-width: 42ch;
      }
    }
    .hero-container {
      position: absolute;
      bottom: -30px;
      left: -20px;
      img {
        margin: auto;
        animation: spin 7s linear infinite;
        width: 100px;
      }
    }
  }
}
@-moz-keyframes spin {
  100% {
    -moz-transform: rotate(360deg);
  }
}
@-webkit-keyframes spin {
  100% {
    -webkit-transform: rotate(360deg);
  }
}
@keyframes spin {
  100% {
    -webkit-transform: rotate(360deg);
  }
}
@-moz-keyframes slide {
  100% {
    -moz-transform: rotate(45deg);
  }
}
@-webkit-keyframes slide {
  100% {
    -webkit-transform: rotate(45deg);
  }
}
@keyframes slide {
  100% {
    -webkit-transform: rotate(45deg);
  }
}
.btnContainer {
  position: absolute;
  margin: auto;
  bottom: 0 !important;
  padding: 20px 0;
  z-index: 5;
}
.tryForFreeBtn {
  cursor: pointer;
  background-color: white !important;
  border-radius: 50px !important;
  padding: 25px !important;
  font-weight: bold;
  margin-bottom: 20px;
  scroll-behavior: smooth;

  a{
    text-decoration: none;
    color: black;
  }
}
.tryForFreeBtn:hover {
  background-color: black !important;
  color: white;

  a{
    color: white;
  }
}
@media only screen and (max-width: 1000px) {
  .bigBtnContainer {
    display: none;
  }
  .MainContainer {
    
    height: 100vh !important;
 
    .content {
      margin: auto;
      padding-top: 100px;
      display: flex;
      flex-direction: column;
      align-items: center;
      text-align: center;

      .smallBtnContainer {
        display: block;
        order: 3;

     
      }
      .imgContainer {
        grid-row: 2;

        img{
          max-width: 530px;
          height: auto;
        }
      }
      .textContainer {
        text-align: center !important;
        font-size: calc((1.1 - 1) * 1.2vw + 1.2rem) !important;
      }
    }
  }
}

@media only screen and (max-width: 380px) {
  .MainContainer {
    height: 100% !important;
    .content {
      display: grid;
      grid-auto-flow: row;
      grid-template-columns: none;
      text-align: center;
      padding-top: 60px;

      .bigBtnContainer {
        display: none;
      }
      .smallBtnContainer {
        display: block;
        margin: auto;
        grid-row: 3;

    
      }
      .imgContainer {
        grid-row: 2;
      }
      .textContainer {
        padding-top: 60px;
        text-align: center !important;
        font-size: calc((1.1 - 1) * 1.2vw + 1.2rem) !important;
      }
    }
  }
}
</style>