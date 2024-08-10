<script setup lang="ts">


import { Tabs, TabsContent, TabsList, TabsTrigger } from '@/components/ui/tabs'
const loading = ref(false);
const list = [
    {
        title: "Today",
        component: resolveComponent("TabsToday")

    }, {
        title: "Week",
        component: '<div>Week</div>'
    },
    {
        title: "Month",
        component: "<div>Month</div>"
    }, {
        title: "Year",
        component: "<div>Year</div>"
    }
]
</script>

<template>
    <div class="grid gap-8">
        <header class="flex items-start justify-between">

            <div class="grow">
                <p>Hi Welcomeback Babi
                </p>
                <h1>Dashboard</h1>

                <TabsToday />
            </div>

            <div class="w-[120px] h-[36px] bg-neutral-200"></div>

        </header>

        <main class="grid gap-2">

        
                <Tabs default-value="Today" class="w-[400px]" >
                    <TabsList>
                        <TabsTrigger v-for="item, index in list" :key="index" :value="item.title">
                            {{ item.title }}
                        </TabsTrigger>
                    </TabsList>
                    <TabsContent v-for="item, index in list" :key="index" :value="item.title">
                        {{ item.component }}
                    </TabsContent>

                
                

                </Tabs>
           
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