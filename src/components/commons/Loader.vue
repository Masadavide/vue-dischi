<template>
    <div class="loader">
        <div class="text">Loading...</div>
    </div>
</template>

<script>
export default {
    name: 'Loader',
}
</script>

<style lang="scss" scoped>
.loader {
    position: fixed;
    top: 0;
    left: 0;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: 100%;
    height: 100%;
    background: white;
}
.text {
    text-transform: uppercase;
    letter-spacing: 2px;
}
</style>