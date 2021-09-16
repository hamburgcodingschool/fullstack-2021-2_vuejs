<template>
  <div class="flex flex-col content-center">
    <h1 class="text-4xl text-center my-8">Example List</h1>
    <UserList />
  </div>
</template>

<script>
import UserList from "./components/UserList.vue";

export default {
  name: "App",
  components: {
    UserList,
  },
};
</script>

<style scoped></style>
>
