<template>
    <footer class="container-fluid">
        <div class="row">
            <p class="lead"> Copyright &copy; {{cYear}}</p>
        </div>
    </footer>
</template>

<script>
    export default {
        data(){
            return{
                cYear:new Date().getUTCFullYear()
            }
        }
    }
</script>

<style scoped>

</style>