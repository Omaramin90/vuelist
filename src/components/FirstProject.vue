<template>
  <div class="list">

    <h1>TO DO LIST IN VUE.JS</h1>
    <br>
    <br>
     Simply Add your task in the text box below, and click on each item to remove!<br>

<input type="text" v-model="task"> <input type="button" class="btn btn-dark" value="Add Task!" @click="addTask()">

    <br>

    <ul>
      <li v-for="(t,index) in tasks" :key="index"> {{t}}

        <button id="remove" @click="removeTask(index)">Completed</button>

      </li>

    </ul>

  </div>
</template>

<script>
export default {
name: 'FirstProject',

  data(){

      return {
        tasks : [],

        task: ''

      }
  },

  methods:{

    addTask(){
      this.tasks.push(this.task)
      this.task = ""

    },

    removeTask(index)
    {
      this.tasks.splice(index, 1)
    }
  }
}
</script>

<style>
h1{
  font-family: oswald;
  font-weight: bolder;
  text-decoration: underline;
}
.list{
  color:whitesmoke;
  font-family: oswald;
  font-size: larger;
}
body, html{
  padding:0;
  margin:0;
  width:100%;
  min-height:100vh;
}
body{
  background-color:black;
}
.remove{
  size: letter;
}
</style>