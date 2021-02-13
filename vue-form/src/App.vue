<template>
    <form v-on:submit.prevent="submitForm">
        <div>
            <label for="username">id:</label>
            <input id="username" type="text" v-model="username">
        </div>
        <div>
            <label for="password">pw:</label>
            <input id="password" type="password" v-model="password">
        </div>
        <button type="submit">login</button>
    </form>
</template>

<script>
    import axios from 'axios';

    export default {
        data : function () {
            return {
                username : "",
                password : ""
            }
        },

        methods: {
            submitForm : function () {
                // e.preventDefault();
                alert(1);
                console.log(this.username, this.password);
                var data = {
                    username : this.username,
                    password : this.password
                }


                axios.post('https://jsonplaceholder.typicode.com/users',data)
                    .then(response => console.log(response))
                    .catch(error => console.log(error));
            }
        }
    }
</script>

<style>

</style>