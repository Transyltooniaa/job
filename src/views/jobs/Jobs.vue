<template>
    <h1>
        Jobs
    </h1>

    <div class="container">
        <div v-for="job in jobs" :key="job.id" class="jobs">
            <h2>{{ job.title }}</h2>
            <h3>{{ job.company }}</h3>
            <router-link :to="{ name: 'JobDetails', params: { id: job.id } }">View Details</router-link>
        </div>
    </div>
  
  
</template>

<script>
export default {
    data() {
        return {
            jobs: [
                { id: 1, title: 'Frontend Developer', company: 'Google', description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Quasi laudantium vel harum optio, a natus rerum minima praesentium voluptatum impedit iusto, quia nesciunt commodi cumque, libero sint aspernatur illo sunt?' },
                { id: 2, title: 'Backend Developer', company: 'Facebook', description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Quasi laudantium vel harum optio, a natus rerum minima praesentium voluptatum impedit iusto, quia nesciunt commodi cumque, libero sint aspernatur illo sunt?' },
                { id: 3, title: 'Fullstack Developer', company: 'Amazon', description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Quasi laudantium vel harum optio, a natus rerum minima praesentium voluptatum impedit iusto, quia nesciunt commodi cumque, libero sint aspernatur illo sunt?' },
                { id: 4, title: 'DevOps Engineer', company: 'Microsoft', description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Quasi laudantium vel harum optio, a natus rerum minima praesentium voluptatum impedit iusto, quia nesciunt commodi cumque, libero sint aspernatur illo sunt?' },
                { id: 5, title: 'Data Scientist', company: 'Apple', description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Quasi laudantium vel harum optio, a natus rerum minima praesentium voluptatum impedit iusto, quia nesciunt commodi cumque, libero sint aspernatur illo sunt?' },
            ]
        }
    },



}
</script>

<style scoped>

.container {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-wrap: wrap;
}

.jobs {
    border: 1px solid black;
    padding: 10px;
    margin: 50px;
    border-radius: 10px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    background-color: yellowgreen;
    color: black;
    width: 50%;
}

.jobs:hover{
    background-color: crimson;
    color: white;
    transition: all 0.5s;
}

h2 {
    font-size: 2em;
    text-transform: uppercase;
}

h3{
    font-size: 1.5em;
    color: #333;
    font-weight: bold;
}


</style>