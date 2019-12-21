<template>
  <div class="row justify-content-center pt-4">
    <div class="orange-back"></div>
    <div class="col-12">
      <h1 class="page-title text-center text-white">Let's get started NOW!</h1>
    </div>

    <div class="col-lg-6 col-md-8 login-block bg-white px-4 pb-4">
      <div class="cs-logo"></div>
      <div class="row justify-content-center">
        <div class="col-md-8">
          <div class="row">
            <div class="col-12 text-center">
              <button>
                <img src="~/assets/login/google-sign-in.png" alt="" class="google-sign-in-img">
              </button>
              <div class="separator my-5">or</div>
            </div>
          </div>

          <form action="/">
            <div class="form-group">
              <input type="text" class="form-control" placeholder="Username" autocomplete="off" />
            </div>

            <div class="form-group">
              <input type="password" class="form-control" placeholder="Password" autocomplete="off" />
            </div>

            <div class="custom-control custom-checkbox">
              <input type="checkbox" class="custom-control-input" id="remember" />
              <label for="remember" class="custom-control-label">Remember username</label>
            </div>

            <div class="form-group d-flex justify-content-center pt-5">
              <button class="btn btn-warning text-white mx-auto sign-in-button" type="submit">Sign in</button>
            </div>

            <div class="form-group text-center">
              <a href="/" class="text-danger">Forget Password ?</a>
            </div>
          </form>
        </div>
      </div>
    </div>
  </div>
</template>

<style>
.v-application {
  background-image: url("~assets/login/login_background.png") !important;
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat !important;
}
</style>

<style scoped>
.login-block {
  border-radius: 20px;
  position: relative;
  padding-top: calc(75px + 10px);
  margin-top: 75px;
  box-shadow: 2px 2px 2px rgba(0, 0, 0, 0.5);
}

.cs-logo {
  width: 150px;
  height: 150px;
  background-image: url("~assets/login/cs_logo.png");
  background-size: cover;
  background-repeat: no-repeat;
  border-radius: 100%;
  position: absolute;
  left: 50%;
  top: -75px;
  transform: translateX(-50%);
}

.orange-back {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-image: linear-gradient(
    269.56deg,
    #de5a10 0.21%,
    rgba(222, 90, 16, 0.8) 0.22%,
    rgba(247, 171, 27, 0.7) 86.76%
  );
}

.separator{
  display: flex;
  align-items: center;
  color: rgba(142, 142, 142, 0.8);
}
.separator::before, .separator::after{
  content: '';
  flex-grow: 1;
  border-bottom: 1px solid rgba(142, 142, 142, 0.8);
}
.separator::before{
  margin-right: 30px;
}
.separator::after{
  margin-left: 30px;
}

.sign-in-button{
  background-color: #F8941E;
}

.google-sign-in-img{
  width: 100%;
  height: auto;
}
</style>
