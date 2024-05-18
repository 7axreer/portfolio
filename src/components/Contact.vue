<template>
    <section class="contact" id="contact">
        <div class="container">
            <div class="contact__content">
                <div class="contact__box">
                    <p class="contact__text" v-html="contactMe"></p>
                    <p class="contact__sub" v-html="contactDes"></p>

                    <div class="contact__form">
                        <form action="" @submit="onSubmit">
                            <div class="input__box">
                                <label for="input__name" class="contact__label">{{ langData.contactName[lang ? "en" : "ru"] }}</label>
                                <input type="text" class="contact__input input__name" placeholder="Saidaxror" />
                            </div>
                            <div class="input__box">
                                <label for="input__name" class="contact__label">{{ langData.contactNumber[lang ? "en" : "ru"] }}</label>
                                <input type="text" class="contact__input input__num" placeholder="+998 99 122 88 41" />
                            </div>
                            <div class="input__box">
                                <label for="input__name" class="contact__label">{{ langData.contactUsername[lang ? "en" : "ru"] }}</label>
                                <div class="input__username">
                                    <i class="fab fa-telegram"></i>
                                    <input type="text" class="contact__input input__user" placeholder="@username" />
                                </div>
                            </div>
                            <button class="input__button">SEND</button>
                        </form>
                    </div>
                </div>
                <div class="line"></div>

                <div class="contact__form contact__media">
                    <form action="" @submit="onSubmit">
                        <div class="input__box">
                            <label for="input__name" class="contact__label">{{ langData.contactName[lang ? "en" : "ru"] }}</label>
                            <input type="text" class="contact__input input__name" placeholder="Saidaxror" />
                        </div>
                        <div class="input__box">
                            <label for="input__name" class="contact__label">{{ langData.contactNumber[lang ? "en" : "ru"] }}</label>
                            <input type="text" class="contact__input input__num" placeholder="+998 99 122 88 41" />
                        </div>
                        <div class="input__box">
                            <label for="input__name" class="contact__label">{{ langData.contactUsername[lang ? "en" : "ru"] }}</label>
                            <div class="input__username">
                                <i class="fab fa-telegram"></i>
                                <input type="text" class="contact__input input__user" placeholder="@username" />
                            </div>
                        </div>
                        <button class="input__button">SEND</button>
                    </form>
                </div>

                <div class="contact__details">
                    <ul class="contact__nums">
                        <li>+998 99 122 88 41</li>
                        <li>+998 94 006 88 41</li>
                        <li>saidaxororpc7@gmail.com</li>
                    </ul>
                    <ul class="contact__list">
                        <li>
                            <a href="#about" class="contact__link"><i class="fas fa-user"></i></a>
                        </li>
                        <li>
                            <a href="#project" class="contact__link"><i class="fas fa-tasks"></i></a>
                        </li>
                        <li>
                            <a href="#service" class="contact__link"><i class="fas fa-laptop-code"></i></a>
                        </li>
                        <li>
                            <a href="#skills" class="contact__link"><i class="fas fa-code"></i></a>
                        </li>
                        <li>
                            <a href="#contact" class="contact__link"><i class="fas fa-inbox-out"></i></a>
                        </li>
                    </ul>
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
        methods: {
            onSubmit(e) {
                e.preventDefault();
            },
        },
        computed: {
            contactMe() {
                return this.lang ? this.langData.contactMe.en : this.langData.contactMe.ru;
            },
            contactDes() {
                return this.lang ? this.langData.contactDes.en : this.langData.contactDes.ru;
            },
        },
    };
</script>

<style></style>
