<template>
    <div
        class="lg:flex justify-center w-52 bg-gray-900/90 shadow-2xl shadow-blue-900/25 h-full  hidden">

        <div class="flex flex-col space-y-20 p-4">

            <!-- Profile Picture -->
            <div class="pt-7">
                <div
                    class="w-[130px] h-[130px] rounded-full border-2 border-transparent outline-2 outline-green-400 overflow-hidden cursor-pointer">
                    <img src="../../assets/Images/me.jpg" class="w-full h-full object-cover bg-top" alt="Profile">
                </div>
            </div>

            <!-- Tabs -->
            <div class="w-full flex flex-col space-y-4">
                <!-- Home -->
                <div @click="tabNo('1')"
                    class="flex items-center space-x-2 hover:bg-green-500 cursor-pointer rounded-tl-2xl rounded-br-2xl p-2 w-full" :class="{ 'bg-green-500': no == 1 }" >
                    <span class="pi pi-home"></span>
                    <span>Home</span>
                </div>

                <!-- About Me -->
                <div @click="tabNo('2')"
                    class="flex items-center space-x-2 hover:bg-green-500 cursor-pointer rounded-sm rounded-tl-2xl rounded-br-2xl p-2 w-full" :class="{ 'bg-green-500': no == 2 }">
                    <span class="pi pi-user"></span>
                    <span>About Me</span>
                </div>

                <!-- Services -->
                <div @click="tabNo('3')"
                    class="flex items-center space-x-2 hover:bg-green-500 cursor-pointer rounded-sm rounded-tl-2xl rounded-br-2xl p-2 w-full" :class="{ 'bg-green-500': no == 3 }">
                    <span class="pi pi-sparkles"></span>
                    <span>Services</span>
                </div>

                <!-- Gallrey -->
                <div @click="tabNo('4')"
                    class="flex items-center space-x-2 hover:bg-green-500 cursor-pointer rounded-sm rounded-tl-2xl rounded-br-2xl p-2 w-full" :class="{ 'bg-green-500': no == 4 }">
                    <span class="pi pi-images"></span>
                    <span>Gallrey</span>
                </div>

                <!-- Contact Me -->
                <div @click="tabNo('5')"
                    class="flex items-center space-x-2 hover:bg-green-500 cursor-pointer rounded-sm rounded-tl-2xl rounded-br-2xl p-2 w-full" :class="{ 'bg-green-500': no == 5 }">
                    <span class="pi pi-inbox"></span>
                    <span>Contact Me</span>
                </div>
            </div>

        </div>
    </div>
</template>


<script>
export default {
    data() {
        return {
            no: "1"
        }
    },
    methods: {
        tabNo(no) {
            this.no = no
            this.$emit('tab-changed', no)
            
        }
    }
}
</script>