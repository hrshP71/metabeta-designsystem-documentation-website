<template>
  <div :class="className" class="preview h-100 padding-0-xl">
        <p class="text-s"> {{text}} </p>
  </div>
</template>

<script>
export default {
    props:{
        text:{
            type: String,
            default: '',
        },
        className:{
            type: String,
            default: '',
        }
    }
}
</script>

<style lang="scss">
@import 'node_modules/metabeta-design-system/metabeta/assets/styles/partials/_mb_color.scss';
@import 'node_modules/metabeta-design-system/metabeta/assets/styles/partials/_mb_space.scss';
@import 'node_modules/metabeta-design-system/metabeta/assets/styles/partials/_mb_utility.scss';
.preview{
    @include flex-center-center();
    @include border-radius(s);
    @include shadow($space-xxxl, "bottom", $color-gray-900);
}
</style>