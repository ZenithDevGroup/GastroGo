<template>
  <div>
    <div class="customerProfile">
      <div class="imgContainer">
        <img v-bind:src=imageUrl alt="" />
      </div>
      <div class="profileInfo">
        <div>
          <p>
            {{ comment }}
          </p>
        </div>
        <div class="personalInfo">
          <p id="name">- {{ name }}</p>
          <p id="position">{{ position }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["comment", "name", "position", "imageUrl"],
};
</script>
<style lang="scss" scoped>
.customerProfile {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  grid-gap: 100px;
  justify-content: space-between;
  align-content: center;
  text-align: left;

  .profileInfo {
    display: flex;
    flex-direction: column;
    justify-content: center;

    p {
      font-size: 20px;
      line-height: 1.5;
    }
    .personalInfo {
      padding-top: 40px;
      #name {
        font-weight: bold;
        font-size: 14px;
      }
      #position {
        font-size: 12px;
        color: gray;
      }
    }
  }
  .profileInfo > div:nth-child(1) {
    p {
      max-width: 40ch;
    }
  }
  .imgContainer {
    display: flex;
    justify-content: right;
    img {
      vertical-align: middle;
      width: 100%;
      height: auto;
      max-width: 475px;
      max-height: 600px;
    }
  }
}

@media only screen and (max-width: 1100px) {
  .customerProfile {
    display: flex;
    flex-direction: column;
    justify-content: space-evenly;
  }
  .profileInfo {
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center !important;

    p {
      padding: 10px 0;
      line-height: 1.5;
    }
  }
  .imgContainer {
    display: flex;
    justify-content: center !important;
    img {
      vertical-align: middle;
      width: 100%;
      height: 100%;
      max-width: 475px;
      max-height: 600px;
    }
  }
}

@media not all and (min-resolution: 0.001dpcm) {
  @supports (-webkit-appearance: none) {
    @media only screen and (max-width: 1100px) {
      .customerProfile {
        display: flex;
        flex-direction: column;
        justify-content: space-between;
      }
      .profileInfo {
        display: flex;
        justify-content: center;
        align-items: center;
        text-align: center !important;

        p {
          padding: 10px 0;
          line-height: 1.3;
        }
      }
      .imgContainer {
        display: flex;
        justify-content: center !important;
        padding-bottom: 60px;
        img {
          vertical-align: middle;
          width: 100%;
          height: 100%;
          max-width: 475px;
          max-height: 600px;
        }
      }
    }
  }
}
</style>