<template>
  <header>
    <div class="menu-logo">
      <img src="https://upload.wikimedia.org/wikipedia/commons/7/75/Spotify_icon.png" alt="">
    </div>
  </header>
</template>

<script>
export default {
  name: 'Header',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../assets/style/variables.scss';

header{
  height: 100px;
  background-color: $primarycolor;

  .menu-logo{
    height: 100px;
    width: 100px;
    
    img{
      width: 100%;
      height: 100%;
    }
  }

}
</style>
