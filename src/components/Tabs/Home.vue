<template>
    <div class="backface-hidden absolute w-full h-full lg:shadow-2xl rounded lg:shadow-black/35 flex items-center justify-center text-white lg:backdrop-blur-xs"
      style="transform: rotateY(0deg) translateZ(400px);">
  
      <!-- Scrolling Container for Smaller Screens -->
      <div
        class="relative w-full h-full p-1 lg:p-5 overflow-y-auto sm:max-h-[98vh] sm:min-h-[80vh]">
        
        <div class="max-w-full h-full mx-auto flex flex-col lg:flex-row items-center lg:justify-around space-y-16">
  
          <!-- Profile Picture -->
          <div class="pt-20 lg:hidden">
            <div class="w-[80px] h-[80px] rounded-full border-2 border-transparent outline-1 outline-green-400 overflow-hidden cursor-pointer">
              <img src="../../assets/Images/me.jpg" class="w-full h-full object-cover bg-top" alt="Profile">
            </div>
          </div>
  
          <!-- Left Side -->
          <div class="w-full h-fit lg:p-3 flex flex-col space-y-12 text-center lg:text-left">
            <div class="flex flex-col space-y-4">
              <p class="font-bold text-lg lg:text-3xl tracking-wide">
                Hi! I`m <span class="text-green-500">AKMAL</span>,
                <br>
                A <span class="text-green-500">Web Developer</span>
              </p>
              <p class="text-xs lg:tracking-wide font-light">
                Known for crafting seamless user experiences and scalable applications, I excel in driving project success through innovation and precision.
              </p>
            </div>
            <div class="max-w-full lg:max-w-3/6 flex items-center space-x-3">
              <span class="w-full">
                <button class="w-full px-2 py-1 border border-green-500 rounded-sm text-green-500 hover:bg-green-500 hover:text-white cursor-pointer duration-300 text-xs lg:text-sm">
                  Contact Me
                </button>
              </span>
              <span class="w-full">
                <button class="px-2 py-1 bg-green-500 hover:bg-green-400 cursor-pointer w-full rounded-sm duration-300 text-xs lg:text-sm">
                  Hire Me
                </button>
              </span>
            </div>
          </div>
  
          <!-- Right Side -->
          <div class="w-fit relative p-3 hidden lg:block">
            <div class="absolute -top-2 -right-2 w-[7rem] h-[3px] bg-green-400 z-50"></div>
            <div class="absolute -top-2 -right-2 w-[3px] h-[7rem] bg-green-400 z-50"></div>
            <div>
              <div class="flex justify-center items-center w-[200px] h-[500px]">
                <img src="../../assets/Images/hero10.png" alt="Bash SVG" class="w-[250px] h-[170px]">
              </div>
            </div>
            <div class="absolute -bottom-2 -left-2 w-[7rem] h-[3px] bg-green-400 z-50"></div>
            <div class="absolute -bottom-2 -left-2 w-[3px] h-[7rem] bg-green-400 z-50"></div>
          </div>
  
        </div>
      </div>
    </div>
  </template>
  