<template>
    <div class="MainComponent">
        <div></div>
        <div class="content">
            <h1>Get in touch </h1>
            <a href="mailto:">example@email.com</a>
        </div>
        <div></div>
    </div>
</template>
<style lang="scss" scoped>
.MainComponent{
    display: grid;
    grid-template-columns: 1fr 4fr 1fr;
    height: 560px;
    .content{
        display: grid;
        grid-auto-flow: row;
        grid-gap: 100px;
        align-content: center;
        justify-content: center;
        text-align: center;
        h1{
            font-size: 56px;
            letter-spacing: 1.5px;
        }

        a{
            text-decoration: none;
            color: black;
        }
    }
}
</style>