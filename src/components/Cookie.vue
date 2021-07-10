<template>
  <div class="col-md-12">
    <div class="mb-3">
      <label class="form-label">User Name :</label>
      <input v-model="cookie" type="text" class="form-control" id="exampleFormControlInput1" placeholder="Please enter your username">
      <br>
      <div class="btn-group d-flex">
        <button @click="setCookie" class="btn btn-outline-success d-flex">Send to Cookie</button>
        <button @click="getCookie" class="btn btn-outline-warning d-flex">Get from Cookie</button>
        <button @click="deleteCookie" class="btn btn-outline-danger d-flex">Delete</button>
      </div>
    </div>
    <p><strong>Cookie Value: </strong></p>
    <div class="border p-1 mb-3 border-secondary d-flex justify-content-center align-items-center">
      <p>{{incomingCookie}}</p>
    </div>
  </div>
</template>

<script>
import Cookies from "js-cookie"
export default {
name: "Cookie",
  data(){
    return{
      cookie : " ",
      incomingCookie : " "
    }
  },
  methods : {
    setCookie(){
      Cookies.set("value", this.cookie, { expires: 7 })
    },
    getCookie(){
      this.incomingCookie = Cookies.get("value")
    },
    deleteCookie(){
      Cookies.remove("value")
      this.cookie = ""
      this.incomingCookie = ""
    }
  }
}
</script>

<style scoped>


</style>
