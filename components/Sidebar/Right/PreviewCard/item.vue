<template>
    <div :class="wrapperClasses" class="p-3 border-b cursor-pointer hover:bg-gray-100 dark:hover:bg-dim-300">
        <slot></slot>
    </div>
</template>

<script setup>
const wrapperClasses = computed(() => 'transition ease-in-out duration-500 border-white-200 dark:border-gray-700'
)
</script>