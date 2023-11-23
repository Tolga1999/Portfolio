<script>
import { gsap } from "gsap";

import { ScrollTrigger } from "gsap/ScrollTrigger";


// client side scripting
gsap.registerPlugin(ScrollTrigger);
export default {
    mounted() {
        let tl2 = gsap.timeline({
            scrollTrigger: {
                trigger: ".h3-project",
                start: "top 70%",
                end: "bottom 10%",
                // markers: true,
                scrub: 5,
            },
        })
        
        // tl sets
        tl2.set(".h3-project", {
            opacity: 0,
            yPercent: 100,
        })

        tl2.set(".img-project", {
            opacity: 0,
            yPercent: 100,
        })

        tl2.set(".p-project", {
            opacity: 0,
            yPercent: 100,
        })

        tl2.set(".anchor-project", {
            opacity: 0,
            yPercent: 100,
        })

        tl2.set("hr", {
            width: "0",
            opacity: 0,
        })

        // tl to's
        tl2.to(".h3-project", {
            opacity: 1,
            yPercent: 0,
        })

        tl2.to(".img-project", {
            opacity: 1,
            yPercent: 0,
        })

        tl2.to(".p-project", {
            opacity: 1,
            yPercent: 0,
        })

        tl2.to(".anchor-project", {
            opacity: 1,
            yPercent: 0,
        })

        tl2.to("hr", {
            width: "100%",
            opacity: 1,
        })
    }
}
</script>

<template>
    <section class="last-section">
        <h3 class="h3-project">Vervoerregio Amsterdam</h3>
        <article>
            <img class="img-project" src="/img/iPhone15pro.png" alt="iphone 15 pro project foto">
            <div>
                <p class="p-project">Project for Vervoerregio Amsterdam focusing on WCAG guidelines and the specific check
                    ups between their
                    partners.
                </p>
                <a class="anchor-project" href="/">See more</a>
            </div>
            <hr>
        </article>
    </section>
</template>

<style scoped>
section {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
}

article {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    flex-grow: 0.4;
}

div {
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    flex-grow: 0.4;
}

img {
    width: 100%;
}

p {
    margin: 0;
}

a {
    font-weight: 600;
    text-decoration: none;
    color: var(--c-text);
    border: 3px solid var(--c-border-bottom);
    padding: 0.5em 1em;
    width: 30%;
}

hr {
    margin-bottom: 1.5em;
}
</style>