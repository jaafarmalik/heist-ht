<script lang="ts">
import { defineComponent, PropType } from 'vue'

export default defineComponent({
   Name: 'LinkItem',
   props: {
      LinkLabel: {
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
         <span class="navlink-wrapper__label">{{ LinkLabel }}</span>
      </a>
   </div>
</template>

<style scoped>
@font-face {
   font-family: W95;
   src: url('/font/Levi-Windows.ttf');
}

.navlink-wrapper a {
   width: 110px;
   display: flex;
   color: #f4f4f4;
   flex-direction: column;
   align-items: center;
   font-family: W95;
   font-size: 1em;
   text-decoration: none;
}

.navlink-wrapper__icon {
   height: 65px;
   width: 110px;
   user-select: none;
   pointer-events: none;
   background-repeat: no-repeat;
   background-position: center;
}
</style>