<template>
  <div>
    <Navbar />
    <div class="home">
      <div class="home__infos">
        <h1 class="home__title">Bienvenue</h1>
        <div class="create-post">
          <label class="create-post__title" for="post">Partagez vos pensées:</label>
          <textarea
          ></textarea>
          <div>
            <button class="trash-button" @click="deleteFile">
              <i class="fas fa-trash-alt"></i>
            </button>
          </div>
          <div class="create-post__file">
            <label class="add__file" for="post__file">Ajouter un fichier</label>
            <input
              type="file"
              id="post__file"
              name="image"
              @change="onFileSelected"
              aria-label="file selection"
            />
          </div>
          <button class="create-post__button" >
            <span > Envoi du post...</span>
            <span > Créer un post.</span>
          </button>
        </div>
      </div>
      <div class="home__main">
        <h2>Fil d'actualité</h2>
        <div class="line-break"></div>
        <div >
        </div>
        <div >
          <p class="home__main__warn">
            Il n'y a actuellement pas de publications. Créez-en donc une ! :)
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Navbar from '../components/Navbar.vue';

export default {
   name: "Home",
   components:{
       Navbar
   }
}
</script>

<style scoped lang=scss>



.home{
    display: flex;
    flex-direction: column;
    flex-wrap: xrap;
    text-align: center;
    justify-content: center;
    align-items: center;
    padding-top: 30px;

    &__infos{
        display: flex;
        flex-direction: column;
        align-items: center;
    }
    &__title{
        padding-bottom: 10px;
        color: white;

    }
    &__main{
        padding-top: 20px;
        color: white;
        font-size: 18px;
        h2{
            padding-bottom: 18px;
        }
    }

    .create-post{
        color: white;
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        padding-bottom: 30px;
        background-color: #2e4453;
        border-radius: 15px;

        &__title{
            margin: auto;
            font-size: 30px;
            padding: 10px;

        }
        &__file, &__button{
            margin: auto;
            padding: 10px;
        }
    }
    .trash-button{
        font-size: 20px;
        margin:5px 0px;
        margin-left: 8px;
        border: none;
        border-radius: 3px;
        background-color: rgb(119, 113, 113);
        box-shadow: 2px 2px 5px rgb(34, 33, 33);
        &:hover{
            background-color: rgb(202, 181, 181);
            box-shadow: none;
            cursor: pointer;
            /* color: white; */
        }
    }
    .add__file{
        font-size: 20px;
        padding-right: 5px;
    }
    textarea{
        width: 95%;
        height: 150px;
        margin: 7px;
    }
}

</style>