<script setup>
import {FontAwesomeIcon} from "@fortawesome/vue-fontawesome";

defineProps({
  show: Boolean,
  imgSrc: String
})

</script>

<template>
  <div class="preview" :class="[show ? 'show' : '']">
    <div class="content">
      <div class="closeButton" @click="$emit('toggleShow')">
        <font-awesome-icon icon="fa-solid fa-x" />
      </div>
      <img :src="imgSrc" alt="Preview of artefact">
    </div>
  </div>
</template>

<style scoped>
.preview {
  z-index: 2;
  display: none;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  justify-content: center;
  align-items: center;

  background-color: rgba(0, 0, 0, 0.4);

  &.show {
    display: flex;
  }
  & > .content {
    position: relative;
    max-width: 80%;
    max-height: 80%;

    & > img {
      object-fit: contain;
      width: 100%;
      height: 100%;
    }
    & > .closeButton {
      position: absolute;
      right: 0;
      width: 1.5em;
      height: 1.5em;
      border-radius: 1em;
      margin: 0.5em;
      font-size: xx-large;

      display: flex;
      justify-content: center;
      align-items: center;

      background-color: rgba(0, 0, 0, 0.8);
      cursor: pointer;
      &:hover {
        color: white;
        background-color: rgba(0, 0, 0, 1);
      }
    }
  }
}
</style>