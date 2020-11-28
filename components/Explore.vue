<template>
  <div class="container">
  <b-card no-body class="overflow-hidden" style="max-width: 1440px;">
    <b-row no-gutters>
      <b-col md="6">
        <b-card-img src="../assets/bromo.jpg" alt="Image" class="rounded-0" style="max-width: 100%;" height="515px"></b-card-img>
      </b-col>
      <b-col md="6">
        <b-card-body title="About" >
          <b-card-text>
            <div class="accordion" role="tablist">
              <b-card no-body class="mb-1">
                <b-card-header header-tag="header" class="p-1" role="tab">
                  <b-button block v-b-toggle.accordion-1 variant="info">Information</b-button>
                </b-card-header>
                <b-collapse id="accordion-1" visible accordion="my-accordion" role="tabpanel">
                  <b-card-body>
                    <b-card-text>{{ text }}</b-card-text>
                  </b-card-body>
                </b-collapse>
              </b-card>

              <b-card no-body class="mb-1">
                <b-card-header header-tag="header" class="p-1" role="tab">
                  <b-button block v-b-toggle.accordion-2 variant="info">Lokasi</b-button>
                </b-card-header>
                <b-collapse id="accordion-2" accordion="my-accordion" role="tabpanel">
                  <b-card-body>
                    <b-card-text>{{ lokasi }}</b-card-text>
                  </b-card-body>
                </b-collapse>
              </b-card>

              <b-card no-body class="mb-1">
                <b-card-header header-tag="header" class="p-1" role="tab">
                  <b-button block v-b-toggle.accordion-3 variant="info">Information</b-button>
                </b-card-header>
                <b-collapse id="accordion-3" accordion="my-accordion" role="tabpanel">
                  <b-card-body>
                    <b-card-text class="info-covid">{{ info }}</b-card-text>
                  </b-card-body>
                </b-collapse>
              </b-card>
            </div>
          </b-card-text>
        </b-card-body>
      </b-col>
    </b-row>
  </b-card>
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
        protokol:`Tetap waspada dan tidak panik.

2. Hindari keramaian baik itu tempat tertutup maupun tempat terbuka.

3. Gunakan masker di mana saja dan kapan saja bahkan dalam ruangan.

4. Ciptakan ruangan dengan ventilasi yang baik seperti, membuka jendela sesering mungkin.

5. Tetap jaga kebersihan tangan serta hindari menyentuh bagian wajah sebelum mencuci tangan.

6. Selalu terapkan jaga jarak pada aktivitas sehari-hari.
`
      }
    }
}
</script>

<style scooped>
.container {
  background: linear-gradient(127.37deg, #6CC6CB 19.14%, #FEA858 87.36%);
  margin-top: 100px;
  padding: 30px 30px 30px 30px;
}
.info-covid {
  text-align: center;
  background-color: orange;
  font-weight: bold;

}
</style>