<template>
  <div>
    Both lines below should appear blue when viewport width is above 639px.
  </div>
  <div class="scoped">SCOPED</div>
  <div class="unscoped">UNSCOPED</div>
</template>

<style lang="postcss" scoped>
.scoped {
  @apply text-red-500;
}

@screen sm {
  .scoped {
    @apply text-blue-500;
  }
}
</style>

<style lang="postcss">
.unscoped {
  @apply text-red-500;
}

@screen sm {
  .unscoped {
    @apply text-blue-500;
  }
}
</style>

<style>
#app {
  font-family: sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  margin-top: 60px;
}
</style>