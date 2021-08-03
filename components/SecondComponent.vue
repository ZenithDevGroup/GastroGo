<template>
  <div class="MainContainer">
    <div></div>
    <div class="content">
      <div>
        <h1>We determined that you're our target audience</h1>
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
  background-color: rgb(247, 121, 104);
  .content {
    height: 560px;
    display: grid;
    grid-template-columns: auto;
    justify-content: center;
    text-align: center;
    color: white;
  }
  .content > div {
    margin: auto;

    h1{
      padding: 40px;
      font-size: clamp(1rem, 6vw, 4rem);
    }
  }
}
</style>