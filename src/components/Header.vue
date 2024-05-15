<template>
    <nav class="nav">
        <div class="container">
            <div class="nav__content">
                <a href="#header" class="nav__logo">portfolio</a>

                <ul class="nav__list" :class="{ active: isActive }">
                    <li>
                        <a href="#about" class="nav__link" @click="showNav">About</a>
                    </li>
                    <li>
                        <a href="#project" class="nav__link" @click="showNav">Projects</a>
                    </li>
                    <li>
                        <a href="#service" class="nav__link" @click="showNav">Services</a>
                    </li>
                    <li>
                        <a href="#skills" class="nav__link" @click="showNav">Skills</a>
                    </li>
                    <li>
                        <a href="" class="nav__link" @click="showNav">Testimonials</a>
                    </li>
                    <li>
                        <a href="" class="nav__link" @click="showNav">Contact</a>
                    </li>

                    <div class="nav__lang">
                        <button class="lang" @click="lang = !lang">{{ lang ? "Uz" : "En" }}</button>
                    </div>
                </ul>

                <button class="hamburger" @click="showNav">
                    <i class="far fa-bars"></i>
                </button>

                <div class="overlay" @click="showNav" :class="{ active: isActive }">
                </div>

            </div>
        </div>
    </nav>

   

    <header class="header" id="header">
        <div class="container wrap">
            <div class="header__content">
                <div class="header__left">
                    <h1 class="header__title">
                        <span>I'm</span> <br />
                        Full Stack<br />
                        Front-End <br />
                        Developer.
                    </h1>
                    <button class="header__btn">DOWNLOAD CV <i class="far fa-arrow-to-bottom"></i></button>
                </div>
                <div class="header__right">
                    <img src="@/assets/img/me.png" alt="" />
                </div>
            </div>
        </div>
    </header>

</template>

<script>
export default {

    data() {
        return {
            isActive: false,
            lang: true,
        };
    },

    methods: {
        showNav() {
            this.isActive = !this.isActive;
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

.nav__logo {
    font-size: 21px;
    font-family: var(--openSemiBold);
    color: var(--second-color);
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
    font-size: 16px;
    padding: 5px;
    border-radius: 5px;
    transition: 0.3s;

}

.lang:hover {
    background: var(--second-color);    
    color: var(--white-color);
    

}


</style>
