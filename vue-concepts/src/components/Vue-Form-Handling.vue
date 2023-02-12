<template>
    <div>
        <!-- Uses v-model for 2 way binding -->
      <h1> VueFormHandling</h1>

      <form @submit="submitForm">
        <div>
            <label for="name">Name {{formValues.name }}</label> <br>
            <input type="text" v-model="formValues.name">
        </div>
        <div>
            <label for=""> TextArea </label> <br>
            <textarea v-model="formValues.text"></textarea>
        </div>
        <div>
            <label for="">Select Box {{formValues.language }}</label> <br>
            <select v-model="formValues.language">
                <option value="">Select Your Language</option>
             <option value="Vue">Vue</option>
             <option value="Flutter">Flutter</option>
             <option value="Kotlin">Kotlin</option>
             <option value="Laravel">Laravel</option>
            </select>
        </div>
        <br>
        <div>
            <h2>Multiple Selection</h2>
             <p v-for="loc in formValues.locations">{{ loc }}</p>
            <select multiple v-model="formValues.locations">
            <option value="">Select Location</option>
            <option value="Florida">Florida</option>
            <option value="Manchester">Manchester</option>
            <option value="Mtwapa">Mtwapa</option>
            </select>
        </div> <br>
        <hr> <br>
        <div>
            <h1>CheckBox {{ formValues.checked }}</h1>
            <input type="checkbox" v-model="formValues.checked">
            <h1>Check Box 2 Languages {{ formValues.skills }}</h1>
            <label for="">Html</label>
            <input type="checkbox" value="html" v-model="formValues.skills">
            <label for="">Css</label>
            <input type="checkbox" value="css" v-model="formValues.skills">
            <label for="">js</label>
            <input type="checkbox" value="js" v-model="formValues.skills">
        </div>
        <div>
            <h2>Radio Buttons School Levels  {{ formValues.level }}</h2>
      
            <div>
                <p>Secondary</p>
                <input type="radio" value="secondary" v-model="formValues.level">
            </div>
            <div>
                <p>University</p>
                <input type="radio" value="University" v-model="formValues.level">
            </div>
            <div>
                <p>PhD</p>
                <input type="radio" value="PhD" v-model="formValues.level">
            </div>
        </div>
        <button type="submit">Submit</button>
      </form>

    </div>
</template>

<script>
export default {
  

    data() {
        return {
            formValues:{
                name:"jomobrain1",
                text:"This is just dummy text",
                language:"",
                locations:[],
                checked:true,
                skills:[],
                level:""
            }
        };
    },

    methods:{
        submitForm(ev){
            ev.preventDefault()
            console.log(this.formValues);
        }
    }

    
};
</script>

<style>
h1{
    margin-bottom: 40px;
}
</style>