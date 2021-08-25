<template lang="pug">
v-app
  table
  
    // the display row
    tr
      th(colspan="4") 00000000
  
    tr
      td 7
      td 8
      td 9
      td X
  
    tr
      td 4
      td 5
      td 6
      td
        v-btn(
          fab
          color="warning"
        )
          v-icon mdi-minus
  
    tr
      td 1
      td 2
      td 3
      td
        v-btn(
          fab
          color="warning"
        )
          v-icon mdi-plus

</template>
