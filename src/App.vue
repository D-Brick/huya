<template>
    <div id="app">
        <Head/>
        <Navigator/>
    </div>
</template>

<script lang="ts">
    import { Component, Prop, Vue} from 'vue-property-decorator'
    import Head from '@/components/Head.vue'
    import Navigator from '@/components/Navigator.vue'
    
    @Component({
        components: {
            Head,
            Navigator
        },
    })
    export default class App extends Vue {

    }
</script>

<style lang="stylus">
    body
        margin 0
        padding 0
</style>
