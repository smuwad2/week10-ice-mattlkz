<script>
    // TODO: Complete the code
    export default { 
        data() {
            return {
                
            }
        },
        // Hint: insert properties task (Object) and idx (Number)
    }
</script>

<template>
    <!-- TODO: add your template code here --> 
     <div class="card mb-3" style="width: 18rem;">

    <div class="card-body">
      <h5 class="card-title">Deadline: {{ task.deadline }}</h5>
      <p class="card-text">{{ entry }}</p>
      <p class="text-muted">Mood: {{ mood }}</p>
      
      <!-- Slot to display content passed from parent (the delete button) -->
      <slot></slot>
    </div>
  </div>
</template>


