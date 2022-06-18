<template>
  <div id="app">
    <HelloWorld msg="Mailchimp Signup"/>
    <MailchimpForm />
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import MailchimpForm from './components/MailchimpForm.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    MailchimpForm
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
