<template>
    <div class="works" id="work">
        <h3>Projects and Works</h3>
        <div class="underline"></div>
        <div class="content">
            <h3>Wanna see my Projects ?</h3>
            <p>
                I have worked on many Small and Big Projects, and I am a member
                of Datacenter team in my Department at College working as
                Frontend(Angular) Developer. Check out my page to view all my
                projects and works.
            </p>
            <a
                href="https://github.com/jitiendran?tab=repositories"
                target="_blank"
                ><i class="fab fa-github"></i> View My Projects</a
            >
        </div>
    </div>
</template>

<style lang="scss" scoped>
@import "../../scss/abstract";
.works {
    background: $primary_gradient;
    height: 100vh;
    @include flex(
        $direction: column,
        $align-items: center,
        $justify-content: center,
        $gap: 1em
    );
    color: $white;
    h3 {
        @include font(
            $font-family: $primary_font,
            $font-size: 2em,
            $font-weight: 600
        );
    }
    .underline {
        height: 2.4px;
        width: 10em;
        background: $white;
    }
    .content {
        padding: 3em 25em;
        text-align: center;
        @include smooth-font;
        h3 {
            font-size: 1.7em;
        }
        p {
            margin-top: 1em;
            font-family: $primary_font;
            font-size: 1.4em;
            margin-bottom: 2em;
        }
        a {
            i {
                font-size: 1.2em;
                margin-right: 0.5em;
            }
            font-family: $primary_font;
            font-weight: 600;
            padding: 0.5em 1em;
            font-size: 1.4em;
            border-radius: 0.3em;
            background: $white;
            text-decoration: none;
            color: #000;
        }
    }
    @media all and (max-width: 769px) {
        font-size: 0.9em;
        width: 100%;
        .content {
            padding: 1.25em;
        }
    }
}
</style>
