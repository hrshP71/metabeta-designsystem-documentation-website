<template>
    <div class="h-100 display-flex-flex-flex-flex" :class="className">
        <p class="absolute-mixin" v-if="content"> {{content}} </p>
        <slot class="margin-l-0-0-0" name="content"></slot>
    </div>
</template>

<script>
export default {
    props:{
        className: {
            type: String,
            default: '',
        },
        content: {
            type: String,
            default: '',
        }
    }
}
</script>

<style lang="scss" scoped>
    @import 'node_modules/metabeta-design-system/metabeta/assets/styles/partials/_mb_color.scss';
    @import 'node_modules/metabeta-design-system/metabeta/assets/styles/partials/_mb_space.scss';
    @import 'node_modules/metabeta-design-system/metabeta/assets/styles/partials/_mb_utility.scss';
    .center{
        @include flex-center-center;
    }
    .grid-mixin{
        @include grid-mixin(5, 'col', true, 250px, 'start');
    }
    .circle{
        margin: auto;
        @include border-radius('circle');
    }
    .absolute-mixin{
        @include absolute(50,50);
    }
</style>