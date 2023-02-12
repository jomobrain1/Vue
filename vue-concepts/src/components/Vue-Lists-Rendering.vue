<template>
    <div>
       <h1>List Rendering</h1> 
       <!-- Rendering an array -->
       <div v-for="(lang,index) in languages" :key="lang">
           <p>{{ index + 1 }}  {{lang}}</p>
       </div> <hr> <br> <br>
       
      <section class="flex">
        <div  v-for="work in workers" :key="work.id">
           <div >
            <p>{{ work.name }}</p>
            <b>{{ work.role }}</b> <br>
           <small>{{ work.salary }}</small>
           </div>
       </div>
      </section>
      <hr> <br> <br>
      <!-- Loop 3 -->
       <div class="flex1">
           <section v-for="dev in devs" :key="dev.name">
             <p>{{ dev.name }}</p>
             <p v-for="d in dev.stack">
              <h3>{{ d }}</h3>
             </p>
           </section>
       </div>

       <!-- iteration with index and values -->
       <div v-for="(value,key,index) in bio" :key="value">
          <p>{{ key }} {{ value }} {{ index }}</p>
       </div>

    </div>
</template>

<script>
export default {   

    data() {
        return {
            languages:["Vue","javascript","flutter","php"],
            workers:[
                {   id:1,
                    name:"jomobrain1",
                    role:"front-end engineer",
                    salary:160450
                },
                {   id:2,
                    name:"richmondy",
                    role:"backend",
                    salary:260450
                },
                {   id:3,
                    name:"marygoldwine",
                    role:"mobile",
                    salary:60450
                }
            ],
            devs:[
                {
                    name:"purity",
                    stack:['node','react','aws']
                },
                {
                    name:"jomo",
                    stack:['laravel','vue','flutter']
                }
            ],
            bio:{
                name:"jomoRay",
                age:23,
                school:"jsbits"
            }
        };
    },
   
};
</script>

<style scoped>
.flex,.flex1{
    display: flex;
    flex-wrap: wrap;
    gap: 1em;
    justify-content: center;
}
.flex>*,.flex1>*{
    flex-basis: 30%;
    min-width: 15rem;
    padding: 20px 15px;
    background: steelblue;
    color: #ffff;
}
.flex1>*{
    background: orangered;
}
</style>