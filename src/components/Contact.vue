<template>
    <section class="contact" id="contact">
        <div class="container">
            <div class="contact__content">
                <div class="contact__box">
                    <p class="contact__text">CONTACT <span>ME*</span></p>
                    <p class="contact__sub">Please enter you informations correctly and we will cantact you <span>as soon as possible</span> :)</p>

                    <div class="contact__form">
                        <form action="" @submit="onSubmit">
                            <div class="input__box">
                                <label for="input__name" class="contact__label">Name</label>
                                <input type="text" class="contact__input input__name" placeholder="Saidaxror" />
                            </div>
                            <div class="input__box">
                                <label for="input__name" class="contact__label">Phoone number</label>
                                <input type="text" class="contact__input input__num" placeholder="+998 99 122 88 41" />
                            </div>
                            <div class="input__box">
                                <label for="input__name" class="contact__label">Telegram username</label>
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
                            <label for="input__name" class="contact__label">Name</label>
                            <input type="text" class="contact__input input__name" placeholder="Saidaxror" />
                        </div>
                        <div class="input__box">
                            <label for="input__name" class="contact__label">Phoone number</label>
                            <input type="text" class="contact__input input__num" placeholder="+998 99 122 88 41" />
                        </div>
                        <div class="input__box">
                            <label for="input__name" class="contact__label">Telegram username</label>
                            <div class="input__username">
                                <i class="fab fa-telegram"></i>
                                <input type="text" class="contact__input input__user" placeholder="@username" />
                            </div>
                        </div>
                        <button class="input__button">SEND</button>
                    </form>
                </div>

                <!-- <div class="contact__details">
                    <ul>
                        <li>
                            +998 99 122 88 41
                        </li>
                        <li>
                            +998 94 006 88 41
                        </li>
                    </ul>
                    <ul class="contact__list">
                        <li>
                            <a href="#about" class="contact__link">About</a>
                        </li>
                        <li>
                            <a href="#projects" class="contact__link">Projects</a>
                        </li>
                        <li>
                            <a href="#service" class="contact__link">Services</a>
                        </li>
                        <li>
                            <a href="#skills" class="contact__link">Skills</a>
                        </li>
                        <li>
                            <a href="#contact" class="contact__link">Contact</a>
                        </li>
                    </ul>
                </div> -->
            </div>
        </div>
    </section>
</template>

<script>
    export default {
        methods: {
            onSubmit(e) {
                e.preventDefault();
            },
        },
    };
</script>

<style></style>
