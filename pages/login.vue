<script>
export default {
    data(){
        return{
            firstName:"",
            LastName:"",
            hide:false
        }
    },
    methods:{
        submit(){
             const fname="sucheta"
              const lname="saha"
              if(this.firstName==fname && this.LastName==lname){
                 this.$router.push('/')
              }
        },
        hideLogin(){
            this.hide=!this.hide
        }
    }
}
</script>
<template>
    <div>
        <b-container>

        <b-button @click=" hideLogin">Hide-login</b-button>
        <div class="card" v-if="!hide">
            <div class="card-body">
                                <div class="login-box">
  <h2>Login</h2>
                <b-form>
                    <b-form-group>
                           <div class="user-box">
                        <label>First Name</label>
                        <b-form-input v-model="firstName"></b-form-input>
                           </div>
                    </b-form-group>
                      <b-form-group>
                            <div class="user-box">
                        <label >Last Name</label>
                        <b-form-input v-model="LastName"></b-form-input>
                            </div>
                    </b-form-group>
                    <div class="vertical-center">
                    <b-button class="submit" @click="submit">Submit</b-button>
                    </div>
               <!-- <nuxt-link to="/">abbbbbb</nuxt-link>-->
                </b-form>
            </div>
        </div>
    </div>
        </b-container>
    </div>
</template>
<style scoped>
body {
  margin:0;
  padding:0;
  font-family: sans-serif;
  background: linear-gradient(#141e30, #243b55) !important;
}
.card {
    position: relative;
    display: flex;
    flex-direction: column;
    min-width: 0;
    word-wrap: break-word;
    background: #141e30 !important;
    background-clip: border-box;
    border: 1px solid rgba(0, 0, 0, 0.125);
    border-radius: 0.25rem;
        position: absolute;
  top: 50%;
  left: 50%;
  width: 400px;
  padding: 40px;
  transform: translate(-50%, -50%);
    box-shadow: 0 10px 20px rgba(0,0,0,0.19), 0 6px 6px rgba(0,0,0,0.23);
}
.login-box h2 {
  margin: 0 0 30px;
  padding: 0;
  color: #fff;
  text-align: center;
}

.login-box .user-box {
  position: relative;
}

.login-box .user-box input {
  width: 100%;
  padding: 10px 0;
  font-size: 16px;
  color: #fff;
  margin-bottom: 30px;
  border: none;
  border-bottom: 1px solid #fff;
  outline: none;
  background: transparent;
}
label {
    display: inline-block;
    margin-bottom: 0.5rem;
    color: white;
}
.vertical-center {
  margin: 0;
  position: absolute;
  top: 75%;
  left:38%;
}
.submit{
     position: relative;
  display: inline-block;
  background-color:#03e9f4 ;
  padding: 8px 20px;
  color: #141e30;
  font-size: 15px;
  text-decoration: none;
  overflow: hidden;
  transition: .5s;
  margin-top: 30px;
  border: none;
  letter-spacing: 2px;
}
</style>