<script>
export default {
    name: 'Header'
}
</script>

<template>

    <header>
        <div class="logo">
            <img src="/public/Logo.webp" alt="Logo">
        </div>
        <h1>Yu-Gi-Oh Api</h1>
    </header>
  
</template>

<style lang="scss" scoped>

header {
    width: 100%;
    height: 80px;
    display: flex;
    align-items: center;
    .logo {
        img{
            width: 60px;
            margin: 0 20px;
        }
    }
    h1 {
        line-height: 80px;
    }
}

</style>