<script setup>
import { ref } from 'vue';
import { router } from '@inertiajs/vue3';
import { Link } from '@inertiajs/inertia-vue3';
import TweetyPielogo from 'vue-material-design-icons/Twitter.vue';
import Magnify from 'vue-material-design-icons/Magnify.vue';
import DotsHorizontal from 'vue-material-design-icons/DotsHorizontal.vue';
import Feather from 'vue-material-design-icons/Feather.vue';
import Close from 'vue-material-design-icons/Close.vue';
import ChevronDown from 'vue-material-design-icons/ChevronDown.vue';
import Earth from 'vue-material-design-icons/Earth.vue';
import ImageOutline from 'vue-material-design-icons/ImageOutline.vue';
import FileGifBox from 'vue-material-design-icons/FileGifBox.vue';
import Emoticon from 'vue-material-design-icons/Emoticon.vue';
import ArrowLeft from 'vue-material-design-icons/ArrowLeft.vue';
import MenuItem from '@/Components/MenuItem.vue';

let randImg2 = ref(`https://picsum.photos/id/${(Math.random() * 200).toFixed(0)}/100`);
</script>

<template>
    <div class="fixed w-full">
        <div id="nav" class="max-w-[1400px] flex mx-auto">
            <div class="lg:w-3/12 w-[60px] h-[100vh] max-w-[350px] lg:px-4 lg:mx-auto">
                <div class="p-2 px-3 mb-4">
                    <h2>Logo</h2>
                </div>
                <Link :href="route('post.home')"><MenuItem iconString="Home" ></MenuItem></Link>
                <!--
                <MenuItem iconString="Explore" />
                -->
                <Link :href="route('pages.notifications')"><MenuItem iconString="Notifications" /></Link>
                <Link :href="route('pages.messages')"><MenuItem iconString="Messages" /></Link>
                <Link :href="route('pages.profile')"><MenuItem iconString="Profile" /></Link>
            </div>
            <div class="lg:w-7/12 w-11/12 border-x border-gray-800 relative">
                <div class="bg-black bg-opacity-50 backdrop-blur-md z-10 absolute w-full">
                    <div class="border-gray-800 border-b w-full">
                        <div class="w-full text-white text-[22px] font-extrabold p-4">
                            Profile
                        </div>
                        <!-- aquí iría un div para poner la foto de perfil y una foto encima de la de pefil como "banner"-->

                        <div class="flex">
                            <div
                                class="flex items-center justify-center w-full h-[60px] text-white text-[17px] font-extrabold p-4 hover:bg-gray-500 hover:bg-opacity-30 cursor-pointer transition duration-200 ease-in-out">
                                <div class="inline-block text-center border-b-4 border-b-[#1C9CEF] h-[60px]">
                                    <div class="my-automt-4">Posts</div>
                                </div>
                            </div>
                            <div
                                class="w-full h-[60px] text-gray-500 text-[17px] font-extrabold p-4 hover:bg-gray-500 hover:bg-opacity-30 cursor-pointer transition duration-200 ease-in-out">
                                <div class="text-center">Multimedia</div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <div class="absolute top-0 z-0 overflow-auto scrollbar-hide">
                <div class="mt-[126px]">

                </div>
                <slot />
                <div class="pb-4">
                    
                </div>
            </div>
            <div class="lg:block hidden lg:w-4/12 h-screen border-l border-gray-800 pl-4">
                <div class="w-full p-1 mt-2 px-4 lg:flex items-center rounded-full hidden bg-[#212327]">
                    <Magnify fillcolor="#5e5c5c" :size="25" />
                    <input type="text" placeholder="Search" class="appeareance-none w-full border-0 py-2 bg-[#212327] text-gray-100 palceholder-gray-500 leading-tight focus:ring-0">
                </div>
                <div class="w-full mt-4 rounded-lg lg:block hidden bg-[#212327]">
                    <div class="w-full p-4 text-white font-extrabold mb-6 text-[20px]">
                        What's happening
                    </div>
                    <div class="h-[80px] hover:bg-gray-800 cursor-pointer transition duration-200 ease-in-out">
                        <div class="flex p-3 justify-between h-[80px] py-3">
                            <div>
                                <div class="text-[14px] text-gray-400">
                                    Basketball tournament LIVE
                                </div>
                                <div class="w-full text-white font-extrabold mb-6 text-[17px]">
                                    GP de Tourin 2023
                                </div>
                            </div>
                            <img class="rounded-xl" :src="randImg2" alt="" />
                        </div>
                    </div>
                    <div class="hover:bg-gray-800 cursor-pointer transition duration-200 ease-in-out">
                        <div class="flex p-3 justify-between">
                            <div>
                                <div class="text-[14px] text-gray-400">
                                    Trending at your country
                                </div>
                                <div class="w-full text-white font-extrabold text-[17px]">
                                    #ELNANO
                                </div>
                                <div class="text-[14px] text-gray-400">
                                    33,3k posts
                                </div>
                            </div>
                            <DotsHorizontal fillcolor="#5e5c5c" />
                        </div>
                    </div>
                    <div class="hover:bg-gray-800 cursor-pointer transition duration-200 ease-in-out">
                        <div class="flex p-3 justify-between">
                            <div>
                                <div class="text-[14px] text-gray-400">
                                    Trending - Sports
                                </div>
                                <div class="w-full text-white font-extrabold text-[17px]">
                                    #Alonso
                                </div>
                                <div class="text-[14px] text-gray-400">
                                    33,3k posts
                                </div>
                            </div>
                            <DotsHorizontal fillcolor="#5e5c5c" />
                        </div>
                    </div>
                    <div class="hover:bg-gray-800 cursor-pointer transition duration-200 ease-in-out">
                        <div class="flex p-3 justify-between">
                            <div>
                                <div class="text-[14px] text-gray-400">
                                    Trending - Politics
                                </div>
                                <div class="w-full text-white font-extrabold text-[17px]">
                                    #inflacion
                                </div>
                                <div class="text-[14px] text-gray-400">
                                    266,3k posts
                                </div>
                            </div>
                            <DotsHorizontal fillcolor="#5e5c5c" />
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import { Link } from "@inertiajs/inertia-vue3";
    export default {
        components:{
            Link
        },
        props:{
            posts: Object
        }
    }
</script>

<style>
body {
    background-color: lightgreen;
}

/* si se usa un móvil, cambia la vista de la barra de navegación a una vista de columna pegada a la izquierda de la pantalla */
@media (max-width: 1024px) {
    #nav {
        flex-direction: column;
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        z-index: 1;
    }

    /* mueve el icono del botón de postear al lado del icono */
    #post {
        margin-top: 45vh;
    }
}
</style>
