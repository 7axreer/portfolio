<template>
    <Header :navScroll="scrollToElement" />
    <Social />
    <About ref="scrollToElementRef" />
    <Project ref="scrollToProjectRef" />
    <Service />
    <Skills />
</template>


<script>
import SmoothScroll from "smooth-scroll";

const scroll = new SmoothScroll();

import Header from "@/components/Header.vue";
import Social from "@/components/Social.vue";
import About from "@/components/About.vue";
import Project from "@/components/Project.vue";
import Service from "@/components/Service.vue";
import Skills from "@/components/Skills.vue";

import Lenis from "lenis";

// const lenis = new Lenis({
//     duration: 3,
//     easing: (t) => Math.min(1, 1.001 - Math.pow(2, -10 * t)),
// });

// function raf(time) {
//     lenis.raf(time);
//     requestAnimationFrame(raf);
// }

// requestAnimationFrame(raf);

export default {
    components: {
        Header,
        Social,
        About,
        Project,
        Service,
        Skills,
    },
    data() {
        return {};
    },
    // methods: {
    //     scrollToElement(e) {
    //       console.log(`scroll.animateScroll(${e});`);
    //         const scroll = new SmoothScroll();
    //         const element = this.$refs.scrollToElementRef?.$el.nextElementSibling;
    //         const project = this.$refs.scrollToProjectRef?.$el;

    //         scroll.animateScroll(e);

    //         if (e == 'element') {
    //             scroll.animateScroll(element);
    //         } else if (e == 'project') {
    //             scroll.animateScroll(project);
    //         } else if (e == 'project') {
    //             scroll.animateScroll(project);
    //         }
    //     },
    // },

    //  @click="navScroll('element')"
    //   @click="navScroll('project')"
    // @click="navScroll('project')"
};
</script>

<style></style>
