<template>
  <div class="MainContainer">
    <div class="content">
      <div>
        <h1>{{ $t('completely-free')}}</h1>
        <p>
          {{ $t('freemium')}}
        </p>
        <ButtonComponent />
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.MainContainer {
  display: flex;
  height: 100vh;
  position: relative;
  justify-content: center;
  background-color: rgb(247, 121, 104);
  .content {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    color: white;
    width: 80%;
    // padding: 40px 0;
    max-width: 1320px;
  }
  .content > div {
    text-align: center;

    h1 {
      padding-bottom: 40px ;
      font-size: clamp(1rem, 6vw, 2.5rem);
    }
    p {
      padding-bottom: 40px;
      line-height: 1.5;
      text-align: center;
      font-size: clamp(1rem, 6vw, 1.2rem);
      max-width: 60ch;
      text-align: justify;
    }
  }
}


@media only screen and (max-width: 1100px) {
  .MainContainer{
    height: 100% !important;
    .content{
      padding: 60px 0;
    }
  }
}
</style>