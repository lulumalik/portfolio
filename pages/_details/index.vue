<template>
  <div>
    <client-only>
      <modalData v-if="modal" @close="modal = false" class="px-2">
        <div>
          <img v-if="imageData !== ''" :src="imageData" alt="modal" style="margin:0px auto;max-width:75vw;max-height:80vh;" />
        </div>
      </modalData>
    </client-only>

    <keep-alive>
      <component v-bind:is="$route.params.details" @select="selectImage"></component>
    </keep-alive>
  </div>
</template>

<script>
import cordova from "~/components/post/cordova";
import nuxtjs from "~/components/post/nuxt";
import vuejs from "~/components/post/vue";
import modalData from "~/components/modal.vue";
export default {
  components: {
    cordova,
    nuxtjs,
    vuejs,
    modalData
  },
  data() {
    return {
      modal: false,
      imageData:""
    }
  },
  methods :{
    selectImage(e) {
      this.modal = true
      this.imageData = e
    }
  }
};
</script>
