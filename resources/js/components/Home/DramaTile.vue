<template>
    <div class="inline-block w-36 lg:w-60 rounded-[10px]">
        <img :src="imgSrc" class="w-full rounded-[10px]" />
        <div class="mt-4">
            <h2 class="text-lg font-semibold text-center">{{ title }}</h2>
            <h3 class="text-center">
                Seasons {{ seasons }}
                <span class="w-full text-right">Eps {{ episodes }}</span>
            </h3>
        </div>
    </div>
</template>

<script>
export default {
    name: "DramaTile",
    props: {
        imgSrc: String,
        title: String,
        seasons: Number,
        episodes: Number,
    },
};
</script>
