<template>
    <div id="app">
        <hello></hello>
    </div>
</template>

<script>
    import Hello from './components/Hello'

    export default {
        name: 'app',
        components: {
            Hello
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
