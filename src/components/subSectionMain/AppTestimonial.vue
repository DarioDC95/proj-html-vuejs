<script>
    export default {
        data() {
            return {
                cards_people: [
                    {
                        image: '/src/assets/szabo-viktor-1266895-unsplash-1024x1024.png',
                        name: 'Michkel Anegl',
                        title: 'Marketing Management',
                        text: 'When, while lovely valley teems with vapour around meand meridian sun strikes the upper impenetrable foliage of my trees, and but a thousand.',
                    },
                    {
                        image: '/src/assets/philipe-cavalcante-539505-unsplash-1024x1024.png',
                        name: 'Michkel Anegl',
                        title: 'Marketing Management',
                        text: 'When, while lovely valley teems with vapour around meand meridian sun strikes the upper impenetrable foliage of my trees, and but a thousand.',
                    },
                    {
                        image: '/src/assets/fabio-spinelli-695744-unsplash-1024x1024.png',
                        name: 'Michkel Anegl',
                        title: 'Marketing Management',
                        text: 'When, while lovely valley teems with vapour around meand meridian sun strikes the upper impenetrable foliage of my trees, and but a thousand.',
                    },
                ],
                cards_brands: [
                    '/src/assets/client-1-1.png',
                    '/src/assets/clienty-2.png',
                    '/src/assets/clienty-4.png',
                    '/src/assets/client-5.png',
                    '/src/assets/clienty-3.png'
                ]
            }
        }
    }
</script>

<template>
    <section class="testimonial">
        <div class="mycontainer">
            <div class="container-fluid">
                <div class="row title-row">
                    <div class="col">
                        <div class="mycard text-center">
                            <div class="top-title fw-semibold">Testimonial</div>
                            <div class="title mb-5"><span class="fw-bold">What</span> People Say</div>
                            <p>When, while the lovely valley teems with vapour around meand the meridian sun strikes <br> the upper surface.</p>
                        </div>
                    </div>
                </div>
                <div class="myrow d-flex justify-content-between content-row">
                    <div v-for="(value, index) in cards_people" :key="index" class="mycol-4">
                        <div class="mycard text-center">
                            <div class="img">
                                <img :src="value.image" alt="Profile">
                            </div>
                            <div class="stars">
                                <div class="perpendicular-card">
                                    <div class="perpendicular"></div>
                                    <div class="perpendicular"></div>
                                </div>
                                <span></span>
                            </div>
                            <div class="description">
                                <p class="mb-4">{{value.text}}</p>
                                <div class="fw-bold mb-2">{{value.name}}</div>
                                <div>{{value.title}}</div>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="row row-cols-5 brands-row">
                    <div v-for="(value, index) in cards_brands" :key="index" class="col d-flex justify-content-center align-items-center">
                        <div class="mycard">
                            <img :src="value" alt="Logo Brand">
                        </div>
                    </div>
                </div>
            </div>
        </div>        
    </section>
</template>

<style scoped lang="scss">
    @use '../../styles/partials/variables.scss'as *;
    @use '../../styles/partials/mixins.scss'as *;

    .testimonial {
        padding: 150px 0;

        .title-row {
            margin-bottom: 150px;
    
            .top-title {
                color: $text-red;
                font-size: $fs-sm;
            }
            
            .title {
                color: $text-black;
                font-size: $fs-xl;
            }

            p {
                color: $text-black;
                font-size: $fs-sm;
            }
        }

        .content-row {
            margin-bottom: 150px;

            .mycol-4 {
                width: calc((100% - 90px) / 3);
                border-radius: 30px;
                transition: all 0.5s;
    
                &:hover {
                    box-shadow: 0px 0px 50px 0px rgba(128, 128, 128, 0.438);
                }

                .mycard {
                    padding: 0px 35px 40px 35px;
                    border-radius: 30px;
    
                    .img {
                        width: 125px;
                        height: 125px;
                        margin: -65px auto 0;
                        border: 5px solid #b6256f;
                        border-radius: 50%;
    
                        img {
                            max-width: 100%;
                        }
                    }
    
                    .stars {
                        margin-top: 40px;
                        position: relative;
                        display: inline-block;
                        margin-bottom: 2rem;
    
                        &:before {
                            content: "\2606\2606\2606\2606\2606";
                            color: $text-orange;
                            font-size: 25px;
                            background: $bg-linear-orange-180dg;
                            -webkit-background-clip: text;
                            -webkit-text-fill-color: transparent;
                        }
    
                        span {
                            width: 60%;
                            position: absolute;
                            left: 0;
                            top: 0;
                            overflow: hidden;
                            white-space: nowrap;
    
                            &:before {
                                content: "\2605\2605\2605\2605\2605";
                                color: $text-orange;
                                font-size: 25px;
                                background: $bg-linear-orange-180dg;
                                -webkit-background-clip: text;
                                -webkit-text-fill-color: transparent;
                            }
                        }
    
                        .perpendicular-card {
                            position: absolute;
                            top: -8px;
                            left: 40%;
                            z-index: -50;
                            display: flex;
    
                            .perpendicular {
                                border-bottom: 60px solid rgba(211, 211, 211, 0.445);
                                border-left: 0px solid transparent;
                                border-right: 15px solid transparent;
                                transform: skew(-20deg);
                                height: 0;
                                width: 35px;
                                margin-right: 10px;
                            }
                        }
                    }
    
                    .description {
                        font-size: $fs-sm;
                    }
                }
            }
        }
    }
</style>