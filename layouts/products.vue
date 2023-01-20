<template>

  <body>
    <header>
      <nav>
        <NuxtLink to="/">Nuxt 3</NuxtLink>
      </nav>
    </header>

    <div>
      <slot />
    </div>

    <footer>
      <ul>
        <li>
          <NuxtLink to="/">Home</NuxtLink>
        </li>
        <li>
          <NuxtLink to="/about">About</NuxtLink>
        </li>
        <li>
          <NuxtLink to="/products">Products</NuxtLink>
        </li>
      </ul>
    </footer>
  </body>

</template>

<style scoped>
.router-link-exact-active {
  color: #12b488;
}
</style>