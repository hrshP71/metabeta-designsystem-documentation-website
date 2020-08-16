<template>
  <div class="code-block bg-purple-800 h-100">
     <p v-if="comment.length > 1" class="comment"> /* {{comment}} */</p>
     <p v-if="additional.length > 1" class="comment"> /* {{additional}} */</p>
     <p class="class-name">
         .{{className}} {
     </p>
     <ul>
         <li v-for="c in cssCode" :key="c.key">
            <span class="key"> {{c.key}} <span :class="{'display-none-none-none-none' : mixin}"> : </span> </span> {{c.value}}<span class="key padding-0-0">;</span>
            <p v-if="!c.key && !c.value ">
                {{c}}
            </p>
         </li>
     </ul>
     <p class="class-name">
         }
     </p>
  </div>
</template>

<script>
export default {
    props:{
        className:{
            type: String,
            default: 'div',
        },
        cssCode:{
            type: Array,
            default: () => [],
        },
        comment:{
            type: String,
            default: ''
        },
        additional:{
            type: String,
            default: '',
        },
        mixin: {
            type: Boolean,
            default: false,
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
        padding: $space-xxl;
        .class-name{
            color: $color-yellow-500;
        }
        li{
            margin: 10px 0;
            color: $color-orange-400;
        .key{
            padding: 0 0 0 30px;
            color: $color-pink-500;
            &.padding-0-0{
                padding:0 0;
            }
        }
        }
        .comment{
            color: $color-blue-100;
            margin-bottom: 20px;
        }
    }
</style>