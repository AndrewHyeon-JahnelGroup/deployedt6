<template>
  <div class="frontpage">
    <div class="row">
      <div class="col-md-6 content">
        <br />
        <h3>Who we are</h3>
        <br />
        <div class="mission1">
          <p>{{ content }}</p>
        </div>
      </div>
      <div class="col-md-6" >
      </div>
    </div>
    <br />
    <br />
    <br />
    <br />
    <div class="row">

      <div class="col-md-6" >
      </div>
      <div class="col-md-6" >
        <br />
        <h3>Company Mission</h3>
        <br />
        <div class="mission">
          <p>{{content2}}</p>
        </div>
      </div>

    </div>
    <br />
    <br />
    <br />
    <br />
    <div class="row">

      <div class="col-md-6" >
        <br />
        <h3>Design. Create. Build. </h3>
        <br />
        <div class="mission">
          <p>{{content2}}</p>
        </div>
      </div>
      <div class="col-md-6" >
      </div>

    </div>

    <div class = "loadercontainer">
      <div class="loader">
        <div id="largeBox"></div>
        <div id="smallBox"></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'AboutPage',
  data () {
    return {
      msg: 'About',
      content: 'Team Six is a small group of highly capable and experienced engineers who engage in world-class Product Development. We are skilled at doing basic research and concept development. By nature, we are systems engineers; and our skill set is in the realm of mechanical, thermodynamic, fluid systems, controls, electrical, user interface, computer, and software design. We also have a great deal of experience with industrial design. Our client list is strictly confidential and will remain so for the foreseeable future.',
      content2: 'orem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry\'s standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desk'
    }
  }
}
</script>

<style>
.mission {
  text-align: left
}
.frontpage {
  text-align: center;
  margin-top: 25px;
  margin-bottom: 25px;
}
.abt {
  text-align: center
}

.content{

  text-align: center
}
#about {
  width: 80%;
  text-align: center;
}

.mission1 {
}

</style>
