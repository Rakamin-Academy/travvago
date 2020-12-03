<template>
    <div class="container">
    <div>
      <b-navbar b-navbar type="light">
      <b-navbar-nav class="ml-auto">
          <b-nav-item href="/">Home /</b-nav-item>
          <b-nav-item href="#" disabled>Destination</b-nav-item>
          <b-nav-form>
            <b-form-input size="sm" class="mr-sm-2" placeholder="Search"></b-form-input>
            <b-button size="sm" class="search2 my-2 my-sm-0" type="submit">Search</b-button>
          </b-nav-form>

        </b-navbar-nav>
    </b-navbar>
    </div>
    </div>
</template>

<script>
  export default {
    
  }
</script>

<style scoped>
.container {
  position: absolute;
  margin-left: 500px;
  margin-top: 190px;
}
/* tablet version */
@media (min-width: 768px) {
  .container {
  margin-left: 270px;
  margin-top: 100px;
  }
}
</style>