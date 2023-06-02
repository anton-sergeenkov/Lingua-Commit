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
	width: 65px;
	font-family: Roboto-Medium;
	text-align: center;
	color: #241ae3;
}
</style>
