<script>
</script>

<template>
  <AppHeader />
  
  <section class="circle-h1-container">
    <img class="circle-svg" src="/svg/circle1.svg" alt="homescreen circle">
    <h1>Frontend Developer</h1>
  </section>

  <div class="scroll-down">
    <img src="/svg/arrow-right-down.svg" alt="arrow right down">
    <span class="scroll-down-text">Scroll down</span>
  </div>
</template>

<style>
.circle-h1-container {
  height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.circle-svg {
  flex-grow: 2;
  width: 100%;
  max-width: 35em;
  transform: translateY(-1.5em);
}

h1 {
  z-index: 1;
  transform: translateY(-4.5em);
}

.scroll-down {
  display: flex;
  position: absolute;
  align-items: center;
  bottom: 0;
  right: 0;
  margin: 1.5em 0.75em;
}

.scroll-down-text {
  font-size: 1.25em;
  font-weight: 600;
}
</style>
