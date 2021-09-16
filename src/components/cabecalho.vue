<template>
    <header>
        <h1>{{ valor }}</h1>
    </header>
</template>

<script>
export default {
    props: ["valor"],
}
</script>

<style>
header {
    top: 0px;
    width: 100%;
    height: 50px;
    display: flex;
    color: white;
    position: fixed;
    align-items: center;
    justify-content: center;
    background: rgb(108,101,222);
    background: radial-gradient(circle, rgba(108,101,222,1) 0%, rgba(166,82,196,1) 100%);
}
</style>