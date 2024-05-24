<script>

export default {
    data() {
        return {
            info: [
                {
                    img: 'buy-comics-digital-comics.png',
                    text: "DIGITAL COMICS",
                },
                {
                    img: 'buy-comics-merchandise.png',
                    text: "DC MERCHANDISE",
                },
                {
                    img: 'buy-comics-subscriptions.png',
                    text: "SUBSCRIPTION",
                },
                {
                    img: 'buy-comics-shop-locator.png',
                    text: "COMIC SHOP LOCATOR",
                },
                {
                    img: 'buy-dc-power-visa.svg',
                    text: "DC POWER VISA",
                },
            ],
            link: [
                {
                    nome: 'DC Comic',
                    voci: [
                        'Carachter',
                        'Comic',
                        'Movie',
                        'TV',
                        'Games',
                        'Videos',
                        'News'
                    ]
                },
                {
                    nome: 'Shop',
                    voci: [
                        'Shop DC',
                        'Shop Dc Collection'
                    ]
                },
                {
                    nome: 'DC',
                    voci: [
                        'Terms of Use',
                        'Pricacy',
                        'Terms of Use',
                        'Terms of Use',
                        'Terms of Use',
                        'Terms of Use',
                        'Terms of Use',

                    ]
                },
                {
                    nome: 'SITES',
                    voci: [
                        'Dc',
                        'MAD Magazine',
                        'DC Kids',
                        'DC Universe'

                    ]
                }

            ],
            social: [
                'footer-facebook.png',
                'footer-twitter.png',
                'footer-youtube.png',
                'footer-pinterest.png',
                'footer-periscope.png',
            ],
           
            
        }
    },
    methods:{
        getImg(percorso){
            let risultato = new URL('../assets/' + percorso, import.meta.url);
            return risultato.href
        }
    }
}
</script>
<template>
    <footer>
        <div class="container-fluid bck-blu py-3">
            <div class="container">

                <div class="row justify-content-around">
                    <div v-for="element in info" class="col d-flex align-items-center">
                        <img :src="getImg(element.img)">
                        <span>{{ element.text }}</span>
                    </div>
                </div>
            </div>
        </div>

        <div class="container-fluid py-3">
            <div class="container">

                <div class="row">
                    <div class="col-6">
                        <div class="row">
                            <div v-for="element, i in link" class="col-4">
                                <h4>{{ element.nome }}</h4>
                                <ul>
                                    <li v-for="voce, i in link[i].voci">{{ voce }}</li>
                                </ul>
                            </div>

                        </div>
                    </div>
                    <div class="col-6 dc-bck">
                        <img src="../assets/dc-logo-bg.png">
                    </div>

                </div>
            </div>
        </div>
        <div class="container-fluid bck-grey py-3">
            <div class="container">
                <div class="row">
                    <div class="col-6"><Button>SIGN-UP NOW!</Button></div>
                    <div class="col-6 social d-flex align-items-center justify-content-end">
                        <a href="">FOLLOW US</a>
                        <img v-for="element in social" :src="getImg(element)">
                    </div>
                </div>
            </div>
        </div>
    </footer>

</template>

<style scoped>
footer {
    background-image: url('../assets/footer-bg.jpg');
    background-position: center;
    background-size: cover;
}

img {
    width: 50px;
    aspect-ratio: 1;
    object-fit: contain;
}

.dc-bck img {
    width: 100%;
}

span {
    padding: 0 0.5rem;
}

ul {
    padding: 0;
}

li {
    list-style: none
}

button {
    padding: 0.5rem;
    border: 2px solid rgb(0, 89, 255);
    background-color: gray;
    color: white;
    font-weight: bold;
}

.social img {
    width: 30px;
    margin: 0 0.5rem;
}

.bck-blu {
    background-color: rgb(0, 89, 255);
}

.bck-grey {
    background-color: rgb(46, 46, 46);
}
</style>
