<template>
    <div class="h-100 display-flex-flex-flex-flex center" :class="className">
        <p>{{content}}</p>
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
</style>