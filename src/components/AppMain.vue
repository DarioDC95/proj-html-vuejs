<script>
    export default {
        
    }
</script>

<template>
    <main>
        <section class="business-planning">
            <div class="mycontainer">
                <div class="container-fluid">
                    <div class="row align-items-center">
                        <div class="col-6 px-0">
                            <div class="mycard-description">
                                <div class="title mb-5"><span class="fw-bold">Business Planning</span> Digital Technology <span class="fw-bold">Modern Solution !</span></div>
                                <p class="mb-5">When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper surface.</p>
                                <div>
                                    <button class="try">Try It Now</button>
                                    <button class="explore">Explore More</button>
                                </div>
                            </div>
                        </div>
                        <div class="col-6 px-0">
                            <div class="mycard">
                                <img src="../assets/header.png" alt="Logo Desk">
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>
    </main>
</template>

<style scoped lang="scss">
    @use '../styles/partials/variables.scss'as *;
    @use '../styles/partials/mixins.scss'as *;

    main {
        padding-bottom: 200px;

        .business-planning {
            background-color: $bg-blue;
            padding: 30px 0px 200px 0px;

            img {
                max-width: 100%;
            }

            .mycard-description {
                padding-right: 200px;
                color: $text-white;

                .title {
                    font-size: $fs-xxl;
                }

                p {
                    padding-right: 150px;
                    font-size: $fs-sm;
                    color: $text-lightblue;
                }
                
                .try {
                    @include button-linear-gradient($bg-linear-orange, $bg-linear-lightblue);
                    padding: 10px 50px;
                    margin-right: 1.5rem;
                }

                .explore {
                    @include button-linear-gradient($bg-linear-lightblue, $bg-linear-orange);
                    padding: 10px 50px;
                }
            }
        }
    }    
</style>