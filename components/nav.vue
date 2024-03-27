<template>
    <nav class="bg-white border-gray-200 py-2.5 fixed w-full z-50">
      <div class="container flex flex-wrap justify-between items-center mx-auto px-4">
        <a href="/" class="flex items-center">
          <img src="/public/duck-svgrepo-com.svg" class="h-6 mr-3 sm:h-9" alt="Logo of Academia Găștilor Galbene">
          <span class="self-center text-xl font-semibold whitespace-nowrap">Academia Găștilor Galbene</span>
        </a>
        <button @click="toggleMobileMenu" class="inline-flex items-center p-2 ml-3 text-sm text-gray-500 rounded-lg lg:hidden hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-gray-200" type="button">
          <span class="sr-only">Open main menu</span>
          <svg v-if="!mobileMenuOpen" class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7"></path>
          </svg>
          <svg v-else class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"></path>
          </svg>
        </button>
        <div :class="{ 'block': mobileMenuOpen, 'hidden': !mobileMenuOpen }" class="w-full lg:flex lg:w-auto" id="mobile-menu-2">
          <ul class="flex flex-col mt-4 lg:flex-row lg:space-x-8 lg:mt-0">
            <li>
              <a href="/" class="block py-2 pl-3 pr-4 text-gray-700 rounded lg:bg-transparent lg:text-yellow-500 lg:p-0" aria-current="page">Acasa</a>
            </li>
            <li>
              <a href="/about" class="block py-2 pl-3 pr-4 text-gray-700 rounded hover:bg-gray-50 lg:hover:bg-transparent lg:border-0 lg:hover:text-yellow-500 lg:p-0">Despre Noi</a>
            </li>
            <li>
              <a href="/products" class="block py-2 pl-3 pr-4 text-gray-700 rounded hover:bg-gray-50 lg:hover:bg-transparent lg:border-0 lg:hover:text-yellow-500 lg:p-0">Preturi</a>
            </li>
            <li>
              <a href="/contact" class="block py-2 pl-3 pr-4 text-gray-700 rounded hover:bg-gray-50 lg:hover:bg-transparent lg:border-0 lg:hover:text-yellow-500 lg:p-0">Contact</a>
            </li>
          </ul>
        </div>
      </div>
    </nav>
  </template>
  
  <script>
  export default {
    data() {
      return {
        mobileMenuOpen: false
      };
    },
    methods: {
      toggleMobileMenu() {
        this.mobileMenuOpen = !this.mobileMenuOpen;
      }
    }
  };
  </script>
  