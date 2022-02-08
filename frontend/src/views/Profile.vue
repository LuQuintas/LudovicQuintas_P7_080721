<template>
    <Navbar/>
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
import Navbar from '../components/Navbar.vue';
export default {
  components: { Navbar },
    name:'Profil',

    methods: {
        
        logout: function(){
            this.$router.push('/');
        }
    }
}
</script>

<style scoped>

</style>
