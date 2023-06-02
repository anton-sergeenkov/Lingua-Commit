<template>
    <div>
        <div class="wrapper">
            <slot></slot>
        </div>
    </div>
</template>

<style scoped>
.wrapper {
    --color: var(--color-green);

    display: inline-block;
	padding: 0;
    padding-right: 20px;
	font-size: 15px;
	margin: 10px;
	line-height: 1.7;
	border-radius: 4px;
	border: 1px solid rgba(var(--color), .1);
	border-left: 5px solid rgba(var(--color), .4);
	background-color: rgba(var(--color), .1);
}
</style>
