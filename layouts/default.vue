<script setup lang="ts">

</script>

<template>
    <div class="flex flex-col lg:flex-row">
        <div>
            <Sidebar />
         
        </div>


        <div class="p-4">
            <slot />
        </div>

    </div>
</template>