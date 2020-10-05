<template>
  <div v-show="visible && state_visible" class="overlay">
    <div class="overlay--pane">
      <header>
        <h2>Are you ready!?</h2>
        <button @click="close()">
          Close
        </button>
      </header>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    visible: {
      type: Boolean,
      required: true,
      default: false
    }
  },
  data () {
    return {
      state_visible: true
    };
  },
  methods: {
    close () {
      this.$emit("hideOverlay");
    }
  }
};
</script>

<style scoped>
  .overlay {
    position: fixed;
    background-color: rgba(0,0,0,0.6);
    top: 0;
    left: 0;
    height: 100vh;
    width: 100vw;
    display: grid;
    justify-items: center;
    align-items: center;
  }

  .overlay--pane {
    height: 50%;
    width: 50%;
    margin: 0 auto;
    background-color: white;
    padding: 2rem;
  }

  .overlay--pane > header {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
  }

  .overlay--pane > header > h2 {
    color: black;
  }
</style>
