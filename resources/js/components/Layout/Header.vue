<template>
    <header class="container py-4">
        <div class="flex flex-col">
            <div class="pb-4"><img class="h-12" src="/logo.svg" /></div>
            <div class="flex items-center justify-between">
                <router-link class="hidden lg:inline" to="/">
                    Home
                </router-link>
                <router-link class="hidden lg:inline" to="/drama">
                    Drama List
                </router-link>
                <router-link class="hidden lg:inline" to="/k-show">
                    K Show
                </router-link>
                <router-link class="hidden lg:inline" to="/popular">
                    Popular Drama
                </router-link>
                <router-link class="hidden lg:inline" to="/trending">
                    Trending
                </router-link>
                <button>
                    <span class="block lg:hidden material-icons">menu</span>
                </button>
                <div
                    class="flex items-center py-1 border border-white rounded w-[200px] lg:w-auto"
                >
                    <button class="flex items-center">
                        <span class="mx-2 material-icons">search</span>
                    </button>
                    <input
                        class="w-full bg-black border-0 outline-0"
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
