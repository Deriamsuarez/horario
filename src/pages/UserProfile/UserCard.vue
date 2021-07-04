<template>
  <card class="card-user">
    <div slot="image">
      <img src="@/assets/img/pc2.jpg" alt="...">
    </div>
    <div>
      <div class="author">
        <img class="avatar border-white" src="@/assets/img/faces/deriam.jpg" alt="...">
        <h4 class="title">Deriam Suárez
          <br>
          <a href="#">
            <small>@deriamsuarez</small>
          </a>
        </h4>
      </div>
      <p class="description text-center">
        <em>"Los mejores programadores están construidos 
         sobre las bases <br>Pruebas-Error"</em>
      </p>
    </div>
    <hr>
    <div class="text-center">
      <div class="row">
        <div v-for="(info, index) in details" :key="index" :class="getClasses(index)">
          <h5>{{info.title}}
            <br>
            <small>{{info.subTitle}}</small>
          </h5>
        </div>
      </div>
    </div>
  </card>
</template>
<script>
export default {
  data() {
    return {
      details: [
        {
          title: "13",
          subTitle: "Proyectos completados"
        },
          {
            title: "13.2$",
            subTitle: "p/hora"
          },
        {
          title: "FrontEnd Developer",
          subTitle: "Especialidad"
        },
      ]
    };
  },
  methods: {
    getClasses(index) {
      var remainder = index % 3;
      if (remainder === 0) {
        return "col-lg-3 offset-lg-1";
      } else if (remainder === 2) {
        return "col-lg-4";
      } else {
        return "col-lg-3";
      }
    }
  }
};
</script>
<style>
</style>
