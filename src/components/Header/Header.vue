<template>
    <div class="header">
        <Content />
    </div>
</template>

<script lang="ts">
import Content from "./Content.vue";

export default {
    components: { Content },
};
</script>

<style lang="scss" scoped>
.header {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    height: 84vh;
    .navbar {
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
}
</style>
