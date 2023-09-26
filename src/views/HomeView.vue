<template>
    <nav class="w-full fixed top-0 bg-slate-200 p-4 flex justify-between items-center">
        <h2 class="md:text-2xl text-md font-bold ">Apple Page</h2>
        <ul class="flex items-center space-x-4">
            <li>
                <router-link to="" class="md:text-md text-sm">Home</router-link>
            </li>
            <li>
                <router-link to="" class="md:text-md text-sm">About</router-link>
            </li>
            <li>
                <router-link to="" class="md:text-md text-sm">Products</router-link>
            </li>
            <li>
                <router-link to="" class="md:text-md text-sm">Contacts</router-link>
            </li>
        </ul>
    </nav>
    <section class="w-full min-h-[300px] bg-slate-100 flex items-center md:flex-nowrap flex-wrap pt-10">
        <div class="md:w-1/2 w-full flex flex-col flex-wrap justify-center py-4 px-8 md:order-1 order-2">
            <p class="md:text-3xl text-xl uppercase font-bold mb-2 md:text-left text-center">Apple Page Store</p>
            <p>Menyediakan produk produk berkualitasi dari apple</p>
        </div>
        <div class="md:w-1/2 w-full md:order-2 order-1">
            <img :src="mb1" alt="" class="w-[80%] h-[90%] block mx-auto">
        </div>
    </section>
    <section class="w-full min-h-[300px] flex items-center md:flex md:flex-nowrap flex-wrap">
        <div class="md:w-1/2 w-full flex flex-col flex-wrap justify-center py-4 px-8 md:order-1 order-2">
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Qui officia, neque? Perspiciatis molestias dolorum, neque tempore! Excepturi pariatur inventore non architecto voluptatem similique deserunt, fugit laudantium tenetur asperiores dignissimos, aut.</p>
        </div>
        <div class="md:w-1/2 w-full p-8 h-full md:order-2 order-1">
            <img :src="image2" alt="" class="w-[90%] h-[90%] block mx-auto">
        </div>
    </section>
    <section class="mt-2">
        <p class="text-center md:text-2xl">PRODUCT KAMI</p>
        <div class="w-full min-h-[300px] flex items-center p-8 flex-wrap justify-center space-x-2 ">
            <div class="md:w-[24%] w-[90%] min-h-[350px] shadow-lg mb-2 overflow-hidden rounded-md hover:shadow-md" v-for="i in data" :key="i">
                <img :src="`/src/assets/img/${i.image}`" alt="" class="w-full h-[200px]">
                <div class="h-[150px] p-4 flex items-center">
                    <p>{{i.name}}</p>
                </div>
            </div>
        </div>
    </section>
    <footer class="px-4 py-8 bg-slate-900">
        <p class="text-white ml-8 mb-4 text-xl font-bold">Follow Me</p>
        <ul class="ml-8">
            <li class="mb-2"><a href="" class="text-white">Gmail</a></li>
            <li class="mb-2"><a href="" class="text-white">Facebook</a></li>
            <li class="mb-2"><a href="" class="text-white">Whatsapp</a></li>
        </ul>
        <p class="text-center text-white">CopyRight By Apple Page</p>
    </footer>
</template>
<script setup>
import mb1 from "@/assets/img/mb-1-removebg-preview.png"
import image2 from "@/assets/img/image-2.jpg"
import data from "@/assets/data/product.json"
</script>