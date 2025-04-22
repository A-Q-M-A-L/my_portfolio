<template>
    <div class="backface-hidden absolute w-full h-full flex items-center justify-center text-white lg:shadow-2xl rounded lg:shadow-black/35 backdrop-blur-xs "
        style="transform: rotateY(90deg) translateZ(400px);">


        <div class="relative w-full h-full p-3">

            <div class="max-w-full h-full mx-auto flex flex-col space-y-5">


                <div class="w-full lg:p-3 flex flex-col space-y-10">

                    <!-- Name and discripition -->
                    <div class="w-full flex flex-col space-y-5 ">
                        <div
                            class="font-bold text-lg lg:text-3xl tracking-wide text-shadow text-shadow-lg text-shadow-green-900 text-green-500">
                            About Me</div>


                        <p class="text-xs tracking-wide">
                            Hi! I`m <span class="text-green-500">AKMAL</span>,

                            A <span class="text-green-500">Web Developer</span>
                        </p>

                        <p class="text-xs lg:tracking-wide font-light text-justify lg:text-left">I am a skilled Full Stack Developer specializing
                            in HTML, CSS, JavaScript, Vue.js, Node.js, Express.js, Pug, MongoDB, and Tailwind CSS. Known
                            for crafting seamless user experiences and scalable applications, I excel in driving project
                            success through innovation and precision.
                        </p>
                    </div>

                    <!-- My Expertise and Langs -->

                    <div class="about-flex">

                        <!-- Name Country phone Etc... -->
                        <div class="w-full h-fit flex flex-col items-center justify-between space-y-5">
                            <!-- Experience and Country -->
                            <div class="about-desc">
                                <!-- Experience -->
                                <div class="about-exp">
                                    <p class="text-green-600">Experience :</p>
                                    <p>4+ years</p>
                                </div>


                                <!-- Country -->
                                <div class="about-exp">
                                    <p class="text-green-600">Country :</p>
                                    <p>Pakistan</p>
                                </div>
                            </div>

                            <!-- Availability and satisfied Clients -->
                            <div class="about-desc">
                                <!-- Availability -->
                                <div class="about-exp">
                                    <p class="text-green-600">Availability :</p>
                                    <p>24/7</p>
                                </div>


                                <!-- satisfied Clients -->
                                <div class="about-exp">
                                    <p class="text-green-600">Satisfied Clients:</p>
                                    <p>200+</p>
                                </div>
                            </div>


                            <!-- Phone No and satisfied Clients -->
                            <div class="about-desc">
                                <!-- Phone No -->
                                <div class="about-exp">
                                    <p class="text-green-600">Phone No :</p>
                                    <p>+923428999005</p>
                                </div>


                                <!-- satisfied Clients -->
                                <div class="about-exp">
                                    <p class="text-green-600">Degree :</p>
                                    <p>CS</p>
                                </div>
                            </div>


                        </div>

                        <!-- My Expertise in Languages -->
                        <div class="w-full h-full flex flex-col space-y-4 text-xs">

                            <div>
                                <strong class="font-light">HTML 5</strong>
                                <div id="lang"
                                    class="relative w-full h-[4px] bg-[linear-gradient(to_right,_#22c55e_100%,_transparent_0%)]">
                                </div>
                            </div>

                            <div>
                                <strong class="font-light">CSS</strong>
                                <div id="lang"
                                    class="relative w-full h-[4px] bg-[linear-gradient(to_right,_#22c55e_87%,_transparent_100%)]">
                                </div>
                            </div>

                            <div>
                                <strong class="font-light">JavaScript</strong>
                                <div id="lang"
                                    class="relative w-full h-[4px] bg-[linear-gradient(to_right,_#22c55e_75%,_transparent_90%)]">
                                </div>
                            </div>

                            <div>
                                <strong class="font-light">Vue Js</strong>
                                <div id="lang"
                                    class="relative w-full h-[4px] bg-[linear-gradient(to_right,_#22c55e_75%,_transparent_90%)]">
                                </div>
                            </div>

                            <div>
                                <strong class="font-light">Tailwind Css</strong>
                                <div id="lang"
                                    class="relative w-full h-[4px] bg-[linear-gradient(to_right,_#22c55e_87%,_transparent_100%)]">
                                </div>
                            </div>

                            <div>
                                <strong class="font-light">Node Js</strong>
                                <div id="lang"
                                    class="relative w-full h-[4px] bg-[linear-gradient(to_right,_#22c55e_70%,_transparent_100%)]">
                                </div>
                            </div>

                            <div>
                                <strong class="font-light">Express Js</strong>
                                <div id="lang"
                                    class="relative w-full h-[4px] bg-[linear-gradient(to_right,_#22c55e_80%,_transparent_100%)]">
                                </div>
                            </div>

                            <div>
                                <strong class="font-light">Mongo DB</strong>
                                <div id="lang"
                                    class="relative w-full h-[4px] bg-[linear-gradient(to_right,_#22c55e_60%,_transparent_85%)]">
                                </div>
                            </div>



                        </div>
                    </div>

                    <!-- Hire me and Contact Me Buttons -->
                    <div class="max-w-full lg:max-w-3/6 flex items-center justify-center space-x-3 lg:px-3">


                        <button
                            class="px-2 py-1 border border-green-500 rounded-sm text-green-500 hover:bg-green-500 hover:text-white cursor-pointer duration-300 text-xs lg:text-sm font-extralight w-full">Contact
                            Me</button>


                        <button
                            class="px-2 py-1 bg-green-500 hover:bg-green-400 cursor-pointer rounded-sm duration-300 text-xs lg:text-sm font-extralight w-full">Hire
                            Me</button>

                    </div>
                </div>

         


            </div>



        </div>




    </div>
</template>


<style scoped>
#lang::before {

    content: '';
    position: absolute;
    /* background: rgb(6, 47, 233); */
    border: 1px solid transparent;
    outline: 1px solid green;
    width: 100%;
    inset: 0;
    z-index: -1;
}
</style>