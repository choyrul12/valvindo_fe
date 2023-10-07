<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <nav class="bg-[#002062] text-white px-5 py-3 flex justify-between">
    <div class="logo flex items-center"> 
      <img src="logo.png" alt="" class="w-28">
      <div class="space-x-4 ml-5"> 
        <router-link to="/about">About us</router-link>
        <router-link to="/new">News</router-link>
        <router-link to="/help">Help</router-link>
      </div>
    </div>
    <div class="space-x-4">
      
    </div>
    <div class="hidden md:flex space-x-4">
      <router-link to="/">Register</router-link>
      <button class="px-3 py-1 text-sm rounded-sm bg-red-600 hover:bg-red-700 text-white">Sign In</button>
    </div>
    <div class="md:hidden">
      <!-- Mobile Menu (Hamburger Icon) -->
      <!-- Implement mobile menu toggling logic here -->
    </div>
  </nav>
  <div class="bg-[#405789] px-5 py-3">
    <div class="container mx-auto flex items-center justify-between">
      <!-- Left side of the secondary navbar -->
      <div class="flex items-center">
        <button class="bg-[#203B75] text-white px-4 py-2 rounded-md mr-4 hover:bg-blue-600 focus:outline-none focus:ring-2 focus:ring-blue-500">
          All Products
        </button>
      </div>

      <!-- Right side of the secondary navbar -->
      <div class="flex-grow relative">
        <div class="relative flex">
          <input
            type="text"
            placeholder="Search..."
            class="text-white rounded-md px-4 py-2 w-full focus:outline-none focus:ring-2 focus:ring-blue-500"
          />
          <button
            type="button"
            class="absolute right-0 top-0 bottom-0 px-4 py-2 bg-[#002062] text-white rounded-r-md hover:bg-blue-600 focus:outline-none focus:ring-2 focus:ring-blue-500"
          >
            <svg
              xmlns="http://www.w3.org/2000/svg"
              class="h-6 w-6 text-white hover:text-gray-600 cursor-pointer"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M21 21l-6-6m0-6a6 6 0 11-12 0 6 6 0 0112 0z"
              />
            </svg>
          </button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  // Your component logic here
}
</script>
