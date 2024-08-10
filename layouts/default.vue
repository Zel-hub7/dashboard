<script setup lang="ts">

</script>

<template>
    <div class="flex  flex-col lg:flex-row">
        <div>
            <Sidebar />
         
        </div>


        <div class="p-8 w-full ">
            <slot />
        </div>

    </div>
</template>