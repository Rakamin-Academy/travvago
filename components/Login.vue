<template>
  <div>
    <div class="tab col-md-4 offset-md-4">
    <b-tabs 
    content-class="mt-4" 
    align="center"
    active-nav-item-class="font-weight-bold text-secondary">
      <b-tab title="Log in" active>
          <!-- form login start -->
      <div class="form-container  ml-auto mr-auto">
        <b-form @submit="onSubmit" v-if="show">
          <h6>Enter your email for<span> Login</span></h6>
          <b-form-group
            id="input-group-1"
            label="Email address:"
            label-for="input-1"
          >
            <b-form-input
              id="input-1"
              v-model="form.email"
              type="email"
              required
              placeholder="Your email"
            ></b-form-input>
          </b-form-group>

          <b-form-group id="input-group-2" label="Password:" label-for="input-2">
            <b-form-input
              id="input-2"
              v-model="form.password"
              required
              placeholder="Password"
            ></b-form-input>
          </b-form-group>

          <b-btn-group inline >
          <nuxt-link to=""
          class="link"> Forgot Password?
          </nuxt-link>
          <b-button type="login" class="button">Login</b-button>
          </b-btn-group>
          <br>
          <nuxt-link to="/">
          <b-button class="button-home col-lg-12  mt-3 ml-auto mr-auto" type="home">Back to Home</b-button>
          </nuxt-link>
        </b-form>
      </div>
      </b-tab>
      <!-- form login end -->

      <!-- form sign up start -->
      <b-tab title="Sign up">
        <div>
    <b-form @submit="onSubmit" v-if="show">
      <h6>Enter your data for<span> Sign up</span></h6>
        <b-form-group
          id="input-group-1"
          label="Email address:"
          label-for="input-1"
        >
          <b-form-input
            id="input-1"
            v-model="form.email"
            type="email"
            required
            placeholder="Email"
          ></b-form-input>
        </b-form-group>

        <b-form-group id="input-group-2" label="Password:" label-for="input-2">
          <b-form-input
            id="input-2"
            v-model="form.password"
            required
            placeholder="Password"
          ></b-form-input>
        </b-form-group>

        <b-form-group id="input-group-2" label="Confirm:" label-for="input-2">
          <b-form-input
            id="input-2"
            v-model="form.password"
            required
            placeholder="Enter password"
          ></b-form-input>
        </b-form-group>

        <b-button class="button-signup" type="submit" >Sign up</b-button>
        <nuxt-link to="/home">
        <b-button class="button-home col-lg-12  mt-3 ml-auto mr-auto" type="home">Back to Home</b-button>
        </nuxt-link>
        </b-form>
      </div>
      </b-tab>
    </b-tabs>
  </div>
  </div>
</template>

<script>
export default {
      data() {
      return {
        form: {
          email: '',
          name: '',
        },
        show: true
      }
    },
    methods: {
      onSubmit(evt) {
        evt.preventDefault()
        alert(JSON.stringify(this.form))
      },
    }
}
</script>

<style scoped>
.tab{
  margin-top: 200px;
  /* border: 1px solid #A2A2A2; */
  filter: drop-shadow(0px 4px 4px rgba(0, 0, 0, 0.41));
  padding: 30px;
}
h6 {
  text-align: center;
  color: grey;
}
span {
  font-weight: 700;
}
.button {
  background: linear-gradient(255.51deg, #FEA858 30.34%, #ED765C 63.07%);
  width: 150px;
}
.link {
  color: grey;
  margin-right: 120px;
}
#input-group-1, #input-group-2{
  color: grey;
}
.button-home {
  background: linear-gradient(255.51deg, #FEA858 30.34%, #ED765C 63.07%);
}
.button-signup {
  background: linear-gradient(255.51deg, #FEA858 30.34%, #ED765C 63.07%);
  width: 150px;
  margin-left: 125px;
}
.title {
  color: #F85E1D;
}

@media (min-width: 992px) {
.link {
  margin-right: 200px;
}
.button-signup {
  margin-left: 320px;
}
}
</style>>

