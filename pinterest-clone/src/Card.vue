<template>
  <div class="relative">
    <img :src="src" class="rounded-lg" />
    <div
      class="absolute bg-dark opacity-50 inset-0 w-full h-full rounded-lg"
    ></div>
    <div class="absolute top-0 w-full h-full flex flex-col justify-between p-3">
      <div class="flex items-center justify-between">
        <button type="button" class="flex items-center">
          <p class="font-semibold text-white">UI</p>
          <span class="material-icons text-white">expand_more</span>
        </button>
        <button
          class="rounded-full py-3 px-5 text-white bg-primary font-semibold"
        >
          Save
        </button>
      </div>
      <div class="flex items-center w-full">
          <button type="button" class="ml-auto mr-2 bg-white w-8 h-8 flex items-center justify-center rounded-full p-2 text-dark opacity-80 hover:opacity-100">
              <span class="material-icons text-base">ios_share</span>
          </button>
          <button type="button" class=" bg-white rounded-full w-8 h-8 flex items-center justify-center p-2 text-dark opacity-80 hover:opacity-100">
              <span class="material-icons text-base">more_horiz</span>
          </button>
      </div>
    </div>
  </div>
</template>
 
<script>
export default {
  props: ["src"],
};
</script>

<style>
</style>