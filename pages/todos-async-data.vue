<template>
  <section>Todos count: {{ todos.length }}</section>
</template>

<script>
import gql from "graphql-tag";

export default {
  async asyncData(context) {
    const client = context.app.apolloProvider.defaultClient;

    // a little delay to demo that client-side nav waits for data to load
    await new Promise(resolve => setTimeout(resolve, 1500));

    const result = await client.query({
      query: gql`
        query {
          todos {
            id
            title
          }
        }
      `
    });

    return {
      todos: result.data.todos
    };
  }
};
</script>
