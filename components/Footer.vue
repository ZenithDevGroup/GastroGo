<template>
  <div class="customCol">
    <div class="MainContainer">
      <div></div>
      <div class="content">
        <!-- <div class="icons">
          <p>Follow us on</p>
          <div>
            <a href=""> <v-icon large>mdi-instagram</v-icon></a>
            <v-icon large>mdi-facebook</v-icon>
          </div>
        </div> -->
        <div class="imgContainer">
          <img src="~/assets/images/logo.svg" alt="" />
          <p>GastroGo</p>
        </div>
        <!-- <div class="customCol"> -->
        <div class="customRow">
          <NuxtLink v-bind:to="section1">Home</NuxtLink>
          <!-- <NuxtLink v-bind:to="section2">About</NuxtLink> -->
          <NuxtLink v-bind:to="section3">Features</NuxtLink>
          <!-- <NuxtLink v-bind:to="section3">Partners</NuxtLink> -->
          <NuxtLink v-bind:to="section4">Pricing</NuxtLink>

          <NuxtLink v-bind:to="section4">FAQ</NuxtLink>
        </div>
        <div class="icons">
          
          <a href=""> <v-icon large dark>mdi-instagram</v-icon> </a>
           <a href=""><v-icon large dark>mdi-facebook</v-icon></a>
        </div>
        <!-- <div class="iconsSmall">
            <p>Follow us on</p>
            <div>
              <a href=""> <v-icon large>mdi-instagram</v-icon></a>
              <v-icon large>mdi-facebook</v-icon>
            </div>
          </div> -->

        <!-- <div>
            <p style="text-align: left; color: blue; font-weight: 400">
              Sign up to our newsletter
            </p>
            <div class="emailContainer">
              <div style="width: 100%">
                <input
                  type="email"
                  name=""
                  id=""
                  placeholder="someemail@email.com"
                />
              </div>
              <div style="width: 100%">
                <v-btn :elevation="0" outlined>JOIN</v-btn>
              </div>
            </div>
          </div> -->
        <!-- </div> -->
      </div>
      <div></div>
    </div>
    <div class="pos">
      <div></div>
      <div class="row terms">
        <p>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
          eiusmod tempor.
        </p>
        <div class="links">
          <a href="">Terms</a>
          <a href="">Privacy</a>
          <a href="">Security</a>
        </div>
      </div>
      <div></div>
    </div>
  </div>
</template>
<script>
export default {
  props: ["section1", "section2", "section3", "section4", "section5"],
};
</script>
<style lang="scss" scoped>
.customCol {
  display: grid;
  grid-auto-flow: row;
  // grid-gap: 20px;

  .MainContainer {
    background-color: black;
    display: grid;
    grid-template-columns: 1fr 4fr 1fr;
    justify-content: center;
    text-align: center;
    padding-top: 30px;
    padding-bottom: 10px;
    color: white;
    font-family: "Josefin Sans";

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
// .iconsSmall {
//   display: none;
// }
// .MainContainer {
//   display: grid;
//   grid-template-columns: 1fr 4fr 1fr;
//   justify-content: center;
//   text-align: center;
//   p {
//     font-size: 12px;
//   }
//   .content {
//     display: grid;
//     // margin: 20px 0;
//     padding: 0 !important;
//     grid-template-columns: repeat(3, 1fr);
//     justify-content: space-between;

//     div {
//       justify-self: start;
//     }
//   }
//   .customRow {
//     width: 100%;
//     display: flex;
//     flex-direction: row;
//     justify-content: space-between;
//     align-content: center;

//     a {
//       text-decoration: none;
//       color: grey;
//       font-size: 12px;
//       font-weight: 500;
//     }
//     a:hover {
//       font-weight: bold;
//     }

//     div {
//       justify-self: center;
//     }
//   }
//   .icons {
//     display: flex;
//     justify-content: center;
//     flex-direction: column;

//     // div {
//     //   padding: 10px;
//     // }
//   }

//   .emailContainer {
//     display: grid;
//     grid-template-columns: 5fr 1fr;
//     button {
//       border-radius: 0;
//       outline: 0.5px solid grey;
//       color: white;
//       background-color: rgb(155, 155, 155);
//       height: 100%;
//       width: 100%;
//       letter-spacing: 4px;
//     }
//     input[type="email"] {
//       outline: 0.5px solid gray;
//       width: 100%;
//       padding: 10px;
//       color: grey;
//     }
//     ::placeholder {
//       font-size: 12px;
//       letter-spacing: 4px;
//     }
//     input:focus {
//       border: none;
//       margin: 0;
//       outline: 0.5px solid black;
//     }
//   }
// }
.pos {
  background-color: rgb(163, 127, 135);
  display: grid;
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

      a{
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
