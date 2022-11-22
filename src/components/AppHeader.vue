<script>
export default {
    name: 'AppHeader',
}
</script>

<template>
    <header>
        <div class="container">
            <div class="logo">
                <img src="/breakingbad.jpg" alt="logo">
            </div>
            <h1>Breaking Bad Api</h1>
        </div>
    </header>
</template>

<style lang="scss" scoped>
    
.container{
    display: flex;
    align-items: center;
    margin: 20px;    
    .logo{
        height: 50px;
        margin: 10px;
        img{
        height: 100%;
        }
    }
}   
</style>