<template>
    <div>
        <p>{{str}}</p>
        <app-header 
            v-bind:propsData="str"
            v-on:renew="renewStr"
            ></app-header>
    </div>
</template>

<script>
import AppHeader from './components/AppHeader.vue';

export default {
    data : function (){
        return {
            str : 'data Str',
            flag : false
        }
    },

    components : {
        'app-header' : AppHeader
    },

    methods: {
        renewStr : function () {
            this.flag = !this.flag ;
            if(this.flag){
                this.str = "바뀌지롱";
            } else {
                this.str = "또바뀌었네";
            }
        }
    },
}
</script>

<style>

</style>