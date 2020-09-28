<template>
  <a href="/" tabindex="0">
    <div class="line" />
    <div class="line" />
    <div class="line" />
  </a>
</template>

<script>
export default {}
</script>

<style scoped>
  a {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: 4rem;
    height: 4rem;
    border: 0.3rem solid #000;
    background-color: black;
    transition: all .6s ease-in-out;
  }

  a:hover, a:active, a:focus {
    background-color:white;
    border: 0.3rem solid gold;
    transition: all .4s ease-in-out;
  }

  a:hover > .line,
  a:focus > .line,
  a:active > .line {
    border-bottom: 0.3rem solid gold;
    transition: all 1s ease-in;
  }

  .line {
    width: 2rem;
    height: 0.2rem;
    border-bottom: 0.19rem solid white;
    margin-top: .2rem;
    position: relative;
    margin-bottom: .2rem;
    opacity: 1;
    transform: rotate(0deg);
    transition: all .4s ease-in;
  }

  a:hover > .line:first-of-type,
  a:focus > .line:first-of-type,
  a:active > .line:first-of-type {
    position: absolute;
    transform: rotate(45deg);
    transition: all .3s ease-in;
  }

  a:hover > .line:nth-child(2),
  a:focus > .line:nth-child(2),
  a:active > .line:nth-child(2) {
    opacity: 0;
    transition: all .1s ease-in;
  }

  a:hover > .line:last-of-type,
  a:focus > .line:last-of-type,
  a:active > .line:last-of-type {
    position: absolute;
    transform: rotate(-45deg);
    transition: all .3s ease-in;
  }

</style>
