
	<code>
    
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

    </code>
