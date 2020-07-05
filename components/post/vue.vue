<template>
  <div>
    <div class="mx-auto px-4 sm:px-8 py-2 text-center">
      <div class="text-center max-w-lg mx-auto mt-6">
        <div class="font-bold text-gray-600 block mx-auto rounded-sm">
          <div style="font-size:30px;">Vue Project Example</div>
        </div>
        <div class="h-2 bg-gray-400 w-64 mt-4 block mx-auto rounded-sm"></div>
        <div class="h-2 bg-gray-400 w-48 mt-2 block mx-auto rounded-sm"></div>
      </div>
    </div>
    <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3">
      <div v-for="(card, index) in 8" @click="selectImage(`/assets/crowdsourcing/web/Web_${index + 1}.png`)" :key="index" class="px-4 py-4">
        <img :src="`/assets/crowdsourcing/web/Web_${index + 1}.png`" alt="image_vue" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    selectImage(e) {
      this.$emit("select", e)
    }
  }
}
</script>
