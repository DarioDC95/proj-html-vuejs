<script>
    import AppCardSlider from '../sunCardComponents/AppCardSlider.vue';
    export default {
        components: {
            AppCardSlider,
        },
        data() {
            return {
                cardsSlider: [
                    {
                        image: '/src/assets/8wa60okr-1-790x576.jpg',
                        title: 'Basket of Flower on table',
                        area: 'Branding Strategy'
                    },
                    {
                        image: '/src/assets/84316050-0af0-49db-a53a-241d47ddad0e-2-790x576.jpg',
                        title: 'Purinky Products',
                        area: 'Digital Experience'
                    },
                    {
                        image: '/src/assets/a247b00b-3621-470f-b4b8-b3ac46f25907-1-790x576.jpg',
                        title: 'Satisfy Poster',
                        area: 'Branding Strategy'
                    },
                    {
                        image: '/src/assets/84316050-0af0-49db-a53a-241d47ddad0e-2-790x576.jpg',
                        title: 'Mock-up Template',
                        area: 'Ecommerce'
                    },
                    {
                        image: '/src/assets/a247b00b-3621-470f-b4b8-b3ac46f25907-1-790x576.jpg',
                        title: 'Landing Page',
                        area: 'Digital Strategy'
                    },
                ],
                translate: 0,
                active: 0,
            }
        },
        mounted() {
            let row = document.querySelector('.title-row');
            let widthRow = row.getBoundingClientRect().width;
            let mycardContainer = document.getElementsByClassName('mycard-container');
            
            for(let i = 0; i < mycardContainer.length; i++) {
                mycardContainer[i].style.width = `calc((${widthRow}px / 3) - 35px)`;
            }
        },
        methods: {
            getColWidth() {
                let col = document.getElementById('col_Slider-0');
                const colWidth = col.getBoundingClientRect().width;
                return colWidth
            },
            slideRight() {
                let width = this.getColWidth();

                if (this.translate < (width * (this.cardsSlider.length - 3))) {
                    this.translate += width;
                    let rowSlider = document.getElementById('rowslider');
                    rowSlider.style.transform = `translateX(-${this.translate}px)`;
                    rowSlider.style.transition = "all 0.5s";
                }
            },
            slideLeft() {
                let width = this.getColWidth();

                if (this.translate > 0) {
                    this.translate -= width;
                    let rowSlider = document.getElementById('rowslider');
                    rowSlider.style.transform = `translateX(-${this.translate}px)`;
                    rowSlider.style.transition = "all 0.5s";
                }
            }
        }
    }
</script>

<template>
    <section class="slider">
        <div class="mycontainer">
            <div class="title-row d-flex justify-content-between flex-nowrap">
                <div class="mycol-6">
                    <div class="mycard">
                        <div class="top-title fw-semibold">Portfolio</div>
                        <div class="title"><span class="fw-bold">latest</span> work</div>
                    </div>
                </div>
                <div class="mycol-6 d-flex align-items-end">
                    <div class="mycard mb-3 d-flex">
                        <button @click="slideLeft()" class="first-button"><i class="fa-solid fa-arrow-left"></i></button>
                        <button @click="slideRight()"><i class="fa-solid fa-arrow-right"></i></button>
                    </div>
                </div>
            </div>
            <div id="rowslider" class="content-row d-flex">
                <div v-for="(value, index) in cardsSlider" :key="index" :id="`col_Slider-${index}`" class="mycol">
                    <div class="mycard-container">
                        <AppCardSlider :element="value"/>
                    </div>
                </div>
            </div>
            <div class="circles-row">
                <div class="mycol">
                    <div class="mycard d-flex justify-content-center">
                        <div v-for="(value, index) in (cardsSlider.length - 2)" :key="index" :id="`circleId-${index}`" class="circle"></div>
                    </div>
                </div>
            </div>
        </div>        
    </section>
</template>

<style scoped lang="scss">
    @use '../../styles/partials/variables.scss'as *;
    @use '../../styles/partials/mixins.scss'as *;

    .slider {
        padding: 100px 0 70px 0;
        overflow: hidden;
        background-color: #f6f6f6;

        .title-row {
            width: 100%;
            margin-bottom: 80px;
    
            .top-title {
                color: $text-red;
                font-size: $fs-sm;
            }
            
            .title {
                color: $text-black;
                font-size: $fs-xl;
            }

            .first-button {
                margin-right: 30px;
            }

            button {
                width: 50px;
                height: 50px;
                border: 1px solid $text-orange;
                border-radius: 50%;
                background-color: $bg-white;
                color: $text-orange;
                font-size: 25px;

                &:hover {
                    box-shadow: 0px 0px 30px 0px rgba(128, 128, 128, 0.884);
                    background: $bg-linear-orange;
                    color: $text-white;
                }
            }
        }

        .content-row {
            margin-bottom: 100px;

            .mycol {
                padding-right: 48px;

                .mycard-container {
                    height: 100%;
                }
            }
        }

        .circles-row {

            .mycard {

                .circle {
                    width: 10px;
                    height: 10px;
                    margin: 0 10px;
                    border-radius: 50%;
                    background-color: lightgrey;
                }
            }
        }
    }
</style>