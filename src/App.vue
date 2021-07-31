<template>
    <div id="home">
        <div class="up-wrap">
            <div class="up" @click="jump">
                <i class="fas fa-arrow-up"></i>
            </div>
        </div>
        <Navbar />
        <Header />
        <About />
        <Works />
        <Footer />
    </div>
</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";
import Header from "./components/Header/Header.vue";
import Navbar from "./components/Navbar/Navbar.vue";
import About from "./components/About/About.vue";
import Works from "./components/Works/Works.vue";
import Footer from "./components/Footer/Footer.vue";

@Options({
    components: { Header, Navbar, About, Works, Footer },
})
export default class App extends Vue {
    jump(): void {
        window.location.hash = "";
        window.location.hash = "home";
    }
}
</script>

<style lang="scss">
.up-wrap {
    float: right;
    bottom: 0;
    left: 90%;
    position: fixed;
    font-size: 1.5em;
    padding: 0.5em;
    z-index: 10;
    .up {
        width: 40px;
        height: 40px;
        cursor: pointer;
        background: linear-gradient(to right, #7f00ff, #e100ff);
        border-radius: 50%;
        display: flex;
        align-items: center;
        justify-content: center;
        color: #fff;
        box-shadow: 1px 1px 15px 6px #fff;
    }
    @media all and (max-width: 769px) {
        width: 113%;
    }
    @media all and (max-width: 426px) {
        width: 169.5%;
    }
    @media all and (max-width: 376px) {
        width: 179.2%;
    }
    @media all and (max-width: 321px) {
        width: 201.5%;
    }
}
</style>
