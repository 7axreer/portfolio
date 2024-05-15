<template>
    <section class="project" id="project">
        <div class="container wrap">
            <div class="project__content">
                <h2 class="section__title">My Projects</h2>

                <Swiper
                    class="project__cards swiper"
                    :space-between="30"
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
                    <SwiperSlide class="project__card swiper-slide">
                        <div class="project__img">
                            <img src="@/assets/img/robot.svg" alt="" />
                        </div>
                        <div class="project__info">
                            <span class="project__des">Website</span>
                            <p class="project__name">robo.uz</p>
                        </div>
                        <a href="" class="project__btn"> See Project <i class="far fa-external-link"></i> </a>
                    </SwiperSlide>

                    <SwiperSlide class="project__card swiper-slide">
                        <div class="project__img">
                            <img src="@/assets/img/huawei.png" alt="" />
                        </div>
                        <div class="project__info">
                            <span class="project__des">Website</span>
                            <p class="project__name">heawei.com</p>
                        </div>
                        <a href="" class="project__btn"> See Project <i class="far fa-external-link"></i> </a>
                    </SwiperSlide>

                    <SwiperSlide class="project__card swiper-slide">
                        <div class="project__img">
                            <img src="@/assets/img/dji.svg" alt="" />
                        </div>
                        <div class="project__info">
                            <span class="project__des">Website</span>
                            <p class="project__name">dji.com</p>
                        </div>
                        <a href="" class="project__btn"> See Project <i class="far fa-external-link"></i> </a>
                    </SwiperSlide>

                    <SwiperSlide class="project__card swiper-slide">
                        <div class="project__img">
                            <img src="@/assets/img/mcdonalds.svg" alt="" />
                        </div>
                        <div class="project__info">
                            <span class="project__des">Website</span>
                            <p class="project__name">mcdonalds.com</p>
                        </div>
                        <a href="" class="project__btn"> See Project <i class="far fa-external-link"></i> </a>
                    </SwiperSlide>

                    <SwiperSlide class="project__card swiper-slide">
                        <div class="project__img">
                            <img src="@/assets/img/burger-king.svg" alt="" />
                        </div>
                        <div class="project__info">
                            <span class="project__des">Website</span>
                            <p class="project__name">burgerking.com</p>
                        </div>
                        <a href="" class="project__btn"> See Project <i class="far fa-external-link"></i> </a>
                    </SwiperSlide>

                    <SwiperSlide class="project__card swiper-slide">
                        <div class="project__img">
                            <img src="@/assets/img/toyota.svg" alt="" />
                        </div>
                        <div class="project__info">
                            <span class="project__des">Website</span>
                            <p class="project__name">toyota.com</p>
                        </div>
                        <a href="" class="project__btn"> See Project <i class="far fa-external-link"></i> </a>
                    </SwiperSlide>

                    <SwiperSlide class="project__card swiper-slide">
                        <div class="project__img">
                            <img src="@/assets/img/adobe.jpg" alt="" />
                        </div>
                        <div class="project__info">
                            <span class="project__des">Website</span>
                            <p class="project__name">adobe.com</p>
                        </div>
                        <a href="" class="project__btn"> See Project <i class="far fa-external-link"></i> </a>
                    </SwiperSlide>

                    <SwiperSlide class="project__card swiper-slide">
                        <div class="project__img">
                            <img src="@/assets/img/disney.jpg" alt="" />
                        </div>
                        <div class="project__info">
                            <span class="project__des">Website</span>
                            <p class="project__name">disney.com</p>
                        </div>
                        <a href="" class="project__btn"> See Project <i class="far fa-external-link"></i> </a>
                    </SwiperSlide>
                </Swiper>

                <div class="project__swipe">
                    <p>Swipe to see other projects</p>
                    <img src="@/assets/img/swipe.png" alt="" />
                </div>
            </div>
        </div>
    </section>
</template>

<script>
    import { Swiper, SwiperSlide } from "swiper/vue";
    import { Navigation } from "swiper/modules";
    import "swiper/css/navigation";
    import "swiper/css";

    export default {
        components: {
            Swiper,
            SwiperSlide,
        },
        setup() {
            return {
                modules: [Navigation],
            };
        },
    };
</script>

<style>
    .swiper {
        width: 865px;
        padding: 20px;
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
    }

    .swiper-button-prev::after,
    .swiper-button-next::after {
        font-size: 20px;
        font-weight: bold;
    }
</style>
