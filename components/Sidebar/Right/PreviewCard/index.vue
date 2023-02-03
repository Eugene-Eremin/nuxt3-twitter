<template>
    <div class="overflow-hidden dark:bg-dim-700 m-2 border rounded-2xl bg-gray-50 border-white-200 dark:border-gray-700">
        <h1 class="border-white-200 dark:border-gray-700 dark:text-white border-b p-3 text-xl font-extrabol text-gray-900">
            {{ props.title }}
        </h1>

        <slot></slot>

        <div class="transition ease-in-out duration-500 dark:hover:bg-dim-300 hover:bg-gray-100 cursor-pointer p-3 text-sm text-blue-400">
            Show more
        </div>
    </div>
</template>

<script setup>

const props = defineProps({
    title: {
        type: String,
        required: true
    }
})
    
</script>