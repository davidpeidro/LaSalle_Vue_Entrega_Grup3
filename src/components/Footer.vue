<template>
  <v-footer class="mt-5 rounded-1 footer" padless>
    <v-row justify="center" no-gutters>
      <v-btn
        v-for="link in links"
        :key="link"
        color="white"
        text
        rounded
        class="ml-2"
      >
        <router-link id="underline-link" v-if="link.isRouterLink" :to="link.href"> {{link.label}} </router-link>
        <a id="underline-link" v-else :href="link.href" target="_blank"> {{link.label}} </a>
      </v-btn>
      <v-col class="primary lighten-2 py-4 text-center white--text" cols="12">
        {{ new Date().getFullYear() }} — <strong>ToDo App- Grupo 3</strong>
      </v-col>
    </v-row>
  </v-footer>
</template>
<script>
export default {
  data: () => ({
    links: [
      { label: "Home", isRouterLink: true, href: "/" },
      { label: "About Us", isRouterLink: true, href: "/about-us" },
      {
        label: "GitHub",
        isRouterLink: false,
        href: "https://github.com/nvianaperez/ToDoList-group3",
      },
    ]    
  }),
};
</script>

<style>

  #underline-link {
    text-decoration: none;
  }

</style>
