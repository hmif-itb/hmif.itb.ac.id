<template>
  <div class="d-flex flex-column background">
    <div>
      <Navbar />
    </div>
    <PageTitle>
      <h2>Meet the Team</h2>
    </PageTitle>
    <v-container class="" style="flex: 1">
      <v-row v-for="(dept, i) in people" :key="i">
        <v-col :md="2" :cols="12">
          <div class="font-weight-bold color-orange mt-3">
            {{ dept.dept }}
          </div>
        </v-col>
        <v-col>
          <v-row>
            <v-col :cols="6" :sm="3" v-for="(person, j) in dept.people" :key="j">
              <TeamProfile :name="person.name" :title="person.title" />
            </v-col>
          </v-row>
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
import TeamProfile from "../../components/TeamProfile";

export default {
  components: {
    TeamProfile,
    PageTitle,
    Footer,
    Navbar,
    Logo,
    VuetifyLogo
  },
  data: () => ({
    people: [
      {
        dept: "President",
        people: [
          { name: "Luthfi Eko Trinowo", title: "President" }
        ]
      },
      {
        dept: "General Secretary",
        people: [
          { name: "Pandyaka Aptanagi", title: "Secretary General" },
          { name: "Raras Pradnya Pramudita", title: "Secretary" },
          { name: "Alya Mizani", title: "Secretary" },
          { name: "Fitria Budi Ananda", title: "Treasurer" },
          { name: "Felicia Gillian Tekad Tuerah", title: "Treasurer" },
          { name: "Vincent Budianto", title: "Head of Data & Archive" },
        ]
      },
      {
        dept: "People & Culture",
        people: [
          { name: "Juro Sutantra", title: "VP of People & Culture" },
          { name: "Ihsan Imaduddin Azhar", title: "Head of People" },
          { name: "Yasyfiana Fariha Putrisusari", title: "Deputy Head of People" },
          { name: "Irena Irmalasari", title: "Head of Culture" },
          { name: "Tafia Alifianty Dinita Putri", title: "Deputy Head of Culture" },
        ]
      },
      {
        dept: "Internal Affairs",
        people: [
          { name: "M. Ridwan Hady A", title: "VP of Internal Affairs" },
          { name: "Taufikurrahman Anwar", title: "Head of Academic & Welfare" },
          { name: "Hollyana Puteri Haryono", title: "Deputy Head of Academic & Welfare" },
          { name: "Ahmad Rizal Alifio", title: "Head of Infrastructure & Household" },
          { name: "Muhammad Raihan Iqbal", title: "Deputy Head of Infrastructure & Household" },
          { name: "Ariq Radhitama", title: "Head of Extracurricular Development" },
          { name: "Fakhrurrida Clarendia Widodo", title: "Deputy Head of Extracurricular Development" },
          { name: "Rayza Mahendra Guntara Harsono", title: "Head of Kinship" },
          { name: "Daffa Pratama Putra", title: "Deputy Head of Kinship" },
        ]
      },
      {
        dept: "External Affairs",
        people: [
          { name: "Muhammad Rafi Zhafran", title: "VP of External Affairs" },
          { name: "Aisyah Nurul Izzah Adma", title: "Head of Intracampus" },
          { name: "Cynthia Athena Mahadewi Subroto", title: "Deputy Head of Intracampus" },
          { name: "Claudia Renata Maharani Danardono", title: "Head of Extracampus" },
          { name: "M. Irfaan Dzakiy", title: "Deputy Head of Extracampus" },
          { name: "Kintan Sekar Adinda", title: "Head of Alumni Relations" },
          { name: "Chandrika Azharyanti", title: "Deputy Head of Alumni Relations" },
          { name: "Desya Anugrah Setya Putri", title: "Head of Community Service" },
          { name: "Ananda Yulizar Muhammad", title: "Deputy Head of Community Service" },
        ]
      },
      {
        dept: "Technology",
        people: [
          { name: "Muhammad Aditya Hilmy", title: "VP of Technology" },
          { name: "Aliffiqri Agwar", title: "Head of Tech Issues & Exploration" },
          { name: "Fabian Zhafransyah", title: "Deputy Head of Tech Issues & Exploration" },
          { name: "Irfan Sofyana Putra", title: "Head of Competition & Community" },
          { name: "Muhammad Zunan Alfikri", title: "Deputy Head of Competition & Community" },
          { name: "Jofiandy Leonata Pratama", title: "Head of Tech Career Development" },
          { name: "Nyoman Kevin Cahyadi Giri", title: "Deputy Head of Tech Career Development" },
        ]
      },
      {
        dept: "Inkubator-IT",
        people: [
          { name: "Gardahadi", title: "CEO of Inkubator-IT" },
          { name: "Yoel Susanto", title: "COO of Inkubator-IT" },
          { name: "Michelle Theresia", title: "Deputy COO of Inkubator-IT" },
          { name: "Muhammad Fariz Luthfan Wakan", title: "CTO of Inkubator-IT" },
          { name: "Bagas Setyo Wicaksono", title: "Deputy CTO of Inkubator-IT" },
          { name: "Nada Afra Sabrina", title: "CMO of Inkubator-IT" },
          { name: "Patrick Segara", title: "Deputy CMO of Inkubator-IT" },
        ]
      },
      {
        dept: "Media & Information",
        people: [
          { name: "Almyra Ramadhina", title: "VP of Media & Information" },
          { name: "Ainun Fitryh Vianiryzki", title: "Head of Content Creator" },
          { name: "Muhammad Cisco Zulfikar", title: "Deputy Head of Content Creator" },
          { name: "Zalikha Adiera Gambetta", title: "Head of Publication" },
          { name: "Gregorius Jovan Kresnadi", title: "Deputy Head of Publication" },
        ]
      },
      {
        dept: "Senatorial",
        people: [
          { name: "Daeng Muhammad Yusuf Aqsha Alfarabi", title: "Senate" },
          { name: "Muhamad Ilman Sukarsa", title: "Head of Senatorial Relations" },
          { name: "Fabianus Harry Setiawan", title: "Deputy Head of Senatorial Relations" },
          { name: "Radhinansyah Hemsa Ghaida", title: "Head of Political & Social Issues" },
          { name: "Rafi Abbel Mohammad", title: "Deputy Head of Political & Social Issues" },
        ]
      }
    ]
  })
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
