<script>
export default {
    name: 'AppHeader',
    props:{
        title: String
    }
}
</script>

<template>
    <header>
        <div class="container">
            <div class="logo">
                <img src="/breakingbad.jpg" alt="logo">
            </div>
            <h2> {{title}} </h2>
        </div>
    </header>
</template>

<style lang="scss" scoped>


.container{
    display: flex;
    align-items: center;  
    .logo{
        height: 50px;
        margin: 10px;
        img{
        height: 100%;
        }
    }
} 
</style>