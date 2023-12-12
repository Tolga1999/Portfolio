<script setup>
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";

// /define props for component (properties)
const props = defineProps({
    nameProject: String,
    imgUrl: String,
    projectText: String,
    seeMore: String,
    projectSpecsText: String,
})

// client side scripting - lifecycle hook in script setup
gsap.registerPlugin(ScrollTrigger);

onMounted(() => {
    let tl2 = gsap.timeline({
        scrollTrigger: {
            trigger: ".h3-project",
            start: "top bottom",
            end: "50 10%",
            // markers: true,
            scrub: 5,
        },
    })

    // tl sets
    tl2.set(".h3-project", {
        opacity: 0,
        yPercent: 500,
    })

    tl2.set(".img-project, .p-project, .specs-text, .anchor-project", {
        opacity: 0,
        yPercent: 100,
    })

    tl2.set("hr", {
        width: "0",
        opacity: 0,
    })

    // tl to's
    tl2.to(".scroll-down-projects-container", {
        opacity: 0
    })

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
    
    tl2.to(".specs-text", {
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
})
</script>

<template>
    <section class="last-section">
        <h3 class="h3-project">{{ nameProject }}</h3>
        <article>
            <img class="img-project" :src="imgUrl" alt="project image">
            <div>
                <p class="p-project"> {{ projectText }}
                </p>
                <p class="specs-text">{{ projectSpecsText }}</p>
                <a class="anchor-project" :href="seeMore">See more</a>
            </div>
        </article>
        <hr>
    </section>
</template>

<style scoped>
section {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
}

h3{
    flex-grow: 1.25;
}

article {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    gap: 3em;
}

div {
    display: flex;
    flex-direction: column;
    justify-content: flex-end;
}

img {
    width: 100%;
    max-width: 50em;
}

p {
    margin: 0;
}

.specs-text{
    margin-top: 1em;
}

a {
    font-weight: 600;
    text-decoration: none;
    color: var(--c-text);
    border: 3px solid var(--c-border-bottom);
    padding: 0.5em 1em;
    max-width: 8em;
    display: flex;
    justify-content: center;
    margin: 1.5em 0;
    margin-top: 1em;
}

hr {
    margin-bottom: 1.5em;
}

@media (min-width: 725px) {
    section{
        justify-content: center;
    }
    h3{
        font-size: 2em;
    }

    p{
        width: 75%;
    }

    article{
        flex-direction: row-reverse;
        align-items: flex-end;
    }

    img{
        transform: translateY(-5em);
    }

    hr{
        margin-top: 1em;
    }

    section:last-child{
        margin-bottom: 1em;
    }
}
</style>