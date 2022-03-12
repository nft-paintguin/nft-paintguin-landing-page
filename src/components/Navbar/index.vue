<template>
  <div
    class="navbar-wrapper position-sticky top-0 d-flex px-3"
    :class="[!isTopSealed && 'navbar-wrapper_non-sealed']"
  >
    <!-- <div class="logo">
      <img src="" alt="" />
    </div> -->
    <div class="navbar-list d-flex">
      <div
        v-for="item in navList"
        :key="item.name"
        class="navbar-item content-center"
      >
        <a class="px-2 me-3 position-relative" :href="item.link">
          {{ item.name }}
        </a>
      </div>
    </div>
    <div class="related-link d-flex ms-auto">
      <div
        v-for="item in relatedLinkList"
        :key="item.name"
        class="navbar-item content-center"
      >
        <a class="p-3" :href="item.link">
          <img :src="item.img" width="36" height="36" :alt="item.name" />
        </a>
      </div>
    </div>
    <div class="content-center">Connect Wallet</div>
  </div>
</template>

<script>
  import Discord from '@/assets/discord.png'
  import Opensea from '@/assets/opensea.png'
  import Twitter from '@/assets/twitter.png'

  export default {
    name: 'Navbar',
    props: {
      isTopSealed: {
        requied: true,
        type: Boolean,
      },
    },
    data() {
      return {
        navList: [
          {
            name: 'About',
            link: '#About',
          },
          // {
          //   name: 'Contact',
          //   link: '#Contact',
          // },
          {
            name: 'Roadmap',
            link: '#Roadmap',
          },
          {
            name: 'FAQs',
            link: '#FAQs',
          },
          {
            name: 'Team',
            link: '#Team',
          },
        ],
        relatedLinkList: [
          { link: '', img: Discord },
          { link: '', img: Opensea },
          { link: '', img: Twitter },
        ],
      }
    },
  }
</script>

<style scoped lang="scss">
  .navbar-wrapper {
    height: 100%;
    z-index: 1;
    transition: 0.2s;

    &_non-sealed {
      background-color: #ecfbffee;
    }
  }

  .navbar-item a:after,
  .navbar-item a:before {
    position: absolute;
    top: 0;
    bottom: 0;
    width: 2px;
    content: '';
    background-color: #1890ff;
    transition: transform 0.5s ease;
    transform: scaleY(0);
  }
  .navbar-item a:after {
    right: -0.25rem;
    transform-origin: center bottom;
  }

  .navbar-item a:before {
    left: -0.25rem;
    transform-origin: center top;
  }

  .navbar-item a:hover:after {
    transform: scaleY(1);
    transform-origin: center top;
  }

  .navbar-item a:hover:before {
    transform: scaleY(1);
    transform-origin: center bottom;
  }
</style>
