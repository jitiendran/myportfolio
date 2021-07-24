<template>
    <div class="up">
        up
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
export default class App extends Vue {}
</script>

<style lang="scss">
.up {
    float: right;
    bottom: 0;
    left: 90%;
    position: fixed;
    font-size: 1.5em;
}
</style>
