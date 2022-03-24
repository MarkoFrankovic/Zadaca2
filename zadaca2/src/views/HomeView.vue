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
    {{ovjekt}}
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

  console.log(podatci);
  console.log(podatci2);
  console.log(podatci3);

  let rezultati = await podatci.json();
  let rezultati2 = await podatci2.json();
  let rezultati3 = await podatci3.json();

console.log(rezultati);
console.log(rezultati2);
console.log(rezultati3);

this.commits = rezultati;
this.commits = rezultati2;
this.commits = rezultati3;

}
}
</script>
