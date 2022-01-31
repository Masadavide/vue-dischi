<template>
  <main>
    <div v-if="!loading" class="container">
      <Brani 
      v-for="(brano, index) in BraniArray" 
      :key="index"
      :informazioni="brano"/>
    </div>
    <div v-else>
      <Loader />
    </div>
  </main>
</template>

<script>
import axios from "axios"
import Loader from "./commons/Loader.vue"
import Brani from "./commons/Brani.vue"
export default {
    name: 'Main',
    data() {
        return {
            apiURL: "https://flynn.boolean.careers/exercises/api/array/music",
            BranoArray: [],
            loading: true
        }
    },
    components: {
        Brani,
        Loader
    },
    created(){
        this.getBrani();
    },
    methods: {
        getBrani(){
            axios
                .get(this.apiURL)
                .then( (risposta) => {
                    // handle success
                    this.BraniArray = risposta.data.response;
                    this.loading = false;
                })
                .catch(function (error) {
                    // handle error
                    console.log(error);
                });
        }
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../assets/style/variables.scss';

main{
  background-color: $secondarycolor;
  width: 100%;
  height: calc(100vh - 100px);

  .container{
    padding: 50px 0;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    text-align: center;
  }
}

</style>
