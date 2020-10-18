<template>
  <div class="container">
    <Header />
    <div class="main-content">
      <section v-for="data in myJson" :key="data.title">
        <h2>{{ data.title }}</h2>
      </section>
    </div>
  </div>
</template>

<script>
import dataMovies from "../data.json";
import Header from "../components/molecules/Header";

export default {
  components: {
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

.title {
  font-family:
    'Quicksand',
    'Source Sans Pro',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
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
