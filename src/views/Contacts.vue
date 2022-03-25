<template>
    <div class="contacts-container">
        <div class="contacts-info-container">
            <h1 class="contact-title">Get In Touch</h1>
            <div class="contacts-row">
                <a class="link" target="_blank" href="https://www.facebook.com/profile.php?id=100015388453834"></a>
                <a class="link" target="_blank" href="https://www.instagram.com/k_hrystik/"></a>
                <a class="link" target="_blank" href="mailto:chrystik21@gmail.com"></a>
                <a class="link" target="_blank" href="tg://resolve?domain=KF_Kristina"></a>
            </div>
        </div>
        <BurgerMenu />
    </div>
</template>

<script>
import BurgerMenu from '../components/BurgerMenu.vue'

export default {
    name: "Contacts",
    components: {BurgerMenu},
}

</script>

<style scoped>

    .contacts-info-container {
        display: flex;
        justify-content: space-between;
        flex-direction: column;
        align-items: center;
        height: 220px;
    }

    .contacts-row {
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        width: 1000px;
    }

    .contacts-row a {
        width: 100px;
        height: 100px;
        border-radius: 50%;
        box-shadow: 0px 0px 30px 0px rgb(0 0 0 / 25%);
        transition: 0.5s ease-in-out;
        box-shadow: 0px 0px 20px 0px rgb(0 0 0 / 0%) inset, 0px 0px 20px 0px rgb(0 0 0 / 20%);
    }

    .contacts-row a:nth-child(1) {
        background-image: url(../assets/img/fb.svg);
        background-repeat: no-repeat;
        background-position: center;
        background-size: 35%;
    }

    .contacts-row a:nth-child(2) {
        background-image: url(../assets/img/inst.svg);
        background-repeat: no-repeat;
        background-position: center;
        background-size: 35%;
    }

    .contacts-row a:nth-child(3) {
        background-image: url(../assets/img/mail.svg);
        background-repeat: no-repeat;
        background-position: center;
        background-size: 35%;
    }

    .contacts-row a:nth-child(4) {
        background-image: url(../assets/img/tl.svg);
        background-repeat: no-repeat;
        background-position: center;
        background-size: 35%;
    }

    .contacts-row a:hover {
        transform: none;
        box-shadow: 0px 0px 20px 0px rgb(0 0 0 / 20%) inset, 0px 0px 20px 0px rgb(0 0 0 / 0%);
        transition: 0.5s ease-in-out;
    }

    .contact-title {
        color: #0e0e0e;
    }

    @media (max-width: 1399.98px) {
        .contacts-row {
            width: 900px;
        }
    }

    @media (max-width: 1199.98px) {
        .contacts-row {
            width: 800px;
        }
    }

    @media (max-width: 991.98px) {
        .contacts-row {
            width: 700px;
        }

        .contacts-row a {
            width: 80px;
            height: 80px;
        }
    }

    @media (max-width: 767.98px) {
        .contacts-row {
            width: 450px;
        }
    }

    @media (max-width: 575.98px) {
        .contacts-row {
            width: 200px;
            flex-wrap: wrap;
            justify-content: space-between;
            min-height: 200px;
            align-items: stretch;
        }
        .contacts-row a {
            width: 60px;
            height: 60px;
            margin: 10px;
        }
    }

</style>
