<template>
    <div>
        <section class="container mt-8 mb-16">
            <carousel class="text-white" :items-to-show="1" wrap-around>
                <slide :key="slide">
                    <img
                        class="w-full h-[200px] md:h-[350px] lg:h-[500px] rounded-lg"
                        src="slide-1.jpg"
                    />
                </slide>
                <slide :key="slide">
                    <img
                        class="w-full h-[200px] md:h-[350px] lg:h-[500px] rounded-lg"
                        src="slide-2.jpg"
                    />
                </slide>

                <template #addons>
                    <navigation />
                </template>
            </carousel>
        </section>

        <section class="container grid grid-cols-2 gap-6 my-16">
            <div class="col-span-2 border-t-4 border-white lg:col-span-1">
                <h2 class="my-4 text-xl">Recently Watched</h2>
                <DramaBox
                    imageSrc="movie-1.jpg"
                    title="Fight Club (2001)"
                    updatedAt="4 hours ago"
                />
            </div>
            <div class="col-span-2 border-t-4 border-white lg:col-span-1">
                <h2 class="my-4 text-xl">Recently Watched</h2>
                <div
                    class="grid items-start grid-cols-2 jusify-between gap-x-6 gap-y-4"
                >
                    <div v-for="item in 4" class="col-span-1">
                        <DramaBox
                            imageSrc="movie-1.jpg"
                            title="Fight Club (2001)"
                            updatedAt="4 hours ago"
                        />
                    </div>
                </div>
            </div>
        </section>
        <section class="container my-16">
            <h2 class="mb-8 text-lg">Most Popular Drama</h2>
            <div
                class="flex py-4 overflow-x-scroll hide-scroll-bar scrollbar-thin scrollbar-thumb-gray-700 scrollbar-track-gray-300"
            >
                <div class="flex flex-nowrap gap-x-8 lg:gap-x-16">
                    <DramaTile
                        v-for="item in 10"
                        imgSrc="/movie-2.jpg"
                        title="Game of Thrones"
                        :seasons="8"
                        :episodes="80"
                    />
                </div>
            </div>
        </section>

        <Footer />
    </div>
</template>

<script>
import "vue3-carousel/dist/carousel.css";
import { Carousel, Slide, Navigation } from "vue3-carousel";
import DramaBox from "../components/Home/DramaBox.vue";
import DramaTile from "../components/Home/DramaTile.vue";
import Footer from "../components/Layout/Footer.vue";

export default {
    name: "Home",
    components: {
        Carousel,
        Slide,
        Navigation,
        DramaBox,
        DramaTile,
        Footer,
    },
};
</script>

<style>
.carousel__icon {
    color: white;
}
</style>
