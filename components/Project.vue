<script>
</script>

<template>
    <section class="last-section">
        <h3>Vervoerregio Amsterdam</h3>
        <article>
            <img src="/img/iPhone15pro.png" alt="iphone 15 pro project foto">
            <div>
                <p>Project for Vervoerregio Amsterdam focusing on WCAG guidelines and the specific check ups between their
                    partners.
                </p>
                <a href="/">See more</a>
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

div{
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