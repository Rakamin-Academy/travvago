<template>
  <div class="container-destination">

  <div class="header">
    <h1>Destination</h1>
    
    <b-button class="explore home" href="/" >Back to Home</b-button>

      
      <b-card-group class="card-group" deck>
      <b-card
        title="Card Title"
        img-src="../assets/bromo.jpg"
        img-alt="Image"
        img-top
        tag="article"
        style="max-width: 20rem;"
        class="mb-3"
        
      >
        <b-card-text>
          Some quick example text to build on the card title and make up the bulk of the card's content.
        </b-card-text>

        <b-button class="explore" href="/explore" >Explore</b-button>
      </b-card>

      <b-card
        title="Card Title"
        img-src="../assets/bromo.jpg"
        img-alt="Image"
        img-top
        tag="article"
        style="max-width: 20rem;"
        class="mb-3"
      >
        <b-card-text>
          Some quick example text to build on the card title and make up the bulk of the card's content.
        </b-card-text>

        <b-button class="explore" href="#" >Explore</b-button>
      </b-card>

      <b-card
        title="Card Title"
        img-src="../assets/bromo.jpg"
        img-alt="Image"
        img-top
        tag="article"
        style="max-width: 20rem;"
        class="mb-3"
      >
        <b-card-text>
          Some quick example text to build on the card title and make up the bulk of the card's content.
        </b-card-text>

        <b-button class="explore" href="#" >Explore</b-button>
      </b-card>

      <b-card
        title="Card Title"
        img-src="../assets/bromo.jpg"
        img-alt="Image"
        img-top
        tag="article"
        style="max-width: 20rem;"
        class="mb-3"
      >
        <b-card-text>
          Some quick example text to build on the card title and make up the bulk of the card's content.
        </b-card-text>

        <b-button class="explore" href="#" >Explore</b-button>
      </b-card>
      </b-card-group>
  </div>
  </div>
</template>

<script>
export default {

}
</script>

<style scooped>
@import url('https://fonts.googleapis.com/css2?family=Satisfy&display=swap');

.container-destination {
  background: linear-gradient(127.37deg, #6CC6CB 19.14%, #FEA858 87.36%);
  background-size: cover;
  margin-top: 100px;
  width: 100%;
  height: 100%;
  margin-top: -10px;
}
.header h1 {
  
  display: flex;
  font-family: 'Satisfy', cursive;
  margin-bottom: 50px;
  color: white;
  justify-content: center;
  font-weight: bold;
  font-size: 48px;
  padding: 40px 0 30px 0;
  filter: drop-shadow(0px 4px 4px rgba(0, 0, 0, 0.41));
}
.card-group {
  margin-left: 55px;
  filter: drop-shadow(0px 4px 4px rgba(0, 0, 0, 0.41));
}
.explore {
  color: black;
  border: 1px solid grey;
  background: linear-gradient(180deg, #9DF2DA 0%, #FFFFFF 100%);
  filter: drop-shadow(0px 4px 4px rgba(0, 0, 0, 0.41));
}
.explore:hover{
  color: #F85E1D;
}
.home{
  margin-top: -90px;
}
.home:hover{
  color: #F85E1D;
}
.top {
  margin-top: -60px;
  width: 150px;
}
/* Desktop Version */
@media (min-width: 992px) {
.container-destination {
  margin-top: 100px;
  margin-left: 100px;
  width: 1440px;
  height: 100%;
  margin-top: -10px;
}
.header h1 {
  margin-bottom: 50px;
  justify-content: center;
  font-size: 64px;
  padding: 50px 0 10px 0;
}
.card-group {
  justify-content: center;
  margin-right: 50px;
}
.home{
  margin-top: -350px;
}
}
</style>