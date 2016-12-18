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
        height: 100%;
        width: 100%;
        position: absolute;
        top: 0;
        left: 0;
        display: -webkit-flex;
        display: flex;
        -webkit-align-items: center;
        align-items: center;
        -webkit-justify-content: center;
        justify-content: center;
    }
</style>
