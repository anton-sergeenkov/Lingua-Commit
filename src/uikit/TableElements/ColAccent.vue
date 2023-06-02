<script setup>
import Col from './Col.vue'
</script>

<template>
    <Col className="wrapper">
        <slot></slot>
    </Col>
</template>

<style scoped>
.wrapper {
    font-weight: 600;
	color: #b603fc;
}
</style>
