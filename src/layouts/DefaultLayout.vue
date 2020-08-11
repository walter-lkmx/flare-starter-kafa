<template>
  <div class="default-layout">
    <simple-header>
      <template v-slot:logo>
        <g-image src="~/assets/images/kafa-logo.svg" alt="logo"></g-image>
      </template>
      <template v-slot:navigation>
        <simple-nav-item to="/services/maritime-fcl">Marítimo FCL</simple-nav-item>
        <simple-nav-item to="/services/maritime-lcl">Marítimo LCL</simple-nav-item>
        <simple-nav-item to="/services/terrestrial">Terrestre</simple-nav-item>
        <simple-nav-item to="/services/aerial">Aéreo</simple-nav-item>
        <simple-nav-item to="/services/ferro">Ferroviario</simple-nav-item>
        <simple-nav-item to="/Contact">Contacto</simple-nav-item>
      </template>
      <template v-slot:nav-toggle>
        <g-image src="~/assets/images/navigation-icon.svg" alt="logo"></g-image>
      </template>
      <template v-slot:actions>
      </template>
      <template v-slot:nav-toggle-close>
        <g-image src="~/assets/images/navigation-close-icon.svg" alt="cerrar navegación"></g-image>
      </template>
    </simple-header>
    <slot/>
    <simple-footer>
      <no-column class="container">
           <g-image src="~/assets/images/kafa-logo.svg" alt="logo"></g-image>
           <div class="link-block">
            <div class="link-item">
              <g-link to="/privacy">Aviso de Privacidad</g-link>
            </div>
            <div class="link-item">
              <g-link to="/terms">Términos y Condiciones</g-link>
            </div>
          </div>
           <span>Derechos Reservados ®2020</span>
      </no-column>
    </simple-footer>
  </div>
</template>


<style lang="scss" scoped>
.default-layout {
  header {
    .nav-item {
      font-weight: 900;
      text-transform: uppercase;
    }
  }
  .footer {
    .container {
        display: grid;
        grid-template-columns: 0.5fr 1fr 0.5fr;
        grid-template-rows: 100%;
        grid-gap: $gutter;
        text-align: left;
        .link-block {
          display: grid;
          grid-template-columns: 1fr 1fr;
          grid-gap: 0;
          align-self: center;
          a {
            display: block;
            color: white;
            text-decoration: none;
            margin-bottom: 0.5rem;
          }
          @include respond-to("small and down") {
            grid-template-columns: 100%;
            grid-template-rows: auto auto auto;
          }
        }
        @include respond-to("small and down") {
          text-align: center;
          grid-template-columns: 100%;
          grid-template-rows: 50px 1fr 50px;
          grid-row-gap: $gutter;
          img {
            margin: 0 auto;
          }
        }
      }
      h3 {
        color: white;
        margin-bottom: $gutter;
        font-weight: 700;
      }
      span {
        align-self: center;
      }
  }
}
</style>