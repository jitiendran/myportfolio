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
@import "../../scss/abstract";

.header {
    height: 84vh;
    .navbar {
        padding: 2em;
        margin: auto;
        @include flex(
            $direction: row,
            $align-items: center,
            $justify-content: flex-end,
            $gap: 1.5em
        );
    }

    @media all and (max-width: 769px) {
        width: 100%;
        height: 100%;
    }
}
</style>
