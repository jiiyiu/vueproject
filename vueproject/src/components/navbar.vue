<template>
<nav>
    <v-toolbar>
        <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>

        <v-toolbar-title >
            <span class="font-weight-thin">CECI EST UN SITE TEST</span>
        </v-toolbar-title>

        <v-spacer></v-spacer>

        <v-btn icon>
            <v-icon>mdi-magnify</v-icon>
        </v-btn>
    </v-toolbar>

    <v-navigation-drawer
      v-model="drawer"
      absolute
      temporary
    >
      <v-list-item>
        <v-list-item-avatar>
          <v-img src="data:image/jpeg;base64,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"></v-img>
        </v-list-item-avatar>

        <v-list-item-content>
          <v-list-item-title>JiiYiu</v-list-item-title>
        </v-list-item-content>
      </v-list-item>

      <v-divider></v-divider>

      <v-list dense>

        <v-list-item
          v-for="item in items"
          :key="item.title"
          link
        >
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

</nav>
</template>

<script>
export default {
    data () {
      return {
        drawer: null,
        items: [
          { title: 'Home'},
          { title: 'About' },
        ],
      }
    },
  }
</script>