<script >
import Card from './components/card.vue';

export default {
  components: { Card },
  data:()=>({
    trabajos:[
    {  
      "id" : '1',
    "logoUrl":"https://cdn.svgporn.com/logos/descript-icon.svg",
      "titleDescription": "Desarrollador Full stack / .net / Angular",
      "skills":[
        {
          "logoSkill":"https://cdn.svgporn.com/logos/javascript.svg",
          "nombreSkill":".JavaScript"
        },
        {
          "logoSkill":"https://cdn.svgporn.com/logos/c-plusplus.svg",
          "nombreSkill":".Net"
        },
      ],
      "empresa":"Tu Talento",
      "localizacion":"Bogotá",
      "salario":"5M - 7M",
      "moneda":"USD",
      "vacantes":"1",
      "dias":"5",
    },
    {  
      "id" : '2',
    "logoUrl":"https://cdn.svgporn.com/logos/dovetail-icon.svg",
      "titleDescription": "Ingeniero de datos Sr",
      "skills":[
        {
          "logoSkill":"",
          "nombreSkill":"Sql"
        },
        {
          "logoSkill":"",
          "nombreSkill":"Nube"
        },
        {
          "logoSkill":"https://cdn.svgporn.com/logos/c-plusplus.svg",
          "nombreSkill":"Python"
        },
      ],
      "empresa":"evaluaserve.com",
      "localizacion":"Remoto",
      "salario":"Confidencial",
      "moneda":"",
      "vacantes":"1",
      "dias":"2",
    },
    {  
      "id" : '3',
    "logoUrl":"https://cdn.svgporn.com/logos/jetbrains-space-icon.svg",
      "titleDescription": "Diseñador web  o Fullstack",
      "skills":[
        {
          "logoSkill":"https://cdn.svgporn.com/logos/javascript.svg",
          "nombreSkill":"JavaScript"
        },
        {
          "logoSkill":"https://cdn.svgporn.com/logos/html-5.svg",
          "nombreSkill":"Html"
        },
      ],
      "empresa":"Cadenas de valor sa",
      "localizacion":"Remoto",
      "salario":"2.5M - 3M",
      "moneda":"COP",
      "vacantes":"1",
      "dias":"2",
    },
    ]
  }),
}

</script>

<template>
  <main class="container ">
    <div v-for="trabajo in trabajos" :key="trabajo.id">
      <Card 
      :trabajo=trabajo
      />
    </div>
  </main>
</template>

<style scoped>


</style>
