<template>
  <div>
    <navbar />
    <bodyHome />
  </div>
</template>

<script>
import navbar from '~/components/navbar.vue'
import bodyHome from "~/components/home/index"

export default {
  components: {
    navbar,
    bodyHome
  }
}
</script>