<template>
          <div class="avatar">
          <a href="https://codepen.io/MarioDesigns/">
            <img
              src="~/assets/images/henry-perks-BJXAxQ1L7dI-unsplash.jpg"
              alt="Skytsunami"
            />
          </a>
        </div>
</template>
<style lang="scss" scoped>
@keyframes float {
  0% {
    box-shadow: 0 5px 15px 0px rgba(0, 0, 0, 0.6);
    transform: translatey(0px);
  }
  50% {
    box-shadow: 0 25px 15px 0px rgba(0, 0, 0, 0.2);
    transform: translatey(-20px);
  }
  100% {
    box-shadow: 0 5px 15px 0px rgba(0, 0, 0, 0.6);
    transform: translatey(0px);
  }
}
.avatar {
 
  height: auto;
  fill: cover;
  box-sizing: border-box;
  border: 5px white solid;
  overflow: hidden;
  box-shadow: 0 5px 15px 0px rgba(0, 0, 0, 0.6);
  transform: translatey(0px);
  animation: float 6s ease-in-out infinite;
  img {
    width: 100%;
    height: auto;
  }
}
</style>