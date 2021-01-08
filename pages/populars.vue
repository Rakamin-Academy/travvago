<template>
  <div>
    <div class="head">
      <Navbar />
    </div>
    <h1 class="header">Populars Galery</h1>
    <div class="row mb-4">
      <div
        class="container col-md-4 mt-4"
        v-for="destination in destinations.slice(0, 9)"
        :key="destination.id"
      >
        <b-card-group class="card">
          <b-card
            :img-src="destination.image"
            :img-alt="destination.name"
            img-top
            img-width="500px"
            img-height="400px"
            class="text-galery"
          >
            <div>
              <b-form-rating
                id="rating-inline"
                variant="warning"
                inline
                :value="destination.ratings"
              ></b-form-rating>
            </div>

            <b-card-text>
              {{ destination.name }} <br>
              {{ destination.address }}
            </b-card-text>
          </b-card>
        </b-card-group>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      destinations: [],
    };
  },
  created() {
    fetch("https://travvago-backend.herokuapp.com/api/v1/destination/all")
      .then((response) => response.json())
      .then((data) => {
        this.destinations = data.results;
      });
  },
};
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Lato:ital,wght@1,300&display=swap");

.head {
  background-color: #85929e;
}
.header {
  display: flex;
  font-family: "Lato", sans-serif;
  margin-bottom: -20px;
  color: #f85e1d;
  justify-content: center;
  font-weight: bold;
  font-size: 30px;
  padding: 40px 0 10px 0;
}
.text-galery {
  text-transform: uppercase;
  font-size: 20px;
}
.card {
  min-height: 100%;
}
/* tablet version */
@media (min-width: 768px) and (max-width: 991.98px) {
  .header {
    font-size: 40px;
  }
  .img-wrapper img {
    width: 300px;
    height: 200px;
  }
}
/* Desktop Version */
@media (min-width: 992px) {
  .header {
    font-size: 48px;
  }
  .carousel-wrapper {
    padding: 40px;
  }
  .img-wrapper img {
    margin: auto;
    width: 600px;
    height: 400px;
  }
}
</style>