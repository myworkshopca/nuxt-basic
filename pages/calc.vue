<template lang="pug">
v-app
    v-card(
        class = "mx-auto"
        max-width = "500"
        outlined
    )
        table
            // display the result.
            tr
              th(colspan = "4")
                v-text-field(
                    filled
                    clearable
                    v-model="result"
                )
            // reminder area.
            //tr
            //  td(colspan = "4")
            //    span {{ result }}
            // first row 7, 8, 9
            tr
              td( 
                v-for="n in [7, 8, 9]"
                :key="n"
              )
                v-btn(
                  large
                  fab
                  color = "deep-purple darken-4"
                  @click="numberClick(n)"
                ) 
                  v-icon(
                      color = "grey lighten-5"
                  ) {{ "mdi-numeric-" + n + "-circle" }}
              td 
                v-btn(
                 large
                 fab
                 color = "red lighten-1"
                ) 
                    v-icon mdi-close
            // second row: 4, 5, 6
            tr
              td( 
                v-for="n in [4, 5, 6]"
                :key="n"
              )
                v-btn(
                  large
                  fab
                  color = "deep-purple darken-4"
                  @click="numberClick(n)"
                ) 
                  v-icon(
                      color = "grey lighten-5"
                  ) {{ "mdi-numeric-" + n + "-circle" }}
              td 
                v-btn(
                 large
                 fab
                 color = "red lighten-1"
                ) 
                    v-icon mdi-minus
            tr
              td( 
                v-for="n in [1, 2, 3]"
                :key="n"
              )
                v-btn(
                  large
                  fab
                  color = "deep-purple darken-4"
                  @click="numberClick(n)"
                ) 
                  v-icon(
                      color = "grey lighten-5"
                  ) {{ "mdi-numeric-" + n + "-circle" }}
              td 
                v-btn(
                 large
                 fab
                 color = "red lighten-1"
                 @click="operatorClick('+')"
                ) 
                    v-icon mdi-plus
            tr
              td 
                v-btn(
                 large
                 fab
                 color = "deep-purple darken-4"
                ) 
                    v-icon(
                        color = "grey lighten-5"
                    ) mdi-numeric-0-circle
              td 
                v-btn(
                 large
                 fab
                 color = "deep-purple darken-4"
                )
                    v-icon(
                        color = "grey lighten-5"
                    ) mdi-circle-small
              td 
                v-btn(
                  large
                  fab
                  color = "deep-purple darken-4"
                  outlined
                )
                    v-icon mdi-arrow-left-bold
              td 
                v-btn(
                 large
                 fab
                 color = "red lighten-1"
                ) 
                    v-icon mdi-slash-forward
            tr
              //td
              //  v-btn(
              //    large
              //    color = "green accent-4"
              //    fab
              //  )
              //      v-icon mdi-plus-minus-variant 
              //td
              //  v-btn(
              //    large
              //    fab
              //    color = "red lighten-1"
              //  )
              //      v-icon mdi-exponent
              //td
              th(colspan = "4")
                v-btn(
                 large 
                 color = "red lighten-1"
                 block
                ) 
                    v-icon(
                       large
                    ) mdi-equal
</template>
<script>
export default {

    data: function() {

        return {
            result: "0",
        };
    },

    methods: {

        /**
         * number button click
         */
        numberClick: function(n) {

            if( this.result === "0" ) {
                this.result = "" + n;
            } else {
                this.result = this.result + n;
            }
        },

        /**
         * operator click
         */
        operatorClick: function(operator) {

            if( this.result === "0" ) {
                // ignore.
            } else {
                this.result = this.result + operator;
            }
        },
    }
}
</script>
