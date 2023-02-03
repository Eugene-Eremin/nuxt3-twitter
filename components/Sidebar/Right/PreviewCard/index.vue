<template>
    <div
        :class="twitterBorderColor"
        class="overflow-hidden dark:bg-dim-700 m-2 border rounded-2xl bg-gray-50">
        <h1
            :class="twitterBorderColor"
            class="dark:text-white border-b p-3 text-xl font-extrabol text-gray-900">
            {{ props.title }}
        </h1>

        <slot></slot>

        <div
            :class="defaultTransition"
            class="dark:hover:bg-dim-300 hover:bg-gray-100 cursor-pointer p-3 text-sm text-blue-400">
            Show more
        </div>
    </div>
</template>

<script setup>
const { defaultTransition, twitterBorderColor } = useTailwindConfig()


const props = defineProps({
    title: {
        type: String,
        required: true
    }
})

</script>