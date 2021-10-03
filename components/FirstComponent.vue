
<template>
  <div class="MainContainer">
    <div class="content">
      <div>
        <div class="textContainer">
          <h1>{{ $t('partner') }}</h1>
          <p>{{ $t('become')}}</p>
        </div>
        <div class="imgContainer bigImage">
          <img src="~/assets/hero-images/newdevices.png" alt="" />
        </div>
      </div>
      <div class="imgContainer smallImage">
        <img src="~/assets/hero-images/newdevices.png" alt="" />
      </div>
      <div>
        <button><a href="#section5">{{ $t('try')}}</a></button>
      </div>
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
  display: grid;
  justify-content: center;
  text-align: center;
  overflow: hidden;

  .content {
    margin: auto;
    width: 80%;
    // max-height: 56.25vw;
    display: grid;
    height: 100vh;
    grid-template-rows: repeat(2, auto);
    align-items: center;
    z-index: 2;

    .smallImage {
      display: none;
    }
    div:nth-child(1) {
      display: grid;
      grid-auto-flow: column;

      .textContainer {
        display: flex;
        flex-direction: column;
        align-content: center;
        line-height: 1.3;
        margin: auto;
        text-align: left ;
        color: black;

        h1 {
          font-size: calc((1.1 - 1) * 1.2vw + 3.3rem);
        }
        p {
          font-size: calc((1.1 - 1) * 1.2vw + 1.2rem);
          max-width: 48ch;
        }
      }
    }

    .smallBtnContainer {
      display: none;
    }
    .imgContainer {
      position: relative;
      padding: 25px;
      img {
        width: 85%;
        height: auto;
        min-width: 250px;
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
button {
  cursor: pointer;
  border: 1px solid rgba(139, 139, 139, 0.2);
  background-color: white !important;
  border-radius: 50px !important;
  padding: 16px 20px !important;
  font-weight: bold;
  scroll-behavior: smooth;

  a {
    text-decoration: none;
    color: black;
  }
}
button:hover {
  background-color: black !important;
  color: white;

  a {
    color: white;
  }
}
@media only screen and (max-width: 1000px) {
  .bigBtnContainer {
    display: none;
  }
  .MainContainer {
    .bigImage {
      display: none;
    }
    .smallImage {
      display: block !important;
    }
    .content {
      margin: auto;
      padding-top: 100px;
      display: flex;
      flex-direction: column;
      justify-content: space-around;
      align-items: center;

      div:nth-child(1) {
        display: flex;
        justify-content: space-around;
        flex-direction: column !important;
      }

      .smallBtnContainer {
        display: block;
        order: 3;
        ;
      }
      .imgContainer {
        grid-row: 2;

        img {
          height: auto;
        }
      }
    .textContainer {
        display: flex;
        flex-direction: column;
        align-content: center;
        line-height: 1.3;
        margin: auto;
        text-align: center !important;
        color: black;

        h1 {
          font-size: clamp(1rem, 5vw, 2rem);
        }
        p {
          font-size: calc((1.1 - 1) * 1.2vw + 1.2rem);
          max-width: 48ch;
        }
      }
    }
  }
}
@media only screen and (max-width: 428px) {
.MainContainer{
  height: 120vh !important;
}
}
</style>