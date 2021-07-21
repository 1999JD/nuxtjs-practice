<template>
  <div class="flex flex-col border shadow">
    <h2 class="mb-2 p-4">
      {{ cardTitle }}
    </h2>
    <p class="mb-2 p-4">
      {{ cardBody }}
    </p>
    <footer class="p-4 bg-gray-300">
      {{ cardFooter }}
    </footer>
  </div>
</template>
<script>
export default {
  props: {
    cardTitle: {
      type: String,
      default: 'header'
    },
    cardBody: {
      type: String,
      default: 'body'
    },
    cardFooter: {
      type: String,
      default: 'footer'
    }
  }
}
</script>
