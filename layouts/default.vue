<template>
  <div>
    <div class="container">
      <header class="d-flex justify-content-center py-3">
        <ul class="nav nav-pills">
          <li class="nav-item">
            <NuxtLink
              to="/"
              class="nav-link"
              :class="$route.name === 'index' ? 'active' : ''"
              aria-current="page"
              >Home</NuxtLink
            >
          </li>
          <li class="nav-item">
            <NuxtLink
              to="/about"
              class="nav-link"
              :class="$route.name === 'about' ? 'active' : ''"
              >About</NuxtLink
            >
          </li>
          <li class="nav-item">
            <NuxtLink to="/bendot" class="nav-link">BENDOT</NuxtLink>
          </li>
          <li class="nav-item"><a href="#" class="nav-link">FAQs</a></li>
          <li class="nav-item"><a href="#" class="nav-link">About</a></li>
        </ul>
      </header>
    </div>

    <Nuxt />

    <p>Ini footer</p>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped></style>
