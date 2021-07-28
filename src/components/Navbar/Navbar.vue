<template>
    <div class="header">
        <i class="title">PortFolio</i>
        <div class="navbar">
            <a href="#home">Home</a>
            <a href="#about">About</a>
            <a href="#work">Work</a>
            <a href="#contact">Contact</a>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@import "../../scss/abstract";

.header {
    width: 100%;
    position: relative;
    top: 4em;
    margin-bottom: 7em;
    user-select: none;
    @include flex(
        $direction: row,
        $align-items: center,
        $justify-content: none,
        $gap: 0
    );

    .title {
        left: 0;
        padding: 0.3em;
        position: absolute;
        @include font(
            $font-family: $title-cursive,
            $font-size: 6em,
            $font-weight: 800
        );
        @include smooth-font;
        @include gradient-text($background: $primary_gradient);
    }
    .navbar {
        position: absolute;
        padding: 0em 1em;
        right: 0;
        @include smooth-font;
        @include flex(
            $direction: row,
            $align-items: center,
            $justify-content: none,
            $gap: 1.5em
        );
        @include font(
            $font-family: $nav-font,
            $font-size: 3.4em,
            $font-weight: 600
        );
        a {
            color: $primary_color;
            @extend %links;
        }
    }
}
</style>
