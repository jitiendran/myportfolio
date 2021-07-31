<template>
    <div class="header">
        <i class="fas fa-bars" tabindex="1"></i>
        <i class="title">PortFolio</i>
        <div class="sidenav">
            <i class="fas fa-times" tabindex="1"></i>
            <a href="#home">Home</a>
            <a href="#about">About</a>
            <a href="#work">Work</a>
            <a href="#contact">Contact</a>
        </div>
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
    .fas {
        display: none;
        font-size: 2em;
        margin-left: 1em;
        position: fixed;
        background: #fff;
        padding: 0.4em 0.45em;
        border-radius: 50%;
        box-shadow: 0px 0px 5px 1px rgba(0, 0, 0, 0.2);
    }

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
    .sidenav {
        position: fixed;
        padding: 2em;
        background: #fff;
        width: 30%;
        height: 100%;
        margin-left: -30%;
        transition: all 0.4s ease-in;
        top: 0;
        box-shadow: 0px 0px 5px 5px rgba(0, 0, 0, 0.2);
        z-index: 10;
        @include smooth-font;
        @include flex(
            $direction: column,
            $align-items: center,
            $justify-content: none,
            $gap: 1.5em
        );
        .fas {
            position: absolute;
            top: 0;
            margin-top: 0.75em;
            margin-right: 0.5em;
            right: 0;
            font-size: 1.45em;
            color: $primary_color;
            box-shadow: none;
        }
        a {
            @include font(
                $font-family: $nav-font,
                $font-size: 3em,
                $font-weight: 600
            );
            @include gradient-text($background: $primary_gradient);
            @extend %links;
            &:nth-child(2) {
                margin-top: 1.2em;
            }
        }
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
    @media all and (max-width: 769px) {
        .fas {
            cursor: pointer;
            display: block;
        }
        .fas:focus ~ .sidenav {
            margin-left: 0;
        }
        .sidenav {
            .fas:focus ~ .sidenav {
                margin-left: -30%;
            }
        }
        .title {
            margin-left: 1em;
        }
        .navbar {
            display: none;
        }
    }
    @media all and (max-width: 426px) {
        .sidenav {
            width: 50%;
            margin-left: -50%;
            .fas:focus ~ .sidenav {
                margin-left: -50%;
            }
        }
    }
}
</style>
