<template>
  <button class="nextButton">
    >
  </button>
</template>

<script type="text/javascript">

</script>

<style scoped>
    .nextButton {
        background-color: rgba(0,0,0,1);
        border: none;
        width:3rem;
        height:3rem;
        border-radius: 2rem;
        color:white;
        font-size:2rem;
        font-weight: bold;
        opacity: 1;
        transform:translateY(0px) translateX(0px);
    }

    .nextButton::before {
      background-color:rgba(0,255,225,1);
      position:absolute;
      width: 3rem;
      height:3rem;
      border-radius: 3rem;
      content:'>';
      z-index: 1;
      opacity: 0;
      right:0;
      bottom:0;
    }

    .nextButton::after {
      background-color:rgba(225,0,0,1);
      position:absolute;
      width: 3rem;
      height:3rem;
      border-radius: 3rem;
      content:'>';
      z-index: 1;
      opacity: 0;
      top:0;
      right:0;
    }

    .nextButton:hover::before {
      animation: fake3DAnimationBlue .3s ease;
      animation-fill-mode: forwards;
    }

    .nextButton:hover::after {
      animation: fake3DAnimationRed .3s ease-in;
      animation-fill-mode: forwards;
    }

    @keyframes fake3DAnimationRed {
      100% {
        opacity: .5;
        top:-.5rem;
        left:-.5rem;
      }
    }

    @keyframes fake3DAnimationBlue {
      100% {
        opacity: .5;
        bottom:-1rem;
        left:-.5rem;
      }
    }
</style>
