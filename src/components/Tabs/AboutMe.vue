<template>
    <div class="backface-hidden absolute w-full h-full flex items-center justify-center text-white lg:shadow-2xl rounded lg:shadow-black/35"
        style="transform: rotateY(90deg) translateZ(400px);">

        <!-- Scrollable Container -->
        <div class="relative w-full h-full p-3 overflow-y-auto sm:max-h-[98vh] sm:min-h-[80vh]">

            <div class="max-w-full h-full mx-auto flex flex-col space-y-5">
                <div class="w-full lg:p-3 flex flex-col space-y-10">

                    <!-- Name and Description -->
                    <div class="w-full flex flex-col space-y-5">
                        <div
                            class="font-bold text-lg lg:text-3xl tracking-wide text-shadow text-shadow-lg text-shadow-green-900 text-green-500">
                            About Me
                        </div>

                        <p class="text-xs tracking-wide">
                            Hi! I&#96;m <span class="text-green-500">AKMAL</span>, A <span class="text-green-500">Web
                                Developer</span>
                        </p>

                        <p class="text-xs lg:tracking-wide font-light text-justify lg:text-left">
                            I am a skilled Full Stack Developer specializing in HTML, CSS, JavaScript, Vue.js, Node.js,
                            Express.js, Pug, MongoDB, and Tailwind CSS. Known
                            for crafting seamless user experiences and scalable applications, I excel in driving project
                            success through innovation and precision.
                        </p>
                    </div>

                    <!-- My Expertise and Langs -->
                    <div class="about-flex">
                        <!-- Info -->
                        <div class="w-full h-fit flex flex-col items-center justify-between space-y-5">
                            <div class="about-desc">
                                <div class="about-exp">
                                    <p class="text-green-600">Experience :</p>
                                    <p>4+ years</p>
                                </div>
                                <div class="about-exp">
                                    <p class="text-green-600">Country :</p>
                                    <p>Pakistan</p>
                                </div>
                            </div>

                            <div class="about-desc">
                                <div class="about-exp">
                                    <p class="text-green-600">Availability :</p>
                                    <p>24/7</p>
                                </div>
                                <div class="about-exp">
                                    <p class="text-green-600">Satisfied Clients:</p>
                                    <p>200+</p>
                                </div>
                            </div>

                            <div class="about-desc">
                                <div class="about-exp">
                                    <p class="text-green-600">Phone No :</p>
                                    <p>+923428999005</p>
                                </div>
                                <div class="about-exp">
                                    <p class="text-green-600">Degree :</p>
                                    <p>CS</p>
                                </div>
                            </div>
                        </div>

                        <!-- Skills -->
                        <div class="w-full h-full flex flex-col space-y-4 text-xs">
                            <div>
                                <strong class="font-light">HTML 5</strong>
                                <div class="relative w-full h-[4px] bg-[linear-gradient(to_right,_#22c55e_100%,_transparent_0%)]"
                                    id="lang"></div>
                            </div>
                            <div>
                                <strong class="font-light">CSS</strong>
                                <div class="relative w-full h-[4px] bg-[linear-gradient(to_right,_#22c55e_87%,_transparent_100%)]"
                                    id="lang"></div>
                            </div>
                            <div>
                                <strong class="font-light">JavaScript</strong>
                                <div class="relative w-full h-[4px] bg-[linear-gradient(to_right,_#22c55e_75%,_transparent_90%)]"
                                    id="lang"></div>
                            </div>
                            <div>
                                <strong class="font-light">Vue Js</strong>
                                <div class="relative w-full h-[4px] bg-[linear-gradient(to_right,_#22c55e_75%,_transparent_90%)]"
                                    id="lang"></div>
                            </div>
                            <div>
                                <strong class="font-light">Tailwind Css</strong>
                                <div class="relative w-full h-[4px] bg-[linear-gradient(to_right,_#22c55e_87%,_transparent_100%)]"
                                    id="lang"></div>
                            </div>
                            <div>
                                <strong class="font-light">Node Js</strong>
                                <div class="relative w-full h-[4px] bg-[linear-gradient(to_right,_#22c55e_70%,_transparent_100%)]"
                                    id="lang"></div>
                            </div>
                            <div>
                                <strong class="font-light">Express Js</strong>
                                <div class="relative w-full h-[4px] bg-[linear-gradient(to_right,_#22c55e_80%,_transparent_100%)]"
                                    id="lang"></div>
                            </div>
                            <div>
                                <strong class="font-light">Mongo DB</strong>
                                <div class="relative w-full h-[4px] bg-[linear-gradient(to_right,_#22c55e_60%,_transparent_85%)]"
                                    id="lang"></div>
                            </div>
                        </div>
                    </div>

                    <!-- Buttons -->
                    <div class="max-w-full lg:max-w-3/6 flex items-center justify-center space-x-3 lg:px-3 pb-4">
                        <button @click="$emit('changeTab', '5')"
                            class="px-2 py-1 border border-green-500 rounded-sm text-green-500 hover:bg-green-500 hover:text-white cursor-pointer duration-300 text-xs lg:text-sm font-extralight w-full">
                            Contact Me
                        </button>
                        <a class="w-full" href="mailto:aqmalfaraz@gmail.com">
                            <button
                                class="px-2 py-1 bg-green-500 hover:bg-green-400 cursor-pointer rounded-sm duration-300 text-xs lg:text-sm font-extralight w-full">
                                Hire Me
                            </button>
                        </a>
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
    border: 1px solid transparent;
    outline: 1px solid green;
    width: 100%;
    inset: 0;
    z-index: -1;
}
</style>