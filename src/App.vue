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
    body {
        margin: 0;
        padding: 0;
    }

    #app {
        height: 100px;
        background-color: #ccc;
    }
</style>
