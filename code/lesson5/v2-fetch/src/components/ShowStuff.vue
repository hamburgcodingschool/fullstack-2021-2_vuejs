<template>
  <div>
    <div v-for="(person, i) in people" :key="i" class="personBox">
      <ul>
        <li>{{ person.name }}</li>
        <li>{{ person.email }}</li>
        <li>{{ person.website }}</li>
        <li>{{ person.address.street }}</li>
      </ul>
    </div>
  </div>
  <!-- <button @click="handleClick">Fetch Stuff</button> -->
</template>

<script>
export default {
  data: function () {
    return {
      people: [],
    };
  },
  //   methods: {
  //     handleClick: function () {
  //       console.log("THIS HANDLE:", this);
  //       const component = this;

  //       fetch("https://jsonplaceholder.typicode.com/users")
  //         .then(function (response) {
  //           response.json().then(function (result) {
  //             component.people = result;
  //           });
  //         })
  //         .catch(function (error) {
  //           console.log("ERROR!");
  //           console.log(error);
  //         });
  //     },
  //   },
  mounted: async function () {
    try {
      const response = await fetch(
        "https://jsonplaceholder.typicode.com/users"
      );
      const result = await response.json();
      this.people = result;
    } catch (error) {
      console.log("ERROR!");
      console.log(error);
    }
  },
};
</script>

<style scoped>
.personBox {
  background-color: aquamarine;
  border: solid 2px red;
  margin: 5px;
}
</style>
