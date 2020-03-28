<template>
  <div>
    <div>
      <h2>Using Apollo Object</h2>
      <p>
        <a href="http://localhost:3000/todos">
          /todos (SSR) - this works
        </a>
      </p>

      <p>
        <nuxt-link to="/todos">
          /todos (client-side nav) - this breaks
        </nuxt-link>
      </p>

      <h2>Using asyncData</h2>
      <p>
        <a href="http://localhost:3000/todos-async-data">
          /todos-async-data (SSR) - this works
        </a>
      </p>

      <p>
        <nuxt-link to="/todos-async-data">
          /todos-async-data (client-side nav) - this works too
        </nuxt-link>
      </p>
    </div>
  </div>
</template>
