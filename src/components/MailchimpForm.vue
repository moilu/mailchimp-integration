<template>
  <div class="hello">
    <form @submit.prevent="signUp()" class="submit-form">
        <input type="text" placeholder="Nombre">
        <input type="text" placeholder="Apellido">
        <input type="email" placeholder="Email">
        <button>Enviar</button>
    </form>
  </div>
</template>

<script>
export default {
  name: 'MailchimpForm',
  data() {
    return {
      LIST_ID: 'aaba1bd42e',
      DC: 'us18',
      name: '',
      last_name: '',
      email: ''
    }
  },
  methods: {
    signUp() {
      const API_URL = `https://${this.DC}.api.mailchimp.com/3.0/lists/${this.LIST_ID}`;

      fetch(API_URL, {
        method: 'POST',
        body: JSON.stringify({
          LNAME: '',
          FNAME: ''
        }),
        headers: {
          "Authorization": "auth 2f241f20c50ce0971eafa3017f043e45-us18"
        }
      });
      console.log(`este es tu url ${API_URL}`);
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
.submit-form {
  display: grid;
  gap: 1rem;
  margin: 0 auto;
  max-width: 300px;
}

.submit-form > button {
  background-color: rgb(139, 221, 219);
  color: black;
  font-weight: bolder;
}
</style>
