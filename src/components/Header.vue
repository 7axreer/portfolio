<template>
    <nav class="nav">
        <div class="container">
            <div class="nav__content">
                <a href="/" class="nav__logo">
                    <!-- {{ langData.portfolio[lang ? "en" : "ru"] }} -->
                    <img src="@/assets/img/icon.svg" alt="" />
                </a>

                <ul class="nav__list" :class="{ active: isActive }">
                    <li>
                        <a href="#about" class="nav__link" @click="showNav">{{ langData.about[lang ? "en" : "ru"] }}</a>
                    </li>
                    <li>
                        <a href="#project" class="nav__link" @click="showNav">{{ langData.project[lang ? "en" : "ru"] }}</a>
                    </li>
                    <li>
                        <a href="#service" class="nav__link" @click="showNav">{{ langData.service[lang ? "en" : "ru"] }}</a>
                    </li>
                    <li>
                        <a href="#skills" class="nav__link" @click="showNav">{{ langData.skills[lang ? "en" : "ru"] }}</a>
                    </li>
                    <li>
                        <a href="#contact" class="nav__link" @click="showNav">{{ langData.contact[lang ? "en" : "ru"] }}</a>
                    </li>

                    <div class="nav__lang">
                        <button class="lang" @click="toggleLanguage">
                            {{ lang ? "EN" : "RU" }}
                            <img class="lang__img" src="@/assets/img/us.svg" alt="" v-if="lang" />
                            <img class="lang__img" src="@/assets/img/ru.svg" alt="" v-else />
                        </button>
                    </div>
                </ul>

                <button class="hamburger" @click="showNav">
                    <i class="far fa-bars"></i>
                </button>

                <div class="overlay" @click="showNav" :class="{ active: isActive }"></div>
            </div>
        </div>
    </nav>

    <header class="header" id="header">
        <div class="header__shadow"></div>
        <div class="container wrap">
            <div class="header__content">
                <div class="header__left">
                    <h1 class="header__title">
                        <span>{{ langData.im[lang ? "en" : "ru"] }}</span> <br />
                        {{ langData.frontEnd[lang ? "en" : "ru"] }} <br />
                        {{ langData.developer[lang ? "en" : "ru"] }}.
                    </h1>
                    <a href="/cv.pdf" download="Sobirov Saidaxror - CV" class="header__btn">
                        {{ langData.download[lang ? "en" : "ru"] }}
                        <i class="far fa-arrow-to-bottom"></i>
                    </a>
                </div>
                <div class="header__right">
                    <img src="@/assets/img/Saidaxror.jpg" alt="" />
                </div>
            </div>
        </div>
        <div class="bottom__shadow"></div>
    </header>
</template>

<script>
    import langData from "@/lang.js";
    export default {
        data() {
            return {
                isActive: false,
                lang: true,
                langData: langData,
            };
        },
        methods: {
            showNav() {
                this.isActive = !this.isActive;
            },
            toggleLanguage() {
                this.lang = !this.lang;
                this.$emit("toggle-language");
            },
        },
    };
</script>

<style>
    .hamburger {
        font-size: 21px;
        display: none;
    }

    nav {
        padding: 20px 0;
        width: 100%;
        position: fixed;
        z-index: 100;
        box-shadow: 1px 5px 5px rgba(0, 0, 0, 0.02);
        background: var(--white-color);

        background: rgba(255, 255, 255, 0.719);
        box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
        backdrop-filter: blur(16px);
        -webkit-backdrop-filter: blur(16px);
    }

    .nav__content {
        display: flex;
        align-items: center;
        justify-content: space-between;
    }

    @keyframes logoAnime {
        0% {
            transform: translateY(0);
        }
        50% {
            transform: translateY(5px);
        }
        0% {
            transform: translateY(0);
        }
    }

    .nav__logo {
        font-size: 21px;
        font-family: var(--openSemiBold);
        color: var(--second-color);
        animation: logoAnime 2s infinite linear;
    }

    .nav__logo > img {
        width: 35px;
    }

    .nav__list {
        display: flex;
        align-items: center;
        gap: 40px;
        padding: 5px 0;
    }

    .nav__link {
        color: var(--second-color);
        font-size: 18px;
    }

    .lang {
        width: 62px;
        font-size: 16px;
        padding: 5px;
        border-radius: 5px;
        transition: 0.3s;
        display: flex;
        align-items: center;
        justify-content: space-between;
        gap: 5px;
    }

    .lang > img {
        width: 25px;
    }

    .lang:hover {
        background: var(--second-color);
        color: var(--white-color);
    }

    .lang__select {
        border: none;
        outline: none;
        font-family: var(--openSemiBold);
        font-size: 16px;
        background: none;
    }
</style>
