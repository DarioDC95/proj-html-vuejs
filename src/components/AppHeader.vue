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
            <div class="row">
                <div class="col">
                    <div class="mycard">
                        <img src="../assets/white-logo-2.png" alt="Logo">
                    </div>
                </div>
                <div class="col d-flex align-items-center justify-content-end">
                    <div class="mycard d-flex align-items-center">
                        <ul class="d-flex p-0 m-0 list-type-none">
                            <li v-for="(value, index) in menu" :key="index" class="ms-4">
                                <a class="underline-none" :class="value.active ? 'active' : ''" :href="value.url">{{ value.label }}</a>
                            </li>
                        </ul>
                        <button class="button-blue ms-5">Sign In</button>
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
            font-size: $fs-sm;
            color: $text-white;
            border: none;
            padding: 8px 25px;
            border-radius: 30px;
            transition: all 5s;
            @include button-blue;

            &:hover {
                @include button-orange;
            }
        }
    }

</style>