<template>
    <section class="about" id="about">
        <div class="container about__wrap">
            <div class="about__content">
                <div class="shape__blur"></div>

                <div class="about__left">
                    <div class="about__blur"></div>
                    <img src="@/assets/img/me.png" alt="" />
                </div>

                <div class="about__right">
                    <h2 class="about__title">About <span>Me</span></h2>
                    <p class="about__text">
                        Hi, my name is <span>Saidaxror</span>, I was born in Andijan Region in 2005. Nowadays, I'm front-end developer
                        <br />
                        <br />
                        Mainly, I'm working as a freelancer in UPWORK platform and handed over lots of successful projects to satisfied clients
                        <br />
                        <br />
                        With a focus on creating responsive, user-friendly websites and web applications, I bring creativity and technical expertise
                        to every project. Let's collaborate to bring your vision to life!"
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
                        <p>Education</p>
                    </div>

                    <div class="info__right">
                        <div class="info__detail">
                            <span class="info__date date__media">2023 - <i class="fal fa-hourglass-half"></i></span>
                            <div class="info__texts">
                                <p class="info__name">Institute of Economics and Service, Samarkand</p>
                                <p class="info__sub">Bachelor of Science, Marketing</p>
                                <p class="info__desc">
                                    I am a student at Institute of Economics and Service, one of the best institutes in Uzbekistan. In this institute
                                    I am studying Marketing faculty.
                                </p>
                                <span class="info__date date__pc">2023 - <i class="fal fa-hourglass-half"></i></span>
                            </div>
                        </div>

                        <div class="info__detail">
                            <span class="info__date date__media">2021 - 2023</span>
                            <div class="info__texts">
                                <p class="info__name">Boston Specialized College</p>
                                <p class="info__sub">Computer Science and Computer Engineering</p>
                                <p class="info__desc">
                                    I acquired all the knowledge in Computer Science and Computer Engineering at the Specialized College in the Boston
                                    district of Andijan region.
                                </p>
                                <span class="info__date date__pc">2023 - current</span>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="info__card">
                    <div class="info__left">
                        <img src="@/assets/img/bag.svg" alt="" />
                        <p>Work Experience</p>
                    </div>

                    <div class="info__right">
                        <div class="info__detail">
                            <span class="info__date date__media">2023 - <i class="fal fa-hourglass-half"></i></span>
                            <div class="info__texts">
                                <p class="info__name">Upwork</p>
                                <p class="info__sub">Front-End Developer</p>
                                <p class="info__desc">
                                    Today I work as a freelancer on the UPWORK platform. I have worked and am working on many projects untill now.
                                </p>
                                <span class="info__date date__pc">2023 - <i class="fal fa-hourglass-half"></i></span>
                            </div>
                        </div>

                        <div class="info__detail">
                            <span class="info__date date__media">2020 to 2022</span>
                            <div class="info__texts">
                                <p class="info__name">ASR Innovation C</p>
                                <p class="info__sub">Graphic Designer</p>
                                <p class="info__desc">
                                    I worked as a graphic designer at Asr Innovation Learning Center. I have made many SMD posts.
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
    export default {};
</script>

<style>
    .scroll-container {
        overflow-y: scroll;
        scroll-behavior: smooth;
    }
</style>
