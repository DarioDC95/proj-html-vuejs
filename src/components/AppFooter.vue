<script>
    export default {
        
    }
</script>

<template>
    <div class="mycontainer">
        <div class="row subscribe">
            <div class="col">
                <div class="mycard">
                    <div class="title-sub">We Offer Awesome Services</div>
                    <p>when, while lovely valley teems with vapour around meand meridian sun strikes the upper surface.</p>
                </div>
            </div>
            <div class="col d-flex justify-content-end align-items-center">
                <div class="mycard">
                    <div class="form-subscribe">
                        <input placeholder="Enter your email Address" type="email" class="input-email">
                        <div class="button-container">
                            <button>Subscribe</button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="row">
            <div class="col">
                <div class="card text-end">
                    <div>footer</div>
                </div>
            </div>
            <div class="col">
                <div class="card text-end">
                    <div>footer</div>
                </div>
            </div>
            <div class="col">
                <div class="card text-end">
                    <div>footer</div>
                </div>
            </div>
            <div class="col">
                <div class="card text-end">
                    <div>footer</div>
                </div>
            </div>
        </div>
        <div class="row">
            <div class="col">
                <div class="card text-end">
                    <div>footer</div>
                </div>
            </div>
            <div class="col">
                <div class="card text-end">
                    <div>footer</div>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped lang="scss">
    @use '../styles/partials/variables.scss'as *;
    @use '../styles/partials/mixins.scss'as *;

    .subscribe {
        padding: 50px 20px;
        background: $bg-orange;
        border-radius: 30px;

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
    
                    &:hover {
                        background: $bg-orange;
                    }
                }
            }
        }
    }
</style>