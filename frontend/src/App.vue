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

*{
  margin: 0;

}

body{
  // background-image: url("./assets/images/icon-above-font.png");
  margin: auto;
  background-color: #31577a;
}


.card{
  margin: auto;
  max-width: 100%;
  width: 750px;
  color: white;
  background:#2e4453;
  border-radius: 16px;
  margin-top: 50px;
  padding: 25px;
  &__title{
    text-align: center;
    font-weight: 600;
    padding-bottom: 15px;
  }
  &__subtitle{
    text-align: center;
    color:white;
    font-weight: 500;
  }
}

.card__action {
    color:#0a8af3;
    text-decoration: underline;
    &:hover{
      cursor: pointer;
    }
  }

.button{
  background: #1976D2;
  color: white;
  border-radius: 8px;
  font-weight: 600;
  font-size: 25px;
  border: none;
  width: 100%;
  padding: 16px;
  transition: .3s background-color;
  box-shadow:  1px 1px 5px #666;
  transition: .3s box-shadow;
  &:hover {
    cursor:pointer;
    box-shadow: none;
    background: #3c9cd7;
  }
}
</style>