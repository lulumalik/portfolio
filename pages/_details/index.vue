<template>
  <div>
    <navbar />
    <keep-alive>
      <component v-bind:is="$route.params.details"></component>
    </keep-alive>
  </div>
</template>

<script>
import navbar from "~/components/navbar";
import cordova from "~/components/post/cordova";
import nuxtjs from "~/components/post/nuxt";
import vuejs from "~/components/post/vue";
export default {
  components: {
    navbar,
    cordova,
    nuxtjs,
    vuejs
  }
};
</script>
