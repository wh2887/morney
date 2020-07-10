<template>
    <nav>
        <router-link class="item" to="/money">
            <Icon name="money"/>
            记账
        </router-link>

        <router-link class="item" to="/labels">
            <Icon name="labels"/>
            标签
        </router-link>

        <router-link class="item" to="/statistics">
            <Icon name="statistics"/>
            统计
        </router-link>
    </nav>
</template>

<script lang="ts">

  export default {
    name: 'Nav',
  };
</script>

<style lang="scss" scoped>

    nav {
        display: flex;
        box-shadow: 0 0 3px rgba(0, 0, 0, 0.25);
        flex-direction: row;
        font-size: 12px;

        > .item {
            padding: 2px 0;
            width: 33.3333%;
            display: flex;
            justify-content: center;
            align-items: center;
            flex-direction: column;
            .icon {
                width: 32px;
                height: 32px;
            }
        }
    }
</style>