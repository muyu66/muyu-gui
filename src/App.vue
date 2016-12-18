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
    html, body {
        top: 0;
        bottom: 0;
    }
</style>
