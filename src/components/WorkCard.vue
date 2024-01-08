<script setup>
  import {ref} from "vue";

  defineProps({
    title: String,
    date: String,
    linkText: String,
    linkUrl: String,
    logoUrl: String,
    location: String,
    icons: Array,
    moreInfo: {
      list: [String],
      extra: String
    }
  })

  let isHidden = ref(true);
</script>

<template>
  <div class="card">
    <div>
      <div class="header">
        <div>
          <h3 class="title">{{ title }}</h3>
          <span class="date">{{ date }}</span>
        </div>
        <div class="tags">
          <div v-for="icon in icons" :class="icon.color" class="tag">
            {{ icon.name }}
          </div>
        </div>
      </div>
      <div>
        <p class="location">
          <a :href="linkUrl">{{ linkText }}</a>, {{ location }}
        </p>
      </div>
    </div>
    <div class="content">
      <ul>
        <li v-for="info in moreInfo.list">{{ info }}</li>
      </ul>
      <div v-html="moreInfo.extra">
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
    justify-content: space-between;
  }
  .header {
    display: flex;
    gap: 0.5rem;
    width: 70%;
  }
  .logo > img {
    width: 75px
  }
  .title {
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
  .tags {
    position: absolute;
    margin-top: 0.5rem;
    margin-right: 0.5rem;
    top: 0;
    right: 0;
    display: flex;
    gap: 0.2rem;
    align-items: baseline;
    max-width: 35%;
    flex-wrap: wrap;
    justify-content: flex-end;
  }
  .tag {
    font-size: small;
    border-radius: 1em;
    background: black;
    padding: 0 0.5em 0 0.5em;
    color: white;

    &.red {
      background: darkred;
    }
    &.darkblue {
      color: black;
      background-color: #149eca;
    }
    &.purple {
      background-color: #5632d5;
    }
    &.orange {
      background-color: #e2492c;
    }
    &.green {
      color: black;
      background-color: #42d392;
    }
    &.teal {
      background-color: #00546b;
    }
    &.blue {
      background-color: #28799e;
    }
    &.turquoise {
      background-color: #08bef2;
    }
    &.darkred {
      background-color: #ab1d22;
    }
  }
</style>