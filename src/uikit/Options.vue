<template>
    <span class="wrapper">
        <slot></slot>
    </span>
</template>

<style scoped>
.wrapper {
    display: inline-flex;
    justify-content: center;
    align-items: center;
    width: 20px;
    height: 20px;
    margin-right: 5px;
    background-color: #e6e6e8;
    border-radius: 50%;
}
</style>
