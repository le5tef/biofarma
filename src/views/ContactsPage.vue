<template>
  <v-row class="no-gutters" style="position: relative">
    <Map class="pa-0" />
    <Contacts />
  </v-row>
</template>
<script>
import Map from "../components/Map.vue";
import Contacts from "../components/Contacts.vue";
export default {
  components: {
    Map,
    Contacts,
  },
};
</script>