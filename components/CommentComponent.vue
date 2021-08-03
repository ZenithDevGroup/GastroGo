<template>
    <div class="col">
          <div class="comment">
            <h3>"Good support!"</h3>
            <p>
              Lorem ipsum dolor sit amet, consectetur adipiscing elitcLorem
              ipsum dolor sit amet, consecteturs
            </p>
          </div>
          <div class="customerProfile">
            <div class="imgContainer">
              <img
                src="~/assets/images/philip-martin-5aGUyCW_PJw-unsplash.jpg"
                alt=""
              />
            </div>
            <div class="profileInfo">
              <p id="name">Melissa James</p>
              <p id="position">Manager at TechCream</p>
            </div>
          </div>
        </div>
</template>
<style lang="scss" scoped>

  .customerProfile {
      display: grid;
      grid-auto-flow: column;
      grid-gap: 10px;
      padding-top: 20px;
      justify-content: start;
      align-content:center;
      text-align: left;

      .profileInfo{
        display: flex;
        flex-direction: column;
        justify-content: center;
      }
    .imgContainer {
      img {
        vertical-align: middle;
        width: 50px;
        height: 50px;
        border-radius: 50%;
      }
    }

    #name{
        font-weight: bold;
        font-size: 14px;
    }
    #position{
        font-size: 12px;
        color: gray;
    }
  }
  .comment {
    width: 100%;
    height: auto;
    padding: 20px;
    background-color: white;
    border: 1px solid black;
    border-radius: 10px;
    color: black;
    position: relative;
    text-align: left;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-content: center;

    h3 {
      padding-bottom: 20px;
    }
  }
    .comment::after {
    content: "";
    position: absolute;
    height: 10px;
    width: 10px;
    bottom: -10px;
    right: 90%;
    background-color: gray;
    clip-path: polygon(0 0, 100% 0, 0 100%);
  }
</style>