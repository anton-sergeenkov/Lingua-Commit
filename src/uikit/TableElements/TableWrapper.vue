<script setup>
defineProps(['className'])
</script>

<template>
    <div :class="['wrapper', className]">
        <slot></slot>
    </div>
</template>

<style scoped>
.wrapper {
	padding: 10px;
    background-color: #fff;
    height: 100%;
}
</style>
