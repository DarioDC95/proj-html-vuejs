<script>
    export default {

    }
</script>

<template>
    <section class="start-project">
        <div class="mycontainer">
            <div class="container-fluid">
                <div class="row align-items-center">
                    <div class="col-6">
                        <div class="mycard-img ms-5 d-flex justify-content-end align-items-end">
                            <img src="../../assets/men-data.png" alt="Immagine Data">
                        </div>
                    </div>
                    <div class="col-6">
                        <div class="mycard-description">
                            <h6>Start Your Project</h6>
                            <div class="title mb-5"><span class="fw-bold">Grow Your Business</span> With Our Strategy</div>
                            <p class="mb-5">When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper surface of the impenetrabke foliage of my trees, and but a few stray gleams steal into the inner sanctuary.</p>
                            <div>
                                <button class="try">Try It Now</button>
                                <button class="explore">Explore More</button>
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

    .start-project {
        background-color: $bg-blue;
        padding: 70px 0 250px 0;

        .mycard-img {
            width: 60%;
            background-image: url(../../assets/nemoodar.png);
            background-position: center;
            background-size: contain;
            background-repeat: no-repeat;

            img {
                max-width: 100%;
                transform: translateY(100px) translateX(50px);
            }
        }

        .mycard-description {
                padding: 0 100px;
                color: $text-white;
                transform: translateY(100px);

                .title {
                    font-size: $fs-xxl;
                }

                p {
                    padding-right: 50px;
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
                    padding: 10px 40px;
                }
            }
    }
</style>