<template>
    <section class="skills" id="skills">
        <div class="container">
            <div class="skills__content">
                <h1 class="section__title service__title">Skills</h1>
                <div class="skills__wrap">
                    <div class="skills__top">
                        <div class="skills__color skills__red"><i class="far fa-times"></i></div>
                        <div class="skills__color skills__yellow"><i class="far fa-horizontal-rule"></i></div>
                        <div class="skills__color skills__green"><i class="far fa-expand-alt"></i></div>
                    </div>

                    <div class="skills__window">
                        <div class="skills__card">
                            <h2 class="skills_title"><i class="far fa-code"></i> Main Tools</h2>
                            <div class="skills__box">
                                <div class="skills__skill" v-for="skill in mainTools" :key="skill.id">
                                    <img :src="skill.img" alt="" class="skills__img" />
                                    <p class="skills__name">{{ skill.name }}</p>
                                    <span class="skills__des">{{ skill.des }}</span>
                                </div>
                            </div>
                        </div>

                        <div class="skills__card second__card">
                            <h2 class="skills_title"><i class="far fa-scrubber"></i> Other Tools</h2>
                            <div class="skills__box">
                                <div class="skills__skill" v-for="skill in otherTools" :key="skill.id">
                                    <img :src="skill.img" alt="" class="skills__img" />
                                    <p class="skills__name">{{ skill.name }}</p>
                                    <span class="skills__des">{{ skill.des }}</span>
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
    export default {
        data() {
            return {
                skills: skills,
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
    };
</script>

<style></style>
