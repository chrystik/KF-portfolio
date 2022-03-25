<template>
    <div class="website-works">
        <div class="work-card" data-simplebar>
            <a target="_blank" href="https://chrystik.github.io/konstruct.github.io/" class="worktype-container link menu-link">Adaptive, Bootstrap, Jquery, Parallax background scroll</a>
            <a target="_blank" href="https://chrystik.github.io/hanak.github.io/" class="worktype-container link menu-link">Adaptive, Jquery, Slick, Fancybox, Keyframes</a>
            <a target="_blank" href="http://uawarnft.com/" class="worktype-container link menu-link">Adaptive, Jquery, Keyframes, Elfsight Apps (Instagram widget)</a>
        </div>
        <BurgerMenu />
    </div>
</template>

<script>
import BurgerMenu from '../components/BurgerMenu.vue'

export default {
    name: "Websites",
    components: {BurgerMenu},
}
</script>

<style scoped>
    .worktype-container {
        width: 200px;
        height: 200px;
        background-color: rgb(51, 51, 51);
        border-radius: 20px;
        box-shadow: rgb(0 0 0 / 0%) 0px 0px 20px 0px inset, rgb(0 0 0 / 20%) 0px 0px 20px 0px;
        transition: all 0.5s ease-in 0s;
        display: flex;
        justify-content: center;
        align-items: center;
        font-size: 24px;
        color: #0e0e0e;
        font-weight: 600;
        text-decoration: none;
    }

    .worktype-container:hover {
        box-shadow: rgb(0 0 0 / 20%) 0px 0px 20px 0px inset, rgb(0 0 0 / 0%) 0px 0px 20px 0px;
        transition: all 0.5s ease-in 0s;
    }

    .work-card {
        display: flex;
        justify-content: space-around;
        flex-wrap: wrap;
        width: 880px;
        background-color: rgb(51, 51, 51);
        border-radius: 20px;
        box-shadow: rgb(0 0 0 / 20%) 0px 0px 20px 0px inset, rgb(0 0 0 / 0%) 0px 0px 20px 0px;
        position: fixed;
        top: 50%;
        transform: translate(-50%, -50%);
        left: 50%;
        transition: all 0.5s ease-in-out 0s;
        display: flex;
        justify-content: space-between;
        padding: 20px 50px 20px 50px;
    }

    .work-card .worktype-container {
        margin: 20px;
        padding-left: 5px;
        padding-right: 5px;
        font-size: 18px;
    }

    @media (max-width: 1399.98px) {
        .work-card {
            width: 700px;
        }
        
        .menu-link {
            width: 180px;
            height: 180px;
        }
    }

    @media (max-width: 1199.98px) {
        .work-card {
            width: 600px;
            padding: 20px 30px 20px 30px;
        }

        .menu-link {
            width: 150px;
            height: 150px;
            font-size: 16px;
        }

        .work-card .worktype-container {
            font-size: 16px;
        }

    }

    @media (max-width: 991.98px) {
        .work-card {
            width: 560px;
        }

        .menu-link {
            font-size: 18px;
        }

        .work-card .worktype-container {
            margin-left: 5px;
            margin-right: 5px;
        }
    }

    @media (max-width: 767.98px) {
        .work-card {
            width: 400px;
        }

        .menu-link {
            font-size: 16px;
        }
    }

    @media (max-width: 575.98px) {
        .work-card {
            flex-direction: column;
            width: fit-content;
            height: 450px;
            padding: 15px;
        }

        .work-card .worktype-container {
            margin-top: unset;
            margin-bottom: unset;
            font-size: 14px;
        }

        .menu-link {
            width: 130px;
            height: 130px;  
        }
    }
</style>
