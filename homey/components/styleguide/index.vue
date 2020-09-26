<template>
  <div class="styleguide">
    <section class="style--atoms">
      <h2>Atoms</h2>
      <p>Here you can find all the atoms</p>
      <div class="atoms--items">
        <Logo />
        <HeaderItem />
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
        <p>Nothing yet</p>
      </div>
    </section>
  </div>
</template>

<script>
// =============== ATOMS ===============
import Logo from '../atoms/Logo'
import HeaderItem from '../atoms/HeaderItem'

// =============== Molecules ===============
import Header from '../molecules/Header'

// =============== ORGANISMS ===============

export default {
  components: {
    Logo,
    HeaderItem,
    Header
  }
}
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
