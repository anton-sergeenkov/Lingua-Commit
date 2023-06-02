<template>
    <table class="wrapper">
        <slot></slot>
    </table>
</template>

<style scoped>
.wrapper {
    width: 100%;
	font-size: 13px;
    margin-bottom: 10px;
	border-collapse: collapse;
	box-shadow: var(--box-shadow-table);
	background-color: #fff;
}
.wrapper:last-child {
    margin-bottom: 0;
}
</style>
