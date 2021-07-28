<template id="content">
    <div class="content">
        <div class="info">
            <h3>Hey There!</h3>
            <h3>I am <span id="text" class="info-text"></span></h3>
            <div class="btn-wrap">
                <button @click="goToAbout">About Me</button>
                <button @click="goToWorks">My Works</button>
            </div>
        </div>
        <div class="img">
            <div class="blob">
                <img src="../../assets/me.png" alt="My-Image" />
            </div>
        </div>
    </div>
</template>

<script lang="ts">
import { init } from "ityped";
document.onreadystatechange = () => {
    if (document.readyState === "complete") {
        const text: any = document.getElementById("text");
        init(text, {
            showCursor: false,
            strings: [
                "Jitiendran KS",
                "Currently Studing at MIT",
                "a Frontend Developer",
                " a Angular Geek",
            ],
        });
    }
};

export default {
    methods: {
        goToAbout: () => {
            window.location.hash = "about";
        },
        goToWorks: () => {
            window.location.hash = "work";
        },
    },
};
</script>

<style lang="scss" scoped>
@import "../../scss/abstract";

.content {
    display: grid;
    padding: 2em;
    grid-template-columns: repeat(2, 1fr);
    @include font(
        $font-family: $primary_font,
        $font-size: 1.1em,
        $font-weight: 600
    );
    @include smooth-font;
    .info {
        @include flex(
            $direction: column,
            $align-items: center,
            $justify-content: center,
            $gap: 0
        );
        h3 {
            @include font(
                $font-family: inherit,
                $font-size: 1.9em,
                $font-weight: 600
            );
            @include smooth-font;
            margin-bottom: 1.5em;
            .info-text {
                @include gradient-text($background: $primary_gradient);
            }
        }
        .btn-wrap {
            @include flex(
                $direction: row,
                $align-items: center,
                $justify-content: space-around,
                $gap: 0
            );
            width: 100%;
            button {
                padding: 0.5em 0.75em;
                border-radius: 0.3em;
                @include font(
                    $font-family: inherit,
                    $font-size: 1.25em,
                    $font-weight: 600
                );
                @extend %buttons;
                &:nth-child(1) {
                    background: $primary_gradient;
                    color: #fff;
                }
                &:hover {
                    transform: scale(1.03);
                }
            }
        }
    }
    .img {
        @include flex(
            $direction: row,
            $align-items: center,
            $justify-content: center,
            $gap: 0
        );
        .blob {
            background: $primary_gradient;
            border-radius: 30% 70% 70% 30% / 30% 34% 66% 70%;
            margin-top: 5em;
            width: 405px;
            height: 378px;
            display: flex;
            justify-content: center;
            img {
                margin-top: -5em;
                width: 300px;
                height: 360px;
                border-radius: 50%;
            }
        }
    }
    .typicalWrapper::after {
        content: "|";
        animation: blink 1s infinite step-start;
    }

    @keyframes blink {
        50% {
            opacity: 0;
        }
    }
}
</style>
