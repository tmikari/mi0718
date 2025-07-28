<template>
  <v-container>
    <v-row justify="center" class="mt-5">
      <v-col cols="12" md="6">
        <v-card>
          <v-card-title>検索結果</v-card-title>
          <v-card-text>
            <p><strong>単語：</strong> {{ word }}</p>
            <p><strong>品詞：</strong> {{ partOfSpeech }}</p>
            <p><strong>意味：</strong> {{ definition }}</p>
          </v-card-text>
          <v-card-actions>
            <v-btn color="primary" @click="$router.push('/')">戻る</v-btn>
          </v-card-actions>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import { mapGetters } from 'vuex'

export default {
  computed: {
    ...mapGetters ('search',[
      'getWord', 
      'getDefinition', 
      'getPartOfSpeech',
      'getError'
    ]),
    word() {
      return this.getWord
    },
    definition() {
      return this.getDefinition
    },
    partOfSpeech() {
      return this.getPartOfSpeech
    },
    error() {
      return this.getError
    }
  }
}
</script>
