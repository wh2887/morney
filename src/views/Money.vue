<template>
    <Layout class-prefix="layout">
        <NumberPad/>
        <Types :xxx="333"/>
        <Notes/>
        <Tags/>
    </Layout>
</template>

<script lang="ts">

  import NumberPad from '@/components/Money/NumberPad.vue';
  import Tags from '@/components/Money/Tags.vue';
  import Types from '@/components/Money/Types.vue';
  import Notes from '@/components/Money/Notes.vue';

  export default {
    name: 'Money',
    components: {Notes, Types, Tags, NumberPad},
  };
</script>

<style lang="scss">
    .layout-content {
        display: flex;
        flex-direction: column-reverse;
    }
</style>
