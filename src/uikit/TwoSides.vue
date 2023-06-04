<template>
    <div class="wrapper">
        <div class="column half">
            <slot name="first">User Default1</slot>
        </div>
        <div class="column half">
            <slot name="last">User Default2</slot>
        </div>
    </div>
</template>

<style scoped>
.wrapper {
	display: flex;
	margin: 10px 0px;
}
.column {
	margin: 0px 5px;
}
.half {
	width: 50%;
}
</style>
