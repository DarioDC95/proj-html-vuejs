<script>
    export default {
        
    }
</script>

<template>
    <section class="latest-posts">
        <div class="mycontainer">
            <div class="container-fluid">
                <div class="row title-row">
                    <div class="col">
                        <div class="mycard text-center">
                            <div class="top-title fw-semibold">Blog</div>
                            <div class="title mb-2"><span class="fw-bold">Latest</span> Posts</div>
                            <p>When, while the lovely valley teems with vapour around meand the meridian sun strikes <br> the upper surface.</p>
                        </div>
                    </div>
                </div>
                <div class="row gx-5 content-row">
                    <div class="col-6">
                        <div class="mycard news-up">
                            <div class="sub-card">
                                <div>
                                    <div class="date mb-4">April 21, 2019 • by Paul</div>
                                    <h5 class="fw-bold mb-4">Amazon gets CCI nod to acquire 49% stake in</h5>
                                    <p class="m-0">When, while the lovely valley teems with vapor around me, and the meridian sun s ...</p>
                                </div>
                                <div>
                                    <button>Read More</button>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="col-3">
                        <div class="mycard">
                            <div>
                                <div class="date mb-4">April 21, 2019 • by Paul</div>
                                <h5 class="fw-bold mb-4">Clearing Corporations get SEBI nod to invest in overnight funds</h5>
                                <p class="mb-5">When, while the lovely valley teems with vapor around me, and the meridian sun s ...</p>
                                <button>Read More</button>
                            </div>
                        </div>
                    </div>
                    <div class="col-3">
                        <div class="mycard">
                            <div>
                                <div class="date mb-4">April 21, 2019 • by Paul</div>
                                <h5 class="fw-bold mb-4">Shabnam Dhillion, wife of RSSB hief Gurinder Dhillon, passes away in London</h5>
                                <p class="mb-4">When, while the lovely valley teems with vapor around me, and the meridian sun s ...</p>
                                <button>Read More</button>
                            </div>
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

    .latest-posts {
        padding-top: 500px;

        .title-row {
            margin-bottom: 100px;
    
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
            
            .mycard {
                background: linear-gradient(167deg, rgba(2,2,48,1) 0%, rgba(6,11,60,1) 43%, rgba(20,43,104,1) 100%);
                padding: 0px 50px 50px 50px;
                height: 430px;
                border-radius: 30px;
                color: $text-white;
                display: flex;
                flex-direction: column;
                justify-content: end;
    
                button {
                    @include button-standard($bg-white, $text-black);
                    padding: 12px 40px;

                    &:hover {
                        background: $bg-linear-orange-180dg;
                        background-color: none;
                    }
                }
            }

            .mycard.news-up {
                background-image: url(../../assets/headway-537308-unsplash-1380x703.jpg);
                background-size: cover;
                padding: 0;

                .sub-card {
                    background-color: rgba(0, 0, 0, 0.367);
                    border-radius: 30px;
                    padding: 0px 50px 50px 50px;
                    width: 100%;
                    height: 100%;
                    display: flex;
                    flex-direction: row;
                    align-items: flex-end;

                    p {
                        padding-right: 100px;
                    }

                    button {
                        white-space: nowrap;
                    }
                }
            }
        }
    }
</style>