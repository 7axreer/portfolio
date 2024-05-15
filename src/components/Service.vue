<template>
    <section class="service" id="service">
        <div class="container">
            <div class="service__content">
                <h1 class="section__title service__title">Our Servies</h1>
                <div class="service__cards">
                    <div class="service__card">
                        <div class="service__name">
                            <i class="fas fa-code"></i>
                            <h2>Front-End Development</h2>
                        </div>

                        <p class="service__des">
                            With expertise in front-end technologies like <span>Vue.JS</span>, <span>React</span>, and <span>Bootstrap</span>, I build
                            interactive user interfaces that enhance user experience and engagement.
                        </p>
                    </div>
                    <div class="service__card">
                        <div class="service__name">
                            <i class="far fa-phone-laptop"></i>
                            <h2>Responsive Design</h2>
                        </div>

                        <p class="service__des">
                            With expertise in front-end technologies like <span>Vue.JS</span>, <span>React</span>, and <span>Bootstrap</span>, I build
                            interactive user interfaces that enhance user experience and engagement.
                        </p>
                    </div>
                    <div class="service__card third__card">
                        <div class="service__name">
                            <i class="far fa-cogs"></i>
                            <h2>Website Optimization</h2>
                        </div>

                        <p class="service__des">
                            With expertise in front-end technologies like <span>Vue.JS</span>, <span>React</span>, and <span>Bootstrap</span>, I build
                            interactive user interfaces that enhance user experience and engagement.
                        </p>
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
    height: 250px;
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
