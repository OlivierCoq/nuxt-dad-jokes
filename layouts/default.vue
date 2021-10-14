<template>
  <div class="ctr">
      <AppHeader />
      <nuxt />
  </div>
</template>

<script>
import AppHeader from '../components/AppHeader';

export default {
    components: {
        AppHeader
    }
}
</script>

<style>

    body {
        font-family: Arial, Helvetica, sans-serif;
        background-color: #f4f4f4;;
    }

    .ctr {
        max-width: 800px;
        margin: 2rem auto;
        overflow: hidden;
        padding: 1rem 2rem;
        background-color: #fff;
    }
</style>