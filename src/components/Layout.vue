<template>
    <div class="layout-wrapper" :class="classPrefix && `${classPrefix}-wrapper`  ">
        <div class="content" :class="classPrefix && `${classPrefix}-content`  ">
            <!--            slot用于存放变化的内容-->
            <slot/>
        </div>
        <Nav/>
    </div>
</template>

<script lang="ts">

  export default {
    props: ['classPrefix'],
    name: 'Layout'
  };
</script>

<style lang="scss" scoped>
    .layout-wrapper {
        display: flex;
        flex-direction: column;
        height: 100vh;
    }

    .content {
        flex-grow: 1;
        overflow: auto;
    }
</style>