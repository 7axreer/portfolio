<template>
    <section class="project" id="project">
        <div class="container wrap">
            <div class="project__content">
                <h2 class="section__title">{{ langData.projectSec[lang ? "en" : "ru"] }}</h2>

                <Swiper
                    class="project__cards swiper"
                    :space-between="30"
                    :autoplay="{
                        delay: 2500,
                        disableOnInteraction: false,
                    }"
                    :navigation="true"
                    :modules="modules"
                    centeredSlides
                    :grab-cursor="true"
                    :loop="true"
                    :breakpoints="{
                        815: {
                            slidesPerView: 2.5,
                        },
                    }">

                    <SwiperSlide class="project__card swiper-slide" v-for="project in projects" :key="project">
                        <div class="project__img">
                            <img :src="project.img" alt="" />
                        </div>
                        <div class="project__info">
                            <span class="project__des">{{ lang ? project.des.en : project.des.ru}}</span>
                            <p class="project__name">{{ project.name }}</p>
                        </div>
                        <a href="" class="project__btn"> {{ langData.projectBtn[lang ? "en" : "ru"] }} <i class="far fa-external-link"></i> </a>
                    </SwiperSlide>
                    
                </Swiper>
            </div>
        </div>
    </section>
</template>

<script>
    import skills from "@/data";
    import langData from "@/lang.js";
    import { Swiper, SwiperSlide } from "swiper/vue";
    import { Navigation, Autoplay } from "swiper/modules";
    import "swiper/css/navigation";
    import "swiper/css";
    export default {
        props: {
            lang: {
                type: Boolean,
                required: true,
            },
        },
        components: {
            Swiper,
            SwiperSlide,
        },
        setup() {
            return {
                modules: [Navigation, Autoplay],
            };
        },
        data() {
            return {
                skills: skills,
                langData: langData,
            };
        },
        computed: {
            projects() {
                return this.skills.filter((skill) => [11, 12, 13, 14, 16, 17].includes(skill.id));
            },

        }
    };
</script>

<style>
    .swiper {
        width: 865px;
        padding: 20px;
        position: relative;
    }

    .swiper-button-prev,
    .swiper-button-next {
        color: #000000;
        background: rgba(255, 255, 255, 0.41);
        box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
        backdrop-filter: blur(3px);
        -webkit-backdrop-filter: blur(3px);
        border-radius: 5px;
        padding: 10px;
        width: 40px;
        height: 40px;
        display: grid;
        place-items: center;
        position: absolute;
    }

    .swiper-button-prev::after,
    .swiper-button-next::after {
        font-size: 20px;
        font-weight: bold;
    }
</style>
