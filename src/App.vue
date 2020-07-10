<template>
    <div id="app">
        <router-view/>
    </div>
</template>

<style lang="scss">
    @import "~@/assets/styles/helper.scss";
    @import "~@/assets/styles/reset.scss";

    body {
    }

    #app {
        font-family: $font-hei;
        font-size: 16px;
        line-height: 1.5;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        color: $color-nearblack;
    }

    #nav {
        padding: 30px;

        a {
            font-weight: bold;
            color: #2c3e50;

            &.router-link-exact-active {
                color: #42b983;
            }
        }
    }
</style>
