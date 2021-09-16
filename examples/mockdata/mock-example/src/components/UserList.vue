<template>
  <table class="table-auto text-center">
    <thead>
      <tr>
        <th px-4 py-2>Name</th>
        <th px-4 py-2>Email</th>
        <th px-4 py-2>Website</th>
      </tr>
    </thead>
    <tbody>
      <tr v-for="(user, i) in apiResponseData" :key="i">
        <td class="border px-4 py-2">{{ user.name }}</td>
        <td class="border px-4 py-2">{{ user.email }}</td>
        <td class="border px-4 py-2">{{ user.website }}</td>
      </tr>
    </tbody>
  </table>
</template>

<script>
export default {
  data: function () {
    return {
      apiResponseData: undefined,
    };
  },
  mounted: async function () {
    const url = "http://localhost:8080/mockData.json";
    // const url = "https://jsonplaceholder.typicode.com/users";

    const response = await fetch(url);
    const result = await response.json();

    this.apiResponseData = result;
  },
};
</script>

<style></style>
