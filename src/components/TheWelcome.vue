<script setup>
import WelcomeItem from './WelcomeItem.vue'
import DocumentationIcon from './icons/IconDocumentation.vue'
import ToolingIcon from './icons/IconTooling.vue'
import EcosystemIcon from './icons/IconEcosystem.vue'
import CommunityIcon from './icons/IconCommunity.vue'
import SupportIcon from './icons/IconSupport.vue'
import ElementCard from "@/components/ElementCard.vue";
import {ref} from "vue";
import WorkCard from "@/components/WorkCard.vue";

  const schools = ref([
    {
      title: "Baccalauréat en génie logiciel",
      date: "Décembre 2023",
      linkText: "École de technologie supérieure (ÉTS)",
      linkUrl: "https://www.etsmtl.ca/",
      logoUrl: "src/assets/logoETS.jpg",
      location: "Montréal"
    },
    {
      title: "Session d’études à l’étranger",
      date: "Automne 2022",
      linkText: "Université de Nantes – Polytech",
      linkUrl: "https://www.univ-nantes.fr/",
      logoUrl: "src/assets/logoNantes.png",
      location: "France"
    },
    {
      title: "Diplôme d’études collégiales",
      date: "Informatique de gestion - 2018",
      linkText: "Collège de Bois-de-Boulogne",
      linkUrl: "https://www.bdeb.qc.ca/",
      logoUrl: "src/assets/logoBdeb.svg",
      location: "Montréal"
    },
    {
      title: "Programme Explore",
      date: "Immersion anglaise - 2017",
      linkText: "University of Regina",
      linkUrl: "https://www.uregina.ca/",
      logoUrl: "src/assets/logoUofR.jpg",
      location: "Saskatchewan"
    }
  ])

  const works = ref([
    {
      title: "Développeur Web - Administrateur Système",
      date: "Depuis janvier 2019 (4 ans)",
      linkText: "Groupe Forman",
      linkUrl: "https://groupeforman.ca/",
      location: "Mont-Blanc",
      icons : [
        {
          name: "EmberJS",
          color: "orange"
        },
        {
          name: "VueJs",
          color: "green"
        },
        {
          name: ".NET",
          color: "purple"
        },
        {
          name: "MySQL",
          color: "teal"
        },
        {
          name: "Linux"
        },
        {
          name: "WordPress",
          color: "blue"
        },
        {
          name: "Azure",
          color: "turquoise"
        }
      ],
      moreInfo: {
        list: [
          "Création des sites web pour différents projets",
          "Gestion des logiciels et des équipements avec Azure et SharePoint",
          "Support informatique"
        ],
        extra: "<h3>Principaux Projets</h3>\n" +
            "        <p>\n" +
            "          <a href=\"https://skimontblanc.com/\">https://skimontblanc.com/</a><br>\n" +
            "          <a href=\"https://groupeforman.ca/\">https://groupeforman.ca/</a><br>\n" +
            "          <a href=\"https://ambiance-nature.com/\">https://ambiance-nature.com/</a><br>\n" +
            "          <a href=\"https://latableedespionniers.com/\">https://latableedespionniers.com/</a><br>\n" +
            "          Et bien plus!\n" +
            "        </p>"
      }
    },
    {
      title: "Développeur Frontend",
      date: "Été 2022 - Stage (4 mois)",
      linkText: "Graitec inc.",
      linkUrl: "https://graitec.com/ca-en/",
      location: "Montréal",
      moreInfo: {
        list:[
        "Migration d’une application Razor vers une technologie Web moderne",
        "Création de différents modules dont la génération de rapport PDF, l’intégration de dessins techniques à l’interface et un système de commentaires",
        "Organisation d’un atelier sur le développement Responsive avec HTML/CSS"
      ]},
      icons : [
        {
          name: "React",
          color: "darkblue"
        },
        {
          name: ".NET",
          color: "purple"
        },
        {
          name: "MySQL",
          color: "teal"
        }
      ]
    },
    {
      title: "Développeur Fullstack",
      date: "Été 2022 - Stage (4 mois)",
      linkText: "Bell Canada",
      linkUrl: "https://www.bell.ca/",
      location: "Montréal",
      icons : [
        {
          name: "EmberJS",
          color: "orange"
        },
        {
          name: "VueJs",
          color: "green"
        },
        {
          name: ".NET",
          color: "purple"
        },
        {
          name: "SQL Server",
          color: "darkred"
        }
      ],
      moreInfo: {
        list:[
          "Support et ajout de fonctionnalités à une application servant à installer la fibre optique",
          "Refonte du système de révisions et d’automatisation",
          "Documentation des différentes fonctionnalités",
          "Méthode de développement agile"
      ]}
    },{
      title: "Développeur Fullstack",
      date: "Été 2022 - Stage (4 mois)",
      linkText: "Bell Canada",
      linkUrl: "https://www.bell.ca/",
      location: "Montréal",
      icons : [
        {
          name: "EmberJS",
          color: "orange"
        },
        {
          name: ".NET",
          color: "purple"
        },
        {
          name: "SQL Server",
          color: "darkred"
        }
      ],
      moreInfo: {
        list:[
        "Mise en production d’une application servant à installer la fibre optique",
        "Maintenance de plusieurs applications supportées par l’équipe"
      ]}
    },{
      title: "Développeur Logiciel",
      date: "Hiver 2018 - Stage Collégial (4 mois)",
      linkText: "JBM Logic Inc.",
      linkUrl: "https://www.jbmlogic.com/",
      location: "Boucherville",
      icons : [
        {
          name: "Apex",
          color: "red"
        },
        {
          name: "Oracle",
          color: "red"
        },
        {
          name: "PL/SQL",
          color: "red"
        }
      ],
      moreInfo: {
        list:[
          "Migration du logiciel développé par l’entreprise vers la technologie Apex 5.1",
          "Création de composantes compatibles avec l’architecture actuelle"
        ]}
    },{
      title: "Tuteur informatique",
      date: "2015-2018 (3 ans)",
      linkText: "Collège de Bois-de-Boulogne",
      linkUrl: "https://www.bdeb.qc.ca/",
      location: "Montréal",
      moreInfo: {
        list:[
          "Assister les étudiants à travers les cours d’informatique"
        ]}
    }

  ])
