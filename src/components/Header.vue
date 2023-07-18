<template>
  <header class="header">
    <div class="header__row">
      <div class="header__column">
        <a href="#" class="header__logo">
          <img src="@/assets/header/logo.svg" alt="">
        </a>
      </div>
      <div class="header__column">
        {{ new Date().toLocaleTimeString() }}
      </div>
      <div class="header__column">
        <button @click="hand" class="border-2 border-red-800 btn">Button</button>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  
}
</script>

<style lang="">
  
</style>