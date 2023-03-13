<template>
    <header class="container py-4">
        <div class="flex flex-col">
            <div class="pb-4"><img class="h-12" src="/logo.svg" /></div>
            <div class="flex items-center justify-between">
                <router-link to="/"> Home </router-link>
                <router-link to="/drama"> Drama List </router-link>
                <router-link to="/k-show"> K Show </router-link>
                <router-link to="/popular"> Popular Drama </router-link>
                <router-link to="/trending"> Trending </router-link>
                <div class="flex items-center py-1 border border-white rounded">
                    <button class="flex items-center">
                        <span class="mx-2 material-icons">search</span>
                    </button>
                    <input
                        class="bg-black border-0 outline-0"
                        placeholder="Search here..."
                    />
                </div>
            </div>
        </div>
    </header>
</template>

<script>
export default {
    name: "Header",
};
</script>
