<template>
    <Navbar/>
    <div class="main">
        <div class="card">
            <h1 class="card__title" v-if="mode == 'login'"> Connexion </h1>
            <h1 class="card__title" v-else> Inscription </h1>
            <p class="card__subtitle" v-if="mode == 'login'" > Tu n'as pas encore de compte ? <span class="card__action" @click="switchToCreateAccount"> Créer un compte </span></p>
            <p class="card__subtitle" v-else> Tu as déjà un compte ? <span class="card__action" @click="switchToLogin"> Se connecter </span></p>
            <div class="form">
                <input v-model="email" class="form-input" type="text" placeholder="Adresse mail">
            </div>
            <div class="form" v-if="mode == 'create'">
                <input v-model="firstName" type="text" class="form-input " placeholder="Prénom">
                <input v-model="lastName" type="text" class="form-input " placeholder="Nom">
            </div>
            <div class="form">
                <input v-model="password" class="form-input" type="Password" placeholder="Mot de passe "> 
            </div>
            <div class="form" >
                <button class="button" @click="login"  >
                    <span >Connexion</span>
                </button>

            </div>
        </div>
    </div>
</template>

<script>
import Navbar from '../components/Navbar.vue';

export default {
  components: { Navbar },
    name: 'Login',
    data () {
        return {
            mode: 'login',
            email:'',
            prénom:'',
            nom:'',
            paswword:'',
        }
    },

    methods: {
        switchToCreateAccount: function () {
            this.mode = 'create';
        },
        switchToLogin: function (){
            this.mode = 'login'
        },
        login : function (){
            this.$router.push('/profile')
        }
    }  
}

</script>


<style scoped>



.form{
    display: flex;
    flex-wrap: wrap;
    margin: 16px 0px;
    gap: 26px;
}
.form-input{
    padding: 10px;
    border: none;
    background:#f2f2f2;
    flex: 1;
    font-size: 16px;
    color: black;
}
.form-input::placeholder{
    color: #aaaaaa;
}

</style>