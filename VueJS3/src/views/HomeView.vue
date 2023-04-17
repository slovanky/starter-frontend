<template>
  <div class="w-full h-screen p-8 flex items-center justify-center">
    <div class="w-full md:w-[800px] p-8 flex flex-col gap-8 bg-slate-50 border border-slate-100 rounded-xl">
      <div class="flex gap-2 items-center justify-center">
        <button @click="() => changeLanguage('ar')" class="px-2 py-1 bg-blue-100 rounded">عربي</button>
        <button @click="() => changeLanguage('en')" class="px-2 py-1 bg-blue-100 rounded">English</button>
      </div>
      <div class="flex items-center justify-center text-xl">{{ $t('welcome') }}</div>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    changeLanguage(lang) {
      this.$i18n.locale = lang;
    },
  },
};
</script>
