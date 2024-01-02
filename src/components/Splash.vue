<template>
  <div class="section-navlinks">
    <LinkItem LinkLabel="Home" IconPath="'link-icon/home-light-48.png'">
    </LinkItem>
    <LinkItem LinkLabel="Contact" IconPath="'link-icon/contact-48.png'">
    </LinkItem>
    <LinkItem LinkLabel="Organization" IconPath="'link-icon/organization-48.png'">
    </LinkItem>
    <LinkItem LinkLabel="About" IconPath="'link-icon/about-48.png'">
    </LinkItem>
    <LinkItem LinkLabel="Archive" IconPath="'link-icon/archive-48.png'">
    </LinkItem>
  </div>

  <div class="section-splash">
    <img :src="imgUrl" />
  </div>

  <div class="section-navlinks">
    <LinkItem LinkLabel="Discord" IconPath="'link-icon/discord-crop-bw-48.png'">
    </LinkItem>
    <LinkItem LinkLabel="Twitter" IconPath="'link-icon/twitter-48.png'">
    </LinkItem>
    <LinkItem LinkLabel="Instagram" IconPath="'link-icon/instagram-48.png'">
    </LinkItem>
    <LinkItem LinkLabel="Store" IconPath="'link-icon/store-48.png'">
    </LinkItem>
  </div>
</template>

<script lang="ts">
import LinkItem from './LinkItem.vue'

export default {
  name: 'Splash',
  data() {
    return {
      imgUrl: './splash/window_heist.png',
    };
  },
  methods: {
    changeImage(newUrl: string): void {
      this.imgUrl = newUrl;
    },

  },
  components: {
    LinkItem,
  }
};
</script>

<style>
/* Links Container */
.section-navlinks {
  width: 100%;
  display: flex;
  height: 20%;
}

/* Splash Image */
.section-splash {
  display: flex;
  height: 60%;
  justify-content: center;
  max-width: 100%;
}

.section-splash img {
  user-select: none;
  align-self: center;
}
</style>
    