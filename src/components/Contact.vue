<template>
    <section class="contact" id="contact">
        <div class="container">
            <div class="contact__content">
                <div class="contact__box">
                    <p class="contact__text" v-html="contactMe"></p>
                    <p class="contact__sub" v-html="contactDes"></p>

                    <div class="contact__form">
                        <form action="" @submit.prevent="onSubmit">
                            <div class="input__box">
                                <label for="input__name" class="contact__label">{{ langData.contactName[lang ? "en" : "ru"] }}</label>
                                <input v-model="formData.name" type="text" class="contact__input input__name" placeholder="Saidaxror" required />
                            </div>
                            <div class="input__box">
                                <label for="input__name" class="contact__label">{{ langData.contactNumber[lang ? "en" : "ru"] }}</label>
                                <input
                                    @input="liveValidate"
                                    v-model="formData.number"
                                    type="text"
                                    class="contact__input input__num"
                                    :placeholder="placeholder"
                                    required />
                                <p class="error" v-if="error">{{ error }}</p>
                            </div>
                            <div class="input__box">
                                <label for="input__name" class="contact__label">{{ langData.contactUsername[lang ? "en" : "ru"] }}</label>
                                <textarea
                                    v-model="formData.message"
                                    type="text"
                                    class="contact__input input__num"
                                    placeholder="Your Message"
                                    required />
                            </div>
                            <button type="submit" class="input__button">SEND</button>
                        </form>
                    </div>
                </div>
                <div class="line"></div>

                <div class="contact__form contact__media">
                    <form action="" @submit.prevent="onSubmit">
                        <div class="input__box">
                            <label for="input__name" class="contact__label">{{ langData.contactName[lang ? "en" : "ru"] }}</label>
                            <input v-model="formData.name" type="text" class="contact__input input__name" placeholder="Saidaxror" required />
                        </div>
                        <div class="input__box">
                            <label for="input__name" class="contact__label">{{ langData.contactNumber[lang ? "en" : "ru"] }}</label>
                            <input v-model="formData.number" type="text" class="contact__input input__num" placeholder="+998 99 122 88 41" required />
                        </div>
                        <div class="input__box">
                            <label for="input__name" class="contact__label">{{ langData.contactUsername[lang ? "en" : "ru"] }}</label>
                            <textarea v-model="formData.message" type="text" class="contact__input input__num" placeholder="Your Message" required />
                        </div>
                        <button class="input__button">SEND</button>
                    </form>
                </div>

                <div class="contact__details">
                    <ul class="contact__nums">
                        <li>
                            <a href="tel:+998991228841"><i class="fal fa-phone-alt"></i> +998 99 122 88 41</a>
                        </li>
                        <li>
                            <a href="tel:+998940068841"><i class="fal fa-phone-alt"></i> +998 94 006 88 41</a>
                        </li>
                        <li>
                            <a href="https://mail.google.com/mail/?view=cm&fs=1&to=saidaxororpc7@gmail.com" target="_blank"
                                ><i class="fal fa-envelope"></i> saidaxororpc7@gmail.com</a
                            >
                        </li>
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
                            <a href="#contact" class="contact__link"><i class="fas fa-phone-rotary"></i></a>
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
                formData: {
                    name: "",
                    number: "",
                    message: "",
                },
                placeholder: "+998 99 122 88 41",
            };
        },
        methods: {
            async onSubmit() {
                const botToken = "7417284057:AAHeefZBU-g74o5Qtb6XgzDtRTx_RH-T23M";
                const chatId = "6458498045";

                let phoneNumber = this.formData.number.trim();
                if (!phoneNumber.startsWith("+998")) {
                    phoneNumber = "+998" + phoneNumber;
                } else {
                    this.number;
                }

                const telegramMessage = [
                    "Сиз учун янги хабар ⤵️",
                    ``,
                    `👤 Name: ${this.formData.name}`,
                    `☎️ Number: ${phoneNumber}`,
                    `💬 Message: ${this.formData.message}`,
                ].join("\n");

                try {
                    const response = await fetch(`https://api.telegram.org/bot${botToken}/sendMessage`, {
                        method: "POST",
                        headers: {
                            "Content-Type": "application/json",
                        },
                        body: JSON.stringify({
                            chat_id: chatId,
                            text: telegramMessage,
                        }),
                    });

                    if (response.ok) {
                        alert("Message sent successfully!");
                        this.formData.name = "";
                        this.formData.number = "";
                        this.formData.message = "";
                    } else {
                        alert("Error sending message.");
                    }
                } catch (error) {
                    console.error("Error:", error);
                    alert("Error sending message.");
                }

                // Check if the phone number starts with "+998"
            },
            liveValidate() {
                // Raqamlar va bo'shliqlardan tashqari barcha belgilarni olib tashlash
                this.formData.number = this.formData.number.replace(/[^\d\s+]/g, "");

                // Validatsiya qilish
                const regex = /^\+?(\d{3}\s\d{2}\s\d{3}\s\d{2}\s\d{2})$/;
                if (!regex.test(this.formData.number)) {
                    this.formData.number = this.formData.number.slice(0, 16);
                    991228841;
                }
                if (!regex.test(this.formData.number)) {
                    this.placeholder = "Please enter a number only";
                    setTimeout(() => {
                        this.placeholder = "+998 99 122 88 41";
                    }, 2000);
                } else {
                    this.placeholder = "";
                }
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

<style scoped>
    .error {
        font-size: 14px;
        color: #ffffff;
    }
</style>
