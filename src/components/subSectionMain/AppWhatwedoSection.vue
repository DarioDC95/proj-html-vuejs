<script>
    export default {
        data() {
            return {
                cards: [
                    {
                        image: '/src/assets/Group-247.png',
                        title: 'Data Analyst',
                        text: 'When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper'
                    },
                    {
                        image: '/src/assets/Group-538.png',
                        title: 'SEO Optimization',
                        text: 'When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper'
                    },
                    {
                        image: '/src/assets/Group-566.png',
                        title: 'Security Data',
                        text: 'When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper'
                    },
                    {
                        image: '/src/assets/Group-567.png',
                        title: 'Branding Strategy',
                        text: 'When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper'
                    },
                ]
            }
        }
    }
</script>

<template>
    <section class="what-we-do">
            <div class="mycontainer">
                <div class="container-fluid">
                    <div class="row title-row">
                        <div class="col">
                            <div class="mycard text-center">
                                <div class="top-title">Our Services</div>
                                <div class="title mb-2"><span class="fw-bold">What</span> We Do</div>
                                <p>When, while the lovely valley teems with vapour around meand the</p>
                            </div>
                        </div>
                    </div>
                    <div class="row content-row">
                        <div v-for="(value, index) in cards" :key="index" class="col-3">
                            <div class="mycard text-center">
                                <div class="img">
                                    <img :src="value.image" alt="Logo Group">
                                </div>
                                <div class="description">
                                    <h3 class="fw-bold mb-4">{{value.title}}</h3>
                                    <p class="mb-0">{{value.text}}</p>
                                </div>
                                <button><i class="fa-solid fa-arrow-right"></i></button>
                            </div>
                        </div>
                    </div>
                    <div class="row row-button">
                        <div class="col">
                            <div class="mycard text-center">
                                <button>View All Services</button>
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

    .what-we-do {
            font-size: $fs-sm;
            padding: 100px 0;

            .title-row {
                margin-bottom: 200px;

                .top-title {
                    color: $text-red;
                }
    
                .title {
                    font-size: $fs-xl;
                }
            }

            .content-row {
                margin-bottom: 130px;

                .col-3 {
                    border-radius: 40px;
                    transition: all 0.5s;
    
                    &:hover {
                        background-color: $bg-blue;
                    }
    
                    &:hover .img {
                        box-shadow: 0px 0px 50px 0px rgba(128, 128, 128, 0.438);
                    }
    
                    &:hover .description {
                        color: $text-white;
                    }
    
                    &:hover button {
                        opacity: 1;
                    }
    
                    .img {
                        width: 220px;
                        height: 220px;
                        display: flex;
                        align-items: center;
                        margin: 0 auto;
                        transform: translateY(-50%);
                        padding: 20px;
                        background-color: $bg-white;
                        border-radius: 30px;
        
                        img {
                            max-width: 100%;
                        }
                    }
    
                    .description {
                        width: 70%;
                        margin: 0 auto;
                        margin-top: -90px;
                        color: $text-black;
                    }
    
                    button {
                        opacity: 0;
                        width: 70px;
                        height: 70px;
                        border: none;
                        border-radius: 50%;
                        background: $bg-linear-orange;
                        color: $text-white;
                        font-size: 25px;
                        transform: translateY(50%);
    
                        &:hover {
                            box-shadow: 0px 0px 30px 0px rgba(128, 128, 128, 0.884);
                        }
                    }
                }
            }

            .row-button {

                button {
                    @include button-linear-gradient($bg-linear-orange, $bg-linear-lightblue);
                    box-shadow: 0px 0px 50px 0px rgba(188, 42, 110, 0.793);
                    transition: box-shadow 1s;
                    padding: 10px 50px;

                    &:hover {
                        box-shadow: 0px 0px 50px 0px rgba(27, 74, 140, 0.792);
                    }
                }
            }
        }
</style>