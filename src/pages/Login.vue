<template>
  <q-page class="flex flex-center bg-primary">
    <q-card
      style="width: 300px; height: auto; display: flex; flex-direction: column; align-items: center"
    >
      <q-img src="../assets/logo.png" ratio="1" width="200px" />

      <q-card-section class="q-pt-none full-width">
        <q-input filled v-model="login.email" label="Email" />
        <q-input class="q-mt-sm" v-model="login.password" filled label="Password" :type="login.isPwd ? 'password' : 'text'">
        <template v-slot:append>
          <q-icon
            :name="login.isPwd ? 'visibility_off' : 'visibility'"
            class="cursor-pointer"
            @click="login.isPwd = !login.isPwd"
          />
        </template>
      </q-input>
      </q-card-section>

      <q-card-actions class="full-width">
        <q-btn class="q-mx-sm" color="primary" label="Login" @click="$router.push({ name: 'home' })" style="width: 100%"/>
      </q-card-actions>
      <q-card-actions class="full-width">
        <q-btn flat no-caps class="q-mx-sm" color="primary" label="Esqueci minha senha" @click="$router.push({ name: 'esqueciSenha' })" style="width: 100%"/>
      </q-card-actions>
    </q-card>

    <q-card class="my-card">
      <q-img src="https://cdn.quasar.dev/img/parallax2.jpg" basic>
        <div class="absolute-bottom text-subtitle2 text-center">
          Title
        </div>
      </q-img>
    </q-card>
  </q-page>
</template>

<script>
export default {
  name: 'PageIndex',
  data () {
    return {
      login: {
        email: '',
        password: '',
        isPwd: true
      }
    }
  },
  methods: {
  }
}
</script>
