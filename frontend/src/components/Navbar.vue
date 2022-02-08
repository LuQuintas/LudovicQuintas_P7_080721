<template>
  <nav class="navbar">
    <div class=navbar-logo>
      <img class=navbar-logo__img src="../assets/images/icon-left-font-monochrome-white.png" alt="">
    </div>
    <ul class="menu-nav">
      <li @click="profil">
        <p class="profil">
          <i class="fas fa-user"></i>
          <span>Profil</span>
        </p>
      </li>
      <li @click="logout">
        <p class="déconnexion">
          <i class="fas fa-sign-in-alt"></i>
          <span>Déconnexion</span> 
        </p>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: 'NavBar',
  props: {
  },
  methods: {
    profil : function (){
      this.$router.push('/profile')
    },
    logout : function (){
      this.$router.push('/')
    }
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
 @import "../assets/scss/navbar.scss";

</style>
