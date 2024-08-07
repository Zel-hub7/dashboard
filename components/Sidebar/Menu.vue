<script setup>
const items = ref([
    {
        title: "Overview",
        path: "/"
    }, {
        title: "Transactions",
        path: "/transaction"
    }, {
        title: "Account",
        path: "/account"
    }, {
        title: "Contact",
        path: "/contact"
    }, {
        title: "Settings",
        path: "/settings"
    },
])
</script>



<template>
    <div>
        <header class="flex items-center-gap-2 p-4 hover:scale-[101%] transition cursor-pointer">
            <Logo />
            <p class="font-bold">
                Nuxt-Finance
            </p>
        </header>

        <div class="px-6 grow">
            <div class="grid gap-2">
                <div v-for="(item, index) in items" :key="index" class="flex items-center gap-2 px-2 py-1 transition rounded cursor-pointer hover:bg-neutral-100">
                    <span>{{ item.title }}</span>
                </div>
            </div>
        </div>

    </div>
</template>