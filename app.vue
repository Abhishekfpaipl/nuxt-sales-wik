<template>
  <div>
    <NuxtRouteAnnouncer />
  </div>
  <TopNav v-if="!hide" />
  <NuxtPage />
  <FooterBar v-if="!hide" />
</template>

<script>

export default {
  name: 'App',
  computed: {
    hide() {
      const hiddenPages = ['DemoPage1', 'ThankYou', 'LoginPage', 'RegistrationPage', 'free-trial', 'demo', 'sales-demo-one', 'sales-demo-two']
      return hiddenPages.includes(this.$route.name)
    },
  }

}
</script>

<style>
:root {
  --bg-primary: #014c75;
  --bg-secondary: #EB5E28;
  --bg-tertiary: #FEC007;
  --bg-forth: #FBF4F4;
}

.smaller {
  font-size: 10px;
}
</style>