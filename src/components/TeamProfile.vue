<template>
  <div class="card col-md-6">
    <div class="container">
      <div class="col-md-5">
        <p>image goes here</p>
      </div>
      <div class="col-md-7">
        <h2>{{name}}</h2>
        <p class="title">{{title}}</p>

        <p>{{about}}</p>
        <p>{{email}}</p>
        <p><button class="button">Contact</button></p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'TeamProfile',
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
  display: flex
}
.card {
  padding: 20px;
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
</style>
