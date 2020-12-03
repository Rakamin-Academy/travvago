<template>
    <div>
    <b-jumbotron class="jumbotron">
        <div class="container">
        <p class="animate__animated animate__jackInTheBox" id="display-4">Temukan hal-hal menakjubkan <br/> untuk dilakukan Kapan saja, dimana saja.</p>
        <!-- <b-nav-form class="search">
        <b-form-input size="lg" class="form-input mr-sm-2 " placeholder="Search Destination"></b-form-input>
        <b-button size="lg" class="button my-2 my-sm-0" type="submit">Search</b-button>
        </b-nav-form> -->
        </div>
    </b-jumbotron>
    </div>
</template>

<script>
export default {
    
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Permanent+Marker&display=swap');

.jumbotron {
    background-image: url(../assets/bali.jpg);
    background-size: cover;
    height: 682px;
    text-align: center;
    position: relative;
}
.jumbotron .container {
    z-index: 1;
    position: relative;
}
.jumbotron::after {
    content: '';
    display: block;
    width: 100%;
    height: 100%;
    background: linear-gradient(180deg, rgba(29, 116, 248, 0.5) 0%, rgba(0, 0, 0, 0.125) 100%);
    position: absolute;
    bottom: 0;
    left: 0;
}
.jumbotron, #display-4 {
    font-size: 36px;
    font-family: 'Permanent Marker', cursive;
    color: white;
    line-height: 52px;
    text-shadow: 0px 4px 4px rgba(0, 0, 0, 0.75);
}
#display-4{
    margin-top: 300px;
    text-shadow: 0px 4px 4px #F85E1D;
}
.jumbotron .btn {
    color: white;
}
.btn {
    margin-top: 10px;
}
.button:active {
    position: relative;
    top: 7px;
    box-shadow: none;
}
.search {
    margin-left: 10px;
}
.search .button {
    background: linear-gradient(180deg, #FEA858 0%, #F85E1D 100%);
    box-shadow: inset 0px 4px 4px rgba(0, 0, 0, 0.25);
}

/* tablet version */
@media (min-width: 768px) {
.search {
    margin-left: 110px;
}
}

/* Desktop Version */
@media (min-width: 992px) {
.jumbotron {
    margin-top: -100px;
    height: 782px;
}
#display-4 {
    margin-top: 360px;
}
.btn {
    margin-top: 0;
}
.search {
    margin-left: 325px;
}
}
</style>