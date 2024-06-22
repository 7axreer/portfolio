<template>
    <section class="about" id="about">
        <div class="container about__wrap">
            <div class="about__content">
                <div class="shape__blur"></div>

                <div class="about__left">
                    <img src="@/assets/img/Saidaxror.jpg" alt="" />
                    <div class="about__blur"></div>
                </div>

                <div class="about__right">
                    <h2 class="about__title">
                        {{ langData.aboutMe[lang ? "en" : "ru"] }} <span>{{ langData.aboutMeMe[lang ? "en" : "ru"] }}</span>
                    </h2>
                    <p class="about__text">
                        {{ langData.aboutMeTextFirst[lang ? "en" : "ru"] }}
                        <br />
                        <br />
                        {{ langData.aboutMeTextSecond[lang ? "en" : "ru"] }}
                        <br />
                        <br />
                        {{ langData.aboutMeTextThird[lang ? "en" : "ru"] }}
                    </p>
                </div>
            </div>
        </div>
    </section>
    <!-- <hr/> -->
    <section class="info">
        <div class="container wrap">
            <div class="info__content">
                <div class="info__card">
                    <div class="info__left">
                        <img src="@/assets/img/books.svg" alt="" />
                        <p> {{ langData.education[lang ? "en" : "ru"] }}</p>
                    </div>

                    <div class="info__right">
                        <div class="info__detail">
                            <span class="info__date date__media">2023 - <i class="fal fa-hourglass-half"></i></span>
                            <div class="info__texts">
                                <p class="info__name"> {{ langData.institute[lang ? "en" : "ru"] }}</p>
                                <p class="info__sub">{{ langData.instituteFac[lang ? "en" : "ru"] }}</p>
                                <p class="info__desc">
                                    {{ langData.instituteDes[lang ? "en" : "ru"] }}
                                </p>
                                <span class="info__date date__pc">2023 - <i class="fal fa-hourglass-half"></i></span>
                            </div>
                        </div>

                        <div class="info__detail">
                            <span class="info__date date__media">2021 - 2023</span>
                            <div class="info__texts">
                                <p class="info__name">  {{ langData.collage[lang ? "en" : "ru"] }}</p>
                                <p class="info__sub">  {{ langData.collageFac[lang ? "en" : "ru"] }}</p>
                                <p class="info__desc">
                                     {{ langData.collageDes[lang ? "en" : "ru"] }}
                                </p>
                                <span class="info__date date__pc">2021 to 2023</span>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="info__card">
                    <div class="info__left">
                        <img src="@/assets/img/bag.svg" alt="" />
                        <p>{{ langData.work[lang ? "en" : "ru"] }}</p>
                    </div>

                    <div class="info__right">
                        <div class="info__detail">
                            <span class="info__date date__media">2023 - <i class="fal fa-hourglass-half"></i></span>
                            <div class="info__texts">
                                <p class="info__name">  {{ langData.upwork[lang ? "en" : "ru"] }}</p>
                                <p class="info__sub">{{ langData.upworkInfo[lang ? "en" : "ru"] }}</p>
                                <p class="info__desc">
                                   {{ langData.upworkDes[lang ? "en" : "ru"] }}
                                </p>
                                <span class="info__date date__pc">2023 - <i class="fal fa-hourglass-half"></i></span>
                            </div>
                        </div>

                        <div class="info__detail">
                            <span class="info__date date__media">2020 to 2022</span>
                            <div class="info__texts">
                                <p class="info__name">{{ langData.asr[lang ? "en" : "ru"] }}</p>
                                <p class="info__sub">{{ langData.asrInfo[lang ? "en" : "ru"] }}</p>
                                <p class="info__desc">
                                    {{ langData.asrDes[lang ? "en" : "ru"] }}
                                </p>
                                <span class="info__date date__pc">2020 to 2022</span>
                            </div>
                        </div>

                        <!-- <div class="info__detail">
                            <span class="info__date date__media">2015 to 2016</span>
                            <div class="info__texts">
                                <p class="info__name">Codesign</p>
                                <p class="info__sub">Web Manager</p>
                                <p class="info__desc">
                                    Lorem Ipsum is simply dummy text of the printing and. Lorem Ipsum has been the industry's standard dummy text
                                    unknown printer took a galley centuries,
                                </p>
                                <span class="info__date date__pc">2015 to 2016</span>
                            </div>
                        </div> -->
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
import langData from "@/lang.js";

export default {
    props: {
        lang: {
            type: Boolean,
            required: true,
        },
    },
    data() {
        return {
            langData: langData,
        };
    },
};
</script>

<style>
.scroll-container {
    overflow-y: scroll;
    scroll-behavior: smooth;
}
</style>
