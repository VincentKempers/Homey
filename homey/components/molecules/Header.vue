<template>
  <header>
    <nav>
      <h1 class="font-logo">
        Balthazar's movies
      </h1>
    </nav>
  </header>
</template>

<script>
export default {
  components: {
  }
};
</script>

<style scoped>
header {
  width: 100%;
}

nav {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
   padding: 1rem 4.5rem 1rem 0;
}

header > nav > h1 {
  font-size: 1.5rem;
  color: #FFC000;
  letter-spacing: 20px;
  text-transform: uppercase;
  margin-top: 3rem;
}

header > nav > h1:before{
  content:'';
  border-bottom: 1px solid #FFC000;
  width: 4em;
  display: block;
  margin: 0 auto;
  /* position: absolute; */
  top: 0;
  transform: rotate(90deg) translateX(-5rem);
}

</style>
