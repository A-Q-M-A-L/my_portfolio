<template>
    <!-- Contact ME -->
    <div class="backface-hidden absolute w-full h-full flex flex-col items-left space-y-12 lg:shadow-2xl rounded lg:shadow-white/5 lg:p-6"
        style="transform: rotateX(90deg) translateZ(322px);">

        <!-- Heading -->
        <div
            class="font-bold text-lg lg:text-3xl tracking-wide text-shadow text-shadow-lg text-shadow-green-900 text-green-400 flex flex-col lg:flex-row space-y-5 lg:space-y-0 items-center justify-between">
            <p class="text-left w-full">Contact Me</p>

            <div class="mt-4 lg:mt-0 flex items-center justify-center space-x-2 text-shadow-none text-[1rem]">

                <a href="https://www.linkedin.com/in/akmal-faraz-591756319" target="_blank" aria-label="LinkedIn">
                    <div
                        class="flex items-center justify-center border-[7px] hover:bg-green-500 hover:text-white border-transparent outline-1 outline-green-500 rounded-full cursor-pointer">
                        <span class="pi pi-linkedin"></span>
                    </div>
                </a>

                <a href="https://www.instagram.com/a.k.m.a_l/" target="_blank" aria-label="Instagram">
                    <div
                        class="flex items-center justify-center border-[7px] hover:bg-green-500 hover:text-white border-transparent outline-1 outline-green-500 rounded-full cursor-pointer">
                        <span class="pi pi-instagram"></span>
                    </div>
                </a>

                <a href="https://web.facebook.com/profile.php?id=100093138069993" target="_blank" aria-label="Facebook">
                    <div
                        class="flex items-center justify-center border-[7px] hover:bg-green-500 hover:text-white border-transparent outline-1 outline-green-500 rounded-full cursor-pointer">
                        <span class="pi pi-facebook"></span>
                    </div>
                </a>

                <a href="mailto:aqmalfaraz@gmail.com" aria-label="Email">
                    <div
                        class="flex items-center justify-center border-[7px] hover:bg-green-500 hover:text-white border-transparent outline-1 outline-green-500 rounded-full cursor-pointer">
                        <span class="pi pi-envelope"></span>
                    </div>
                </a>

            </div>
        </div>

        <!-- Form Section -->
        <div class="w-full mx-auto rounded-lg  h-full text-sm font-light relative">
            <form v-if="!submitted && !loader" @submit.prevent="handleSubmit" ref="formRef" class="space-y-4"
                enctype="multipart/form-data">

                <!-- Spam honeypot -->
                <input type="text" name="_honey" style="display:none">
                <input type="hidden" name="_captcha" value="false">
                <input type="hidden" name="_template" value="box">

                <div>
                    <label class="block text-white text-sm font-medium mb-1">Name</label>
                    <input type="text" name="name" v-model="form.name" required
                        class="w-full px-4 py-2 border border-slate-300 rounded-md outline-none focus:border-white" />
                </div>

                <div>
                    <label class="block text-white text-sm font-medium mb-1">Email</label>
                    <input type="email" name="email" v-model="form.email" required
                        class="w-full px-4 py-2 border border-slate-300 rounded-md focus:border-white outline-none" />
                </div>

                <div>
                    <label class="block text-white text-sm font-medium mb-1">Message</label>
                    <textarea name="message" v-model="form.message" required
                        class="w-full px-4 py-2 border border-slate-300 rounded-md focus:border-white outline-none"
                        rows="4"></textarea>
                </div>

                <div>
                    <label class="block text-white text-sm font-medium mb-1">Attach Document (optional)</label>
                    <input type="file" name="attachment" ref="fileRef"
                        class="w-full px-4 py-2 border border-slate-300 rounded-md focus:border-white outline-none" />
                </div>

                <button type="submit" :disabled="loader"
                    class="bg-green-500 hover:bg-green-600 text-white px-4 py-2 rounded-md transition duration-300 cursor-pointer disabled:opacity-50 disabled:cursor-not-allowed lg:mt-4 mt-0">
                    Send Message
                </button>
            </form>

            <!-- Thank You Section -->
            <div v-else-if="submitted && !loader" class="text-center space-y-4 p-6 flex items-center justify-center h-full flex-col">
                <h2 class="text-2xl font-semibold text-green-500">Thank You!</h2>
                <p class="text-slate-600">Your message has been successfully sent. I’ll get back to you soon.</p>
                <button class="text-green-500 underline hover:text-green-600 cursor-pointer" @click="resetForm">
                    Send another message
                </button>
            </div>

            <!-- Loader -->
            <div v-if="loader" class="absolute inset-0 flex justify-center items-center z-20">
                <div class="relative w-16 h-16 animate-[spin_1.2s_linear_infinite]">
                    <div v-for="n in 7" :key="n"
                        :style="{ transform: `rotate(${n * 360 / 7}deg) translate(0, -1.2rem)` }"
                        class="absolute top-1/2 left-1/2 w-2 h-2 bg-green-500 rounded-full animate-spin-dot">
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>
import { ref } from 'vue'

const submitted = ref(false)
const loader = ref(false)
const formRef = ref(null)
const fileRef = ref(null)

const form = ref({
    name: '',
    email: '',
    message: ''
})

const handleSubmit = async () => {
    loader.value = true;
    const data = new FormData(formRef.value)
    if (fileRef.value?.files[0]) {
        data.append("attachment", fileRef.value.files[0])
    }

    try {
        await fetch("https://formsubmit.co/aqmalfaraz@gmail.com", {
            method: "POST",
            body: data
        })
        submitted.value = true
    } catch (error) {
        alert("Error sending message. Please try again.")
    } finally {
        loader.value = false
    }
}

const resetForm = () => {
    form.value = { name: '', email: '', message: '' }
    submitted.value = false
    formRef.value.reset()
    if (fileRef.value) fileRef.value.value = null
}
</script>

<style scoped>
@keyframes pulse-scale {
    0%, 100% {
        transform: scale(1);
        opacity: 0.3;
    }
    50% {
        transform: scale(1.5);
        opacity: 1;
    }
}

.animate-spin-dot {
    animation: pulse-scale 1.2s infinite ease-in-out;
}
</style>
