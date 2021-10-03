<template>
  <div class="MainContainer">
    <div class="content">
      <div class="secondContainer">
        <div>
          <h1>{{$t('contact-today')}}</h1>
       
          <p>
           {{ $t('question')}}
          </p>
        </div>

        <div class="form">
          <form action="https://gastrogo.us7.list-manage.com/subscribe/post?u=fad4b74bab60983c035d27c68&amp;id=fd6de1d688" method="post">
            <div class="input">
              <input type="text" name="NAME" id="name" :placeholder="$t('name')" />

              <input type="email" name="EMAIL" id="email" :placeholder="$t('email')" />
            </div>
            <div>
              <textarea
                name="MESSAGE"
                id=""
                cols="38"
                rows="10"
                :placeholder="$t('message')"
              ></textarea>
            </div>

            <div class="btnContainer">
              <v-btn type="submit">Send</v-btn>
            </div>
          </form>
        </div>
      </div>
      <div class="firstContainer">
        <v-card>
          <h1>{{$t('any')}}</h1> 
          <h1>{{$t('josef')}}</h1>
          <div class="imgContainer">
            <img
              src="~/assets/images/josef.jpg"
              alt=""
            />
            <div>Josef Jensen</div>
            <div>{{$t('person')}}</div>
          </div>
          <div>
            <v-icon>mdi-email</v-icon>
            <p>josef@gastrogo.dk</p>
          </div>
          <div>
            <v-icon>mdi-phone</v-icon>
            <p>+45 28 57 16 48</p>
          </div>
        </v-card>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.MainContainer {
  display: flex;
  justify-content: center;
  align-content: center;
  height: 100vh;


.secondContainer{
  height: 100%;
  display: flex !important;
  flex-direction: column;
  justify-content: space-around;
}
  .secondContainer > div:nth-child(1) {
    h1 {
      padding-bottom: 20px;
      font-size: calc((1.1 - 1) * 1.2vw + 2.5rem);
      color: rgb(202, 11, 53);
    }
  }
  .content {
    margin: auto;
    width: 80%;
    display: grid;
    justify-content: space-around;
    align-content: center;
    align-items: center;
    grid-template-columns: 1.5fr 1fr;
    // min-height: 800px !important;
    max-width: 1260px;
    gap: 60px;

    .firstContainer {
      max-width: 430px;
      .imgContainer img {
        width: 120px;
        height: 120px;
        border-radius: 50%;
        object-fit: cover;
      }
      .imgContainer > div:nth-child(1) {
        padding: 20px;
      }
      .imgContainer > div:nth-child(2) {
        padding: 10px;
      }
      .v-card {
        border-radius: 30px;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        padding: 20px 20px 40px 20px;
        text-align: center;
        align-content: center;
        height: 100%;
        background-color: black;
        color: white;
      }
      h1 {
        padding: 10px 20px;
      }

      .v-icon {
        padding: 20px 0;
        color: white;
      }

      .v-icon:hover {
        color: pink;
        cursor: pointer;
      }
    }

    .form {
      padding-top: 60px;
      .input {
        display: flex;
        flex-direction: row;
      }

      input[type="text"],
      input[type="email"] {
        margin-bottom: 20px;
        width: 100%;
        border-bottom: 2px solid gray;
        padding: 10px 0;
      }
      input[type="text"] {
        margin-right: 10px;
      }
      input[type="email"] {
        margin-left: 10px;
      }
      textarea {
        margin: 0;
        resize: none;
        width: 100%;
        border-radius: 0;
        border-bottom: 2px solid gray;
        // padding: 10px 20px;
      }
      .btnContainer {
        width: 100%;
        display: flex;
        justify-content: right !important;
        padding: 20px 0;
      }

      input[type="text"]:focus,
      input[type="email"]:focus,
      textarea:focus {
        border-bottom: 2px solid red;

        outline: none !important;
      }
      // input[type="text"]:hover,
      // input[type="email"]:hover,
      // textarea:hover {
      //   border-bottom: 2px solid black;

      //   outline: none !important;
      // }
    }
  }
}
 @media not all and (min-resolution: 0.001dpcm) {
  @supports (-webkit-appearance: none) {
    @media only screen and (max-width: 1000px) {
    .firstContainer{
      margin-top: 60px;
    }
    }
     .btnContainer {
       text-align: right !important;

        button{
          align-items: right;
        }
      }
  }}
@media only screen and (max-width: 1000px) {
  .MainContainer {
    height: 100%;
   padding: 60px 0;
  }
  .content {
    text-align: center;
    display: flex !important;
    flex-direction: column;
  }
}
@media only screen and (max-width: 1366px) and (max-height: 768px) {
  .MainContainer {
    height: 100%;
    position: relative;
    padding-top: 120px;
    padding-bottom: 80px;
  }
  .content {
    text-align: center;
    display: flex !important;
    flex-direction: row;
    gap: 60px;
  }
}
@media only screen and (max-width: 1100px) and (max-height: 768px) {
  .MainContainer {
    height: 100%;
    position: relative;
    padding-top: 120px;
    padding-bottom: 80px;
  }
  .content {
    text-align: center;
    display: flex !important;
    flex-direction: column;
    gap: 60px;
  }
}
</style>
