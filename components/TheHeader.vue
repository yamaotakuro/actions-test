<template>
  <header class="l-header">
    <div class="c-fluid">
      <ul class="l-header__list">
        <li class="l-header__item"><Nuxt-link to="/">Home</Nuxt-link></li>
        <!-- <li class="l-header__item"><NuxtLink to="/about">About</NuxtLink></li> -->
      </ul>
    </div>
  </header>
</template>

<style lang="scss">
@use '@/assets/sass/foundation' as f;
.l-header {
  &__list {
    display: flex;
    justify-content: center;
  }
  &__item {
    margin-right: 1em;
    a {
      display: flex;
      align-items: center;
      height: 50px;
    }
    &:last-child {
      margin-right: 0;
    }
  }
}
</style>
