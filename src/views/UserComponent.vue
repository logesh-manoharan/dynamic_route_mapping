<template>
    <div>
        <h1>User Component</h1>  
        <p>User - {{$route.params.id}}</p>
    </div>
</template>

<script>
export default {
    name: "UserComponent"
}
</script>