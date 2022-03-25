<template>
    <div class="about">
        <aside>
            <div v-for="(filesrc, index) in filesrcs" :key="index">
                <div @click="downloadWithAxios(filesrc.src, filesrc.title)">
                    <svg class="download-icon" height="48" viewBox="0 0 48 48" width="48" xmlns="http://www.w3.org/2000/svg">
                        <path d="M33 12v23c0 4.42-3.58 8-8 8s-8-3.58-8-8v-25c0-2.76 2.24-5 5-5s5 2.24 5 5v21c0 1.1-.89 2-2 2-1.11 0-2-.9-2-2v-19h-3v19c0 2.76 2.24 5 5 5s5-2.24 5-5v-21c0-4.42-3.58-8-8-8s-8 3.58-8 8v25c0 6.08 4.93 11 11 11s11-4.92 11-11v-23h-3z"/>
                    </svg>
                </div>
            </div>
        </aside>
        <div class="about-content">
            <h2>A bit about me</h2>
            <p>Almost three years of experience in the Front-End development. Involved in custom landing pages and multi-page websites.</p>
            <h2>What I do for fun</h2>
            <p>I code different cases like sliders, games or non-trivial animations.</p>
            <h2>What is more...</h2>
            <p>I am keen on drawing, travelling and taking pictures.</p>
        </div>
        <div class="cv">
            <svg width="24.000000000000004" height="24.000000000000004" xmlns="http://www.w3.org/2000/svg">
                <path fill="#0e0e0e" id="svg_2" d="m10.368,19.102c0.349,1.049 1.011,1.086 1.478,0.086l5.309,-11.375c0.467,-1.002 0.034,-1.434 -0.967,-0.967l-11.376,5.308c-1.001,0.467 -0.963,1.129 0.085,1.479l4.103,1.367l1.368,4.102z"/>
            </svg>
            <h3>CV</h3>
        </div>
        <BurgerMenu />
    </div>
</template>

<script>
import axios from 'axios'
import BurgerMenu from '../components/BurgerMenu.vue'

export default {
    name: "About",
    components: {BurgerMenu},
    data() {
        return {
            filesrcs: [
                {
                    title: 'CV.jpg',
                    src: require('../assets/CV.jpg'),
                }
            ]
        }
    },
    methods: {
        forceFileDownload(response, title) {
            console.log(title)
        const url = window.URL.createObjectURL(new Blob([response.data]))
        const link = document.createElement('a')
        link.href = url
        link.setAttribute('download', title)
        document.body.appendChild(link)
        link.click()
        },
        downloadWithAxios(url, title) {
        axios({
            method: 'get',
            url,
            responseType: 'arraybuffer',
        })
            .then((response) => {
            this.forceFileDownload(response, title)
            })
            .catch(() => console.log('error occured'))
        },
    }
}

</script>

<style scoped>
.about {
    width: 900px;
    height: 550px;
    background-color: rgb(51, 51, 51);
    border-radius: 20px;
    box-shadow: rgb(0 0 0 / 20%) 0px 0px 20px 0px inset, rgb(0 0 0 / 0%) 0px 0px 20px 0px;
    transition: all 0.5s ease-in-out 0s;
    display: flex;
    justify-content: space-between;
    padding: 20px 50px 20px 50px;
    position: relative;
}

aside {
    width: 10%;
    display: flex;
    align-items: center;
    justify-content: center;
}

aside div {
    width: 80px;
    height: 80px;
    border-radius: 50%;
    box-shadow: 0px 0px 30px 0px rgb(0 0 0 / 25%);
    transition: 0.5s ease-in-out;
    box-shadow: 0px 0px 20px 0px rgb(0 0 0 / 0%) inset, 0px 0px 20px 0px rgb(0 0 0 / 20%);
    display: flex;
    align-items: center;
    justify-content: center;
    cursor: pointer;
}

aside div:hover {
    transform: none;
    box-shadow: 0px 0px 20px 0px rgb(0 0 0 / 20%) inset, 0px 0px 20px 0px rgb(0 0 0 / 0%);
    transition: 0.5s ease-in-out;
}

.about-content {
    padding-left: 60px;
}

.about-content h2 {
    font-size: 32px;    
}

.about-content p {
    font-size: 22px;
    line-height: 36px;
}

.cv {
    position: absolute;
    bottom: 140px;
    left: 30px;
    animation: bounce 2s infinite;
}

.cv svg{
    position: absolute;
    bottom: 60px;
    left: 15px;
    transform: scale(1.7) rotate(-20deg);
}

@keyframes bounce {
  0%, 20%, 50%, 80%, 100% {
    transform: translateY(0) translateX(0);
  }
  40% {
    transform: translateY(-25px) translateX(10px);
  }
  60% {
    transform: translateY(-10px) translateX(5px);
  }
}


@media (max-width: 1399.98px){
    .about {
        width: 800px;
        height: 500px;
    }

    .about-content p {
        font-size: 18px;
        line-height: 30px;
    }

    .cv {
        bottom: 90px;
    }
}

@media (max-width: 1199.98px) {
    .about {
        width: 700px;
        height: 450px;
    }

    aside div {
        width: 70px;
        height: 70px;
    }

    .download-icon {
        transform: scale(0.9);
    }

    .about-content h2 {
        font-size: 28px;
    }

    .about-content p {
        font-size: 16px;
        line-height: 28px;
    }
}

@media (max-width: 991.98px) {
    .about {
        width: 600px;
        height: 400px;
    }

    .about-content {
        padding-left: 50px;
    }

    .about-content h2 {
        font-size: 24px;
    }

    .about-content p {
        font-size: 15px;
        line-height: 26px;  
    }

    .cv {
        bottom: 45px;
        left: 10px;
    }
}

@media (max-width: 767.98px) {
    .about {
        width: 400px;
        height: 490px;
        flex-direction: column-reverse;
        align-items: flex-end;
        padding: 30px;
    }

    aside div {
        width: 50px;
        height: 50px;
    }

    .download-icon {
        transform: scale(0.7);
    }

    .about-content {
        padding-left: unset;
    }

    .cv {
        bottom: 23px;
        left: 255px;
    }

    .cv svg {
        bottom: 18px;
        left: 40px;
        transform: scale(1.3) rotate(45deg);
    }

    @keyframes bounce {
        0%, 20%, 50%, 80%, 100% {
            transform: translateX(0);
        }
        40% {
            transform: translateX(30px);
        }
        60% {
            transform: translateX(15px);
        }
    }
}

@media (max-width: 575.98px) {
    .about {
        width: 260px;
    }

    .about-content h2 {
        font-size: 20px;
    }

    .about-content p {
        font-size: 14px;
        line-height: 22px;
    }

    .cv {
        left: 130px;
    }
}

</style>