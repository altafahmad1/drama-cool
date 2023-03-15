<template>
    <footer class="container my-16">
        <div
            class="bg-secondary rounded-[10px] grid grid-cols-2 lg:grid-cols-4 p-8 justify-between gap-y-8"
        >
            <div v-for="item in 4" class="col-span-1">
                <h2 class="mb-4 text-lg font-semibold">Dramas</h2>
                <p>Last of Us</p>
                <p>You</p>
                <p>Game of Thrones</p>
                <p>Breaking Bad</p>
                <p>Better Call Saul</p>
                <p>Squid Game</p>
                <p>La Casa de Papel</p>
            </div>
        </div>
    </footer>
</template>

<script>
export default {
    name: "Footer",
};
</script>
