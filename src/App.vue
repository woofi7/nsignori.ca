<script setup>
import HelloWorld from './components/HelloWorld.vue'
import TheWelcome from './components/TheWelcome.vue'
</script>

<template>
  <header>
    <img alt="Vue logo" class="logo" src="./assets/logo.svg" width="125" height="125" />
    <p>Nicolas Signori</p>
    <p>Langues : français, anglais</p>
    <p>nicolas.signori.1@ens.etsmtl.ca</p>
  </header>

  <main>
    <section>
      <h1>Introduction</h1>
      <p>Ubique vocibus partiendo dissentiunt vim duo. Posidonium legere scelerisque cubilia constituto eruditi ultricies erroribus. Vitae alienum constituto iusto luctus class offendit erat sententiae. Vocibus magnis mea contentiones accommodare evertitur torquent nonumy leo. Arcu expetenda cubilia definiebas quaeque nunc.</p>
    </section>

    <section>
      <h1>Formations académiques</h1>
      <div>
        <h2> Baccalauréat en génie logiciel</h2>
        <span>Décembre 2023</span>
        <p>École de technologie supérieure (ÉTS), Montréal</p>
        <div>
          <h2>Session d’études à l’étranger</h2>
          <span>Automne 2022</span>
          <p>Université de Nantes – Polytech, France</p>
        </div>
      </div>

      <div>
        <h2>Programme Explore</h2>
        <span>2017</span>
        <p>
          Immersion anglaise<br>
          University of Regina, Saskatchewan
        </p>
      </div>

      <div>
        <h2>Diplôme d’études collégiales</h2>
        <span>2018</span>
        <p>
          Informatique de gestion<br>
          Collège de Bois-de-Boulogne, Montréal
        </p>
      </div>
    </section>

    <section>
      <h1>Connaissances particulières</h1>
      <p>Langages : JavaScript, HTML/CSS, C#, Java, C, C++, PHP, Assembleur, Python, PL/SQL</p>
      <p>Framework : Dotnet, EmberJs, React, VueJs</p>
      <p>Outils de développement : Git, JetBrains, Visual Studio</p>
      <p>Systèmes d’exploitation : Windows, Linux (Ubuntu, Debian)</p>
      <p>Autre : DevOps, Docker, GitHub Actions, GDB, Azure Functions, Google Cloud</p>
    </section>

    <section>
      <h1>Expériences professionnelles</h1>
      <div>
        <h2>Développeur frontend</h2>
        <span>Été 2022</span>
        <p>Graitec inc., Montréal</p>
        <span>Stage S3</span>
        <ul>
          <li>Migration d’une application Razor vers une technologie Web moderne</li>
          <li>Création de différents modules dont la génération de rapport PDF, l’intégration de dessins techniques à l’interface et un système de commentaires</li>
          <li>Organisation d’un atelier sur le développement Responsive avec HTML/CSS</li>
        </ul>
      </div>
      <div>
        <h2>Développeur Fullstack</h2>
        <span>Été 2022</span>
        <p>Bell Canada, Montréal</p>
        <span>Stage S2</span>
        <ul>
          <li>Migration d’une application Razor vers une technologie Web moderne</li>
          <li>Création de différents modules dont la génération de rapport PDF, l’intégration de dessins techniques à l’interface et un système de commentaires</li>
          <li>Organisation d’un atelier sur le développement Responsive avec HTML/CSS</li>
        </ul>
      </div>
      <div>
        <h2>Développeur Fullstack</h2>
        <span>Été 2022</span>
        <p>Bell Canada, Montréal</p>
        <span>Stage S2</span>
        <ul>
          <li>Migration d’une application Razor vers une technologie Web moderne</li>
          <li>Création de différents modules dont la génération de rapport PDF, l’intégration de dessins techniques à l’interface et un système de commentaires</li>
          <li>Organisation d’un atelier sur le développement Responsive avec HTML/CSS</li>
        </ul>
      </div>
    </section>

    <section>
      <h1>Expériences de travails</h1>
      <div>
        <h2>Développeur web - Administrateur système</h2>
        <span>Depuis janvier 2019</span>
        <p>Groupe Forman</p>
        <ul>
          <li>Création des sites web pour différents projets</li>
          <li>Gestion des logiciels et des équipements avec Azure et SharePoint</li>
          <li>Installation d’équipements réseau dans de nouvelles succursales</li>
          <li>Support informatique</li>
        </ul>
        <h3>Réalisations</h3>
        <p>
          Mise en place d’un système de création de sites web généralisé pour l’ensemble des clients et implémentation de stratégies de SEO.
        </p>
      </div>
    </section>

    <section>
      <h1>Implications</h1>
      <div>
        <h2>Plateforme web de publication d’articles et balados</h2>
        <span>2020-2023</span>
        <p>L’agenda.ca</p>
        <ul>
          <li>Création du design graphique</li>
          <li>Site web multicouche avec EmberJS et JsonAPI</li>
          <li>Panneau d’administration pour la mise en ligne des articles et des balados sur les différents hébergeurs de contenu</li>
        </ul>
      </div>
    </section>
    <TheWelcome />
  </main>
</template>

<style scoped>

</style>
