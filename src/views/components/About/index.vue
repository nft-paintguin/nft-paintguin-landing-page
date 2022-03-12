<template>
  <div id="About" class="container">
    <div class="py-5">
      <span class="fs-3 fw-bold">About CFABC</span>
    </div>
    <div class="pb-5">
      <span class="">
        a non dapibus molestie, arcu felis mollis orci, in faucibus mi ante sed
        metus. Praesent diam velit, feugiat vel fringilla sit amet, tempus nec
        nisl. Sed fermentum lectus velit, quis scelerisque nisi tincidunt
        molestie. Suspendisse ullamcorper metus nisl. Vivamus dapibus vestibulum
        est a facilisis. Aliquam sit amet quam tincidunt, varius arcu et, cursus
        lorem. Pellentesque viverra sem in ante euismod tincidunt. Phasellus
        scelerisque massa mauris, non commodo felis blandit at. P
      </span>
    </div>
    <div class="d-flex pb-5">
      <div class="mx-auto rounded overflow-hidden shadow-sm">
        <YouTube
          ref="youtube"
          src="https://www.youtube.com/watch?v=FTqs9hiMxPw&ab_channel=CFABC%E9%B5%9D%E8%82%89%E9%BA%B5"
          @ready="onReady"
        />
      </div>
    </div>
  </div>
</template>

<script>
  export default {}
</script>
