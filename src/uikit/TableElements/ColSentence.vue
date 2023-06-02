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
    width: 20px;
    font-weight: 600;
    text-align: center;
}
</style>
