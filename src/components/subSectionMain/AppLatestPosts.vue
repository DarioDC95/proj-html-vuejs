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
                <div class="row content-row">
                    <div class="col-6">

                    </div>
                    <div class="col-3">

                    </div>
                    <div class="col-3">
                        
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
    }
</style>