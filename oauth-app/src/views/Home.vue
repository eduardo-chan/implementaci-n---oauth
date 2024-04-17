<template>
    <div class="home">
        <h1>Login con OAuth</h1>
        <div v-if="!$auth.loading">
            <b-button variant="outline-primary" v-if="!$auth.isAuthenticated" @click="login">Iniciar Sesión</b-button>
            <b-button variant="outline-danger" v-if="$auth.isAuthenticated" @click="logout">Cerrar Sesión</b-button>
        </div>
    </div>
</template>

<script>
    export default {
        name: "home",
        methods: {
            login() {
                this.$auth.loginWithRedirect();
            },
            logout() {
                this.$auth.logout({
                    logoutParams: {
                        returnTo: window.location.origin,
                    },
                });
            },
        },
    };
</script>