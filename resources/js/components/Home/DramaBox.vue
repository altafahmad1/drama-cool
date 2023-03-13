<template>
    <div class="relative">
        <img :src="imageSrc" class="w-full rounded-md" />
        <div
            class="absolute bottom-0 z-10 w-full px-4 pt-2 pb-4 bg-white/10 rounded-br-md rounded-bl-md"
        >
            <h2 class="text-lg font-semibold">{{ title }}</h2>
            <p>{{ updatedAt }}</p>
        </div>
    </div>
</template>

<script>
export default {
    name: "Dramabox",
    props: {
        imageSrc: String,
        title: String,
        updatedAt: String,
    },
};
</script>
