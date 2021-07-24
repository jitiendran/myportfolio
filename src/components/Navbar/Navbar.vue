<template>
    <div class="navbar">
        <a href="#home">Home</a>
        <a href="#about">About</a>
        <a href="#work">Work</a>
        <a href="#contact">Contact</a>
    </div>
</template>

<style lang="scss" scoped>
.navbar {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    display: flex;
    justify-content: flex-end;
    gap: 1.5em;
    padding: 2em;
    font-size: 1.5em;
    font-weight: 600;
    margin: auto;
    a {
        color: #2c3e50;
        text-decoration: none;
        &:hover {
            text-decoration: underline;
        }
    }
}
</style>
