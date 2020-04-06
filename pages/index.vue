<template>
  <div class="background d-flex flex-column" v-bind:class="{ 'active': $vuetify.breakpoint.lgAndUp }">
    <div>
      <Navbar />
    </div>
    <v-container class="d-flex flex-column justify-center" style="flex: 1">
      <div>
        <v-row no-gutter>
          <v-col :cols="12" :md="6">
            <div class="line"></div>
            <h1 class="color-hmif mt-2 font-weight-black">Himpunan Mahasiswa Informatika ITB</h1>
            <p class="mt-2">HMIF ITB adalah suatu organisasi kemahasiswaan yang menaungi mahasiswa program studi Sarjana Teknik Informatika dan Sistem & Teknologi Informasi Institut Teknologi Bandung.</p>
            <div class="mt-2 color-yellow font-weight-bold">#DinamisSinergis</div>
            <div class="color-yellow font-weight-bold">#DrivenToDisrupt</div>
          </v-col>
        </v-row>
      </div>
    </v-container>
    <v-container class="py-5">
      <Footer />
    </v-container>
  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'
import VuetifyLogo from '~/components/VuetifyLogo.vue'
import Navbar from "../components/Navbar";
import Footer from "../components/Footer";

export default {
  components: {
    Footer,
    Navbar,
    Logo,
    VuetifyLogo
  }
}
</script>

<style scoped>
  .background {
    min-height: 100vh;
  }

  .background.active {
    background-image: url('../assets/img/home-bg-bubble.svg');
    background-position: right center;
    background-size: auto 100%;
  }

  .line {
    width: 50px;
    height: 8px;
    border-radius: 4px;
    background: #4E5E4A;
  }

  .color-hmif {
    color: #4E5E4A;
  }

  .color-yellow {
    color: #FFC107;
  }

  .font-weight-black {
    font-weight: 900;
  }
</style>
