<template>
    <div id="app">
        <hello></hello>
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
        height: 100%;
        width: 100%;
        position: absolute;
        top: 0;
        left: 0;
    }
</style>
