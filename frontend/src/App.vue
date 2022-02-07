<template>
  <div id="app">
    <router-view></router-view>
  </div>
</template>

<script>

export default {
  name: 'app',
  components: {
  }

}
</script>


<style lang="scss">

body{
  background-color: #32527a;
  display: flex;
  text-align: center;
  justify-content: center;
  padding: 32px;
}

.card{
  max-width: 100%;
  width: 500px;
  background:white;
  border-radius: 16px;
  padding: 32px;
  &__title{
    text-align: center;
    font-weight: 800;
  }
  &__subtitle{
    text-align: center;
    color:#666;
    font-weight: 500;
  }
}

.card__action {
    color:#2196F3;
    text-decoration: underline;
    &:hover{
      cursor: pointer;
    }
  }

.button{
  background: #2196f3;
  color: white;
  border-radius: 8px;
  font-weight: 800;
  font-size: 15px;
  border: none;
  width: 100%;
  padding: 16px;
  transition: .3s background-color;
  box-shadow:  2px 2px 10px #666;
  transition: .3s box-shadow;
  &:hover {
    cursor:pointer;
    box-shadow: none;
    background: #1976D2;
  }
}

</style>