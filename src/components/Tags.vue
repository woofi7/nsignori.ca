<script setup>
  import {defineProps} from "vue";

  defineProps({
    tags: Array
  })
</script>

<template>
  <div class="tags">
    <div v-for="tag in tags" class="tag" :class="tag.color">
      {{ tag.name }}
    </div>
  </div>
</template>

<style scoped>
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