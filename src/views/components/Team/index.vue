<template>
  <div id="Team">
    <div class="container pb-3">
      <div class="py-5">
        <span class="fs-3 fw-bold">Team</span>
      </div>
      <div class="d-flex">
        <div
          v-for="(item, index) in list"
          :key="index"
          class="flex-fill mx-5 intro"
          role="button"
        >
          <img
            class="rounded-circle shadow"
            :src="item.avatar"
            widrth="120"
            height="120"
            alt=""
          />
          <div>
            <span class="fw-bold fs-5 my-3">
              {{ item.name }}
            </span>
          </div>
          <div>
            <span>
              {{ item.intro }}
            </span>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  import daniel from '@/assets/daniel.png'
  import zhao from '@/assets/zhao.png'
  import pnoodle from '@/assets/pnoodle.png'

  export default {
    data() {
      return {
        list: [
          {
            avatar: daniel,
            name: 'Daniel',
            intro:
              ', aliquam eu felis. Suspendisse porttitor metus sed tortor pharetra pulvinar et ut elit. Maecenas sit amet mi vel velit pharetra consequat. Nullam elit tellus, luctus a velit et, congue faucibus.',
          },
          {
            avatar: pnoodle,
            name: 'DK',
            intro:
              ', aliquam eu felis. Suspendisse porttitor metus sed tortor pharetra pulvinar et ut elit. Maecenas sit amet mi vel velit pharetra consequat. Nullam elit tellus, luctus a velit et, congue faucibus.',
          },
          {
            avatar: zhao,
            name: 'Anthony',
            intro:
              ', aliquam eu felis. Suspendisse porttitor metus sed tortor pharetra pulvinar et ut elit. Maecenas sit amet mi vel velit pharetra consequat. Nullam elit tellus, luctus a velit et, congue faucibus.',
          },
        ],
      }
    },
  }
</script>

<style lang="scss" scoped>
  .intro,
  img {
    transition: 0.2s;
  }
  .intro {
    transition: 0.2s;
    opacity: 0.8;

    &:hover {
      .shadow {
        box-shadow: 0 0.5rem 1.5rem rgba(0, 0, 0, 0.35) !important;
      }

      opacity: 1;
      transform: scale(1.05);
      /* box-shadow: 0 0 0.25rem 0.25rem #888d; */
    }
  }
</style>
