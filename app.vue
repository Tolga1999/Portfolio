<script>
import { gsap } from "gsap";

import { ScrollTrigger } from "gsap/ScrollTrigger";


// client side scripting
gsap.registerPlugin(ScrollTrigger);
export default {
  mounted() {
    gsap.fromTo("h1", { opacity: 0, yPercent: 100 }, { opacity: 1, yPercent: 0, duration: 0.5, delay: 1.5 })
    gsap.fromTo(".circle-svg-1", { opacity: 0, yPercent: 50 }, { opacity: 1, yPercent: 0, duration: 1, delay: 2 })
    gsap.fromTo(".scroll-down", { opacity: 0, yPercent: 100 }, { opacity: 1, yPercent: 0, duration: 1, delay: 3 })

    let tl = gsap.timeline({
      scrollTrigger: {
        trigger: ".creator-coder-h2",
        start: "top bottom",
        end: "250 30%",
        // markers: true,
        scrub: 5,
      },
    })

    let tl2 = gsap.timeline({
      scrollTrigger: {
        trigger: ".worked-projects-h2",
        start: "top bottom",
        end: "bottom 25%",
        // markers: true,
        scrub: 7,
      },
    })

    // tl sets
    tl.set(".scroll-down-homescreen", {
      opacity: 1,
    })

    tl.set(".creator-coder-h2", {
      opacity: 0,
      yPercent: 100,
    })

    tl.set(".hr-first", {
      width: "0",
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
      opacity: 0,
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

    tl2.set(".worked-projects-h2", {
      opacity: 0,
      yPercent: 100,
    })

    tl2.set(".second-circle-svg", {
      scale: 0.9,
      opacity: 0
    })

    // github and scroll down - projects
    tl2.set(".github-link", {
      opacity: 0,
      yPercent: 100,
    })

    tl2.set(".scroll-down-projects", {
      opacity: 0,
      yPercent: 100,
    })

    // tl to's
    tl.to(".scroll-down-homescreen", {
      opacity: 0,
      delay: 2.5,
    })

    tl.to(".creator-coder-h2", {
      opacity: 1,
      yPercent: 0,
    })

    tl.to(".hr-first", {
      width: "100%",
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
      opacity: 1,
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

    tl2.to(".logos", {
      opacity: 0,
      duration: 3,
    })

    tl2.to(".worked-projects-h2", {
      opacity: 1,
      yPercent: 0,
    })

    tl2.to(".second-circle-svg", {
      scale: 1.3,
      opacity: 1,
    })

    // github and scroll down - projects
    tl2.to(".github-link", {
      opacity: 1,
      yPercent: 0,
    })

    tl2.to(".scroll-down-projects", {
      opacity: 1,
      yPercent: 0,
    })

  }
}
</script>

<template>
  <!-- first section -->
  <section class="first-section circle-h1-container">
    <AppHeader />
    <img class="circle-svg-1" src="/svg/circle1.svg" alt="homescreen circle">
    <h1>Frontend Developer</h1>

    <div class="scroll-down scroll-down-homescreen">
      <img src="/svg/arrow-right-down.svg" alt="arrow right down">
      <span class="scroll-down-text">Scroll down</span>
    </div>
  </section>

  <!-- second section -->
  <section class="second-section">
    <h2 class="creator-coder-h2">Creator, Coder and Designer.</h2>
    <hr class="hr-first">

    <article class="introduction-container">
      <h3 class="introduction-h3">Introduction</h3>

      <div class="introduction-p">
        <p>
          Hello! My name is Tolga, I’m 24 years old and I like to design and code projects in Vue.js, Sveltekit and Nuxt.js.
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
        <img class="linkedin-svg" src="svg/linkedin1.svg" alt="linkedin logo">
        <img class="twitter-svg" src="svg/twitter.svg" alt="twitter logo">
        <img class="instagram-svg" src="svg/instagram.svg" alt="instagram logo">
      </div>
    </article>
  </section>

  <!-- third section -->
  <section class="third-section">
    <div class="projects-svg-container">
      <h2 class="worked-projects-h2">Projects that I've worked on.</h2>
      <img class="second-circle-svg" src="/svg/circle2.svg" alt="second cirlce">
    </div>

    <div class="scroll-down-projects-container">
      <NuxtLink class="github-link" to="https://github.com/Tolga1999">Tolga1999 <img src="/svg/github.svg"
          alt="github logo"></NuxtLink>
      <div class="scroll-down scroll-down-projects">
        <img src="/svg/arrow-right-down.svg" alt="arrow right down">
        <span class="scroll-down-text">Scroll down</span>
      </div>
    </div>
  </section>

  <Project :nameProject="'Vervoerregio Amsterdam'" :imgUrl="'/img/devices-mockup-toolgankelijkheid.png'"
    :projectText="'Project for Vervoerregio Amsterdam focusing on WCAG guidelines and the specific check ups between their partners.'"
    :projectSpecsText="'Project Specifications: Sveltekit, Vervoerregio Amsterdam API and Hygraph.'"
    :seeMore="'https://github.com/WesleySchorel/lose-your-head-the-client-case'" />

    <Project :nameProject="'Schiphol Dashboard'" :imgUrl="'/img/devices-mockup-schiphol.png'"
    :projectText="'Dashboard made for Schiphol to visualize flights from Amsterdam to different destinations.'"
    :projectSpecsText="'Project specifications: NodeJs, Express, Ejs, Schiphol API and datamaps D3.js.'"
    :seeMore="'https://github.com/Tolga1999/proof-of-concept'" />

    <Project :nameProject="'Groovy Search'" :imgUrl="'/img/iPhone15pro.png'"
    :projectText="'Fun little project to search your best friends at FDND!'" 
    :projectSpecsText="'Project Specifications: unique design, Sveltekit and Prismic CMS.'" 
    :seeMore="'https://github.com/Tolga1999/your-tribe-for-life-squad-page'"/>
</template>

<style>
section {
  height: 100vh;
}

.second-section,
.third-section {
  padding-top: 1.5em;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

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
  gap: 0.3em;
  align-self: flex-end;
  margin: 1.5em 0.75em;
}

.scroll-down-text {
  font-size: 1.25em;
  font-weight: 600;
}

/* second section */
h2 {
  padding-bottom: 0.5em;
  /* border-bottom: 3px solid var(--c-border-bottom); */
}

hr {
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

/* third section */
.projects-svg-container {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.worked-projects-h2 {
  padding-bottom: 0;
}

.second-circle-svg {
  width: 70%;
  max-width: 20em;
  margin-top: 5em;
}

.github-link {
  display: flex;
  align-items: center;
  gap: 0.3em;
  text-decoration: none;
  color: var(--c-text);
  font-weight: 600;
  font-size: 1.25em;
}

.scroll-down-projects-container {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

@media (min-width: 725px) {
  h1{
    font-size: 6em;
  }

  h2{
    font-size: 4em;
  }
  
  .circle-svg-1{
    scale: 1.1;
  }
  h1{
    align-self: flex-start;
    width: 50%;
    line-height: 1em ;
    transform: translateY(-2em);
  }

  .scroll-down-homescreen{
    transform: translateY(-14em);
  }

  .creator-coder-h2{
    padding-top: 3em;
  }

  .introduction-p p{
    line-height: 1.5em;
    width: 50%;
  }

  /* second section */
  .worked-projects-h2{
    align-self: flex-start;
    width: 50%;
  }

  .second-circle-svg{
    display: none;
  }

}
</style>
