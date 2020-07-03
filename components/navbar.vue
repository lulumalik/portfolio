<template>
  <div>
    <header class="shadow-sm">
      <div class="bg-blue-300 py-1"></div>
      <nav class="flex items-center justify-between flex-wrap bg-white py-4 mx-auto px-8">
        <div class="flex items-center flex-shrink-0 text-white mr-6">
          <a class="text-white no-underline hover:text-white hover:no-underline pl-2" href="#">
            <div style="font-size:25px;" class="px-2 font-bold text-gray-600 block mx-auto rounded">
              Lulu Maulana Malik
            </div>
          </a>
        </div>

        <div class="block lg:hidden">
          <button
            id="nav-toggle"
            class="flex items-center px-3 py-2 border rounded text-gray-600 border-gray-600 hover:text-gray-500 hover:border-gray-500 focus:outline-none"
          >
            <svg
              class="fill-current h-3 w-3"
              viewBox="0 0 20 20"
              xmlns="http://www.w3.org/2000/svg"
            >
              <title>Menu</title>
              <path d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v-2z" />
            </svg>
          </button>
        </div>

        <div
          class="w-full flex-grow lg:flex lg:items-center lg:w-auto hidden lg:block pt-6 lg:pt-0"
          id="nav-content"
        >
          <ul class="list-reset lg:flex justify-end flex-1 items-center">
            <li class="mr-3">
              <a class="inline-block py-2 px-4 active:text-gray-900 no-underline" href="#">
                <div class="text-gray-600 mt-2 font-bold block mx-auto">About</div>
              </a>
            </li>
            <li class="mr-3">
              <a
                class="inline-block text-gray-600 no-underline hover:text-gray-200 hover:text-underline py-2 px-4"
                href="#"
              >
                <div class="text-gray-600 font-bold mt-2 block mx-auto">Profile</div>
              </a>
            </li>
          </ul>
        </div>
      </nav>
    </header>
  </div>
</template>