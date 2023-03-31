<template>
    <div>
        <h1>Hola home</h1>
        <p>Holaaaa</p>
        <p>
            <NuxtLink to="/blog">Ir al blog</NuxtLink>
        </p>
        <h1>Usuarios</h1>
        <User v-for="user in users" :name="user.name" />
    </div>
</template>
<script setup>

import { createClient } from '@supabase/supabase-js'

// Create a single supabase client for interacting with your database
const supabase = createClient('https://xlcrtmastjguisxahvdj.supabase.co', 'eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJzdXBhYmFzZSIsInJlZiI6InhsY3J0bWFzdGpndWlzeGFodmRqIiwicm9sZSI6ImFub24iLCJpYXQiOjE2Nzk1NjA5NDgsImV4cCI6MTk5NTEzNjk0OH0.1D3qe9lcU4aZvV0737sY8gS8knaMk6nMMmefSUQT6BY')

const inputFile = ref();

//async funtion subirFoto() {
    //const { data, error } = await
//}

const { data, error } = await supabase
  .from('photos')
  .select()

console.log(data)

const { data: users } = await useFetch('https://jsonplaceholder.typicode.com/users')

</script>