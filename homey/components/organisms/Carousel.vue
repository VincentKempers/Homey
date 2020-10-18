<template>
  <div>
    <section v-for="data in myJson" :key="data.title">
      <h2 class="content-movie__title">
        {{ data.title ? '' : 'Double Down' }}
      </h2>
      <img class="content-movie__poster" src="../../assets/imgs/imgDoubleDown.png" :alt="data.title ? '' : 'Double Down'">
      <quote>
        <h3 class="content-movie__comment">
          {{ data.title ? '' : 'Sometimes you don\'t watch a film, rather you survive it.' }}
        </h3>
        <em class="content-movie__comment-author">
          {{ data.author ? '' : 'quinoa1984' }}
        </em>
      </quote>
    </section>

    <!-- @TODO: Make component -->
    <!-- <div class="navigation">
      <div class="navigation-prev">
        <p class="navigation-prev__text">previous</p>
        <div class="navigation-prev__line"></div>
      </div>
      <div class="navigation-next">
        <p class="navigation-next__text">previous</p>
        <div class="navigation-next__line"></div>
      </div>
    </div> -->
  </div>
</template>

<script>
import dataMovies from "../../data.json";

export default {
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

<style scoped>
.content-movie__title {
  font-family:
    'Minion Pro Regular',
    serif;
  display: block;
  font-weight: 300;
  font-size: 10rem;
  color: #E3E3E3;
  letter-spacing: 10px;
  position: relative;
  z-index: 10;
}

.content-movie__poster {
  max-width: 40%;
  margin-top: -5rem;
  z-index: 0;
}

quote {
  display:block;
  max-width: 48rem;
  margin: 0 auto;
}

.content-movie__comment {
  color: #E3E3E3;
  font-family:
  'Minion Pro Regular',
    serif;
    font-weight: 100;
  font-size: 3rem;
  z-index: 10;
  position: relative;
  margin-top: -3rem;
}

.content-movie__comment-author {
  font-family: 'Montserrat Medium', sans-serif;
  text-transform: uppercase;
  font-weight: 800;
  color: #FFC000;
  letter-spacing: 18px;
}
</style>
