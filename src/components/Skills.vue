<template>

    <section class="skills" id="skills">
        <div class="container">
            <div class="skills__content">
                <h1 class="section__title service__title">{{langData.skillsSec[lang ? 'en' : 'ru']}}</h1>
                <div class="skills__wrap">
                    <div class="skills__top">
                        <div class="skills__color skills__red" @click="none"><i class="far fa-times"></i></div>
                        <div class="skills__color skills__yellow" @click="addActive"><i class="far fa-horizontal-rule"></i></div>
                        <div class="skills__color skills__green" @click="removeActive"><i class="far fa-expand-alt"></i></div>
                    </div>

                    <div class="skills__window" :class="touch ? 'showSkills' : ''">
                        <div class="skills__card">
                            <h2 class="skills_title"><i class="far fa-code"></i>{{langData.skillsTitle[lang ? 'en' : 'ru']}}</h2>
                            <div class="skills__box">
                                <div class="skills__skill" v-for="skill in mainTools" :key="skill.id">
                                    <img :src="skill.img" alt="" class="skills__img" />
                                    <p class="skills__name">{{ skill.name }}</p>
                                    <span class="skills__des">{{ lang ? skill.des.en : skill.des.ru}}</span>
                                </div>
                            </div>
                        </div>

                        <div class="skills__card second__card">
                            <h2 class="skills_title"><i class="far fa-scrubber"></i> {{langData.skillsTitleSecond[lang ? 'en' : 'ru']}}</h2>
                            <div class="skills__box">
                                <div class="skills__skill" v-for="skill in otherTools" :key="skill.id">
                                    <img :src="skill.img" alt="" class="skills__img" />
                                    <p class="skills__name">{{ skill.name }}</p>
                                    <span class="skills__des">{{ lang ? skill.des.en : skill.des.ru}}</span>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
</template>

<script>
    import skills from "@/data";
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
                skills: skills,
                touch: false,
                langData: langData,
            };
        },
        computed: {
            mainTools() {
                return this.skills.filter((skill) => [1, 2, 3, 4, 6, 7].includes(skill.id));
            },
            otherTools() {
                return this.skills.filter((skill) => [5, 8, 9, 10].includes(skill.id));
            },
        },

        methods: {
            addActive() {
                this.touch = true;
            },
            removeActive() {
                this.touch = false;
            },
        },
    };
</script>

<style>
    .showSkills {
        height: 0;
        overflow: hidden;
    }

    .none {
        height: 100%;
    }
</style>
