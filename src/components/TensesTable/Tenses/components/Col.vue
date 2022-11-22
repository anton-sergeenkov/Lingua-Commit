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
    border: 1px solid rgba(0,0,0,.3);
}
</style>
