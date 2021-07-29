
<template>
  <div class="MainContainer">
    <div></div>
    <div class="content">
      <div class="textContainer">
        <div>
          <p style="color: wheat">
            Our
            <span style="color: white"><strong>Agency will do</strong></span> it
            for you.
          </p>
        </div>
        <div>
          <v-btn>Get Started</v-btn>
        </div>
      </div>
      <!-- <div></div> -->
    </div>
    <div></div>
  </div>
</template>

<style lang="scss" scoped>
.MainContainer {
  height: 100vh;
  position: relative;
  justify-content: center;
  display: grid;
  grid-template-columns: 1fr 4fr 1fr;
  &::before {
    content: "";
    background: linear-gradient(rgba(0, 0, 0, 0.45), rgba(0, 0, 0, 0.45)),
      url("~/assets/images/alesia-kazantceva-VWcPlbHglYc-unsplash.jpg");
    background-size: cover;
    position: absolute;
    background-position: center;
    top: 0px;
    right: 0px;
    bottom: 0px;
    left: 0px;
    opacity: 0.75;
  }
  .content {
    color: black;
    line-height: 0.9;
    text-align: center;
    
    display: flex;
    align-content: center;
    justify-content: center;
    .textContainer {
      position: relative;
      font-size: clamp(4rem, 5vw, 4rem);
      margin: auto;
      color: white;

      button {
        letter-spacing: 2px;
        font-size: 1rem;
        width: 50%;
        padding: 25px 60px;
        color: wheat;
        margin: 40px 0;
        background-color: black;
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