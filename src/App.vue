<template>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <div class="main_container">
    <img alt="IVClogo" class="logo" src="./assets/ivc-logo2.png"/>

    <div class="wrapper">
      <h1>Datos de transferencia</h1>
      <ul>
          <li>Iglesia Viña Cordillera</li>
          <li>65.135.458-7</li>
          <li>Banco Santander</li>
          <li>Cuenta Corriente</li>
          <li>0-000-7224453-2</li>
          <li>lavinacordillera@gmail.com</li>
      </ul>
      <button @click="copy">Copiar datos de transferencia</button>
      <p id="success-message" hidden="hidden">¡Datos copiados!</p>
    </div>
  </div>
    
</template>

<script>

export default {
  data() {
    return {
      account_data: "Iglesia Viña Cordillera\n65.135.458-7\nBanco Santander\nCuenta Corriente\n0-000-7224453-2\nlavinacordillera@gmail.com"
    };
  },
  methods: {
    copy() {
      navigator.clipboard.writeText(this.account_data)
      document.getElementById("success-message").hidden = null
    }
  }
}

</script>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: block;
    place-items: center;
    flex-wrap: wrap;
  }
}
</style>
