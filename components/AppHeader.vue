<template>
    <header>
        <nav>
            <NuxtLink to="#home">Tolga</NuxtLink>
            <NuxtLink to="#projects">Projects</NuxtLink>
            <span>2023</span>
        </nav>
    </header>
</template>

<style scoped>
    header{
        padding-top: 1.5em;
        padding-bottom: 1em;
        border-bottom: 3px solid var(--c-border-bottom);
        width: 100%;
    }

    nav{
        display: flex;
        justify-content: space-between;
        font-size: 1.25em;
    }

    a{
        text-decoration: none;
        color: var(--c-text);
        font-weight: 400;
    }
</style>