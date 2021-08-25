<template lang="pug">
v-app
  h1 Hello World
  h2 Hello second world

  v-row(
    align="center"
    justify="space-around"
  )
    // try the button component.
    v-btn(
      color="primary"
    ) Normal

    v-btn(
      color="success"
    ) Success

    v-btn(
      fab
      dark
      color="error"
    )
      v-icon(
        dark
      ) mdi-ab-testing
</template>
