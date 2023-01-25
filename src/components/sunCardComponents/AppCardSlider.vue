<script>
    export default {
        props: {
            element: Object,
        }
    }
</script>

<template>
    <div class="mycard">
        <div class="img">
            <img :src="element.image" alt="Image">
        </div>
        <div class="description d-flex py-4 px-5 mt-1 justify-content-between align-items-baseline">
            <h5 class="fw-bold">{{element.title}}</h5>
            <div class="label">{{element.area}}</div>
        </div>
    </div>
</template>

<style scoped lang="scss">
    @use '../../styles/partials/variables.scss'as *;
    @use '../../styles/partials/mixins.scss'as *;

    .mycard {
        width: 100%;
        height: 100%;
        border-radius: 40px;
        position: relative;
        background-color: white;
        pointer-events: all;
        z-index: 100;

        &::before {
            opacity: 0;
            content: '';
            display: block;
            position: absolute;
            top: 0;
            width: 100%;
            height: 100%;
            z-index: 50;
            border-radius: 40px;
            background: $bg-linear-orange-180dg;
            transition: opacity 0.8s;
        }

        &:hover {

            &::before {
                opacity: 1;
            }

            h5 {
                color: $text-white;
            }
        }

        .img {
            border-radius: 40px;
            overflow: hidden;
            position: relative;
            z-index: 100;

            img {
                max-width: 100%;
            }
        }

        .description {
            position: relative;
            z-index: 100;

            .label {
                color: $text-grey;
                font-size: $fs-sm;
            }
        }
    }
</style>