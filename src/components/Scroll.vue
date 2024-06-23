<template>
    <section class="scrollUp" :class="{ 'scrollUp__visible': hidden }">
        <button class="scrollUp__button" @click="scrollToTop"><i class="far fa-chevron-up"></i></button>
    </section>
</template>

<script>
    export default {
        data() {
            return {
                hidden: false,
            };
        },
        methods: {
            handleScroll() {
                this.hidden = window.scrollY > 600;
            },
            scrollToTop() {
                window.scrollTo({
                    top: 0,
                    behavior: "smooth",
                });
            },
        },
        mounted() {
            window.addEventListener("scroll", this.handleScroll);
        },
        beforeDestroy() {
            window.removeEventListener("scroll", this.handleScroll);
        },
    };
</script>

<style scoped>
    
</style>
