<template>
  <div class="preview margin-l-0-0-0 h-100">
        <p class="text-s"> {{text}} </p>
  </div>
</template>

<script>
export default {
    props:{
        text:{
            type: String,
            default: '',
        }
    }
}
</script>

<style lang="scss">
@import 'node_modules/metabeta-design-system/metabeta/assets/styles/partials/_mb_color.scss';
@import 'node_modules/metabeta-design-system/metabeta/assets/styles/partials/_mb_space.scss';
.preview{
    padding: $space-xxl;
    @include border-radius(s);
    @include shadow($space-xxxl, "bottom", $color-gray-900);
}
</style>