<template>
    <div
        class="min-h-scrren w-full container-background"
        :style="{ backgroundImage: 'url(' + require('@/assets/image-hero-desktop.jpg') + ')' }"
    >
        <div id="app" class="min-h-screen flex flex-col items-center">
            <Nav />
            <Crowdfunding />
        </div>
    </div>
</template>

<script>
import Nav from "./components/Nav.vue";
import Crowdfunding from "./components/Crowdfunding.vue";

export default {
    name: "App",
    components: { Nav, Crowdfunding },
}
</script>

<style>
.container-background {
    background-repeat: no-repeat;
    background-size: 100vw auto;
    position: relative;
}

.container-background::after {
    content: "";
    display: block;
    background: linear-gradient(rgba(0, 0, 0, 0.384), rgba(255, 255, 255, 0));
    width: 100%;
    height: calc(100vw / 3.6);
    position: absolute;
    top: 0;
    margin: 0;
}

#app {
    position: relative;
    color: white;
    z-index: 1000 !important;
}

html,
body {
    font-family: "Commissioner", sans-serif !important;
    background-color: #fafafa;
}
</style>
