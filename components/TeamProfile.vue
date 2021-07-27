<template>
       <div class="col profile">
          <img
            src="~/assets/images/austin-wade-X6Uj51n5CE8-unsplash.jpg"
            alt=""
          />
          
          <p style="font-size: 12px;padding: 10px 0;font-weight: bold; color: grey">CEO</p>
          <h4>JOSEPH VINCENT</h4>
          <p style="font-size: 12px;padding: 10px 0;color:#707070">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
            eiusmod tempor
          </p>
       
        </div>
</template>
<style lang="scss"scoped>
 .teamProfile {
    display: grid;
    margin: 40px 0;
    width: 100%;
    justify-content: center;
    grid-template-columns: repeat(3, 1fr);
    div {
      justify-self: center;
    }

    .profile{
      text-align: left;
    }
    .col {
    width: 60%;
  }
  
  img {
    width: 100%;
    height: auto;
  }
  }
</style>