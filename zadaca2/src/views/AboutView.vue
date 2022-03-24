<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Zadaća 2"/>

  </div>
</template>

<script>
let objekt = {
name: "AboutView",
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
