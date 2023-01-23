<script>
    export default {
        props: {
            menu: Array,
        }
    }
</script>

<template>
    <header>
        <div class="mycontainer">
            <div class="container-fluid">
                <div class="row">
                    <div class="col px-0">
                        <div class="mycard">
                            <img src="../assets/white-logo-2.png" alt="Logo">
                        </div>
                    </div>
                    <div class="col px-0 d-flex align-items-center justify-content-end">
                        <div class="mycard d-flex align-items-center">
                            <ul class="d-flex p-0 m-0 list-type-none">
                                <li v-for="(value, index) in menu" :key="index" class="ms-4">
                                    <a class="underline-none mx-1" :class="value.active ? 'active' : ''" :href="value.url" @click="$emit('selection', index)">{{ value.label }}</a>
                                </li>
                            </ul>
                            <button class="button-blue ms-5">Sign In</button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </header>
</template>

<style scoped lang="scss">
    @use '../styles/partials/variables.scss'as *;
    @use '../styles/partials/mixins.scss'as *;

    header {
        background-color: $bg-blue;
        padding: 25px 0;

        ul {
            
            li {
                
                a {
                    font-size: $fs-sm;
                    color: $text-white;
                }

                .active {
                    color: $text-orange;
                    font-weight: 600;
                }
            }
        }

        .button-blue {
            @include button-header-footer;
            padding: 8px 25px;
        }
    }
</style>