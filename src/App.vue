<template>
    <div id="app">
        <index></index>
    </div>
</template>

<script>
    import Index from './components/Index'

    export default {
        name: 'app',
        components: {
            Index
        }
    }
</script>

<style>
    #app {
        position: absolute;
        top: 0;
        left: 0;
        height: 100%;
        width: 100%;
    }
</style>
