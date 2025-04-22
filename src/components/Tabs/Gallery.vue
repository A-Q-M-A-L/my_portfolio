<template>
    <!-- Gallery -->
    <div
      class="backface-hidden absolute w-full h-full flex items-center justify-center font-bold text-white lg:shadow-2xl rounded lg:shadow-black/35 backdrop-blur-xs"
      style="transform: rotateY(-90deg) translateZ(400px);">
  
      <!-- Scrollable Container on Small Screens -->
      <div class="relative w-full h-full p-3 overflow-y-auto sm:max-h-[98vh] sm:min-h-[80vh]">
  
        <!-- Wrapper -->
        <div class="max-w-full h-full mx-auto flex flex-col space-y-4">
  
          <!-- Heading -->
          <div class="font-bold text-lg lg:text-3xl tracking-wide text-shadow text-shadow-lg text-shadow-green-900 text-green-500">
            Gallery
          </div>
  
          <!-- Gallery Grid -->
          <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-5 lg:gap-2 w-full pb-2">
  
            <!-- AppLuncher Pro -->
            <div class="gallery-app group">
              <div class="gallery-app-second-gradient">
                <p class="absolute bottom-2.5 left-3 gallery-app-text">AppLuncher Pro</p>
              </div>
              <img src="../../assets/Images/projects/1.png" class="gallery-app-image" alt="">
            </div>
  
            <!-- LoopStudio -->
            <div class="gallery-app group">
              <div class="gallery-app-second-gradient">
                <p class="absolute bottom-2.5 left-3 gallery-app-text">LoopStudio</p>
              </div>
              <img src="../../assets/Images/projects/2.png" class="gallery-app-image" alt="">
            </div>
  
            <!-- ProamSoft Ball -->
            <div class="gallery-app group">
              <div class="gallery-app-second-gradient">
                <p class="absolute bottom-2.5 left-3 gallery-app-text">ProamSoft Ball</p>
              </div>
              <img src="../../assets/Images/projects/3.png" class="gallery-app-image" alt="">
            </div>
  
          </div>
        </div>
      </div>
    </div>
  </template>
  