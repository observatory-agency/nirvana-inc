<template>
    <div>
        <MainNav />
        <Nuxt />
        <Footer />
    </div>
</template>

<style>
:focus:not(:focus-visible) {
    outline: none;
}

html {
    font-family: 'Poppins', sans-serif;
    scroll-behavior: smooth;
}

.content-wrapper {
    width: 94vw;
    width: clamp(16rem, 94vw, 80rem);
    margin-left: auto;
    margin-right: auto;
    position: relative;
}
</style>
