<template>
    <div class="card">
        <h1 class="card__title"> Espace Perso</h1>
        <p class="card__subtitle"> Voici qui je suis...</p>
        <p>Prénom Nom   adresse mail</p>
        <img src="" alt="">
        <div class="form">
            <button class="button" @click="logout">
                Déconnexion
            </button>
        </div>
    </div>
</template>

<script>
export default {
    name:'Profile',

    methods: {
        
        logout: function(){
            this.$router.push('/');
        }
    }
}
</script>

<style scoped>

</style>
