<template>
    <div :class="wrapperClasses" class="p-3 border-b cursor-pointer hover:bg-gray-100 dark:hover:bg-dim-300">
        <slot></slot>
    </div>
</template>

<script setup>
const { defaultTransition, twitterBorderColor } = useTailwindConfig()

const wrapperClasses = computed(() => `${defaultTransition} ${twitterBorderColor}`)
</script>