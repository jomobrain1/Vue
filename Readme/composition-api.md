
### counter app with composition api
    
            <script setup>
            import { ref } from 'vue';
            const count=ref(0)
            </script>

            <template> 

            <main>
                <p>Counter Application</p>
                <p>{{count}}</p>
                <button @click="count++">increment</button>
                <button @click="count--">decrement</button>
            </main>
            </template>

### counter app with options api

          <script >
          export default{
            data() {
              return {
                count: 0
              };
            },
          
            methods: {
              addCount(){
                 this.count++
              }
            },
          }
          </script>
          
          <template> 
          
            <main>
               <h1>Counter Application</h1>
               <h2>{{count}}</h2>
               <button @click="addCount()">increment</button>
               <button @click="count--">decrement</button>
            </main>
          </template>
          
          <style scope>
          
          </style>
          

 
