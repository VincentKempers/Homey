<template>
  <div class="styleguide">
    <section class="style--atoms">
      <h2>Atoms</h2>
      <p>Here you can find all the atoms</p>
      <div class="atoms--items">
        <Logo />
        <HeaderItem />
        <ShinyButton />
        <MobileMenu />
        <NextButton />
      </div>
    </section>
    <section class="style--molecules">
      <h2>Molecules</h2>
      <p>Here you can find all the Molecules</p>
      <div class="molecules--items">
        <Header />
      </div>
    </section>
    <section class="style--organisms">
      <h2>Organisms</h2>
      <p>Here you can find all the Organisms</p>
      <div class="organisms--items">
        <button @click="showOverlay()">
          Click to open overlay
        </button>
        <Overlay :visible="overlayProp" @hideOverlay="hideOverlay" />
      </div>
    </section>
  </div>
</template>

<script>
// =============== ATOMS ===============
import Logo from "../atoms/Logo";
import HeaderItem from "../atoms/HeaderItem";
import ShinyButton from "../atoms/ShinyButton";
import MobileMenu from "../atoms/MobileMenu";
import NextButton from "../atoms/NextButton";

// =============== Molecules ===============
import Header from "../molecules/Header";

// =============== ORGANISMS ===============
import Overlay from "../organisms/Overlay";

export default {
  components: {
    Logo,
    HeaderItem,
    Header,
    MobileMenu,
    ShinyButton,
    NextButton,
    Overlay
  },
  data () {
    return {
      overlayProp: false
    };
  },
  methods: {
    showOverlay () {
      this.overlayProp = true;
    },
    hideOverlay () {
      this.overlayProp = false;
    }
  }
};
</script>

<style scoped>
    .styleguide > section {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-content: center;
        margin: 4rem 0rem;
    }

    .atoms--items {
        display: flex;
        flex-direction: row;
        justify-content: center;
        align-items: center;
    }

    .atoms--items > *{
        margin-right: 2rem;
    }

    .molecules--items, .organisms--items {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items:left;
        margin: 2rem 0;
    }
</style>
