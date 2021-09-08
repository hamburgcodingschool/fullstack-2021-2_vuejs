<template>
  <div>
    <form @submit="handleSubmit">
      <label for="inputId">Id:</label>
      <input type="text" name="id" id="inputId" />
      <br />
      <label for="inputName">Name:</label>
      <input type="text" name="id" id="inputName" />
      <br />
      <label for="inputCity">City:</label>
      <input type="text" name="city" id="inputCity" />
      <br />
      <button type="submit">Add Person</button>
    </form>
  </div>
</template>

<script>
export default {
  methods: {
    handleSubmit: async function (event) {
      event.preventDefault();
      console.log("Event:", event.target.elements.inputName.value);

      const newPerson = {
        id: event.target.elements.inputId.value,
        name: event.target.elements.inputName.value,
        city: event.target.elements.inputCity.value,
      };

      const response = await fetch("http://localhost:3000/api/new_person", {
        method: "POST",
        headers: {
          "Content-Type": "application/json",
        },
        body: JSON.stringify(newPerson),
      });

      const result = await response.json();
      console.log(result);
    },
  },
};
</script>

<style scoped></style>
