<template>
    <div class="jumbotron jumbotron-fluid">
        <div class="container">
            <h1 class="display-4">Temukan hal-hal menakjubkan <br/> untuk dilakukan Kapan saja, dimana saja.</h1>
            <form class="form-inline my-2 my-lg-0 justify-content-center ">
        <input class="form-control mr-sm-2" type="search" placeholder="Search Destination" aria-label="Search">
        <button class="btn button" type="submit">Search</button>
    </form> 
        </div>
    </div>
</template>

<script>
export default {
    
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Permanent+Marker&display=swap');

.jumbotron {
    background-image: url(../assets/bali.jpg);
    background-size: cover;
    height: 682px;
    text-align: center;  
}
.jumbotron, .display-4 {
    font-size: 36px;
    font-family: 'Permanent Marker', cursive;
    color: white;
    line-height: 52px;
    text-shadow: 0px 4px 4px rgba(0, 0, 0, 0.75);
}
.display-4{
    margin-top: 100px;
}
.jumbotron .btn {
    color: white;
}
.btn {
    margin-top: 10px;
}


/* Desktop Version */
@media (min-width: 992px) {
.jumbotron {
    margin-top: -80px;
    height: 782px;
}
.display-4 {
    margin-top: 460px;
}
.btn {
    margin-top: 0;
}
}
</style>