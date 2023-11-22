<script>
import { gsap } from "gsap";

import { ScrollTrigger } from "gsap/ScrollTrigger";


// client side scripting
gsap.registerPlugin(ScrollTrigger);
export default {
  mounted() {
    gsap.fromTo("h1", { opacity: 0 }, { opacity: 1, duration: 1 })

    let tl = gsap.timeline({
      scrollTrigger: {
        trigger: "h2",
        end: "900 60%",
        // markers: true,
        scrub: 5,
      },
    })

    // tl sets
    tl.set(".scroll-down", {
      opacity: 1,
    })

    tl.set("h2", {
      opacity: 0,
      yPercent: 100,
    })

    tl.set(".hr-first", {
      width: "0",
      // x: "-100px",
      opacity: 0,
    })

    tl.set(".introduction-h3", {
      opacity: 0,
      yPercent: 100,
      duration: 10,
    })

    tl.set(".introduction-p", {
      opacity: 0,
      yPercent: 100,
    })

    tl.set(".hr-second", {
      width: "0",
      // x: "-100px",
    })

    tl.set(".contact-me-h3", {
      opacity: 0,
      yPercent: 100,
    })

    // logos
    tl.set(".linkedin-svg", {
      opacity: 0,
      yPercent: 100,
    })

    tl.set(".twitter-svg", {
      opacity: 0,
      yPercent: 100,
    })

    tl.set(".instagram-svg", {
      opacity: 0,
      yPercent: 100,
    })

    // tl to's
    tl.to(".scroll-down", {
      opacity: 0,
      delay: 2.5,
    })

    tl.to("h2", {
      opacity: 1,
      yPercent: 0,
    })

    tl.to(".hr-first", {
      width: "100%",
      // x: 0,
      opacity: 1,
    })

    tl.to(".introduction-h3", {
      opacity: 1,
      yPercent: 0,
    })

    tl.to(".introduction-p", {
      opacity: 1,
      yPercent: 0,
    })

    tl.to(".hr-second", {
      width: "100%",
      // x: 0,
    })

    tl.to(".contact-me-h3", {
      opacity: 1,
      yPercent: 0,
    })

    tl.to(".linkedin-svg", {
      opacity: 1,
      yPercent: 0,
    })

    tl.to(".twitter-svg", {
      opacity: 1,
      yPercent: 0,
    })

    tl.to(".instagram-svg", {
      opacity: 1,
      yPercent: 0,
    })
  }
}
</script>

<template>
  <!-- <div class="scroller"> -->
    <!-- first snap section -->
    <section class="first section circle-h1-container">
      <AppHeader />
      <img class="circle-svg-1" src="/svg/circle1.svg" alt="homescreen circle">
      <h1>Frontend Developer</h1>

      <div class="scroll-down">
        <img src="/svg/arrow-right-down.svg" alt="arrow right down">
        <span class="scroll-down-text">Scroll down</span>
      </div>
    </section>

    <!-- second snap section -->
    <section class="second-section">
      <h2>Creator, Coder and Designer.</h2>
      <hr class="hr-first">

      <article class="introduction-container">
        <h3 class="introduction-h3">Introduction</h3>

        <div class="introduction-p">
          <p>
            Hello! My name is Tolga, I’m 24 years old and I like to design projects in Vue.js, Sveltekit and Nuxt.js.
          </p>
          <p>
            I’m a student at the Amsterdam University of Applied Sciences, in my last year and can’t wait to enter the
            real
            world of web design and development!
          </p>
        </div>
      </article>

      <hr class="hr-second">
      <article class="contact-me-container">
        <h3 class="contact-me-h3">Contact me</h3>

        <div class="logos">
          <img class="linkedin-svg" src="svg/linkedin.svg" alt="linkedin logo">
          <img class="twitter-svg" src="svg/twitter.svg" alt="twitter logo">
          <img class="instagram-svg" src="svg/instagram.svg" alt="instagram logo">
        </div>
      </article>
    </section>

    <!-- third snap section -->
    <section>
      <h2>Projects that I've worked on.</h2>
    </section>

  <!-- </div> -->
</template>

<style>
/* snap scroll */
/* .scroller { */
  /* max-height: 100vh; */
  /* overflow-y: scroll;
  scroll-snap-type: y mandatory;
  scroll-snap-points-y: repeat(5rem);
} */

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

.circle-svg-1 {
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
  display: flex;
  align-items: center;
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
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

h2 {
  padding-bottom: 0.5em;
  /* border-bottom: 3px solid var(--c-border-bottom); */
}

hr{
  border: 2px solid var(--c-border-bottom);
}

.introduction-container {
  flex-grow: 6;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

h3 {
  margin-top: 1em;
}

p {
  margin-bottom: 1em;
}

/* second article */
.contact-me-container {
  /* border-top: 3px solid var(--c-border-bottom); */
  flex-grow: 2;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  margin-bottom: 0.75em;
}

.logos {
  display: flex;
  justify-content: flex-end;
  gap: 0.5em;
}

/* second section end */
</style>
