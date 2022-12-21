<script setup>
    import NavbarItem from './NavbarItem.vue';    
</script>

<template>
        <nav class="relative container mx-auto p-2">
        <!-- Flex container -->
        <div class="flex items-center justify-between">
          <!-- Logo -->
          <div class="pt-2">
            <!-- <img src="img/logo.svg" alt="" /> Perhaps I'll find a logo, or make one --> 
            <h1 class="font-bold text-5xl p-2 rounded-full">
              <a href="index.html" class="hover:text-purple-300 group relative">Coastal</a>
            </h1>
          </div>
          <!-- Menu Items -->
          <div id="menuItems" class="hidden space-x-6 text-lg md:flex">
                <NavbarItem route="about" msg="About Us"/>  
            <!-- <a href="about.html" class="hover:text-purple-300 group relative">
              About Us
              <span class="bg-yellow-300 absolute left-0 -bottom-1 w-0 h-1 transition-all group-hover:w-full"></span>
            </a>
            <a href="contact.html" class="hover:text-purple-300 group relative">
              Contact
              <span class="bg-yellow-300 absolute left-0 -bottom-1 w-0 h-1 transition-all group-hover:w-full"></span>
            </a>
            <a href="gallery.html" class="hover:text-purple-300 group relative">Gallery
              <span class="bg-yellow-300 absolute left-0 -bottom-1 w-0 h-1 transition-all group-hover:w-full"></span>
            </a>
            <a href="events.html" class="hover:text-purple-300 group relative">Events
              <span class="bg-yellow-300 absolute left-0 -bottom-1 w-0 h-1 transition-all group-hover:w-full"></span>
            </a>
            <a href="community.html" class="hover:text-purple-300 group relative">Community
              <span class="bg-yellow-300 absolute left-0 -bottom-1 w-0 h-1 transition-all group-hover:w-full"></span>
            </a>
            <a href="donate.html" class="hover:text-purple-300 group relative">Donate
              <span class="bg-yellow-300 absolute left-0 -bottom-1 w-0 h-1 transition-all group-hover:w-full"></span>
            </a> -->

          </div>
  
          <!-- Hamburger Icon -->
          <!-- <div class="relative m-2 md:hidden" >
            <i class="fa-solid fa-bars fa-2x cursor-pointer" id="menu"></i>
              <div class="container flex justify-center fixed top-20 -left-full w-0 h-screen transition-all ease-in duration-300 bg-pink-400 z-10">
                <div class="flex flex-col pt-4 space-y-5 text-2xl text-white">
                  <a href="about.html" class="hover:text-pink-300">About</a>
                  <a href="contact.html" class="hover:text-pink-300">Contact</a>
                  <a href="gallery.html" class="hover:text-pink-300">Gallery</a>
                  <a href="events.html" class="hover:text-pink-300">Events</a>
                  <a href="community.html" class="hover:text-pink-300">Community</a>
                  <a href="donate.html" class="hover:text-pink-300">Donate</a>
                </div>
              </div>
            </div> -->

        </div>
    </nav>
</template>