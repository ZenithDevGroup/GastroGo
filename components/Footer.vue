<template>
  <div class="col">
    <div class="MainContainer">
      <div></div>
      <div class="content">
        <div class="icons">
          <p>Follow us on</p>
          <div>
            <a href=""> <v-icon large>mdi-instagram</v-icon></a>
            <v-icon large>mdi-facebook</v-icon>
          </div>
        </div>
        <div class="col">
          <div class="customRow" style="text-align: center">
            <div><a href="http://">HOME</a></div>
            <div><a href="http://">ABOUT US</a></div>
            <div><a href="http://">PARTNERS</a></div>
            <div><a href="http://">FAQS</a></div>
            <div><a href="http://">CONTACT US</a></div>
          </div>

          <div>
            <p style="text-align: left; color: blue; font-weight:400">Get started now</p>
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
                <v-btn :elevation="0" outlined>Send</v-btn>
              </div>
            </div>
          </div>
        </div>
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
        <div class="terms">
          <a href="">Terms</a>
          <a href="">Privacy</a>
          <a href="">Security</a>
        </div>
      </div>
      <div></div>
    </div>
  </div>
</template>
<style lang="scss" scoped>
.MainContainer {
  background-color: #fafafa;
  display: grid;
  grid-template-columns: 1fr 4fr 1fr;
  justify-content: center;
  text-align: center;
  p {
    font-size: 12px;
  }
  .content {
    display: grid;
    margin: 20px 0;
    padding: 0 !important;
    grid-template-columns: repeat(2, 1fr);
    justify-content: space-between;

    div {
      justify-self: start;
    }
  }
  .customRow {
    display: flex;
    padding-top: 20px;
    padding-bottom: 20px;
    flex-direction: row;
    justify-content: space-between;
  }
  .icons {
    display: flex;
    justify-content: center;
    flex-direction: column;

    div {
      padding: 10px;
    }
  }
  .pos {
    background-color: #a1a1a1;
    display: grid;
    grid-template-columns: 1fr 4fr 1fr;
    justify-content: space-between;
    padding: 0 20px;
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
      }

      p {
        padding: 8px !important;
        font-size: 12px;
      }
    }
  }

  .col,
  .row {
    margin: 0 !important;
    padding: 0 !important;
  }
  
  .pos{
    padding: 10px;
  }
  a {
    text-decoration: none;
    color: grey;
    font-size: 12px;
    font-weight: 500;
  }
  a:hover {
    font-weight: bold;
  }
  .emailContainer {
    padding-top: 4px;
    padding-bottom: 20px;
    display: grid;
    grid-template-columns: 5fr 1fr;
    button {
      border-radius: 0;
      border: 1px solid grey;
      color: white;
      background-color: rgb(155, 155, 155);
      height: 100%;
      width: 100%;
      letter-spacing: 4px;
    }
    input[type="email"] {
      border: 0.5px solid grey;
      width: 100%;
      padding: 10px;
      color: grey;
    }
    ::placeholder {
      font-size: 12px;
      letter-spacing: 4px;
    }
    input:focus {
      border: none;
      margin: 0;
      outline: 0.5px solid black;
    }
  }
}
</style>
