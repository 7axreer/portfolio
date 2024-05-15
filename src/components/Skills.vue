<template>
    <section class="skills" id="skills">
        <div class="container">
            <div class="skills__content">
                <h1 class="section__title service__title">Skills</h1>
                <div class="skills__wrap">
                    <div class="skills__top">
                        <div class="skills__color skills__red"></div>
                        <div class="skills__color skills__yellow"></div>
                        <div class="skills__color skills__green"></div>
                    </div>
                    <div class="skills__window">
                        <div class="skills__box">
                            <div class="skills__skill" v-for="skill in skills" :key="skill.id">
                                <img :src="skill.img" alt="" class="skills__img" />
                                <p class="skills__name">{{ skill.name }}</p>
                                <span class="skills__des">{{ skill.des }}</span>
                            </div>
                        </div>
                        <div class="skills__box">
                            <div class="skills__skill" v-for="skill in skills" :key="skill.id">
                                <img :src="skill.img" alt="" class="skills__img" />
                                <p class="skills__name">{{ skill.name }}</p>
                                <span class="skills__des">{{ skill.des }}</span>
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
export default {
    data() {
        return {
            skills: skills,
        };
    },
};
</script>

<style></style>
