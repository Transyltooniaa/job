<template>
  <h1>
    Page Not Found
    </h1>

    <div class="container">
        <div class="jobs">
            <h2>404</h2>
            <h3>Page Not Found</h3>
        </div>
    </div>
</template>

<script>
export default {

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


</style>