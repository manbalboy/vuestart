<template>
    <header>
        <h1>header</h1>
        <p>{{propsData}}</p>
        <button v-on:click="sendEvent"> send </button>
    </header>
</template>

<script>
export default {
    props : ['props-data'],
    methods: {
        sendEvent : function () {
            this.$emit('renew');
        }
    }

}
</script>

<style>

</style>