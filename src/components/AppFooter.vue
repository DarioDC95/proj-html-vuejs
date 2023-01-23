<script>
    export default {
        props: {
            footerLink: Array,
        }
    }
</script>

<template>
    <footer>
        <div class="up-footer">
            <div class="mycontainer">
                <section class="subscribe">
                    <div class="container-fluid">
                        <div class="row">
                            <div class="col">
                                <div class="mycard ps-4">
                                    <div class="title-sub">We Offer Awesome Services</div>
                                    <p>when, while lovely valley teems with vapour around meand meridian sun strikes the upper surface.</p>
                                </div>
                            </div>
                            <div class="col d-flex justify-content-end align-items-center">
                                <div class="mycard pe-4">
                                    <div class="form-subscribe">
                                        <input placeholder="Enter your email Address" type="email" class="input-email">
                                        <div class="button-container">
                                            <button>Subscribe</button>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </section>
                <section class="footer-links">
                    <div class="container-fluid">
                        <div class="row">
                            <div class="col px-0">
                                <div class="mycard">
                                    <img class="mb-5" src="../assets/white-logo-2.png" alt="Logo">
                                    <p>When, while lovely valley teems vapour aroundmeand meridian sun strikes the upper impenetrable</p>
                                </div>
                            </div>
                            <div v-for="(value, index) in footerLink" :key="index" class="col px-0">
                                <div class="mycard ms-5">
                                    <div class="title-links mb-4">{{ value.title }}</div>
                                    <ul class="list-type-none p-0">
                                        <li class="mb-2" v-for="(element, indexBeta) in value.links" :key="indexBeta"><a class="underline-none" :href="element.url">{{ element.label }}</a></li>
                                    </ul>
                                </div>
                            </div>
                            <div class="col px-0">
                                <div class="mycard ms-5">
                                    <div class="title-links mb-4">Contact Us</div>
                                    <div class="contact-info mb-4">
                                        <span class="label">Address:</span> <span class="info">Patricia C. Amedee 4401 Waldeck Street Grapevine Nashville, Tx 76051</span>
                                    </div>
                                    <div class="contact-info">
                                        <span class="label">Phone:</span> <span class="info">+99 (0) 101 0000 888</span>
                                    </div>
                                    <div class="contact-info">
                                        <span class="label">Email:</span> <span class="info">info@yourdomain.com</span>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </section>
            </div>
        </div>
        <div class="bottom-footer">
            <div class="mycontainer">
                <div class="container-fluid">
                    <div class="row">
                        <div class="col px-0">
                            <div class="mycard copyright">
                                <div>&copy; 2023 Phlox. All Rights Reserved.</div>
                            </div>
                        </div>
                        <div class="col px-0">
                            <div class="mycard d-flex align-items-center justify-content-end link-social">
                                <div class="me-5">
                                    <a class="underline-none" href="#"><i class="fa-brands fa-instagram"></i></a>
                                </div>
                                <div class="me-5">
                                    <a class="underline-none" href="#"><i class="fa-brands fa-linkedin-in"></i></a>
                                </div>
                                <div class="me-5">
                                    <a class="underline-none" href="#"><i class="fa-brands fa-facebook-f"></i></a>
                                </div>
                                <div class="me-2">
                                    <a class="underline-none" href="#"><i class="fa-brands fa-twitter"></i></a>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </footer>
</template>

<style scoped lang="scss">
    @use '../styles/partials/variables.scss'as *;
    @use '../styles/partials/mixins.scss'as *;

    footer {
        background-color: $bg-blue;

        .up-footer {
            border-bottom: 1px solid grey;

            .subscribe {
                padding: 50px 50px;
                background: $bg-linear-orange;
                border-radius: 30px;
                transform: translateY(-50%);
        
                .title-sub {
                    color: $text-white;
                    font-size: $fs-xl;
                    font-weight: 600;
                }
        
                p {
                    color: $text-white;
                }
        
                .form-subscribe {
                    position: relative;
        
                    .input-email {
                        font-size: $fs-sm;
                        outline: none;
                        width: 550px;
                        border: none;
                        padding: 20px 170px 20px 20px;
                        border-radius: 50px;
                    }
        
                    .button-container {
                        padding: 8px;
                        position: absolute;
                        top: 0;
                        right: 0;
        
                        button {
                            @include button-header-footer;
                            padding: 12px 30px;
                        }
                    }
                }
            }
    
            .footer-links {
                padding-bottom: 50px;
                margin-top: -30px;
    
                p {
                    font-size: $fs-sm;
                    color: $text-grey;
                    padding-right: 50px;
                }
    
                .title-links {
                    color: $text-white;
                    font-size: 22px;
                    font-weight: 600;
                }
    
                a{
                    color: $text-grey;
                    font-size: $fs-sm;
    
                    &:hover {
                        color: $text-white;
                    }
                }
    
                .contact-info {
                    font-size: $fs-sm;
    
                    .label {
                        color: $text-white;
                    }
        
                    .info {
                        color: $text-grey;
                    }
                }
            }
        }

        .bottom-footer {
            padding-top: 40px;
            padding-bottom: 30px;

            .copyright {
                color: $text-grey;
                font-size: 15px;
            }

            .link-social {

                a {
                    color: $text-white;
                    font-size: 20px;

                    &:hover {
                        color: $text-red;
                    }
                }
            }
        }
    }
</style>