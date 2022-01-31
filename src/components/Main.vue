<template>
  <main>
    <div class="container">
      <div class="box">
        <div class="cover">
          <img src="" alt="">
        </div>
        <div class="title">
          New Jersey
        </div>
        <div class="info">
          <div class="author">
            Bon Jovi
          </div>
          <div class="year">
            1988
          </div>
        </div>
        
      </div>
      <div class="box">
        2
      </div>
      <div class="box">
        3
      </div>
      <div class="box">
        4
      </div>
      <div class="box">
        5
      </div>
      <div class="box">
        6
      </div>
      <div class="box">
        7
      </div>
      <div class="box">
        8
      </div>
      <div class="box">
        9
      </div>
      <div class="box">
        10
      </div>
    </div>
  </main>
</template>

<script>
export default {
  name: 'Main',
  props: {
    msg: String
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

    .box{
      height: 400px;
      width: calc((100% - 150px) / 5);
      background-color: red;
      margin-bottom: 20px;

      .cover{
        background-color: blue;
        height: 170px;
        width: 170px;
        margin: 20px auto;
      }

      .title{
        font-size: 25px;
        color: white;
        font-weight: bold;
        text-transform: uppercase;
      }

      .info{
        column-rule: #7d7e7c;
        margin-top: 20px;
        font-size: 17px;
      }
    }
  }
}

</style>
