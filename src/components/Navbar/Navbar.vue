<template>
    <div class="header">
        <i class="title">Port<span>folio</span></i>
        <div class="navbar">
            <a href="#home">Home</a>
            <a href="#about">About</a>
            <a href="#work">Work</a>
            <a href="#contact">Contact</a>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.header {
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: space-between;
    .title {
        padding: 2em;
        font-family: Avenir, Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        font-size: 1.8em;
        font-weight: 800;
        background: linear-gradient(to right, #7f00ff, #e100ff);
        background-clip: text;
        -webkit-text-fill-color: transparent;
        span {
            color: #2c3e50 !important;
        }
    }
    .navbar {
        font-family: Avenir, Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        display: flex;
        gap: 1.5em;
        padding: 2em;
        font-size: 1.5em;
        font-weight: 600;
        a {
            color: #2c3e50;
            text-decoration: none;
            &:hover {
                text-decoration: underline;
            }
        }
    }
}
</style>
