<template>
    <div class="flex flex-col">
        <div>

            <!-- Preview Card : What's happening -->
            <SidebarRightPreviewCard title="What's happening">
                <SidebarRightPreviewCardItem v-for="whatsHappening in whatsHappeningItems">
                    <div>
                        <h2 class="dark:text-white text-md font-bold text-gray-800">{{ whatsHappening.title }}</h2>
                        <p class="text-xs text-gray-400">{{ whatsHappening.count }}</p>
                    </div>
                </SidebarRightPreviewCardItem>
            </SidebarRightPreviewCard>

            <!-- Priview Card : Who to follow -->
            <SidebarRightPreviewCard title="Who to follow">
                <SidebarRightPreviewCardItem v-for="whoToFollow in whoToFollowItems">
                    <div class="flex flex-row items-center justify-between p-2">
                        <div class="flex flex-row">
                            <img class="w-10 h-10 rounded-full" :src="whoToFollow.image" :alt="whoToFollow.name">
                            <div class="flex flex-col ml-2">
                                <h1 class="text-sm fontbold text-gray-900 dark:text-white">{{ whoToFollow.name }}</h1>
                                <p class="text-xs text-gray-400">{{ whoToFollow.handle }}</p>
                            </div>
                        </div>
                        <div class="flex h-full">
                            <button class="px-4 py-2 font-bold dark:text-black text-xs text-white dark:bg-white bg-black rounded-full">Follow</button>
                        </div>
                    </div>
                </SidebarRightPreviewCardItem>
            </SidebarRightPreviewCard>

        </div>
    </div>
</template>

<script setup>
const whatsHappeningItems = ref([
    {
        title: 'SpaceX',
        count: '18.8k Tweets'
    },
    {
        title: '#CodingIsFun',
        count: '8.8k Tweets'
    },
    {
        title: '#artforall',
        count: '1.8k Tweets'
    },
])

const whoToFollowItems = ref([
    {
        name: 'Joe Biden',
        handle: '@JoeBiden',
        image: 'https://picsum.photos/200/200'
    },
    {
        name: 'Joe Biden',
        handle: '@JoeBiden',
        image: 'https://picsum.photos/200/200'
    },
    {
        name: 'Joe Biden',
        handle: '@JoeBiden',
        image: 'https://picsum.photos/200/200'
    },
])
</script>