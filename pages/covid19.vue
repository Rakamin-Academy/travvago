<template>
  <div>
    <div class="head mb-3">
      <Navbar />
    </div>
    <div class="container">
      <h1 class="covid d-flex justify-content-center">
        Update Data Sebaran COVID-19 di Indonesia
      </h1>

      <div class="row mb-4">
        <div
          class="container col-md-4 mt-4"
          v-for="region in stats.regions"
          :key="region"
        >
          <b-card-group deck class="card">
            <b-card
              border-variant="primary"
              :header="region.name"
              header-bg-variant="primary"
              header-text-variant="white"
              align="center"
              class="card-text"
            >
              <b-card-text
                >Kasus Positif: 
                {{ region.numbers.infected }}
                </b-card-text>

              <b-card-text
                >Kasus Meninggal:
                {{ region.numbers.fatal }}
                </b-card-text>

              <b-card-text
                >Angka Kesembuhan:
                {{ region.numbers.recovered }}</b-card-text>
            </b-card>
          </b-card-group>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      stats: [],
    };
  },
  async fetch() {
    this.stats = await fetch(
      "https://dekontaminasi.com/api/id/covid19/stats"
    ).then((res) => res.json());
  },
};
</script>

<style scoped>
.head {
  background-color: #85929e;
}
.card-text {
  font-size: 20px;
}

.covid {
  color: #f85e1d;
  font-weight: bold;
}
.card {
  min-height: 100%;
  max-width: 100%;
}
/* tablet version */
@media (min-width: 768px) {
  .text {
    font-size: 15px;
  }
}
/* desktop versio */
@media (min-width: 992px) {
  .text {
    font-size: 25px;
  }
}
</style>