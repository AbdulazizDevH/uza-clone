<template>
  <header class="header">
    <div class="header__row px-6 pt-6 pb-2.5 xl:container flex justify-between items-end mx-auto">
      <div class="header__column">
        <a href="#" class="header__logo">
          <img src="@/assets/header/logo.svg" alt="LOGO">
        </a>
      </div>
      <div class="header__column w-[55%] mx-8">
        <div class="header__column-row py-5 px-1 text-xs flex justify-between items-center">
          <span class="flex items-center">
            {{ getFullDate() }}
            <b class="font-medium mx-1.5">|</b>
            <time datetime="2024-01-01">{{ time }}</time>
          </span>
          <span></span>
        </div>
        <div class="header__column-row flex items-center bg-white px-4 py-2 w-full rounded-md">
          <i class="bi bi-search opacity-50 text-xl"></i>
          <input type="text" class="text-sm px-[18px] outline-none py-2.5" placeholder="Sayt bo'ylab izlash">
        </div>
      </div>
      <div class="header__column w-80">
        <div class="header__column-row py-2 flex items-center justify-between">
          <div></div>
          <div class="header__socially  flex items-center justify-between w-40">
            <i class="bi bi-facebook"></i>
            <i class="bi bi-twitter"></i>
            <i class="bi bi-instagram"></i>
            <i class="bi bi-youtube"></i>
            <i class="bi bi-telegram"></i>
          </div>
        </div>
        <div class="header__column-row flex items-center justify-end py-2">
          <a href="#" class="header__auth bg-white inline-flex items-center rounded-full border border-[#e2effe]">
            <span class="w-[40px] h-[40px] flex items-center justify-center border text-[#a6c2e2] border-[#e2effe] rounded-full">
              <i class="bi bi-person-circle"></i>
            </span>
            <span class="px-5 py-3 text-xs">Kabinet</span>
          </a>
          <a href="#" class="header__lang bg-white inline-flex items-center ml-5 rounded-full border border-[#e2effe]">
            <span class="px-5 py-3 text-xs">O'zbek</span>
            <span class="w-[40px] h-[40px] flex items-center justify-center border text-xs font-bold border-[#e2effe] rounded-full">
              <i class="bi bi-chevron-down"></i>
            </span>
          </a>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  data() {
    return {
      time: "",
    }
  },
  methods: {
    getFullDate(d = new Date()) {
      let day = d.getDate() < 10 ? "0" + d.getDate() : d.getDate(),
        month = d.getMonth() < 9 ? "0" + (d.getMonth() + 1) : (d.getMonth() + 1),
        year = d.getFullYear() < 10 ? "0" + d.getFullYear() : d.getFullYear();
      return `${day}.${month}.${year}`;
    },
    getFullTime(d = new Date()) {
      let hour = d.getHours() < 10 ? '0' + d.getHours() : d.getHours(),
        min = d.getMinutes() < 10 ? '0' + d.getMinutes() : d.getMinutes(),
        sec = d.getSeconds() < 10 ? '0' + d.getSeconds() : d.getSeconds();
      return this.time = `${hour}:${min}:${sec}`
    }
  },
  mounted() {
    setInterval(this.getFullTime);
  },
}
</script>

<style lang="">
  
</style>