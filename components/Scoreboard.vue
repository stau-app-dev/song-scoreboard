<template>
  <div class="relative overflow-x-auto shadow-md rounded-lg">
    <table class="w-full text-left text-sm text-gray-400">
      <thead class="text-xs uppercase bg-primary text-gray-400">
        <tr>
          <th scope="col" class="py-3 px-6">Rank</th>
          <th scope="col" class="py-3 px-6">Name</th>
          <th scope="col" class="py-3 px-6">Votes</th>
        </tr>
      </thead>
      <tbody class="text-xl">
        <tr
          v-for="(song, index) in songs"
          :key="`song-${index}`"
          class="border-b border-red-700"
        >
          <th
            scope="row"
            class="whitespace-nowrap py-4 px-6 font-medium text-white"
          >
            #{{ index + 1 }}
          </th>
          <td class="py-4 px-6 text-gray-100">
            {{ song.name }} by {{ song.artist }}
          </td>
          <td class="py-4 px-6 text-gray-100">{{ song.upvotes }}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
export default {
  name: 'ScoreboardComponent',
  props: {
    songs: {
      type: Array,
      required: true,
    },
  },
};
</script>

<style lang="postcss" scoped>
tbody {
  tr:nth-child(even) {
    @apply bg-red-800;
  }

  tr:nth-child(odd) {
    @apply bg-red-900;
  }
}
</style>
