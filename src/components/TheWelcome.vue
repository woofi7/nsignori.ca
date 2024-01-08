<script setup>
import WelcomeItem from './WelcomeItem.vue'
import DocumentationIcon from './icons/IconDocumentation.vue'
import ToolingIcon from './icons/IconTooling.vue'
import SupportIcon from './icons/IconSupport.vue'
import {ref} from "vue";
import ProjectCard from "@/components/ElementCard.vue";

  const schools = ref([
    {
      title: "Baccalauréat en génie logiciel",
      date: "Décembre 2023",
      link: {
        text: "École de technologie supérieure (ÉTS)",
        url: "https://www.etsmtl.ca/"
      },
      logoUrl: "src/assets/logoETS.jpg",
      location: "Montréal"
    },
    {
      title: "Session d’études à l’étranger",
      date: "Automne 2022",
      link: {
        text: "Université de Nantes – Polytech",
        url: "https://www.univ-nantes.fr/"
      },
      logoUrl: "src/assets/logoNantes.png",
      location: "France"
    },
    {
      title: "Diplôme d’études collégiales",
      date: "Informatique de gestion - 2018",
      link: {
        text: "Collège de Bois-de-Boulogne",
        url: "https://www.bdeb.qc.ca/"
      },
      logoUrl: "src/assets/logoBdeb.svg",
      location: "Montréal"
    },
    {
      title: "Programme Explore",
      date: "Immersion anglaise - 2017",
      link: {
        text: "University of Regina",
        url: "https://www.uregina.ca/"
      },
      logoUrl: "src/assets/logoUofR.jpg",
      location: "Saskatchewan"
    }
  ])

  const works = ref([
    {
      title: "Développeur Web - Administrateur Système",
      date: "Depuis janvier 2019 (4 ans)",
      link: {
        text: "Groupe Forman",
        url: "https://groupeforman.ca/"
      },
      location: "Mont-Blanc",
      tags : [
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
      link: {
        text: "Graitec inc.",
        url: "https://graitec.com/ca-en/"
      },
      location: "Montréal",
      moreInfo: {
        list:[
        "Migration d’une application Razor vers une technologie Web moderne",
        "Création de différents modules dont la génération de rapport PDF, l’intégration de dessins techniques à l’interface et un système de commentaires",
        "Organisation d’un atelier sur le développement Responsive avec HTML/CSS"
      ]},
      tags : [
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
      link: {
        text: "Bell Canada",
        url: "https://www.bell.ca/"
      },
      location: "Montréal",
      tags : [
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
      link: {
        text: "Bell Canada",
        url: "https://www.bell.ca/"
      },
      location: "Montréal",
      tags : [
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
      link: {
        text: "JBM Logic Inc.",
        url: "https://www.jbmlogic.com/"
      },
      location: "Boucherville",
      tags : [
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
      link: {
        text: "Collège de Bois-de-Boulogne",
        url: "https://www.bdeb.qc.ca/"
      },
      location: "Montréal",
      moreInfo: {
        list:[
          "Assister les étudiants à travers les cours d’informatique"
        ]}
    }
  ]);

const projects = ref([
  {
    title: "Plateforme web de publication d’articles et balados",
    date: "2020-2023",
    sources: [
      {
        text: "Frontend",
        link: "https://github.com/woofi7/lagenda-frontend"
      },
      {
        text: "Backend",
        link: "https://github.com/woofi7/lagenda-backend"
      },
    ],
    link: {
      isDemo: true,
      text: "lagenda.ca",
      url: "https://web.archive.org/web/20221210084806/https://lagenda.ca/"
    },
    tags : [
      {
        name: "EmberJS",
        color: "orange"
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
        name: "JsonAPI"
      },
      {
        name: "Azure Storage",
        color: "turquoise"
      },
      {
        name: "Google OAuth",
        color: "darkred"
      }
    ],
    moreInfo: {
      list: [
        "Création du design graphique",
        "Conception du site web avec EmberJS et .NET + EntityFramework et JsonAPI",
        "Panneau d’administration pour la mise en ligne des articles et des balados sur les différents hébergeurs de contenu",
        "Hébergements des ressources (balados et images) avec Azure Storage",
        "Authentification avec Google OAuth"
      ],
      artefacts: [
        '/lagenda1.png',
        '/lagenda2.png',
        '/lagenda3.jpg',
        '/lagenda4.jpg'
      ]
    }
  },
  {
    title: "Serveur Minecraft Communautaire – Minefield.fr",
    date: "2016-2017",
    link: {
      text: "Minefield.fr",
      url: "https://www.minefield.fr/"
    },
    tags : [
      {
        name: "Java",
        color: "orange"
      },
      {
        name: "Reflection",
        color: "red"
      },
      {
        name: "Graphisme 3D",
        color: "blue"
      }
    ],
    moreInfo: {
      list: [
        "Développement de mods et plugins",
        "Création d’outils graphique dans un espace 3D",
        "Générateur de blocs à partir de fichiers de configuration sans code",
        "Réécriture de plusieurs mods et plugins vers un nouvelle version majeure de Minecraft"
      ]
    }
  },
])
</script>

<template>
  <WelcomeItem>
    <template #icon>
      <DocumentationIcon />
    </template>
    <template #heading>Formations Académiques</template>

    <div class="cardList">
      <ProjectCard v-for="school in schools"
        :title="school.title"
        :date="school.date"
        :link="school.link"
        :logoUrl="school.logoUrl"
        :location="school.location" />
    </div>
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <ToolingIcon />
    </template>
    <template #heading>Expériences Professionnelles</template>

    <div class="cardList">
      <ProjectCard v-for="work in works"
                   :title="work.title"
                   :date="work.date"
                   :link="work.link"
                   :location="work.location"
                   :tags="work.tags"
                   :moreInfo="work.moreInfo"/>
    </div>
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <SupportIcon />
    </template>
    <template #heading>Projets Personnels</template>

    <div class="cardList single">
      <ProjectCard v-for="project in projects"
                :title="project.title"
                :date="project.date"
                :link="project.link"
                :sources="project.sources"
                :tags="project.tags"
                :moreInfo="project.moreInfo"/>
    </div>
  </WelcomeItem>
</template>

<style scoped>
 .cardList {
   display: grid;
   grid-template-columns: repeat(auto-fill, minmax(20rem, 1fr));
   align-items: stretch;
   grid-gap: 0.5rem;
   &.single{
     grid-template-columns: 1fr;
   }
 }
</style>