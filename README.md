1. how to compare two JSON have the same properties without  the order?
  let obj = {name : "person",age:"5"} ;
  let obj1= {name : "person",age:"5"} ;

TASK SOLUTION :

let obj = { name: "person", age: "5" };
let obj1 = { name: "person", age: "5" };

let objStr = JSON.stringify(obj);
let obj1Str = JSON.stringify(obj1);

if (objStr === obj1Str) {
  console.log("The JSON objects have the same properties.");
} else {
  console.log("The JSON objects do not have the same properties.");
}

<------------------------------------------------------------------------------------------>

2.use the rest countries  API  url "https://restcountries.com/v3.1/all" display all the countries flag in the console

TASK SOLUTION :

fetch("https://restcountries.com/v3.1/all")
  .then(response => response.json())
  .then(data => {
    data.forEach(country => {
      console.log(country.flags.png);
    });
  })
  .catch(error => {
    console.log("An error occurred while fetching the data:", error);
  });
<------------------------------------------------------------------------------------------>

3.use the rest countries  API  url "https://restcountries.com/v3.1/all" display all the countries flag in the console give me proper code in json formate 

TASK SOLUTION :

fetch("https://restcountries.com/v3.1/all")
  .then(response => response.json())
  .then(data => {
    data.forEach(country => {
      const name = country.name.common;
      const region = country.region;
      const subregion = country.subregion;
      const population = country.population;

      console.log("Name: " + name);
      console.log("Region: " + region);
      console.log("Subregion: " + subregion);
      console.log("Population: " + population);
      console.log("-----------------------------");
    });
  })
  .catch(error => {
    console.log("An error occurred while fetching the data:", error);
  });






















