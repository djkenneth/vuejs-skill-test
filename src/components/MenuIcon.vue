<template lang="">
    <div class="icon-wrapper">
        <img
            :alt="props.alt"
            :src="'menu/' + props.icon"
            class="icon"
            :class="[!props.title ? 'icon-md' : '']"
        >
        <p v-if="props.title" class="icon-title">{{ props.title }}</p>
    </div>
</template>
<script setup>
    defineOptions({
    name: 'MenuIcon'
    })

    const props = defineProps({
    title: {
        type: String,
    },
    alt: {
        type: String,
    },

    icon: {
        type: String,
    },
    })
</script>
<style lang="scss">
    .icon-wrapper {
        display: flex;
        justify-content: flex-start;
        align-items: center;
        flex-direction: column;
        padding: 5px;

        .icon {
            width: 25px; 
            height: 25px;
        }

        .icon-md {
            width: 35px; 
            height: 35px;
        }

        .icon-title {
            font-size: 0.7rem;
            color: #6E8C99;
            margin-bottom: 0;
        }
    }
</style>