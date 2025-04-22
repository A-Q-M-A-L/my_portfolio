<template>
    <div class="backface-hidden absolute w-full h-full lg:shadow-2xl rounded lg:shadow-black/35 flex items-center justify-center text-white backdrop-blur-xs"
        style="transform: rotateY(180deg) translateZ(400px);">


        <div class="relative w-full h-full p-3">

            <!-- Wrapper -->
            <div class="max-w-full h-full mx-auto flex flex-col space-y-4">

                <!-- Heading -->
                <div
                    class="font-bold text-lg lg:text-3xl tracking-wide text-shadow text-shadow-lg text-shadow-green-900 text-green-500">
                    Services
                </div>

                <!-- Service Grid -->
                <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-2 w-full">

                    <!-- Service Box (repeat this for each) -->
                    <div
                        class="bg-black/30 hover:text-white text-green-500 hover:bg-green-600 rounded-sm hover:scale-105 duration-300 cursor-pointer hover:shadow-2xl hover:shadow-green-500/15 aspect-square flex flex-col items-center justify-center font-semibold text-center p-2 space-y-3">
                        <span class="pi pi-globe text-xl"></span>
                        <div>Custom Web Application</div>
                        <span class="text-[0.60em] font-light">Build scalable, feature-rich web applications from
                            scratch.</span>
                    </div>
                    <div
                        class="bg-black/30 hover:text-white text-green-500 hover:bg-green-600 rounded-sm hover:scale-105 duration-300 cursor-pointer hover:shadow-2xl hover:shadow-green-500/15 aspect-square flex flex-col items-center justify-center font-semibold text-center p-2 space-y-3">
                        <span class="pi pi-desktop text-xl"></span>
                        <div>Responsive Frontend</div>
                        <span class="text-[0.60em] font-light">Design mobile-first, pixel-perfect user
                            interfaces.</span>
                    </div>
                    <div
                        class="bg-black/30 hover:text-white text-green-500 hover:bg-green-600 rounded-sm hover:scale-105 duration-300 cursor-pointer hover:shadow-2xl hover:shadow-green-500/15 aspect-square flex flex-col items-center justify-center font-semibold text-center p-2 space-y-3">
                        <span class="pi pi-cloud text-xl"></span>
                        <div> Backend API</div>
                        <span class="text-[0.60em] font-light">Develop secure and efficient RESTful APIs.</span>
                    </div>
                    <div
                        class="bg-black/30 hover:text-white text-green-500 hover:bg-green-600 rounded-sm hover:scale-105 duration-300 cursor-pointer hover:shadow-2xl hover:shadow-green-500/15 aspect-square flex flex-col items-center justify-center font-semibold text-center p-2 space-y-3">
                        <span class="pi pi-shield text-xl"></span>
                        <div>Authentication Systems</div>
                        <span class="text-[0.60em] font-light">Implement secure login, roles, and access control.</span>
                    </div>
                    <div
                        class="bg-black/30 hover:text-white text-green-500 hover:bg-green-600 rounded-sm hover:scale-105 duration-300 cursor-pointer hover:shadow-2xl hover:shadow-green-500/15 aspect-square flex flex-col items-center justify-center font-semibold text-center p-2 space-y-3">
                        <span class="pi pi-database text-xl"></span>
                        <div>Database Integration</div>
                        <span class="text-[0.60em] font-light">Structure and connect databases for fast, reliable data flow.</span>
                    </div>
                    <div
                        class="bg-black/30 hover:text-white text-green-500 hover:bg-green-600 rounded-sm hover:scale-105 duration-300 cursor-pointer hover:shadow-2xl hover:shadow-green-500/15 aspect-square flex flex-col items-center justify-center font-semibold text-center p-2 space-y-3">
                        <span class="pi pi-gauge text-xl"></span>
                        Performance Optimization
                        <span class="text-[0.60em] font-light">Speed up websites with modern optimization techniques.</span>
                    </div>

                </div>
            </div>




        </div>


    </div>
</template>