</script>

<template>
  <WelcomeItem>
    <template #icon>
      <DocumentationIcon />
    </template>
    <template #heading>Formations académiques</template>

    <div class="cardList">
      <ElementCard v-for="school in schools"
        :title="school.title"
        :date="school.date"
        :linkText="school.linkText"
        :linkUrl="school.linkUrl"
        :logoUrl="school.logoUrl"
        :location="school.location" />
    </div>
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <ToolingIcon />
    </template>
    <template #heading>Expériences professionnelles</template>

    <div class="cardList">
      <WorkCard v-for="work in works"
                   :title="work.title"
                   :date="work.date"
                   :linkText="work.linkText"
                   :linkUrl="work.linkUrl"
                   :logoUrl="work.logoUrl"
                   :location="work.location"
                   :icons="work.icons"
                   :moreInfo="work.moreInfo"/>
    </div>
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <EcosystemIcon />
    </template>
    <template #heading>Ecosystem</template>

    Get official tools and libraries for your project:
    <a href="https://pinia.vuejs.org/" target="_blank" rel="noopener">Pinia</a>,
    <a href="https://router.vuejs.org/" target="_blank" rel="noopener">Vue Router</a>,
    <a href="https://test-utils.vuejs.org/" target="_blank" rel="noopener">Vue Test Utils</a>, and
    <a href="https://github.com/vuejs/devtools" target="_blank" rel="noopener">Vue Dev Tools</a>. If
    you need more resources, we suggest paying
    <a href="https://github.com/vuejs/awesome-vue" target="_blank" rel="noopener">Awesome Vue</a>
    a visit.
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <CommunityIcon />
    </template>
    <template #heading>Community</template>

    Got stuck? Ask your question on
    <a href="https://chat.vuejs.org" target="_blank" rel="noopener">Vue Land</a>, our official
    Discord server, or
    <a href="https://stackoverflow.com/questions/tagged/vue.js" target="_blank" rel="noopener"
      >StackOverflow</a
    >. You should also subscribe to
    <a href="https://news.vuejs.org" target="_blank" rel="noopener">our mailing list</a> and follow
    the official
    <a href="https://twitter.com/vuejs" target="_blank" rel="noopener">@vuejs</a>
    twitter account for latest news in the Vue world.
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <SupportIcon />
    </template>
    <template #heading>Support Vue</template>

    As an independent project, Vue relies on community backing for its sustainability. You can help
    us by
    <a href="https://vuejs.org/sponsor/" target="_blank" rel="noopener">becoming a sponsor</a>.
  </WelcomeItem>
</template>

<style scoped>
 .cardList {
   display: grid;
   grid-template-columns: repeat(auto-fill, minmax(20rem, 1fr));
   align-items: start;
   grid-gap: 0.5rem;
 }
</style>