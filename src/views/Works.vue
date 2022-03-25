<template>
    <div class="works">
        <div class="works-container">
            <router-link to="/websites" class="worktype-container link menu-link" href="websites.html">
                Websites
            </router-link>
            <router-link to="/cases" class="worktype-container link menu-link" href="cases.html">
                Cases
            </router-link>
        </div>
        <BurgerMenu />
    </div>
</template>

<script>
import BurgerMenu from '../components/BurgerMenu.vue'

export default {
    name: "Works",
    components: {BurgerMenu},
}

</script>

<style scoped>
    .works {
        position: relative;
    }

    .works-container {
        display: flex;
        justify-content: space-around;
        align-items: center;
        width: 700px;
    }

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

    @media (max-width: 1399.98px) {
        .works-container {
            width: 650px;
        }
        
        .menu-link {
            width: 180px;
            height: 180px;
        }
    }

    @media (max-width: 1199.98px) {
        .works-container {
            width: 600px;
        }

        .menu-link {
            width: 160px;
            height: 160px;
            font-size: 20px;
        }
    }

    @media (max-width: 991.98px) {
        .works-container {
            width: 500px;
        }

        .menu-link {
            width: 140px;
            height: 140px;
            font-size: 18px;
        }
    }

    @media (max-width: 767.98px) {
        .works-container {
            width: 400px;
        }

        .menu-link {
            width: 120px;
            height: 120px;
            font-size: 16px;
        }
    }

    @media (max-width: 575.98px) {
        .works-container {
            flex-direction: column;
            width: fit-content;
            height: 400px;
        }
    }
</style>