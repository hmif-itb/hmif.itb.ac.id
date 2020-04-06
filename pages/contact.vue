<template>
  <div class="d-flex flex-column background">
    <div>
      <Navbar />
    </div>
    <PageTitle>
      <h2>Hubungi Kami</h2>
    </PageTitle>
    <v-container style="flex: 1">
      <v-row>
        <v-col cols="12" :md="6">
          <div class="font-weight-bold">
            Sekretariat Himpunan Mahasiswa Informatika ITB
          </div>
          <div class="mt-2">
            Gd. Benny Subianto Labtek V Lt. 1, Kampus ITB Ganesha, Jl. Ganesha No. 10, Dago 40132, Bandung, Jawa Barat
          </div>

          <div class="font-weight-bold mt-8">
            Media Sosial
          </div>
          <div class="mt-2">
            Instagram: <a target="_blank" class="no-decoration color-orange" href="https://instagram.com/hmif.itb">@hmif.itb</a>
          </div>
          <div>
            LINE: <a target="_blank" class="no-decoration color-orange" href="https://line.me/R/ti/p/@hmif_itb">@hmif_itb</a>
          </div>

          <div class="font-weight-bold mt-8">
            Pertanyaan Umum dan Kerjasama
          </div>
          <div class="mt-2">
            Apabila Anda memiliki pertanyaan perihal kerjasama atau hal lainnya, silakan menghubungi:
          </div>
          <div class="mt-3">
            Departemen Eksternal HMIF ITB
            <br />
            Contact Person: Muhammad Rafi Zhafran (WA: +6287809344268)
            <br />
            Email: <a target="_blank" class="no-decoration color-orange" href="mailto:hmif_itb@km.itb.ac.id">hmif_itb@km.itb.ac.id</a>
          </div>

          <div class="font-weight-bold mt-8">
            Tawaran Proyek Inkubator-IT
          </div>
          <div class="mt-2">
            Apabila Anda memiliki pertanyaan seputar Inkubator-IT, silakan hubungi:
          </div>
          <div class="mt-3">
            Inkubator-IT
            <br />
            Contact Person: John Doe (WA: +62800000000000)
            <br />
            Email: <a target="_blank" class="no-decoration color-orange" href="mailto:admin@inkubatorit.com">admin@inkubatorit.com</a>
            <br />
            Website: <a target="_blank" class="no-decoration color-orange" href="https://inkubatorit.com">www.inkubatorit.com</a>
          </div>
        </v-col>
      </v-row>
    </v-container>
    <v-container class="py-5">
      <Footer />
    </v-container>
  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'
import VuetifyLogo from '~/components/VuetifyLogo.vue'
import Navbar from "~/components/Navbar";
import Footer from "~/components/Footer";
import PageTitle from "~/components/PageTitle";
import TeamProfile from "~/components/TeamProfile";

export default {
  components: {
    TeamProfile,
    PageTitle,
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

  .no-decoration {
    text-decoration: none;
  }

  .color-hmif {
    color: #4E5E4A;
  }

  .color-yellow {
    color: #FFC107;
  }

  .color-orange {
    color: #FF9800;
  }

  .font-weight-black {
    font-weight: 900;
  }
</style>
