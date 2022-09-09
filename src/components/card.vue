<script >
      export default {
       props: {
        trabajo: Object
       }
      }
</script>
    
    <template>
      <div class="card-empleo header d-flex align-items-center justify-content-center mx-auto mt-3 ">
        <div class="card-logo ">
            <img :src="trabajo.logoUrl" alt="logo-empresa" width="40" >
        </div>
        <div class="card-body p-1">
            <div class="d-flex align-items-center" >
                <div class="card-title">
                    {{trabajo.titleDescription}}
                </div>
                <div class="card-skill d-flex">
                    <div class="card-skill-target d-flex align-items-center" v-for="skill in trabajo.skills"><img v-show="skill.logoSkill" :src="skill.logoSkill" alt="logo-desarrollo" > <span> {{ skill.nombreSkill}}</span></div>
                </div>
            </div>
            <div class="card-feacture d-flex justify-content-between align-items-center">
                <div><i class="bi bi-building"></i> {{trabajo.empresa}}</div>
                <div><i class="bi bi-geo-alt"></i> {{trabajo.localizacion}}</div>
                <div><i class="bi bi-cash"></i> $ {{trabajo.salario}} {{trabajo.moneda}}</div>
                <div><i class="bi bi-people"></i> {{trabajo.vacantes}} {{ trabajo.vacantes > 1 ? "Vacantes": "Vacante"}}</div>
                <div><i class="bi bi-calendar3"></i> {{trabajo.dias}} {{ trabajo.dias > 1 ? "days ago": "day ago"}}</div>
            </div>
        </div>
        
      </div>
    </template>
    
    <style scoped>
        @import url('https://fonts.googleapis.com/css2?family=Roboto+Slab&display=swap');
        @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300;700&family=Roboto+Slab&display=swap');

    .header {
      
      padding: 5px 100px 5px 5px;
      border: 1px solid rgba(0,0,0,.125);
      width: 800px;
      background-color: white;
    }
    
    .header:hover {
        box-shadow: -2px 10px 20px 0px rgba(0, 0, 0, 0.2);
        
    }
    .card-logo{
       text-align: left ;
        padding: 10px;
       
    }
    .card-title{
        font-family: 'Montserrat', 'Roboto Slab', sans-serif;
        
        font-size: 1.2rem;
        font-weight:bolder ;
        margin-right: 15px;
    }
    .card-skill-target{
        font-size: 0.7rem;
        /* font-weight: bold; */
        border: 1px solid #666;
        border-radius: 10px;
        margin-right: 3px;
        
    }
    .card-skill-target img{
        width: 0.7rem;
        margin: 2px 3px;
     
    }
    .card-skill-target span{
        margin-right: 3px;
        margin-left: 3px;
    }

    .card-feacture{
        font-size: 0.8rem;
    }
    </style>
    