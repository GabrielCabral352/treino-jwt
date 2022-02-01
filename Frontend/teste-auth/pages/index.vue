<template>
  <div class="body">
    <div class="login-form-view">
      <form @submit.prevent="submitForm" class="login-form" method="POST">
        <div class="form-header">
          <h1 class="form-title">
            Login
          </h1>
        </div>
        <div class="form-body">
          <div class="input-combo">
            <input name="user" type="text" class="input user-input" placeholder="User">
            <!-- <p>User</p> -->
          </div>
          <div class="input-combo">
            <input name="password" type="password" class="input password-input" placeholder="Password">
            <!-- <p>Senha</p> -->
          </div>
        </div>
        <div class="form-footer">
          <input type="submit" class="form-btn-send" value="Logar" >
        </div>
      </form>
    </div>
  </div>
</template>

<script>
export default {
  data: function() {
    return {
      
    }
  },
  methods:{
    submitForm: (evt)=>{
      evt.preventDefault();

      if(evt.target.method === "post"){
        alert(1)
      }
      //user = evt.srcElement[0].value;
     //pass = evt.srcElement[1].value;
    },
  }
}
</script>

<style scoped>
  @import url('https://fonts.googleapis.com/css2?family=Supermercado+One&display=swap');
  @import url('https://fonts.googleapis.com/css2?family=Lato&display=swap');
  *{
    padding:0;
    margin:0;
    vertical-align:baseline;
    list-style:none;
    border:0;
    
    /* font-family: 'Supermercado One', cursive; */
    font-family: 'Lato', sans-serif;
  }

  .body{
    width: 100%;
    height: 98vh;
    
    background-color: none;
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
  }
  .login-form-view{
    width: 300px;
    height: auto;
    background-color: none;
  }
  .input{
    width: 17rem;
    height: 2.4rem;
    
    border: 0.08rem solid rgba(5, 42, 78, 0.2);
    padding-left: 0.8rem;
  }
  .input:focus{
   border: 0.08rem solid #0f81f0;
   outline: 0;
  }
  .input-combo{
    margin-bottom: 1.5rem;
  }
  .input:focus +p{
   display: none;
  }
  .input-combo > p{
    color: rgba(5, 42, 78, 0.5);
    font-size: 1.1rem;
    pointer-events: none;
    margin: -2rem 0 0 .8rem;
    
  }
  .form-title{
    background-color: none;
    margin: 0 0 1.5rem 0;
  }
  .form-footer{
    display: flex;
    justify-content: flex-end;
    margin: 0 .8rem 0 0;
  }
  .form-btn-send{
    width: 6rem;
    height: 2rem;
    color: white;
    background-color: royalblue;
  }
</style>
