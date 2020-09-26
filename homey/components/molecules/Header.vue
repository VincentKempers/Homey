<template>
  <header>
    <nav>
      <h1>B-movie experience</h1>
      <div class="socials">
        <ul>
          <li>About</li>
          <li>MOTW</li>
          <li>search component</li>
        </ul>
      </div>
    </nav>
  </header>
</template>

<script>
export default {
}
</script>

<style scoped>
header {
  width: 100%;
}

nav {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  padding: 2rem 4.5rem;
  border-bottom: black .4rem solid;
  box-shadow: -.1rem -0.4rem 5rem .4rem rgba(0,0,0,0.4);
}

nav ul {
  list-style: none;
  display: flex;
  flex-direction: row;
  justify-content: space-evenly;
}

nav ul li {
  padding: 0 2rem;
  margin: 0 .8rem;
}
</style>
