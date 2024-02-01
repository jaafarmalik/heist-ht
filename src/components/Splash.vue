<template>
  <section class="section-navlinks">
    <LinkItem LinkLabel="Home" IconPath="'link-icon/01-home.png'" :changeSplash="true" :imgUrl="Paint"
      @iconClicked="showSplash">
    </LinkItem>
    <LinkItem LinkLabel="Contact" IconPath="'link-icon/02-contact.png'" :changeSplash="true" :imgUrl="Contact"
      @iconClicked="showSplash">
    </LinkItem>
    <LinkItem LinkLabel="Organization" IconPath="'link-icon/03-organization.png'" :changeSplash="true" :imgUrl="Members"
      @iconClicked="showSplash">
    </LinkItem>
    <LinkItem LinkLabel="About" IconPath="'link-icon/04-about.png'" :changeSplash="true" :imgUrl="About"
      @iconClicked="showSplash">
    </LinkItem>
    <LinkItem LinkLabel="Archive" IconPath="'link-icon/05-archive.png'" :changeSplash="true" :imgUrl="Archive"
      @iconClicked="showSplash">
    </LinkItem>
  </section>

  <section class="section-splash">
    <img :src="imgUrl" />
  </section>

  <section class="section-navlinks">
    <LinkItem LinkLabel="Discord" IconPath="'link-icon/06-discord.png'" :inNewTab="true"
      redirectUrl="https://www.discord.com">
    </LinkItem>
    <LinkItem LinkLabel="Twitter" IconPath="'link-icon/07-twitter.png'" :inNewTab="true"
      redirectUrl="https://www.twitter.com/heistht/">
    </LinkItem>
    <LinkItem LinkLabel="Instagram" IconPath="'link-icon/08-insta.png'" :inNewTab="true"
      redirectUrl="https://www.instagram.com/heist/">
    </LinkItem>
    <LinkItem LinkLabel="Store" IconPath="'link-icon/09-store.png'" :inNewTab="true" redirectUrl="https://www.heist.net/">
    </LinkItem>
  </section>
</template>

<script lang="ts">
import LinkItem from './LinkItem.vue'

export default {
  name: 'Splash',
  data() {
    return {
      imgUrl: './splash/heist.png',
      Paint: './splash/heist.png',
      Contact: './splash/contact.png',
      Members: './splash/org.png',
      About: './splash/about.png',
      Archive: './splash/archive.png',
    };
  },
  methods: {
    showSplash(newUrl: string): void {
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
  display: flex;
  width: 100%;
  padding: 15px 0 15px 0px;
}

/* Splash Image */
.section-splash {
  width: 100%;
  display: flex;
  justify-content: center;
}

.section-splash img {
  position: absolute;
  justify-content: center;
  align-self: center;
}

@media only screen and (max-width: 400px) {
  .section-splash img {
    width: 99%;

  }
}
</style>
    