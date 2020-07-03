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
              <img :src="card.img" style="top:15px;" :class=" index === 1 ? ' h-24 w-40 relative ' : 'h-32 w-32'" class="mx-auto" alt="images Card">
            </div>
            <div class="text-gray-600 font-bold w-40 mt-8 block mx-auto rounded-sm" style="font-size:18px;">
              {{card.name}}
            </div>
            <div class="text-gray-500 w-48 sm:w-64 block mx-auto rounded-sm">
              {{card.experience}}
            </div>
            <div class="flex justify-center mt-4">
              <div class="rounded-sm py-2 text-gray-100 font-bold px-4 bg-green-300">
                Portofolio
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </main>
</template>

<script>
export default {
  data() {
    return {
      skills: [{
        name: 'Cordova',
        img: '/assets/pngegg.png',
        experience: '1 years experience'
      }, {
        name: 'Node Js',
        img: '/assets/640px-Node.js_logo.svg.png',
        experience: '1 years experience'
      }, {
        name: 'Vue Js',
        img: '/assets/Vue.png',
        experience: '1 years experience'
      }, {
        name: 'Laravel',
        img: '/assets/462px-Laravel.svg.png',
        experience: '6 months experience'
      }, {
        name: 'Electron Js',
        img: '/assets/pngwing.com.png',
        experience: '1 years experience'
      }, {
        name: 'Nuxt Js',
        img: '/assets/nuxt-emoji.png',
        experience: '1 years experience'
      }]
    }
  }
}
</script>