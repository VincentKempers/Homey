<template>
  <button class="shiny--button">
    very shiny
  </button>
</template>

<script>
export default {

}
</script>

<style scoped>
  .shiny--button {
    background: orange;
    color: #fff;
    font-size: 1rem;
    border-radius: 0.5em;
    padding: .5rem 2rem;
    border: none;
    position: relative;
    overflow: hidden;
    line-height: 32px;
  }

  .shiny--button::after {
    content: '';
    position: absolute;
    top: -50%;
    right: -50%;
    bottom: -50%;
    left: -50%;
    background: linear-gradient(to bottom, rgba(229, 172, 142, 0), rgba(255,255,255,0.5) 50%, rgba(229, 172, 142, 0));
    transform: rotateZ(60deg) translate(-5em, 7.5em);
  }

  button:hover::after, button:focus::after {
    animation: sheen 1s ease;
  }

  @keyframes sheen {
  100% {
      transform: rotateZ(60deg) translate(1em, -9em);
    }
  }
</style>
