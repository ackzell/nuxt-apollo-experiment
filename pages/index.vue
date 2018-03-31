<template>
  <v-layout row wrap>
    <v-list>
    <v-list-tile avatar v-for="post in feed" :key="post.id">
      <v-list-tile-title>ID</v-list-tile-title>
      <v-list-tile-content>
        {{ post.id }}
      </v-list-tile-content>
    </v-list-tile>
  </v-list>
  </v-layout>
</template>

<script>
import myFeed from '~/queries/feed.query.gql'

export default {
  data() {
    return {
      feed: []
    }
  },
  apollo: {
    feed: myFeed
  }
}
</script>

