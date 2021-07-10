<template>
  <div class="col-md-12">
    <div class="mb-3">
      <label class="form-label">User Name :</label>
      <input v-model="localValue" type="text" class="form-control" id="exampleFormControlInput1" placeholder="Please enter your username">
      <br>
      <div class="btn-group d-flex">
        <button @click="setValue" class="btn btn-outline-success d-flex">Send to LocalStorage</button>
        <button @click="getValue" class="btn btn-outline-warning d-flex">Get from LocalStorage</button>
        <button @click="deleteValue" class="btn btn-outline-danger d-flex">Delete</button>
      </div>
    </div>
    <p><strong>Local Storage Value: </strong></p>
    <div class="border p-1 mb-3 border-secondary d-flex justify-content-center align-items-center">
      <p>{{incomingValue}}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data(){
    return{
      localValue : " ",
      incomingValue : ""
    }
  },
  methods : {
    setValue(){
      localStorage.setItem("value", this.localValue)
    },
    getValue(){
      this.incomingValue = localStorage.getItem("value")
    },
    deleteValue(){
      localStorage.removeItem("value")
      this.localValue = ""
      this.incomingValue = ""
    }
  }
}
</script>


<style scoped>
label {
  float: left;
  font-weight: bold;
}
p{
  text-align: left;
}

</style>
