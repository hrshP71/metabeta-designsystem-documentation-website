<template>
  <div class="code-block bg-purple-800 h-100">
      <span class="markup">
          &lt;{{markup}} <span class="markup-definition"> class= </span>
      </span>
      <span class="class">"{{classText}}"</span>
      <span class="markup">
          &gt;
          <slot class="padding-xl-l" name="inner"></slot>
          <br />&lt;/{{markup}}&gt;	
      </span>
  </div>
</template>

<script>
export default {
    props:{
        markup:{
            type: String,
            default: 'div',
        },
        classText:{
            type: String,
            default: 'div',
        }
    }
}
</script>

<style lang="scss">
    @import 'node_modules/metabeta-design-system/metabeta/assets/styles/partials/_mb_color.scss';
    @import 'node_modules/metabeta-design-system/metabeta/assets/styles/partials/_mb_space.scss';
    .code-block{
        @include border-radius(s);
        @include shadow($space-xxxl, "bottom", $color-gray-900);
        height: 200px;
        padding: $space-xxl;
        .markup{
            color: $color-teal-600;
            &-definition{
                color: $color-teal-200;
            }
        }
        .class{
            color: $color-yellow-400;
        }
    }
</style>