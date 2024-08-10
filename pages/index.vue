<script setup lang="ts">
import { Tabs, TabsContent, TabsList, TabsTrigger } from '@/components/ui/tabs'
</script>

<template>
    <div class="grid gap-8">
        <header class="flex items-start justify-between">

            <div class="grow">
                <p>Hi Welcomeback Babi
                </p>
                <h1>Dashboard</h1>
            </div>

            <div class="w-[120px] h-[36px] bg-neutral-200"></div>

        </header>

        <main class="grid gap-2">

            <template>
                <Tabs default-value="account" class="w-[400px]">
                    <TabsList>
                        <TabsTrigger value="today">
                            Today
                        </TabsTrigger>
                        <TabsTrigger value="week">
                            This Week
                        </TabsTrigger>
                        <TabsTrigger value="month">
                            This month
                        </TabsTrigger>
                        <TabsTrigger value="year">
                            This year
                        </TabsTrigger>
                    </TabsList>
                    <TabsContent value="today">
                        This is today
                    </TabsContent>
                    <TabsContent value="week">
                        This Week
                    </TabsContent>
                   <TabsContent value="month">
                        This Month
                    </TabsContent>
                    <TabsContent value="year">
                        This year
                    </TabsContent>
                </Tabs>
            </template>
            <!-- <div class="flex items-center gap-3">
               <div v-for='(item, index) in 3' :key="index" class="w-[120px] h-[36px] bg-neutral-200">

               </div>
            </div>

            <section>
                <div class="w-full h-[360px] bg-neutral-200"></div>
            </section> -->
        </main>

        <footer>
            <div class="flex items-center gap-3">
                <div v-for="(item, index) in 3" :key="index" class="w-full h-[260px] bg-neutral-200">

                </div>

            </div>
        </footer>


    </div>

</template>