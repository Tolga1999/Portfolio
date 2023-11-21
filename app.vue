<script>
</script>

<template>
  <div class="scroller">
    <!-- first main section -->
    <section class="first section circle-h1-container">
      <AppHeader />
      <img class="circle-svg" src="/svg/circle1.svg" alt="homescreen circle">
      <h1>Frontend Developer</h1>

      <div class="scroll-down">
        <img src="/svg/arrow-right-down.svg" alt="arrow right down">
        <span class="scroll-down-text">Scroll down</span>
      </div>
    </section>
    <!-- first main section end -->

    <!-- second section -->
    <section class="second-section">
      <h2>Creator, Coder and Designer.</h2>
    </section>
    <!-- second section end -->

  </div>
</template>

<style>
/* snap scroll */
.scroller {
  max-height: 100vh;
  overflow-y: scroll;
  scroll-snap-type: y mandatory;
  scroll-snap-points-y: repeat(5rem);
}

section {
  height: 100vh;
  scroll-snap-align: start;
}
/* snap scroll end */

.circle-h1-container {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.circle-svg {
  flex-grow: 1;
  width: 100%;
  max-width: 35em;
  padding-top: 5em;
  /* transform: translateY(-1.5em); */
}

h1 {
  z-index: 1;
  transform: translateY(-2.5em);
}

.scroll-down {
  align-self: flex-end;
  margin: 1.5em 0.75em;
}

.scroll-down-text {
  font-size: 1.25em;
  font-weight: 500;
}

/* second section */
.second-section {
  padding-top: 0.5em;
}

/* second section end */
</style>
