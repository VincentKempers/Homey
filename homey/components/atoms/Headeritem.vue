<template>
  <router-link :to="url">
    <button class="headerItem--button">
      {{ text }}
    </button>
  </router-link>
</template>

<script>
export default {
  props: {
    text: {
      type: String,
      default: 'something'
    },
    url: {
      type: String,
      default: '/'
    }
  }
};
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
    min-width: 8rem;
    max-width: 9rem;
    transition: background-color .4s ease-in;
  }

  .headerItem--button:hover {
    background-color: rgba(0,0,0,0.6);
    transition: background-color .2s ease-in;
  }

</style>
