<script>
    export default {
        data() {
            return {

            }
        }
    }
</script>

<template>
    <section class="pricing">
        <div class="mycontainer">
            <div class="container-fluid">
                <div class="row title-row">
                    <div class="col">
                        <div class="mycard text-center">
                            <div class="top-title">Price List</div>
                            <div class="title mb-2"><span class="fw-bold">Our</span> Pricing</div>
                            <p>When, while the lovely valley teems with vapour around meand the meridian sun <br> strikes the upper surface.</p>
                        </div>
                    </div>
                </div>
                <div class="row gx-5 content-row">
                    <div class="col-4">
                        <div class="mycard d-flex flex-column align-items-center text-center">
                            <div class="background-number fw-bold">
                                40
                            </div>
                            <div class="content">
                                <h1 class="fw-bold mb-3">Designing</h1>
                                <div class="fw-semibold mb-5">PROCESS</div>
                                <div class="position-relative">
                                    <div class="dollar-symbol fw-semibold ">$</div>
                                    <div class="price fw-bold">40</div>
                                </div>
                                <div class="fw-semibold mb-5">Per Month</div>
                                <ul class="list-type-none mb-5 p-0">
                                    <li class="mb-2"><span class="fw-semibold">Creative</span> Design Enabled</li>
                                    <li class="mb-2"><span class="fw-semibold">Vibrant</span> Color Usage</li>
                                    <li class="mb-2"><span class="fw-semibold">Eye</span> Catching Design</li>
                                    <li class="mb-2"><span class="fw-semibold">Extreme</span> Typography</li>
                                    <li class="mb-2"><span class="fw-semibold">Exceptional</span> Design</li>
                                </ul>
                                <button class="button"><span class="fw-semibold me-5">Order Now</span><div><i class="fa-solid fa-arrow-right"></i></div></button>
                            </div>
                        </div>
                    </div>
                    <div class="col-4">
                        <div class="mycard center-card d-flex flex-column align-items-center text-center">
                            <div class="background-number fw-bold">
                                60
                            </div>
                            <div class="content">
                                <h1 class="fw-bold mb-3">Designing</h1>
                                <div class="fw-semibold mb-5">PROCESS</div>
                                <div class="position-relative">
                                    <div class="dollar-symbol fw-semibold ">$</div>
                                    <div class="price fw-bold">60</div>
                                </div>
                                <div class="fw-semibold mb-5">Per Month</div>
                                <ul class="list-type-none mb-5 p-0">
                                    <li class="mb-2"><span class="fw-semibold">Creative</span> Design Enabled</li>
                                    <li class="mb-2"><span class="fw-semibold">Vibrant</span> Color Usage</li>
                                    <li class="mb-2"><span class="fw-semibold">Eye</span> Catching Design</li>
                                    <li class="mb-2"><span class="fw-semibold">Extreme</span> Typography</li>
                                    <li class="mb-2"><span class="fw-semibold">Exceptional</span> Design</li>
                                </ul>
                                <button><span class="fw-semibold me-5">Order Now</span><div><i class="fa-solid fa-arrow-right"></i></div></button>
                            </div>
                        </div>
                    </div>
                    <div class="col-4">
                        <div class="mycard d-flex flex-column align-items-center text-center">
                            <div class="background-number fw-bold">
                                80
                            </div>
                            <div class="content">
                                <h1 class="fw-bold mb-3">Designing</h1>
                                <div class="fw-semibold mb-5">PROCESS</div>
                                <div class="position-relative">
                                    <div class="dollar-symbol fw-semibold ">$</div>
                                    <div class="price fw-bold">80</div>
                                </div>
                                <div class="fw-semibold mb-5">Per Month</div>
                                <ul class="list-type-none mb-5 p-0">
                                    <li class="mb-2"><span class="fw-semibold">Creative</span> Design Enabled</li>
                                    <li class="mb-2"><span class="fw-semibold">Vibrant</span> Color Usage</li>
                                    <li class="mb-2"><span class="fw-semibold">Eye</span> Catching Design</li>
                                    <li class="mb-2"><span class="fw-semibold">Extreme</span> Typography</li>
                                    <li class="mb-2"><span class="fw-semibold">Exceptional</span> Design</li>
                                </ul>
                                <button class="button"><span class="fw-semibold me-5">Order Now</span><div><i class="fa-solid fa-arrow-right"></i></div></button>
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

    .pricing {
        padding-top: 80px;
        background-color: $bg-blue;

        .title-row {
    
            .top-title {
                color: $text-red;
                font-size: $fs-sm;
            }
            
            .title {
                color: $text-white;
                font-size: $fs-xl;
            }

            p {
                color: $text-white;
                font-size: $fs-sm;
            }
        }

        .content-row {
            margin-top: -280px;
            transform: translateY(50%);

            .mycard {
                background-color: $bg-white;
                box-shadow: 0px 0px 50px 0px rgba(128, 128, 128, 0.438);
                border-radius: 30px;
                padding: 40px 0;
                position: relative;
                overflow: hidden;

                .background-number {
                    font-size: 350px;
                    color: $text-lightgrey;
                    z-index: 0;
                    position: absolute;
                    top: -25%;
                    right: -7%;
                }

                .content {
                    z-index: 1;

                    .dollar-symbol {
                        display: inline;
                        margin: 0 auto;
                        text-align: left;
                        position: absolute;
                        top: 10px;
                        left: 50px;
                    }
    
                    .price {
                        font-size: 100px;
                    }
    
                    ul {
                        font-size: $fs-sm;
                    }

                    .button {
                        display: flex;
                        @include button-linear-gradient($bg-linear-orange-180dg, $bg-linear-lightblue-0dg);
                        padding: 10px 40px;
                    }
                }
            }

            .center-card {
                background: $bg-linear-orange-180dg;
                background-color: none;

                button {
                    font-size: $fs-sm;
                    color: $text-orange;
                    border: none;
                    border-radius: 30px;
                    position: relative;
                    z-index: 100;
                    background-color: $bg-white;
                    display: flex;
                    padding: 10px 40px;
                }
            }
        }
    }
</style>