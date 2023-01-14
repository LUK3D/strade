<script setup lang="ts">

const techs = [
  {
    icon: `<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor" class="w-15 h-15">
  <path d="M12.378 1.602a.75.75 0 00-.756 0L3 6.632l9 5.25 9-5.25-8.622-5.03zM21.75 7.93l-9 5.25v9l8.628-5.032a.75.75 0 00.372-.648V7.93zM11.25 22.18v-9l-9-5.25v8.57a.75.75 0 00.372.648l8.628 5.033z" />
</svg>
`,
    tittle: 'Apple iOS',
    description: 'Apple iOS is a better choice to reach a more engaged user base. Android has a border reach.',
    active: true
  },
  {
    icon: `<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor" class="w-15 h-15">
  <path d="M12.378 1.602a.75.75 0 00-.756 0L3 6.632l9 5.25 9-5.25-8.622-5.03zM21.75 7.93l-9 5.25v9l8.628-5.032a.75.75 0 00.372-.648V7.93zM11.25 22.18v-9l-9-5.25v8.57a.75.75 0 00.372.648l8.628 5.033z" />
</svg>
`,
    tittle: 'Android',
    description: 'Android has a border reach, however, particularly in emerging market, like Asia and Africa.',
  },
  {

    icon: `<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor" class="w-15 h-15">
  <path d="M12.378 1.602a.75.75 0 00-.756 0L3 6.632l9 5.25 9-5.25-8.622-5.03zM21.75 7.93l-9 5.25v9l8.628-5.032a.75.75 0 00.372-.648V7.93zM11.25 22.18v-9l-9-5.25v8.57a.75.75 0 00.372.648l8.628 5.033z" />
</svg>`,
    tittle: 'Cross-Platform',
    description: 'Cross-Platform app development allows to roll out new applications simultaneously and lower expenses.',
  },
  {

    icon: `<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor" class="w-15 h-15">
  <path d="M12.378 1.602a.75.75 0 00-.756 0L3 6.632l9 5.25 9-5.25-8.622-5.03zM21.75 7.93l-9 5.25v9l8.628-5.032a.75.75 0 00.372-.648V7.93zM11.25 22.18v-9l-9-5.25v8.57a.75.75 0 00.372.648l8.628 5.033z" />
</svg>`,
    tittle: 'Progressive',
    description: 'Progressive is a financially attractive alternative, just like Cross-Platform but not dependent on any app stores.',
  },

];


</script>

<template>
  <div class="w-screen h-screen bg-dark-800 flex">
    <div class="w-1/3 h-full bg-dark-600 shadow-4xl flex flex-col">
      <div class="text-2xl font-bold text-white p-8 border-b border-dark-800">
        <h1>strade</h1>
      </div>
      <div class="w-full h-full p-16 flex flex-col justify-center text-left items-start">
        <p class="text-4xl font-bold text-white">Which <span class="text-yellow-400">Platforms</span></p>
        <p class="text-4xl font-bold text-white">Should We Build</p>
        <p class="text-4xl font-bold text-white mb-10">Application For?</p>
        <p class="text-dark-50 ">Lorem ipsum dolor sit amet consectetur adipisicing elit. A suscipit
          repellat
          explicabo
          dolor dolorum quidem
          animi quos minus iure qui eveniet dignissimos rerum laboriosam, perferendis eaque amet natus numquam ab!</p>
      </div>
      <div class="w-full p-8 border-t border-dark-800 flex  justify-between items-center">
        <button class="px-4 py-2 font-semibold text-white bg-dark-200 rounded-lg">Previous</button>
        <p class="text-dark-50">Question 3 of 20</p>
        <button class="px-8 py-2 font-semibold bg-yellow-400 text-dark-800 rounded-lg">Next</button>
      </div>
    </div>
    <div class="w-2/3 h-full  p-20  flex flex-col">
      <div class="w-full h-full grid grid-cols-2 grid-rows-2 shadow-2xl rounded-lg overflow-hidden bg-dark-600">
        <div v-for="(item, index) in techs" :key="index"
          :class="` ${item.active ? 'bg-yellow-400' : 'text-white'} flex flex-col p-8 justify-between border border-dark-800`">
          <div v-html="item.icon" :class="` ${!item.active ? 'text-dark-50' : 'text-dark-800'}`">
          </div>
          <div>
            <p class="font-medium">{{ item.tittle }}</p>
            <p class="text-sm opacity-50">{{ item.description }}</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>

</style>
