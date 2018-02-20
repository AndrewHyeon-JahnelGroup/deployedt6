<template>
  <div class="col-md-6 card-deck">
  <div class="card profile">
    <h5 class="card-header">{{name}}</h5>
    <div class="card-body">
      <div class="card-text container">
        <div class="col-md-6">
          <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcREFGhaIPwHSHJBpk3l4ZfQDi5KogibX0_tuVAstc7-bMoiiJxB">
        </div>
        <div class="col-md-6">

          <p class="title">{{title}}</p>

          <p>{{about}}</p>
          <p>{{email}}</p>
        </div>
      </div>
    </div>
    <div class="card-footer">
      <email-modal />
    </div>
  </div>
  </div>

</template>

<script>
import EmailModal from './EmailModal'

export default {
  name: 'TeamProfile',
  components: {
    EmailModal
  },
  props: ['name', 'about', 'title', 'email'],
  methods: {
    sendEmail: async function sendEmail() {
      var data = this.$data.mgData
      try  {
        await this.axios.post('/send', data)
      } catch (e) {
        console.log(e, 'error')
      }
    }

  },
  data () {

    return {
    }
  }
}
</script>

<style>
/* Three columns side by side */
.container {
  display: flex;
}
.name {
  width: auto;
  position: absolute;
  height: inherit;
  color: #D5D5D5;
  padding-left: 10px
}
.namebar {
  background-color: #6D7993;
  width: 100%;
  height: inherit;
}
.card {
  margin: 10px;
  min-width: 100%;
}
.button {
    border: none;
    outline: 0;
    display: inline-block;
    padding: 8px;
    color: white;
    background-color: #000;
    text-align: center;
    cursor: pointer;
    width: 100%;
}

.button:hover {
    background-color: #555;
}

.card-footer {
  padding: 5px;
  padding-left: 20px;

}
</style>
