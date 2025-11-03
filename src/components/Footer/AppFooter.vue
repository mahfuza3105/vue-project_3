<template>
    <div class="container">
        <div class="footer">
            <p>Copyright@Mohirdev</p>
        </div>
    </div>
</template>
<style scoped>
.container{
    margin-top: 200px;
    justify-content: center;
    display: flex;
}
.footer{
    width: 100%;
    height: 58px;
    display: flex;
    justify-content: center;
    background-color: #02A28F;
    align-items: center;
    color: #ffffff;
}
@media screen and (max-width:768px) {
    .footer{
       width: 1160px; 
    }
    
}
</style>