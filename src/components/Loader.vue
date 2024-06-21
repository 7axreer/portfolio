<template>
    <div class="window">
        <svg viewBox="25 25 50 50">
            <circle r="20" cy="50" cx="50"></circle>
        </svg>

        <div class="card">
            <div class="loader">
                <p>Loading</p>
                <div class="words">
                    <span class="word">pages</span>
                    <span class="word">projects</span>
                    <span class="word">codes</span>
                    <span class="word">skills</span>
                    <span class="word">pics</span>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {};
</script>

<style scoped>
    .window {
        background: #091621;
        width: 100%;
        height: 100vh;
        display: grid;
        place-content: center;
        transition: 0.5s linear;
    }

    p {
        color: var(--white-color);
    }

    svg {
        width: 80px;
        transform-origin: center;
        animation: rotate4 2s linear infinite;
        display: grid;
        height: 100%;
        place-self: center;
    }

    circle {
        fill: none;
        stroke: hsl(214, 97%, 59%);
        stroke-width: 2;
        stroke-dasharray: 1, 200;
        stroke-dashoffset: 0;
        stroke-linecap: round;
        animation: dash4 1.5s ease-in-out infinite;
    }

    @keyframes rotate4 {
        100% {
            transform: rotate(360deg);
        }
    }

    @keyframes dash4 {
        0% {
            stroke-dasharray: 1, 200;
            stroke-dashoffset: 0;
        }

        50% {
            stroke-dasharray: 90, 200;
            stroke-dashoffset: -35px;
        }

        100% {
            stroke-dashoffset: -125px;
        }
    }

    .card {
        padding: 1rem 2rem;
        border-radius: 1.25rem;
    }
    .loader {
        color: rgb(124, 124, 124);
        font-family: var(--syneBold);
        font-size: 30px;
        -webkit-box-sizing: content-box;
        box-sizing: content-box;
        height: 40px;
        padding: 10px 10px;
        display: -webkit-box;
        display: -ms-flexbox;
        display: flex;
        border-radius: 8px;
    }

    .words {
        overflow: hidden;
        position: relative;
    }
    .words::after {
        content: "";
        position: absolute;
        inset: 0;
        background: linear-gradient(var(--bg-color) 10%, transparent 30%, transparent 70%, var(--bg-color) 90%);
        z-index: 20;
    }

    .word {
        display: block;
        font-family: var(--syneRegular);
        height: 100%;
        padding-left: 6px;
        color: var(--first-color);
        animation: spin 4.5s infinite;
    }

    @keyframes spin {
        10% {
            -webkit-transform: translateY(-102%);
            transform: translateY(-102%);
        }

        25% {
            -webkit-transform: translateY(-100%);
            transform: translateY(-100%);
        }

        35% {
            -webkit-transform: translateY(-202%);
            transform: translateY(-202%);
        }

        50% {
            -webkit-transform: translateY(-200%);
            transform: translateY(-200%);
        }

        60% {
            -webkit-transform: translateY(-302%);
            transform: translateY(-302%);
        }

        75% {
            -webkit-transform: translateY(-300%);
            transform: translateY(-300%);
        }

        85% {
            -webkit-transform: translateY(-402%);
            transform: translateY(-402%);
        }

        100% {
            -webkit-transform: translateY(-400%);
            transform: translateY(-400%);
        }
    }
</style>
