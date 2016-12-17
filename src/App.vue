<template>
    <div class="container-fluid" id="app">
        <hello class="row"></hello>
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
    }
</style>
