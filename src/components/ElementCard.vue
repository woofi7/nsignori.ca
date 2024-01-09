<script setup>
  import {FontAwesomeIcon} from "@fortawesome/vue-fontawesome";
  import {ref, defineProps} from "vue";
  import Preview from "@/components/Preview.vue";
  import Tags from "@/components/Tags.vue";

  defineProps({
    title: String,
    date: String,
    link: {
      text: String,
      url: String,
      isDemo: Boolean
    },
    logoUrl: String,
    location: String,
    tags: Array,
    moreInfo: {
      list: [String],
      artefacts: [String],
      extra: String
    },
    sources: Array,
  })

  function toggleArtefactClick(img) {
    showArtefact.value = true;
    imgSrc.value = img;
  }

  function toggleShow() {
    showArtefact.value = !showArtefact.value;
  }

  const showArtefact = ref(false);
  const imgSrc = ref('');
</script>

<template>
  <div class="card">
    <div class="header" :class="tags ? 'hasTags' : ''">
      <Tags v-if="tags" :tags="tags"/>
      <div v-if="logoUrl" class="logo">
        <img :src="logoUrl" alt="Logo ETS">
      </div>
      <div class="title">
        <h3>{{ title }}</h3>
        <span class="date">{{ date }}</span>
        <div v-if="sources">
          <span>Sources: </span>
          <a v-for="source in sources" :href="source.link">
            {{source.text}} <font-awesome-icon icon="fa-brands fa-github"/>&nbsp
          </a>
        </div>
        <div v-if="link">
          <span v-if="link.isDemo">Demo : </span>
          <a :href="link.url">{{ link.text }}</a>
        </div>
      </div>
    </div>
    <div v-if="moreInfo" class="content">
      <ul v-if="moreInfo.list">
        <li v-for="info in moreInfo.list">{{ info }}</li>
      </ul>
      <div v-if="moreInfo.extra" v-html="moreInfo.extra">
      </div>
      <div v-if="moreInfo.artefacts" class="artefacts">
        <div class="artefact" v-for="artefact in moreInfo.artefacts"
             @click="toggleArtefactClick(artefact)">
          <div class="overlay">
            <font-awesome-icon icon="fa-solid fa-magnifying-glass" />
          </div>
          <img :src="artefact" alt="Artefact">
        </div>
        <Preview :show="showArtefact" :imgSrc="imgSrc" @toggleShow="toggleShow"/>
      </div>
    </div>
  </div>
</template>

<style scoped>
  .card {
    position: relative;
    display: flex;
    flex-direction: column;
    background-color: #252525;
    padding: 0.5rem;
    justify-content: flex-start;
  }
  .header {
    display: flex;
    gap: 0.5rem;
    &.hasTags {
      width: 70%;
    }
  }
  .logo > img {
    max-width: 75px;
    max-height: 75px;
  }
  .title {
    display: flex;
    flex-direction: column;
    color: white;
  }
  .content {
    display: flex;
    flex-direction: column;

    & > ul {
      padding-left: 1.5rem;
      padding-bottom: 0.5rem;
    }
  }
  .artefacts {
    display: flex;
    gap: 0.5rem;
    flex-wrap: wrap;
    & > .artefact {
      position: relative;
      flex: 1 0 24%;
      cursor: pointer;
      height: fit-content;
      max-width: 25%;

      & > .overlay {
        position: absolute;
        width: 100%;
        height: 100%;
        display: flex;
        justify-content: center;
        align-items: center;
        font-size: xxx-large;

        background-color: rgba(0, 0, 0, 0.4);
      }
      & > img {
        object-fit: cover;
        object-position: top;
        width: 100%;
        max-height: 200px;
      }
    }
  }
</style>