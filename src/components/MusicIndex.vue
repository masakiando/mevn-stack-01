<template>
  <table class="table is-fullwidth is-striped is-hoverable is-narrow">
  <thead>
    <th style="width: 30%">th1</th>
    <th style="width: 30%">th2</th>
    <th style="width: 20%">th3</th>
    <th style="width: 20%">th4</th>
    </thead>

  <tbody v-for="(song, index) in songs" v-bind:key="index">
    <tr>
      <td>{{ song.artist }}</td>
      <td>{{ song.title }}</td>
      <td>{{ song.album }}</td>
      <td>{{ song.genre }}</td>
    </tr>
  </tbody>

  </table>
</template>

<script>
import MusicData from '@/assets/list.json'

export default {
  data () {
    return {
      songs: MusicData
    }
  }
}
</script>

<style>

</style>
