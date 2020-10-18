<template>
  <div class="container">
    <Header />
    <div class="main-content">
      <!-- doesn't show anything for now -->
      <Carousel />
    </div>
  </div>
</template>

<script>
import dataMovies from "../data.json";
import Header from "../components/molecules/Header";
import Carousel from "../components/organisms/Carousel";

export default {
  components: {
    Carousel,
    Header

  },
  data () {
    return {
      myJson: dataMovies
    };
  },
  computed: {
    showData () {
      return console.log(this.myJson);
    }
  }
};
</script>

<style>
.container {
  background-color: #232323;
  min-height: 100vh;
}

.main-content {
  margin: 0 auto;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
