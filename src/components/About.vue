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
                    <h2 class="about__title">Men <span>haqimda</span></h2>
                    <p class="about__text">
                        Salom, mening ismim <span>Saidaxror</span>, men 2005-yil Andijon viloyatida tavallud topganman. Bugungi kunda Front-end
                        dasturchiman.
                        <br />
                        <br />
                        Asosan bugungi kunda men UPWORK freelancing platformasida freelancer sifatida ish olib boraman va shu kungacha juda ko'plab
                        muvoffaqiyatli proektlarni o'z egalariga topshirganman!
                        <br />
                        <br />
                        Men responsive veb-saytlar, mobil ilovalar, veb ilovalar, veb komponentlar, va animatsiyalar yarataman.
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
                        <p>Ta`lim</p>
                    </div>

                    <div class="info__right">
                        <div class="info__detail">
                            <span class="info__date date__media">2023 - <i class="fal fa-hourglass-half"></i></span>
                            <div class="info__texts">
                                <p class="info__name">Samarqand Iqtisodiyot va Servis Instituti</p>
                                <p class="info__sub">Fanlar bo'yicha bakalavr, Marketing</p>
                                <p class="info__desc">
                                    Men O'zbekistonning eng yaxshi universitetlaridan biri bo'lgan Samarqand Iqtisodiyot va Servis Institutida 1-kurs talabasiman. Bu Instutda men Marketing yo'nalishi bo'yicha o'qiyman
                                </p>
                                <span class="info__date date__pc">2023 - <i class="fal fa-hourglass-half"></i></span>
                            </div>
                        </div>

                        <div class="info__detail">
                            <span class="info__date date__media">2021 - 2023</span>
                            <div class="info__texts">
                                <p class="info__name">Bo'ston Ixtisoslashtirilgan Kollej</p>
                                <p class="info__sub">Kompyuter fanlari va kompyuter muhandisligi</p>
                                <p class="info__desc">
                                    Andijon viloyatining Boston tumanidagi Chuqurlashtirilgan kollejda Kompyuter fanlari va Kompyuter muhandisligi bo'yicha barcha bilimlarni egallaganman.
                                </p>
                                <span class="info__date date__pc">2023 - current</span>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="info__card">
                    <div class="info__left">
                        <img src="@/assets/img/bag.svg" alt="" />
                        <p>Ish Tajribasi</p>
                    </div>

                    <div class="info__right">
                        <div class="info__detail">
                            <span class="info__date date__media">2023 - <i class="fal fa-hourglass-half"></i></span>
                            <div class="info__texts">
                                <p class="info__name">UPWORK</p>
                                <p class="info__sub">Front-End dasturchi</p>
                                <p class="info__desc">
                                    Bugungi kunda UPWORK platformasida freelancer sifatida faoliyat yuritaman. Shu kungacha juda ko'plab loyihalar  ustida ishlaganman va ishlayapman.
                                </p>
                                <span class="info__date date__pc">2022 current </span>
                            </div>
                        </div>

                        <div class="info__detail">
                            <span class="info__date date__media">2017 to 2019</span>
                            <div class="info__texts">
                                <p class="info__name">ASR INNOVATION CENTER</p>
                                <p class="info__sub">Grafik Dizayner</p>
                                <p class="info__desc">
                                    Asr Innavatsion O'quv markazida Grafik dizayner bo'lib ishlaganman. Juda ko'plab SMD postlarini yasaganman.
                                </p>
                                <span class="info__date date__pc">2017 to 2019</span>
                            </div>
                        </div>

                        <div class="info__detail">
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
                        </div>
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
