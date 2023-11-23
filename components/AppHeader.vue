<script>
import { gsap } from "gsap";

export default {
    mounted() {
        gsap.fromTo(".anchor-tolga", { opacity: 0, yPercent: 100 }, { opacity: 1, yPercent: 0, duration: 0.5})
        gsap.fromTo(".anchor-projects", { opacity: 0, yPercent: 100 }, { opacity: 1, yPercent: 0, duration: 0.5, delay: 0.5})
        gsap.fromTo(".span-2023", { opacity: 0, yPercent: 100 }, { opacity: 1, yPercent: 0, duration: 0.5, delay: 1})
    }
}
</script>

<template>
    <header>
        <nav>
            <NuxtLink class="anchor-tolga" to="#home">Tolga</NuxtLink>
            <NuxtLink class="anchor-projects" to="#projects">Projects</NuxtLink>
            <span class="span-2023">2023</span>
        </nav>
    </header>
</template>

<style scoped>
header {
    padding-top: 1.5em;
    padding-bottom: 1em;
    border-bottom: 3px solid var(--c-border-bottom);
    width: 100%;
}

nav {
    display: flex;
    justify-content: space-between;
    font-size: 1.25em;
}

a {
    text-decoration: none;
    color: var(--c-text);
    font-weight: 400;
}
</style>