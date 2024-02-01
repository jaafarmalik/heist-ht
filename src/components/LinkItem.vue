<script lang="ts">
import { defineComponent, PropType } from 'vue'

export default defineComponent({
   name: 'LinkItem',
   props: {
      LinkLabel: {
         type: String as PropType<string>,
         required: true,
      },
      IconPath: {
         type: String as PropType<string>,
         required: true,
      },
      imgUrl: String,
      redirectUrl: String,
      changeSplash: Boolean,
      inNewTab: Boolean,
   },
   methods: {
      iconClicked() {
         if (this.changeSplash) {
            this.$emit('iconClicked', this.imgUrl)
         } else if (this.redirectUrl) {
            if (this.inNewTab) {
               window.open(this.redirectUrl, '_blank');
            } else {
               window.location.href = this.redirectUrl;
            }
         }
      },
   },
})

</script>

<template>
   <div class="navlink-wrapper">
      <a href="#" @click="iconClicked" :target="linkTarget">
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
   width: 65px;
   display: flex;
   color: #f4f4f4;
   flex-direction: column;
   align-items: center;
   font-family: W95;
   font-size: 12px;
   text-decoration: none;
   margin: 4px;
}

.navlink-wrapper__icon {
   height: 48px;
   width: 110px;
   pointer-events: none;
   background-repeat: no-repeat;
   background-position: center;
}

.navlink-wrapper__label {
   margin-top: 0px;
}
</style>