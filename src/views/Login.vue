<template>
    <div>
        <h1>Login</h1>
        <button @click="login">Login</button>
    </div>
</template>

<script>
    export default {
        data(){
            return {

            }
        },
        methods: {
            login(){
                this.$store.dispatch('retrieveToken', {
                    username: this.username,
                    password: this.password,
                }).then(response => {
                        this.$router.push({ name: 'about' })
                })
            }
        }
    }
</script>