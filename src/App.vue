<template>
  <v-app>
    <v-app-bar app color="primary" dark>
      <v-btn v-for="(btn, idx) in btns" :key="idx" text :to="btn.route">{{
        btn.name
      }}</v-btn>
    </v-app-bar>

    <v-main>
      <router-view />
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: "App",

  data: () => ({
    btns: [
      { name: "Work", route: "/" },
      { name: "About me", route: "/aboutme" },
      { name: "Contact", route: "/contact" },
    ],
  }),
};
</script>

<style scoped></style>
