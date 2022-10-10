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
        <tr class="border-b border-red-700 bg-red-900">
          <th
            scope="row"
            class="whitespace-nowrap py-4 px-6 font-medium text-white"
          >
            #1
          </th>
          <td class="py-4 px-6 text-gray-100">Never Gonna Give You Up</td>
          <td class="py-4 px-6 text-gray-100">399</td>
        </tr>
        <tr class="border-b border-red-700 bg-red-800">
          <th
            scope="row"
            class="whitespace-nowrap py-4 px-6 font-medium text-white"
          >
            #2
          </th>
          <td class="py-4 px-6 text-gray-100">Baby</td>
          <td class="py-4 px-6 text-gray-100">300</td>
        </tr>
        <tr class="border-b border-red-700 bg-red-900">
          <th
            scope="row"
            class="whitespace-nowrap py-4 px-6 font-medium text-white"
          >
            #3
          </th>
          <td class="py-4 px-6 text-gray-100">Baby Shark</td>
          <td class="py-4 px-6 text-gray-100">200</td>
        </tr>
        <tr class="border-b border-red-700 bg-red-800">
          <th
            scope="row"
            class="whitespace-nowrap py-4 px-6 font-medium text-white"
          >
            #4
          </th>
          <td class="py-4 px-6 text-gray-100">Count on Me</td>
          <td class="py-4 px-6 text-gray-100">143</td>
        </tr>
        <tr class="border-b border-red-700 bg-red-900">
          <th
            scope="row"
            class="whitespace-nowrap py-4 px-6 font-medium text-white"
          >
            #5
          </th>
          <td class="py-4 px-6 text-gray-100">Take on Me</td>
          <td class="py-4 px-6 text-gray-100">99</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
export default {
  name: 'ScoreboardComponent',
};
</script>
