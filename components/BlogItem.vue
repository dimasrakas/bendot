<template>
  <div class="feature col">
    <div
      class="feature-icon d-inline-flex align-items-center justify-content-center text-bg-primary bg-gradient fs-2 mb-3"
    >
      <svg class="bi" width="1em" height="1em">
        <use xlink:href="#collection"></use>
      </svg>
    </div>
    <h2><slot /></h2>
    <p>
      Paragraph of text beneath the heading to explain the heading. We'll add
      onto it with another sentence and probably just keep going until we run
      out of words.
    </p>
    <a href="#" class="icon-link d-inline-flex align-items-center">
      Call to action
      <svg class="bi" width="1em" height="1em">
        <use xlink:href="#chevron-right"></use>
      </svg>
    </a>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped></style>
