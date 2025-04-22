<template>
    <!-- Hero -->
    <div class="grow w-full h-full lg:mx-6 flex items-center justify-center ">
        <div class="lg:w-[85%] w-full h-[85%]  px-6">

            <!-- Custom Hamburger -->
            <div @click="toggleMenu" class="w-full flex justify-end">
                <button id="menu-btn" type="button" class="z-40 block hamburger lg:hidden focus:outline-none">
                    <span class="hamburger-top"></span>
                    <span class="hamburger-middle"></span>
                    <span class="hamburger-bottom"></span>
                </button>
            </div>


            <!-- mobile menu -->
            <div id="menu"
                class="absolute top-0 bottom-0 left-0 hidden flex-col self-end w-full min-h-screen items-center justify-center  space-y-3 text-lg text-white uppercase bg-gradient-to-bl from-transparent via-[#084b028c] to-transparent z-30 lg:hidden">

                <div class="flex flex-col items-center space-y-11">

                    <!-- Profile Picture -->
                    <div class="pt-7">
                        <div
                            class="w-[65px] h-[65px] rounded-full border-2 border-transparent outline-2 outline-green-400 overflow-hidden cursor-pointer">
                            <img src="../assets/Images/me.jpg" class="w-full h-full object-cover bg-top" alt="Profile">
                        </div>
                    </div>

                    <!-- Mob Menu -->
                    <div class="w-full flex flex-col space-y-4">
                        <!-- Home -->
                        <div @click="rotateTo('1')"
                            class="flex items-center  space-x-2 hover:bg-green-500 cursor-pointer rounded-tl-2xl rounded-br-2xl p-2 w-full">
                            <span class="pi pi-home"></span>
                            <span>Home</span>
                        </div>

                        <!-- About Me -->
                        <div @click="rotateTo('2')"
                            class="flex items-center space-x-2 hover:bg-green-500 cursor-pointer rounded-sm rounded-tl-2xl rounded-br-2xl p-2 w-full">
                            <span class="pi pi-user"></span>
                            <span>About Me</span>
                        </div>

                        <!-- Services -->
                        <div @click="rotateTo('3')"
                            class="flex items-center space-x-2 hover:bg-green-500 cursor-pointer rounded-sm rounded-tl-2xl rounded-br-2xl p-2 w-full">
                            <span class="pi pi-sparkles"></span>
                            <span>Services</span>
                        </div>

                        <!-- Gallrey -->
                        <div @click="rotateTo('4')"
                            class="flex items-center space-x-2 hover:bg-green-500 cursor-pointer rounded-sm rounded-tl-2xl rounded-br-2xl p-2 w-full">
                            <span class="pi pi-images"></span>
                            <span>Gallrey</span>
                        </div>

                        <!-- Contact Me -->
                        <div @click="rotateTo('5')"
                            class="flex items-center space-x-2 hover:bg-green-500 cursor-pointer rounded-sm rounded-tl-2xl rounded-br-2xl p-2 w-full">
                            <span class="pi pi-inbox"></span>
                            <span>Contact Me</span>
                        </div>
                    </div>
                </div>
            </div>


            <div class="relative w-full h-full " style="perspective: 4000px;">
                <div class="absolute w-full h-full transform-style preserve-3d duration-300"
                    :style="{ transform: `${`rotateY(${rotateY}deg)`} ${rotateX ? `rotateX(${rotateX}deg)` : ''}` }">
                    <!-- Home -->
                    <Home @changeTab="rotateTo($event)" />

                    <!-- About me -->
                    <AboutMe @changeTab="rotateTo($event)" />

                    <!-- Services -->
                    <Services />

                    <!-- Gallrey -->
                    <Gallery />

                    <!-- Contact Me -->
                    <Contact />

                    

                </div>

            </div>
        </div>

    </div>
</template>


<script>
import Home from './Tabs/Home.vue';
import AboutMe from './Tabs/AboutMe.vue'
import Services from './Tabs/Services.vue';
import Gallery from './Tabs/Gallery.vue';
import Contact from './Tabs/Contact.vue';






export default {
    props: {
        tabNo: {
            type: String,
            required: true // or false if it's optional
            // default: 1   // you can also set a default if needed
        }
    },
    components: {
        Home,
        AboutMe,
        Services,
        Gallery,
        Contact,
      
    },
    data() {
        return {
            rotateY: 0,
            isInitialTabWatch: true,
            rotateX: null,
        };
    },
    methods: {

        rotateTo(no) {


            const face = no || this.tabNo;

            if (no) {
            this.toggleMenu();
            }
            switch (face) {
                case '1':
                    this.rotateY = 0;
                    this.rotateX = 0
                    break;
                case '2':
                    this.rotateY = -90;
                    this.rotateX = 0
                    break;
                case '3':
                    this.rotateY = -180;
                    this.rotateX = 0
                    break;
                case '4':
                    this.rotateY = -270;
                    this.rotateX = 0
                    break;
                case '5':
                    this.rotateX = -90;
                    this.rotateY = 0
                    break;
            }
        },
        toggleMenu() {
            const hamburger = document.getElementById('menu-btn');
            const mobileMenu = document.getElementById('menu');

            hamburger.classList.toggle('open');
            mobileMenu.classList.toggle('hidden');
            mobileMenu.classList.toggle('flex');


            console.log("menu toggle");

        },

    },
    watch: {
        tabNo: {
            immediate: true,
            handler(newVal, oldVal) {
                console.log('tabNo changed:', oldVal, '->', newVal);
                this.rotateTo();

            }

        }
    }
}

</script>


<style scoped>
.perspective {
    perspective: 1500px;
}

.preserve-3d {
    transform-style: preserve-3d;
    transform-origin: center;
    transition: transform 1s ease;
}



/* Optional: add smoother edges by using anti-aliasing */
* {
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
}
</style>