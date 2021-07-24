<template id="content">
    <div class="content">
        <div class="info">
            <h3>Hey There!</h3>
            <h3>I am <span id="text" class="info-text"></span></h3>
            <div class="btn-wrap">
                <button>About Me</button>
                <button>My Works</button>
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

export default {};
</script>

<style lang="scss" scoped>
.content {
    display: grid;
    padding: 2em;
    grid-template-columns: repeat(2, 1fr);
    .info {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        h3 {
            font-size: 2.2em;
            font-weight: 600;
            .info-text {
                background: linear-gradient(to right, #7f00ff, #e100ff);
                background-clip: text;
                -webkit-text-fill-color: transparent;
            }
            margin-bottom: 1.5em;
        }
        .btn-wrap {
            display: flex;
            align-items: center;
            justify-content: space-around;
            width: 100%;
            button {
                outline: none;
                border: none;
                padding: 0.5em 0.75em;
                border-radius: 0.3em;
                font-weight: 600;
                font-size: 1.3em;
                cursor: pointer;
                &:nth-child(1) {
                    background: linear-gradient(to right, #7f00ff, #e100ff);
                    color: #fff;
                }
                &:hover {
                    transform: scale(1.03);
                }
            }
        }
    }
    .img {
        display: flex;
        align-items: center;
        justify-content: center;
        .blob {
            background: linear-gradient(to right, #7f00ff, #e100ff);
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
