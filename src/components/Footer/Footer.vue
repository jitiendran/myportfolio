<template>
    <div class="footer" id="contact">
        <h3>Contact</h3>
        <div class="underline"></div>
        <div class="content">
            <h3>Wanna Contact me ?</h3>
            <p>Feel free to write a feedback to jitiendranjiji2000@gmail.com</p>
            <div class="icon-wrap">
                <a
                    class="icon"
                    href="https://github.com/jitiendran"
                    target="_blank"
                    ><i class="fab fa-github"></i> Github</a
                >
                |
                <a
                    class="icon"
                    href="https://www.instagram.com/jitiendran_ks/"
                    target="_blank"
                    ><i class="fab fa-instagram"></i> Instagram</a
                >
                |
                <a
                    class="icon"
                    href="https://www.linkedin.com/in/jitiendran-ks-7087811a5/"
                    target="_blank"
                    ><i class="fab fa-linkedin"></i> Linkedin</a
                >
            </div>
            <div class="copywright">
                copyright <i class="far fa-copyright"></i> Jitiendran
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@import "../../scss/abstract";
.footer {
    padding: 1em;
    @include flex(
        $direction: column,
        $align-items: center,
        $justify-content: center,
        $gap: 1em
    );
    h3 {
        @include font(
            $font-family: $nav_font,
            $font-size: 4.5em,
            $font-weight: 800
        );
    }
    .underline {
        height: 2.4px;
        width: 6em;
        background: $grey;
    }
    .content {
        @include flex(
            $direction: column,
            $align-items: center,
            $justify-content: center,
            $gap: 1em
        );
        h3 {
            font-size: 2em;
            font-weight: 600;
            font-family: $primary_font;
        }
        p {
            font-family: $primary_font;
            font-size: 1.4em;
            margin-bottom: 1em;
        }
        .icon-wrap {
            display: flex;
            align-items: center;
            gap: 1em;
            font-family: $primary_font;
            font-size: 1.3em;
            a {
                @extend %links;
                color: #000;
            }
        }
        .copywright {
            margin-top: 1em;
            font-family: $primary_font;
            font-size: 1.2em;
            font-weight: 600;
        }
    }
}
</style>
