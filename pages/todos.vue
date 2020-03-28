<template>
  <section>Todos count: {{ todos.length }}</section>
</template>

<script>
import gql from "graphql-tag";

export default {
  apollo: {
    todos: {
      query: gql`
        query {
          todos {
            id
            title
          }
        }
      `
    }
  }
};
</script>
