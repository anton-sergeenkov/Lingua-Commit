<template>
    <div>
        <div class="wrapper global-info">
            <slot></slot>
        </div>
    </div>
</template>

<style>
.global-info ul {
    margin: 0;
    padding: 10px 20px 10px 20px;
}
</style>

<style scoped>
.wrapper {
    --color: var(--color-green);

    display: inline-block;
	padding: 0;
	font-size: 14px;
	margin: 10px;
	line-height: 1.7;
	border-radius: 4px;
	border: 1px solid rgba(var(--color), .1);
	border-left: 5px solid rgba(var(--color), .4);
	background-color: rgba(var(--color), .1);
}
</style>
