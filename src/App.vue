<template>
    <div class="up-wrap">
        <div class="up" @click="jump">
            <i class="fas fa-arrow-up"></i>
        </div>
    </div>
    <Navbar id="home" />
    <Header />
    <About id="about" />
</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";
import Header from "./components/Header/Header.vue";
import Navbar from "./components/Navbar/Navbar.vue";
import About from "./components/About/About.vue";
@Options({
    components: { Header, Navbar, About },
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
    }
}
</style>
