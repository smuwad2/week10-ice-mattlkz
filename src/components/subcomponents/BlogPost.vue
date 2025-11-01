]<script>
export default {
  props: {
    subject: {
      type: String,
      required: true
    },
    entry: {
      type: String,
      required: true
    },
    mood: {
      type: String,
      required: true
    }
  },
  computed: {
    imgLoc() {
      return `/assets/${this.mood.toLowerCase()}.png`
    }
  }
}
</script>

<template>
  <div class="card mb-3" style="width: 18rem;">
    <img :src="imgLoc" class="card-img-top" :alt="mood">
    <div class="card-body">
      <h5 class="card-title">{{ subject }}</h5>
      <p class="card-text">{{ entry }}</p>
      <p class="text-muted">Mood: {{ mood }}</p>
      
      <!-- Slot to display content passed from parent (the delete button) -->
      <slot></slot>
    </div>
  </div>
</template>

