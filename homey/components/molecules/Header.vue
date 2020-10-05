<template>
  <header>
    <nav>
      <h1>B-movie experience</h1>
      <div class="socials">
        <ul>
          <HeaderItem :url="'/styleguide'" :text="'style page'" />
          <HeaderItem :url="'/'" :text="'MOTW'" />
          <li>Search component</li>
        </ul>
      </div>
    </nav>
  </header>
</template>

<script>
import HeaderItem from "../atoms/HeaderItem";

export default {
  components: {
    HeaderItem
  }
};
</script>

<style scoped>
header {
  width: 100%;
}

header > nav > h1 {
  font-size: 1.5rem;
}

nav {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  padding: 2rem 4.5rem;
  border-bottom: black .4rem solid;
  box-shadow: -.1rem -0.4rem 5rem .4rem rgba(0,0,0,0.2);
}

nav ul {
  list-style: none;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-evenly;
}

nav ul > * {
  margin: 0 .9rem;
}

</style>
