<script setup lang="ts">
import NewPurchase from '@/components/NewPurchase.vue';
import Dept from '@/components/Dept.vue'
import Credits from '@/components/Credits.vue'

</script>

<template>
  <div class="container">
    <div class="row">
      <div class="col-md-4 col-sm-12 mt-3">
        <NewPurchase></NewPurchase>

      </div>

      <div class="col-md-8 col-sm-12 mt-3">
        <Dept />

        <Credits />
      </div>
    </div>

  </div>
</template>
