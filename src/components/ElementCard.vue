<script setup>
  defineProps({
    title: String,
    date: String,
    linkText: String,
    linkUrl: String,
    logoUrl: String,
    location: String
  })
</script>

<template>
  <div class="card">
    <div class="header">
      <div class="logo">
        <img :src="logoUrl" alt="Logo ETS">
      </div>
      <div>
        <h3 class="title">{{ title }}</h3>
        <span class="date">{{ date }}</span>
      </div>
    </div>
    <div>
      <p class="location">
        <a :href="linkUrl">{{ linkText }}</a>, {{ location }}
      </p>
    </div>
  </div>
</template>

<style scoped>
.card {
  display: flex;
  flex-direction: column;
  background-color: #252525;
  padding: 0.5rem;
  justify-content: space-between;
}
.header {
  display: flex;
  gap: 0.5rem;
}
.logo {
  img {
    width: 75px
  }
}
.title {
  color: white;
}
.date {
}
.location {
}
</style>