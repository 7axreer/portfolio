<template>
    <ul class="social">
        <a href="https://t.me/zxx7v" target="_blank" class="social__link telegram tooltip">
            <span class="tooltiptext">Telegram</span>
            <i class="fab fa-telegram"></i>
        </a>

        <a href="https://www.instagram.com/axreer?igsh=MWgyeWRic2ltemtxYw==" target="_blank" class="social__link instagram tooltip">
            <span class="tooltiptext">Instagram</span>
            <i class="fab fa-instagram"></i>
        </a>
        <a href="www.linkedin.com/in/axreer7" target="_blank" class="social__link linkedin tooltip">
            <span class="tooltiptext">LinkedIn</span>
            <i class="fab fa-linkedin-in"></i>
        </a>
        <a href="https://twitter.com/axreer7" target="_blank" class="social__link twitter tooltip">
            <span class="tooltiptext">Twitter</span>
            <i class="fab fa-twitter"></i>
        </a>
        <a href="https://github.com/7axreer" target="_blank" class="social__link github tooltip">
            <span class="tooltiptext">GitHub</span>
            <i class="fab fa-github"></i>
        </a>
    </ul>
</template>

<script>
    export default {};
</script>

<style>
    .social {
        display: flex;
        flex-direction: column;
        align-self: center;
        justify-content: center;
        gap: 20px;
        background: var(--second-color);
        padding: 10px 10px;
        border-radius: 100px;
        position: fixed;
        top: 40%;
        left: 25px;
        z-index: 99;
    }

    .social__link > i {
        font-size: 30px;
        color: var(--white-color);
        transition: 0.2s;
    }

    .instagram {
        font-weight: 800;
    }

    .telegram:hover .fa-telegram {
        color: #0088cc;
    }
    .instagram:hover .fa-instagram {
        color: #c32aa3;
    }
    .linkedin:hover .fa-linkedin-in {
        color: #007bb5;
    }
    .twitter:hover .fa-twitter {
        color: #1da1f2;
    }

    .tooltip {
        position: relative;
        display: inline-block;
        border-bottom: 1px dotted black;
    }

    .tooltip .tooltiptext {
        display: none;
        width: 120px;
        background-color: #091621;
        color: #fff;
        text-align: center;
        padding: 5px 0;
        border-radius: 6px;
        position: absolute;
        right: -140px;
        z-index: 1;
        transition: 0.3s ease;
    }

    .tooltip:hover .tooltiptext {
        display: block;
    }
</style>
