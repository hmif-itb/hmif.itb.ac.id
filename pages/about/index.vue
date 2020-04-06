<template>
  <div class="d-flex flex-column background">
    <div>
      <Navbar />
    </div>
    <PageTitle>
      <h2>Tentang Kami</h2>
    </PageTitle>
    <v-container class="d-flex flex-column justify-center" style="flex: 1">
      <div>
        <v-row no-gutter>
          <v-col :cols="12" :md="6">
            <div class="font-weight-bold">Mission Statement</div>
            <h1 class="color-hmif mt-2 font-weight-black">
              Kami ingin membuat ekosistem penebar manfaat.
            </h1>
            <p class="mt-4">
              Kami percaya bahwa setiap warga HMIF memiliki potensi lebih untuk dapat menebarkan manfaat. Oleh karena itu, kami berupaya menjadikan HMIF ITB sebagai ekosistem yang mampu mengembangkan warga HMIF baik dari sisi ilmu maupun potensi untuk membuat manfaat bagi seluruh rakyat Indonesia.
            </p>
            <div class="mt-2 color-yellow">#DinamisSinergis</div>
            <div class="color-yellow">#DrivenToDisrupt</div>

            <div class="mt-4">
              <nuxt-link class="meet-the-team color-orange font-weight-bold" text to="/about/team" exact>
                Meet the Team
                <v-icon small color="#FF9800" class="ml-2">fas fa-chevron-right</v-icon>
              </nuxt-link>
            </div>
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
import Navbar from "~/components/Navbar";
import Footer from "~/components/Footer";
import PageTitle from "~/components/PageTitle";

export default {
  components: {
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

  .meet-the-team {
    letter-spacing: normal;
    text-decoration: none;
    text-transform: none;
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
