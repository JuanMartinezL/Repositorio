<template>
  <div class="p-5 text-center">© {{ date }} Hecho con 💙 Juan M.</div>
</template>
<script>
export default {
  setup() {
    const date = new Date().getFullYear()

    return {
      date,
    }
  },
}
</script>
<style lang="css"></style>
