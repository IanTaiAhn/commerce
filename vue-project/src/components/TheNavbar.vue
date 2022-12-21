<script setup>
    import NavbarItem from './NavbarItem.vue';

//     document.getElementById("menu").addEventListener("click", (e) => {
//   e.target.nextElementSibling.classList.toggle("translate-x-full");
//   e.target.nextElementSibling.classList.add("min-w-full");
//   e.target.nextElementSibling.classList.add("ease-out");
// });
// console.log("test");
</script>

<template>
    <nav class="relative container mx-auto p-2">
        <!-- Flex container -->
        <div class="flex items-center justify-between">
          <!-- Logo -->
            <div class="pt-2">
            <!-- <img src="img/logo.svg" alt="" /> Perhaps I'll find a logo, or make one --> 
                <h1 class="font-bold text-5xl p-2 rounded-full">
                <a href="home" class="hover:text-gray-400 group relative">Coastal</a>
                </h1>
            </div>
            <!-- Menu Items -->
            <div id="menuItems" class="hidden space-x-6 text-lg md:flex">
                <NavbarItem route="shop" msg="Shop"/>
                <NavbarItem route="about" msg="About Us"/>
                <NavbarItem route="login" msg="Login"/>
            </div>
  
            <!-- Hamburger Icon -->
            <div class="relative m-2 md:hidden" >
                <!-- *TODO Fix hamburger patty -->
                <!-- <i class="fa-solid fa-bars fa-2x cursor-pointer" id="menu"></i> -->
                <!-- <font-awesome-icon icon="fa-solid fa-bars" id="menu"/> -->
                <div class="container flex justify-center fixed top-20 -left-full w-0 h-screen transition-all ease-in duration-300 bg-pink-400 z-10">
                    <div class="flex flex-col pt-4 space-y-5 text-2xl text-white">
                        <NavbarItem route="shop" msg="Shop"/>
                        <NavbarItem route="about" msg="About Us"/>
                        <NavbarItem route="login" msg="Login"/>
                    </div>
                </div>
            </div>

        </div>
    </nav>
</template>