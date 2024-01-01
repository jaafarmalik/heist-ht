<script lang="ts">
import { defineComponent, PropType } from 'vue'

export default defineComponent({
   Name: 'IconLink',
   props: {
      label: {
         type: String as PropType<string>,
         required: true,
      },
      IconPath: {
         type: String as PropType<string>,
         required: true,
      },
   }
})
</script>

<template>
   <div class="navlink-wrapper">
      <a href="">
         <div :style="{ backgroundImage: 'url(' + IconPath + ')' }" class="navlink-wrapper__icon">
         </div>
         <span class="navlink-wrapper__label">{{ label }}</span>
      </a>
   </div>
</template>

<style scoped>
@font-face {
   font-family: W95;
   src: url('/font/W95FA.otf');
}

.navlink-wrapper {
   display: flex;
   justify-content: flex-start;
}

.navlink-wrapper a {
   -webkit-font-smoothing: none;
   color: #f4f4f4;
   align-items: center;
   text-decoration: none;
   display: flex;
   flex-direction: column;
   font-family: W95;
   letter-spacing: 2.5px;
   font-size: 1em;
   height: fit-content;
}

.navlink-wrapper__icon {
   background-position: center;
   width: 125px;
   height: 65px;
}

.navlink-wrapper,
.navlink-wrapper__icon {
   background-repeat: no-repeat;
   user-select: none;
}

.navlink-wrapper__icon {
   pointer-events: none;
}
</style>