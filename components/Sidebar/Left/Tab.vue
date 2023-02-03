<template>
    <div>
        <NuxtLink to="#"
            :class="defaultTransition"
            class="text-black flex items-center rounded-full p-3 w-min hover:bg-gray-200 dark:hover:bg-dim-200 dark:text-white">
            <div class="w-6 h-6 text-dark">
                <slot name="icon"></slot>
            </div>
            <div class="xl:block hidden ml-4 text-xl" :class="textClasses">
                <slot name="name"></slot>
            </div>
        </NuxtLink>
    </div>
</template>

<script setup>
const { defaultTransition } = useTailwindConfig()

const props = defineProps({
    active: {
        type: Boolean,
        default: false
    }
})

const textClasses = computed(() =>
    props.active ? 'font-semibold' : 'font-normal'
)
</script>