<template>
  <div>
    <v-card :loading="loading" class="mx-auto my-12" >
      <template slot="progress">
        <v-progress-linear
          color="deep-purple"
          height="10"
          indeterminate
        ></v-progress-linear>
      </template>

      <div class="title">
       <h1>BASIC</h1>
        <p>Some description</p>
      </div>
      <v-divider class="mx-4"></v-divider>
      <div class="h1Container">
        
          <h1>$10</h1>
          <p>/month</p>
      </div>

      <div class="iconContainer">
       <IconComponent icon="mdi-check" iconDescription="This is some description"/>
        <div>
          <v-icon>mdi-check</v-icon>
          <p>Some text here</p>
        </div>
        <div>
          <v-icon color="#fc6d62">mdi-close</v-icon>
          <p>Some text here</p>
        </div>
      </div>

      <v-divider class="mx-4"></v-divider>

      <v-card-actions>
        <v-btn text @click="reserve" center> GET STARTED </v-btn>
      </v-card-actions>
    </v-card>
  </div>
</template>
<style lang="scss" scoped>
div {
  .title {
    padding: 40px;
  }
  .h1Container {
    margin: 20px;
    h1 {
      padding: 30px 0;
    }
    p{
      padding-bottom: 10px;
    }

  }
  button {
    width: 100%;
  }
  .iconContainer {
    display: flex;
    flex-direction: column;
    text-align: left;
    padding: 30px 0;
    div {
      display: flex;
      justify-content: center;

      p {
        padding: 8px 4px;
      }
    }
  }
}
</style>