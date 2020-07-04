<template>
  <main class="flex-grow flex justify-center items-center">
    <div class="mx-auto px-4 sm:px-8 py-2 text-center">
      <div class="text-center max-w-lg mx-auto mt-6">
        <div class="font-bold text-gray-600 block mx-auto rounded-sm">
          <div style="font-size:30px;">Web Developer</div>
          <div style="font-size:20px;">Since 2019</div>
        </div>
        <div class="h-2 bg-gray-400 w-64 mt-4 block mx-auto rounded-sm"></div>
        <div class="h-2 bg-gray-400 w-48 mt-2 block mx-auto rounded-sm"></div>
      </div>

      <div class="grid grid-cols-6 gap-4 items-start mt-8 mx-auto px-8">
        <div
          v-for="(card, index) in skills"
          :key="index"
          class="col-span-6 sm:col-span-6 md:col-span-3 lg:col-span-2 xl:col-span-2"
        >
          <div class="bg-white shadow-lg rounded-lg px-4 py-6 mx-4 my-4">
            <div class="mx-auto h-40 py-4 bg-gray-200 rounded-md text-center">
              <img
                v-if="card.img"
                :src="card.img"
                style="top:15px;"
                :class=" index === 1 ? ' h-24 w-40 relative ' : 'h-32 w-32'"
                class="mx-auto"
                alt="images Card"
              />
            </div>
            <div
              class="text-gray-600 font-bold w-42 mt-8 block mx-auto rounded-sm"
              style="font-size:18px;"
            >{{card.name}}</div>
            <div class="text-gray-500 w-56 sm:w-64 block mx-auto rounded-sm">{{card.experience}}</div>
            <div
              @click="showDetails(card.path || 'linkedin')"
              class="flex justify-center mt-4 cursor-pointer"
            >
              <div
                :class="card.disabled ? 'bg-gray-400' : 'bg-green-400 hover:bg-green-600'"
                class="rounded-sm py-2 text-gray-100 font-bold px-4"
              >{{ card.name === 'Want to know more?' ? 'Contact' : 'Portofolio'}}</div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </main>
</template>

<script>
import { mapState } from "vuex";
export default {
  computed: {
    ...mapState("post", {
      skills: state => state.skills
    })
  },
  methods: {
    showDetails(path) {
      if (path === "linkedin") {
        window.open('https://www.linkedin.com/in/lulu-maulana-malik-b84b2316b/', "_self")
      } else if (path === 'nodejs') {
        alert('Because nodejs only consist of data and logic, it cannot be displayed')
      } else {
        this.$router.push(path);
      }
    }
  }
};
</script>