

<template>
  
  <div class="bg-gray-100">
      <nav
        class="
          container
          px-6
          py-8
          mx-auto
          md:flex md:justify-between md:items-center
        "
      >
        <div class="flex items-center justify-between">
          <router-link
            to="/"
            class="
              text-xl
              font-bold
              text-gray-800
              md:text-2xl
              hover:text-blue-400
            "
            ><VLogo />
          </router-link>
          <!-- Mobile menu button -->
          <div @click="showMenu = !showMenu" class="flex md:hidden">
            <button
              type="button"
              class="
                text-gray-800
                hover:text-gray-400
                focus:outline-none focus:text-gray-400
              "
            >
              <svg viewBox="0 0 24 24" class="w-6 h-6 fill-current">
                <path
                  fill-rule="evenodd"
                  d="M4 5h16a1 1 0 0 1 0 2H4a1 1 0 1 1 0-2zm0 6h16a1 1 0 0 1 0 2H4a1 1 0 0 1 0-2zm0 6h16a1 1 0 0 1 0 2H4a1 1 0 0 1 0-2z"
                ></path>
              </svg>
            </button>
          </div>
        </div>


        <!-- Mobile-->
        <ul
          :class="showMenu ? 'flex' : 'hidden'"
          class="
            flex-col
            mt-8
            space-y-4
            md:flex
            md:space-y-0
            md:flex-row
            md:items-center
            md:space-x-10
            md:mt-0
          "
        >
          <li class="text-sm font-bold text-gray-800 hover:text-blue-400">
            <a href="">Home</a>
          </li>
          <li class="text-sm font-bold text-gray-800 hover:text-blue-400">
            <a href="/about"> About</a>
          </li>
          <li class="text-sm font-bold text-gray-800 hover:text-blue-400">
             <a href="/Blogs">Blogs</a>
          </li>
          <li class="">
             <a href="/Contact"><button class="bg-blue-500 hover:bg-orange-400 text-white font-bold py-3 px-8 rounded-lg transition ease-in-out duration-500">
           Contact Us!
        </button>
          </a>
          </li>
        </ul>
      </nav>
    </div>

    <a
    href="#"
    class="fixed right-4 bottom-4 inline-blocktext-white font-bold py-2 px-3  bg-slate-300 z-50"
    ><ion-icon name="chevron-up-outline"></ion-icon></a
  >

</template>

<script >
export default {
  data() {
    return {
      showMenu: false,
    };
  },
};
</script>