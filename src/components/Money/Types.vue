<template>
    <div>
        <ul class="types">
            <li :class=" type === '-' && 'selected'" @click="selecteType('-')">支出</li>
            <li :class=" type === '+' && 'selected'" @click="selecteType('+')">收入</li>
        </ul>
    </div>
</template>

<script lang="js">
  export default {
    name: 'Types',
    data() {
      return {
        type: '-'   //- 表示支出    + 表示收入
      }
    },
    methods: {
      selecteType(type) {
        if (type !== '-' && type !== '+') {
          throw new Error('type is unknown')
        }
        this.type = type
      }
    }
  }
</script>

<style lang="scss" scoped>
    @import "~@/assets/styles/helper.scss";

    .types {
        background: #c4c4c4;
        display: flex;
        text-align: center;
        font-size: 24px;

        > li {
            width: 50%;
            height: 64px;
            display: flex;
            justify-content: center;
            align-items: center;
            position: relative;

            &.selected::after {
                content: "";
                position: absolute;
                bottom: 0;
                left: 0;
                width: 100%;
                height: 4px;
                background: $color-nearblack;
            }
        }
    }
</style>