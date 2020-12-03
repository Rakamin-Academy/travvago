<template>
  <div>
      <b-nav class="back">
        <b-nav-item href="/" active>Home /</b-nav-item>
        <b-nav-item href="destination">Destination /</b-nav-item>
        <b-nav-item disabled>Explore</b-nav-item>
      </b-nav>
      <div class="container">
      <b-tabs content-class="mt-3" justified text-danger>

        <!-- first tab start-->
        <b-tab title="Details" active>
          <img class="image" src="../assets/bromo.jpg">
          </b-tab>
        <!-- first tab end -->

        <!-- Second tab start -->
        <b-tab title="About">
          <p>{{ text }}</p>
          <p>{{ lokasi }}</p>
        </b-tab>
        <!-- second tab end -->

        <!-- third tab start -->
        <b-tab title="Travel Tips & Information">
          <img class="image-info" src="../assets/pkw.jpg">
          <p class="info">{{ info }}</p>

          </b-tab>
        <!-- third tab end -->
        
      </b-tabs>
      </div>
  </div>
</template>

<script>
export default {
  data() {
      return {
        text: `
          Gunung Bromo dalam bahasa Tengger dieja "Brama", adalah sebuah gunung berapi aktif di Jawa Timur, Indonesia. Gunung ini memiliki ketinggian 2.329 meter di atas permukaan laut dan berada dalam empat wilayah kabupaten, yakni Kabupaten Probolinggo, Kabupaten Pasuruan, Kabupaten Lumajang, dan Kabupaten Malang. Gunung Bromo terkenal sebagai objek wisata utama di Jawa Timur. Sebagai sebuah objek wisata, Bromo menjadi menarik karena statusnya sebagai gunung berapi yang masih aktif. Gunung Bromo termasuk dalam kawasan Taman Nasional Bromo Tengger Semeru.
        `,
        lokasi:`Letak dan Lokasi Gunung Bromo  secara geografis tepatnya di Provinsi Jawa Timur, tepatnya di kelilingi oleh 4 wilayah pemerintahan Kabupaten karena Gunung Bromo memang terletak di perbatasan Kabupaten tersebut, yaitu Kapupaten Probolinggo, Kabupaten Pasuruan, Kabupaten Malang dan Kabupaten Lumajang.

        Yang unik dari letak dan lokasi Gunung Bromo adalah, terdapat di perbatasan 4 kabupaten di Jawa Timur. Yaitu, kabupaten Malang, kabupaten Pasuruan, kabupaten Probolinggo, dan terakhir adalah kabupaten Lumajang. Namun, jalur terbaik bagi wisatawan yang berasal dari luar kota adalah melalui rute Kabupaten Probolinggo, selain akasesnya mudah dekat dengan Terminal Bayu ANgga Probolinggo dan Stasiun Kereta Api Probolinggo.`,
        info:`
        Termasuk zona orange covid`,
        
        infeksi: `terinfeksi : 62313`,
        sembuh : `sembuh : 54863`,
        meninggal : `meninggal : 4438`,
      }
    }
}
</script>

<style scooped>
.container {
  border: 1px solid black;
  border-radius: 20px;
  height: 782px;
  margin-top: 100px;
  padding: 30px 30px 30px 30px;
}
.info-covid {
  text-align: center;
  background-color: orange;
  font-weight: bold;
}
.image {
  margin-left: 35px;
  margin-bottom: 30px;
  width: 1000px;
  height: 500px;
}
.image-info {
  float: left;
  margin-left: 10px;
  width: 500px;
  height: 650px;
}
.info{
  float: right;
  margin-right: 80px;
  font-size: 30px;
}
.list{
  float: right;
  margin-right: 150px;
}
.back{
  color: #F85E1D;
  background-color: white;
  position: absolute;
  width: 500px;
  margin-left: 400px;
  margin-top: -40px;
}
.back:hover {
  background-color: none;
}

/* tablet version */
@media (min-width: 768px) {
  .image {
  width: 90%;
  height: 90%;
}
.image-info {
  width: 60%px;
  height: 10%px;
}
.back{
  margin-left: 550px;
  margin-top: -40px;
}
}
</style>