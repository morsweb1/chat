<template>
<v-app>
  <v-app-bar app>
    <v-icon class="mr-10">{{ icons.mdiAccount }}</v-icon>
    <h2>{{ oneUser.name }}</h2>
    </v-app-bar>
  <v-main>
    <div style="height: 100%;">
      <nuxt/>
    </div>
  </v-main>
</v-app>
</template>

<script>
import {mapState} from 'vuex'
import {mdiAccount} from '@mdi/js'
export default {
  data: () => ({
    icons: {mdiAccount}
  }),
  computed: {
    ...mapState(['oneUser', 'messages'])
  },
  methods: {
    // message() {
    //   this.$socket.client.emit('craeteMessage', {
    //     text: 'from client '
    //   })
    // }
  }
}
</script>
