<template>
  <div class="login-form"> 
    <h1>Please Login</h1>
    <form>
      <!-- Inputs for email and password-->
      <input type="email" placeholder="Name" v-model="email">
      <input type="password" placeholder="Password" v-model="password">
      
      <!-- error message which appears after pressing button -->
      <p class="error">{{ errorMessage }}</p>
      
      <!-- button --> 
      <div class="button" v-on:click="pushLink()">Login</div>
    </form>
  </div>
</template>

<script>
export default {
  name: 'Login Form',
  components: {},
  data: function () {
    return {
      email: '',
      password: '',
      errorMessage: '',
    }
  },
  methods: {
    pushLink: function () {
      // TODO: make sure to add additional logic for email input
      // now it allows all kinds of text

      // What kind of error message should we show the customer?
      // code determines what input is missing
      if(this.email != '' && this.password != '') this.$router.push('dashboard')
      else if (this.email != '') this.errorMessage = 'Please enter password'
      else if (this.password != '') this.errorMessage = 'Please enter email'
      else this.errorMessage = 'Please enter email and password'
    }
  }
}
</script>

<style scoped>
/* Container for the whole page */
.login-form {
  height: 100vh;
  width: 100vw;
  background-color: #4d5475;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

/* Header above the inputs */
h1 {
  color: white;
  -webkit-animation: pulsate 3s ease-out;
  -webkit-animation-iteration-count: infinite; 
}

/* Form */
form {

}
form input {
  display: block;
  position: relative;
  margin: 4em 0em;
  padding: 2em 4em;
  border-radius: 20px;
  border: none;
}
/* email input */
form input:first-child {
  left: 2em;
  transform: rotate(5deg);
}
/* password input */
form input:nth-child(2) {
  transform: rotate(-5deg);
}
/* error message between button and inputs */
form .error {
  color: #fc3d03;
  font-weight: bold;
}
/* button */
form .button {
  position: relative;
  background-color: #53c940;
  font-weight: bold;
  color: white;
  margin-top: 2rem;
  padding: 1em 1em;
  max-width: 50%;
  left: 50%;
  transform: translateX(-50%) rotate(10deg);
  border-radius: 20px;
  border: none;
  transition: 0.5s;
}
form .button:hover {
  cursor: pointer;
  background-color: lightgreen; 
  color: #4d5475;
  transform: translateX(-50%) rotate(5deg);
}

/* animation we use for the header text*/
@-webkit-keyframes pulsate {
    0% { 
        opacity: 0.5;
    }
    50% { 
        opacity: 1.0;
    }
    100% { 
        opacity: 0.5;
    }
}
</style>
