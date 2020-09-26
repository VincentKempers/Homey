<template>
  <router-link :to="linkForButton">
    <button class="headerItem--button">
      {{ textForButton }}
    </button>
  </router-link>
</template>

<script>
export default {
  props: {
    textForButton: {
      type: String,
      default: 'something'
    },
    linkForButton: {
      type: String,
      default: '/'
    }
  }
}
</script>

<style scoped>
  .headerItem {
    border: none;
    font-size: 1rem;
    width: auto;
    height: auto;
  }

  .headerItem--button {
    background-color: rgba(0,0,0,0.4);
    color:white;
    font-size: 1rem;
    font-weight: 600;
    border: none;
    border-radius: .7rem;
    padding: 1rem;
    transition: background-color .4s ease-in;
  }

  .headerItem--button:hover {
    background-color: rgba(0,0,0,0.6);
    transition: background-color .2s ease-in;
  }

</style>
