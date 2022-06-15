<template>
    <div class="cases-container">
        <div class="work-card">
            <a class="worktype-container link menu-link" target="_blank" href="https://chrystik.github.io/reverse-slider.github.io/">Onepage website-slider (Non-adaptive)</a>
            <a class="worktype-container link menu-link" target="_blank" href="https://chrystik.github.io/tweenmax-animation.github.io/">TweenMax animation for main page</a>
            <a class="worktype-container link menu-link" target="_blank" href="https://chrystik.github.io/zoom-slider.github.io/">Images "zoom"-slider</a>
            <a class="worktype-container link menu-link" target="_blank" href="https://chrystik.github.io/drag-drop.github.io/">Drag and Drop</a>
            <a class="worktype-container link menu-link" target="_blank" href="https://chrystik.github.io/reverse.github.io/">Reverse slider</a>
            <a class="worktype-container link menu-link" target="_blank" href="https://chrystik.github.io/cursor-sensitive.github.io/">Cursor-sensitive lights</a>
            <a class="worktype-container link menu-link" target="_blank" href="https://chrystik.github.io/simple-aim-game.github.io/">Simple aim game</a>
            <a class="worktype-container link menu-link" target="_blank" href="https://chrystik.github.io/validation-form.github.io/">Validation for registration form + Sass</a>
            <a class="worktype-container link menu-link" target="_blank" href="https://chrystik.github.io/investment-calculator.github.io/">Investment calculator + random couting background animation</a>
            <a class="worktype-container link menu-link" target="_blank" href="https://chrystik.github.io/vuex-shop/">Vue.js, vuex shopping cart</a>
        </div>
        <BurgerMenu />
    </div>
</template>

<script>
import BurgerMenu from '../components/BurgerMenu.vue'

export default {
    name: "Cases",
    components: {BurgerMenu},
}
</script>

<style scoped>
    .work-card {
        width: 75%;
        height: 90%;
        background-color: rgb(51, 51, 51);
        border-radius: 20px;
        box-shadow: rgb(0 0 0 / 20%) 0px 0px 20px 0px inset, rgb(0 0 0 / 0%) 0px 0px 20px 0px;
        position: fixed;
        top: 50%;
        transform: translate(-50%, -50%);
        left: 50%;
        transition: all 0.5s ease-in-out 0s;
        display: flex;
        padding: 20px 50px 20px 50px;
        flex-wrap: wrap;
    }

    .worktype-container {
        width: 240px;
        height: 240px;
        background-color: rgb(51, 51, 51);
        border-radius: 20px;
        box-shadow: rgb(0 0 0 / 0%) 0px 0px 20px 0px inset, rgb(0 0 0 / 20%) 0px 0px 20px 0px;
        transition: all 0.5s ease-in 0s;
        display: flex;
        justify-content: center;
        align-items: center;
        font-size: 18px;
        color: #0e0e0e;
        font-weight: 600;
        text-decoration: none;
        padding-left: 5px;
        padding-right: 5px;
        margin-left: 10px;
        margin-right: 10px;
    }
    
    @media (min-width: 1400px) {
        .worktype-container {
            width: 205px !important;
            height: 205px !important;
        }
    }

    @media (max-width: 1399.98px) {
        .worktype-container {
            width: 190px;
            height: 190px;
        }
    }

    @media (max-width: 1199.98px) {
        .work-card {
            overflow: auto;
            padding: 20px;
            max-height: 500px;
        }
        .worktype-container {
            margin-right: unset;
            margin: 5px;
            width: 155px;
            height: 155px;
            font-size: 16px;
        }
    }

    @media (max-width: 991.98px) {
        .work-card {
            width: 530px;
        }
    }

    @media (max-width: 767.98px) {
        .work-card {
            width: 350px;
        }
    }

    @media (max-width: 575.98px) {
        .work-card {
            width: 300px;
            max-height: 400px;
        }

        .worktype-container {
            width: 130px;
            height: 140px;
        }
    }
</style>
