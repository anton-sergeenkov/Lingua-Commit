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
    font-family: Roboto-Medium;
	color: #b603fc;
}
</style>
