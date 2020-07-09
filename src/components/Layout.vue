<template>
    <div class="nav-wrapper">
        <div class="content">
            <!--            slot用于存放变化的内容-->
            <slot/>
        </div>
        <Nav/>
    </div>
</template>

<script lang="ts">
  export default {
    name: 'Layout'
  };
</script>

<style lang="scss" scoped>
    .nav-wrapper {
        border: 1px solid blue;
        display: flex;
        flex-direction: column;
        height: 100vh;
    }

    .content {
        border: 1px solid violet;
        flex-grow: 1;
        overflow: auto;
    }
</style>