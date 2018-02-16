<template>
  <div class="col contact">
    <h4>{{content}}</h4>
    <div>
      <email-form class="text-center" v-bind:mgData="mgData"/>
      <md-button id="submit" class="md-primary" @click="showDialog = false; sendEmail()">Send</md-button>
    </md-dialog-actions>
    </div>
  </div>
</template>

<script>
import EmailForm from './EmailForm'

export default {
  name: 'ContactPage',
  components: {
    EmailForm
  },
  data () {
    return {
      msg: 'Contact Us',
      content: 'Please fill out a quick form to get in contact with us',
      mgData: {
        name: '',
        from: '',
        number:'',
        subject: '',
        text: ''
      }
    }
  },
  methods: {
    sendEmail: async function sendEmail() {
      console.log(this.$data.mgData, 'workshere')
      var submit = document.getElementById('submit');
      var data = this.$data.mgData
      try  {
        await this.axios.post('/send', data)
      } catch (e) {
        console.log(e, 'error')
      }
    }


  }
}
</script>

<style scoped>
.contact {
  margin: 25px;
}
</style>
