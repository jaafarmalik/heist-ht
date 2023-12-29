<template>
  <div class="page-container">

    <!-- Top Links Section -->
    <div class="section-navlinks">

      <!-- Home -->
      <div class="navlink-wrapper">
        <a href="https://www.heist.ht">
          <div class="navlink-wrapper__icon" id="home-icon"></div>
          <p>Home</p>
        </a>
      </div>

      <!-- Contact -->
      <div class="navlink-wrapper">
        <a href="#" @click="changeImage('./splash/window_contact.png')">
          <div class="navlink-wrapper__icon" id="contact-icon"></div>
          <p>Contact</p>
        </a>
      </div>

      <!-- Organization -->
      <div class="navlink-wrapper">
        <a a href="#" @click="changeImage('./splash/window_organization_noexp.png')">
          <div class="navlink-wrapper__icon" id="organization-icon"></div>
          <p>Organization</p>
        </a>
      </div>

      <!-- Archive -->
      <div class="navlink-wrapper">
        <a href="#" @click="changeImage('./splash/window_archive.png')">
          <div class="navlink-wrapper__icon" id="archive-icon"></div>
          <p>Archive</p>
        </a>
      </div>

      <!-- About -->
      <div class="navlink-wrapper">
        <a href="#" @click="changeImage('./splash/window_about.png')">
          <div class="navlink-wrapper__icon" id="about-icon"></div>
          <p>About</p>
        </a>
      </div>
      <!-- End Links Section -->
    </div>



    <!-- Splash Image Section -->
    <div class="section-splash">
      <img :src="imgUrl" />
    </div>


    <!-- Bottom Links Section -->
    <div class="section-navlinks">

      <!-- Discord -->
      <div class="navlink-wrapper">
        <a target="_blank" href="https://discord.gg/JR2mcktyCd">
          <div class="navlink-wrapper__icon" id="discord-icon"></div>
          <p>Discord</p>
        </a>
      </div>

      <!-- Twitter -->
      <div class="navlink-wrapper">
        <a target="_blank" href="https://www.twitter.com/heistht">
          <div class="navlink-wrapper__icon" id="twitter-icon"></div>
          <p>Twitter</p>
        </a>
      </div>

      <!-- Instagram -->
      <div class="navlink-wrapper">
        <a target="_blank" href="https://www.instagram.com/heist">
          <div class="navlink-wrapper__icon" id="instagram-icon"></div>
          <p>Instagram</p>
        </a>
      </div>

      <!-- Shop -->
      <div class="navlink-wrapper">
        <a target="_blank" href="https://www.heist.net/">
          <div class="navlink-wrapper__icon" id="shop-icon"></div>
          <p>Shop</p>
        </a>
      </div>

    </div>
    <!-- End Links Section -->
  </div>
</template>

<script lang="ts">
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
};
</script>
    
<style>

/* Page Container */
.page-container {
  height: 100svh;
  background-color: #000;
  padding: 32px 16px 32px 16px;
}

/* Links */
.section-navlinks {
  width: 100%;
  display: flex;
  justify-content: start;
  height: 20%;
}

.navlink-wrapper {
  display: flex;
  justify-content: flex-start;
  height: auto;
}

.navlink-wrapper img {
  margin-bottom: 8px;
}

.navlink-wrapper a {
}

.navlink-wrapper__icon {
  border: solid 1px red;
  width: 50%;
  height: 50%;
}

/* Splash */
.section-splash {
  display: none;
  width: 100%;
  height: 60%;
  align-items: center;
  flex-direction: column;
  justify-content: center;
}


/*
====================== 
Icon Images +To-Do
======================

Find better way to blocking user input of the elements within .navlink-wrapper (i.e saving,highlighting,dragging etc).
The way I've done it here seems to be the most consistent across multiple devices/browsers.

====================== */
.navlink-wrapper, .navlink-wrapper__icon {
  background-repeat: no-repeat;  
  user-select:none;
  /* pointer-events: none; */
}

.navlink-wrapper__icon {
  pointer-events: none;
}

/*  ---------------- */
/*  Top Link Icons  */
/*  -------------- */
#home-icon {
  background-image: url("/link-icon/home-48.png");
}
#contact-icon {
  background-image: url("/link-icon/contact-48.png");
}
#organization-icon {
  background-image: url("/link-icon/organization-48.png");
}
#archive-icon {
  background-image: url("/link-icon/archive-48.png");
}
#about-icon {
  background-image: url("/link-icon/about-48.png")
}


/*  -------------------- */
/*  Bottom Links Icons  */
/*  ------------------ */
#discord-icon {
  background-image: url("/link-icon/discord-48.png");
}
#twitter-icon {
  background-image: url("/link-icon/x_twitter-48.png");
}
#instagram-icon {
  background-image: url("/link-icon/instagram-48.png");
}
#shop-icon {
  background-image: url("/link-icon/shop-48.png");
}

</style>
    