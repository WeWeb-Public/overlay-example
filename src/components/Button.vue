<template>
    <a :href="link" target="_blank" class="button">
        <p class="label">{{ label }}</p>
    </a>
</template>
<script>
export default {
    name: 'Button',
    props: {
        link: String,
        label: { type: String, default: 'Discover more' },
    },
};
</script>
<style lang="scss" scoped>
.button {
    background-color: #f1cc40;
    border-radius: 8px;
    padding: 10px 14px;
    box-shadow: 4px 4px 0px 0 black;
    display: flex;
    align-items: center;
    justify-content: center;
    border: 2px solid black;
    cursor: pointer;
}
.label {
    color: black;
    text-align: center;
}
</style>
