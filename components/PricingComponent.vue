<template>
  <div class="MainContainer">
    <div class="content">
      <div>
        <h3>Find a plan that's right for you.</h3>
        <p>Every plan comes with a 30-day free trial</p>
      </div>
      <div class="custom-row">
        <CardComponent />
        <CardComponent />
        <CardComponent />
      </div>
    </div>
  </div>
</template>
<style lang="scss" scoped>
.MainContainer {
  display: flex;
  justify-content: center;
  height: 100vh;
  .content {
    padding-top: 100px;
    padding-bottom: 60px;
    width: 80%;
    height: 100%;
    display: grid;grid-template-rows: 1fr 1fr;
    grid-gap: 60px;
    text-align: center;
    align-content: center;
    justify-content: center;

    .custom-row {
      width: 100%;
      display: flex;
      gap: 40px;
      flex-direction: row;
      justify-content: space-between;
      
      div {
        margin-right: 10px;
        width: 100%;
        height: 100%;
        min-width: 375px;
        max-width: 475px;
      }
    }
  }
}
</style>