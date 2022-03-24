<template>
  <v-form>
    <v-container>
      <v-row>
        <v-col
          cols="12"
          sm="6"
          md="3"
        >
          <v-text-field
            label="Regular"
          ></v-text-field>
        </v-col>
      </v-row>

  <v-data-table
    :headers="headers"
    :items="desserts"
    :items-per-page="5"
    class="elevation-1"
  
 

  ></v-data-table>

    </v-container>
  </v-form>
</template>

<script>
/* eslint-disable */
let objekt = {
name: "HomeView",
data: function() {
  return{
    commits: [],

  };
},


async mounted(){
  let podatci = await fetch("https://agify.io/");
  let podatci2 = await fetch("https://genderize.io/");
  let podatci3 = await fetch("https://nationalize.io/");

  let rezultati = await podatci.json();
  let rezultati2 = await podatci2.json();
  let rezultati3 = await podatci3.json();

this.commits.add(rezultati);
this.commits.add(rezultati2);
this.commits.add(rezultati3);

}
}


</script>
