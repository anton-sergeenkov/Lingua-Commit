<template>
    <td :class="['wrapper', className]">
        <slot></slot>
    </td>
</template>

<script setup>
defineProps(['className'])
</script>

<style scoped>
.wrapper {
	padding: 6px;
    border: 2px solid #e6e6e8;
}
</style>
