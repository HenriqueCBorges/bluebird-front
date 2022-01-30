<template>
    <div class="main-login">
      <div class="card-login" >
        <div class="box-logo">
          <img src="../../assets/logo-bb.png" alt="" />
        </div>

        <form @submit.prevent="submit" ref="form" lazy-validation>
          <v-text-field
            label="E-mail"
            placeholder="Digite seu e-mail"
            outlined
          ></v-text-field>

          <v-text-field
            label="Senha"
            placeholder="Digite sua senha"
            outlined
          ></v-text-field>

          <v-btn block x-large color="primary" @click="logar">ENTRAR</v-btn>
        </form>
      </div>
    </div>
</template>

<script>
export default {
  methods: {
    logar(){
      this.$router.push({ name: 'Dashboard' })
    }
  }
};
</script>

<style scoped>
.main-login {
  height: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  background: url("../../assets/background-bubbles.png") no-repeat center center fixed;
  -webkit-background-size: cover;
  -moz-background-size: cover;
  -o-background-size: cover;
  background-size: cover;
}

.bubbles-left {
  position: absolute;
  left: 0;
  bottom: 0;
  height: 240px;
}

.bubbles-right {
  position: absolute;
  right: 0;
  top: 0;
  height: 240px;
}

.card-login {
  position: relative;
  min-height: 470px;
  width: 400px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding: 25px;
  background: #ffffff;
  border-radius: 10px;
  box-shadow: rgba(149, 157, 165, 0.2) 0px 8px 24px;
}

.box-logo {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  margin-bottom: 25px;
}
</style>
