<template>
    <div>
        <p>{{str}}</p>
        <app-header v-bind:propsData="str"></app-header>
    </div>
</template>

<script>
import AppHeader from './components/AppHeader.vue';

export default {
    data : function (){
        return {
            str : 'data Str'
        }
    },

    components : {
        'app-header' : AppHeader
    }
}
</script>

<style>

</style>