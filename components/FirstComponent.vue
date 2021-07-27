
<template>
 <div class="outer">
   <div class="imgContainer">
     
   </div>
      <div class="MainContainer">
    <div></div>
    <div class="col">
     
      <div class="center headline-container">
        <div class="headline-content">
          <h1>SOME HEADING HERE</h1>
          <p>
            Some texts here some text here some text here some text here some
            text herej jdhfjshdfjdsfdsgkfdgkjdfhgjkfdhgkjdfhkfjdhfd
          </p>
        </div>
        <GetStartedBtn />
      </div>
      <div>
        <FloatingImage />
      </div>
    </div>
    <div></div>
  </div>
 </div>
</template>

<style lang="scss" scoped>

.MainContainer {
  display: grid;
  grid-template-columns: 1fr 4fr 1fr;
  background-image: url("~/assets/images/logo.svg");
  .col {
    height: 100vh;
    display: grid;
    padding: 0 !important;
    align-content: center;
    justify-self: center;
    grid-template-columns: 1fr 1fr;

    .headline-container {
      padding: 0 !important;
      display: grid;
      grid-template-rows: auto;
      justify-content: space-between;
      text-align: center;
    }

    .headline-content {
      h1 {
        color: #c76613;
      }
      p {
        color: #535252;
        line-height: 20px;
      }
      p,
      h1 {
        padding-top: 40px !important;
      }
    }
  }
}

// span a {
//   font-size: 18px;
//   color: #cccccc;
//   text-decoration: none;
//   margin: 0 10px;
//   transition: all 0.4s ease-in-out;
//   &:hover {
//     color: #ffffff;
//   }
// }

// .getstarted {
//   display: inline-block;
//   position: fixed;
//   bottom: 10px;
//   left: 10px;
//   width: 20vw;
//   max-width: 250px;
//   min-width: 200px;
//   z-index: 9;
//   img {
//     width: 100%;
//     height: auto;
//   }
// }
</style>