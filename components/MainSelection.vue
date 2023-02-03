<template>
    <div :class="twitterBorderColor" class="border-x">
        <div class="dark:bg-dim-900/80 sticky top-0 px-4 bg-white/80 backdrop-blur-md">
            <h2 class="text-xl font-bold text-gray-800 dark:text-gray-100">{{ props.title }}</h2>
        </div>
        <div v-if="props.loading" :class="twitterBorderColor" class="border-b p-4 justify-center flex items-center">
            <UISpinner />
        </div>
        <div v-else>
            <slot></slot>
        </div>
    </div>
</template>

<script setup>
const { twitterBorderColor } = useTailwindConfig()

const props = defineProps({
    title: {
        type: String,
        required: true
    },
    loading: {
        type: Boolean,
        required: true
    }
})
</script>