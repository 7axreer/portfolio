<template>
    <section class="service" id="service">
        <div class="container">
            <div class="service__content">
                <h1 class="section__title service__title">{{ langData.serviceSec[lang ? "en" : "ru"] }}</h1>
                <div class="service__cards">
                    <div class="service__card">
                        <div class="service__name">
                            <i class="fas fa-code"></i>
                            <h2>{{ langData.serviceName[lang ? "en" : "ru"] }}</h2>
                        </div>

                        <p class="service__des" v-html="serviceText">
                            
                        </p>
                    </div>
                    <div class="service__card">
                        <div class="service__name">
                            <i class="far fa-phone-laptop"></i>
                            <h2>{{ langData.serviceNameRes[lang ? "en" : "ru"] }}</h2>
                        </div>

                        <p class="service__des" v-html="serviceTextRes">

                        </p>
                    </div>
                    <div class="service__card third__card">
                        <div class="service__name">
                            <i class="far fa-cogs"></i>
                            <h2>{{ langData.serviceNameWeb[lang ? "en" : "ru"] }}</h2>
                        </div>

                        <p class="service__des">
                          {{ langData.serviceTextWeb[lang ? "en" : "ru"] }}
                        </p>
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
        computed: {
            serviceText() {
                return this.lang ? this.langData.serviceText.en : this.langData.serviceText.ru;
            },
            serviceTextRes() {
                return this.lang ? this.langData.serviceTextRes.en : this.langData.serviceTextRes.ru;
            }
        },
    };
</script>

<style>
    .service {
        margin: 50px 0 85px 0;
    }

    .service__name {
        display: flex;
        align-items: center;
        justify-content: center;
        flex-direction: column;
        gap: 10px;
        font-family: var(--syneMedium);
    }

    .service__name > h2 {
        font-family: var(--syneMedium);
        font-size: 18px;
    }
    .service__name > i {
        color: var(--first-color);
        font-size: 36px;
    }

    .service__card {
        border: 1px solid var(--second-color);
        border-radius: 20px;
        padding: 20px;
        display: grid;
        place-self: center;
        height: 290px;
    }

    .service__cards {
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        gap: 30px;
    }

    .service__des {
        text-align: center;
        margin-top: 10px;
    }

    .service__des > span {
        color: var(--first-color);
        text-decoration: underline;
    }
</style>
