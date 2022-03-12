<template>
  <div id="FAQs">
    <div class="py-5">
      <span class="fs-3 fw-bold">FAQs</span>
    </div>
    <div class="container text-start d-flex">
      <div class="w-50">
        <div v-for="(item, index) in qas" :key="index" class="my-3">
          <div class="fw-bold fs-5">
            {{ item.question }}
          </div>
          <div class="text-secondary">
            {{ item.answer }}
          </div>
        </div>
      </div>
      <div class="w-50 content-center">
        <img :src="puzzled" alt="" width="300" height="400" />
      </div>
    </div>
  </div>
</template>

<script>
  import puzzled from '@/assets/puzzled.png'

  export default {
    data() {
      return {
        puzzled,
        qas: [
          {
            question: 'question1',
            answer:
              'Lorem ipsum dolor sit amet, consectetur  commodo justo vel ex auctor imperdiet. lacinia arcu varius, rutrum elit at, rutrum leo. Etiam sit amet tempor tortor. Aenean in tortor non leo ultrices fermentum ac a dolor. Fusce in nunc ultricies, aliquam nisi ut, viverra dolor',
          },
          {
            question: 'question2',
            answer:
              'Lorem ipsum dolor sit amet, consectetur  commodo justo vel ex auctor imperdiet. lacinia arcu varius, rutrum elit at, rutrum leo. Etiam sit amet tempor tortor. Aenean in tortor non leo ultrices fermentum ac a dolor. Fusce in nunc ultricies, aliquam nisi ut, viverra dolor',
          },
          {
            question: 'question3',
            answer:
              'Lorem ipsum dolor sit amet, consectetur  commodo justo vel ex auctor imperdiet. lacinia arcu varius, rutrum elit at, rutrum leo. Etiam sit amet tempor tortor. Aenean in tortor non leo ultrices fermentum ac a dolor. Fusce in nunc ultricies, aliquam nisi ut, viverra dolor',
          },
        ],
      }
    },
  }
</script>
