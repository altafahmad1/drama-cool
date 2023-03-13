<template>
    <section class="container">
        <carousel class="text-white" :items-to-show="1" wrap-around>
            <slide :key="slide">
                <img class="w-full h-[500px] rounded-lg" src="slide-1.jpg" />
            </slide>
            <slide :key="slide">
                <img class="w-full h-[500px] rounded-lg" src="slide-2.jpg" />
            </slide>

            <template #addons>
                <navigation />
            </template>
        </carousel>
    </section>

    <section class="container grid grid-cols-2 mt-8 gap-x-6">
        <div class="col-span-1 border-t-4 border-white">
            <h2 class="my-4 text-xl">Recently Watched</h2>
            <drama-box
                imageSrc="movie-1.jpg"
                title="Fight Club (2001)"
                updatedAt="4 hours ago"
            />
        </div>
        <div class="col-span-1 border-t-4 border-white">
            <h2 class="my-4 text-xl">Recently Watched</h2>
            <div
                class="grid items-start grid-cols-2 jusify-between gap-x-6 gap-y-4"
            >
                <div v-for="item in 4" class="col-span-1">
                    <drama-box
                        imageSrc="movie-1.jpg"
                        title="Fight Club (2001)"
                        updatedAt="4 hours ago"
                    />
                </div>
            </div>
        </div>
    </section>

    <section class="container mt-8">Hello World</section>
</template>

<script>
// If you are using PurgeCSS, make sure to whitelist the carousel CSS classes
import "vue3-carousel/dist/carousel.css";
import { Carousel, Slide, Navigation } from "vue3-carousel";
import DramaBox from "../components/Home/DramaBox.vue";

export default {
    name: "Home",
    components: {
        Carousel,
        Slide,
        Navigation,
        DramaBox,
    },
};
</script>

<style>
.carousel__icon {
    color: white;
}
</style>
