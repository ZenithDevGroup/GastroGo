<template>
  <div class="customCol">
    <div class="MainContainer">
      <div></div>
      <div class="content">
        <div class="imgContainer">
          <img src="~/assets/images/logo.svg" alt="" />
          <p>GastroGo</p>
        </div>
        <div class="customRow">
          <NuxtLink to="/">{{$t('home')}}</NuxtLink>
          <!-- <NuxtLink v-bind:to="section1">About</NuxtLink> -->
          <NuxtLink v-bind:to="section2">Features</NuxtLink>
          <NuxtLink v-bind:to="section3">{{$t('pricing')}}</NuxtLink>
        </div>
        <div class="icons">
          <a href="https://www.instagram.com/gastrogoofficial/ ">
            <v-icon large dark>mdi-instagram</v-icon>
          </a>
          <a href="https://www.facebook.com/GastroGoOfficial/"
            ><v-icon large dark>mdi-facebook</v-icon></a
          >
        </div>
      </div>
      <div></div>
    </div>
    <div class="pos">
      <div></div>
      <div class="row terms">
        <p>&copy; {{ currentYear }} - GastroGo ApS (CVR: DK41722797)</p>
      </div>
      <div></div>
    </div>
  </div>
</template>
<script>
export default {
  props: ["section1", "section2", "section3", "section4", "section5"],
  data() {
    return {
      currentYear: new Date().getFullYear(),
    };
  },
};
</script>
<style lang="scss" scoped>
.customCol {
  display: grid;
  grid-auto-flow: row;

  .MainContainer {
    background-color: black;
    display: grid;
    grid-template-columns: 1fr 4fr 1fr;
    justify-content: center;
    text-align: center;
    padding-top: 30px;
    padding-bottom: 10px;
    color: white;
    font-family: "Josefin Sans" !important;

    .imgContainer {
      img {
        width: 30px;
        height: auto;
      }
    }

    .content {
      display: grid;
      grid-template-columns: auto 2fr auto;

      .icons {
        display: flex;
        flex-direction: row;
        justify-content: space-evenly;
        align-items: center;

        a {
          text-decoration: none !important;
        }
      }

      .customRow {
        margin: 0 20px;
        display: flex;
        flex-direction: row;
        justify-content: space-evenly;
        align-items: center;

        a {
          text-decoration: none;
          color: white;
        }
        a:hover {
          font-weight: 700;
        }
      }
    }
  }
}
.pos {
  // background-color: rgb(163, 127, 135);
  background-color: black;
  display: grid;
  font-family: "Josefin Sans" !important;
  grid-template-columns: 1fr 4fr 1fr;
  justify-content: space-between;
  padding: 20px 0;
  .terms {
    display: flex;
    justify-content: space-between;
    a {
      padding-left: 8px !important;
      padding-top: 8px;
      padding-bottom: 8px;
      font-size: 12px;
      font-weight: bold;
      color: white;
      text-decoration: none;
    }

    p {
      color: #fafafa;
      padding: 10px !important;
      font-size: 12px;
    }
  }
}

@media only screen and (max-width: 1100px) {
  .content {
    display: flex !important;
    flex-direction: column;
    margin: 10px 0;
    padding: 0 !important;
    justify-content: space-between;
    align-content: center;
    text-align: center;

    .customRow {
      padding: 20px 0;
      justify-content: center;
      display: grid !important;
      grid-gap: 10px;
      text-align: center;
      grid-template-columns: repeat(2, 1fr);
    }
    .icons {
      display: grid !important;
      grid-auto-flow: column;
      text-align: center;
      justify-content: center;

      a {
        text-decoration: none;
      }
    }
  }
  .terms {
    display: flex !important;
    justify-content: center;
    flex-direction: column;
    align-content: center;
    text-align: center;

    .links {
      width: 100%;
      text-align: center;
    }
  }
}
</style>
