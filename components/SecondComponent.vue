<template>
  <div class="MainContainer">
    <div></div>
    <div class="content">
      <div>
        <h1>SOME HEADLINE HERE</h1>
        <p>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
          eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad
          minim veniam, quis nostrud exercitation ullamco laboris nisi ut
          aliquip ex ea commodo consequat.
        </p>
      </div>
    </div>
    <div></div>
  </div>
</template>

<style lang="scss" scoped>
.MainContainer {
  display: grid;
  grid-template-columns: 1fr 4fr 1fr;
  background-color: white;
  .content {
    height: 560px;
    display: grid;
    grid-template-columns: auto;
    justify-content: center;
    text-align: center;
    background-color: white;
  }
  .content > div {
    margin: auto;
  }

  h1{
      padding: 40px;
  }
}
</style>