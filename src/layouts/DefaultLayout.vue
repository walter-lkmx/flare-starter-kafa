<template>
  <div class="default-layout">
    <simple-header>
      <template v-slot:logo>
        <g-image src="~/assets/images/kafa-logo.svg" alt="logo"></g-image>
      </template>
      <template v-slot:navigation>
        <simple-nav-item to="/service/maritime-fcl">Marítimo</simple-nav-item>
        <simple-nav-item to="/">Terrestre</simple-nav-item>
        <simple-nav-item to="/">Aéreo</simple-nav-item>
        <simple-nav-item to="/">Ferro</simple-nav-item>
        <simple-nav-item to="/">Contacto</simple-nav-item>
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
      <triplet-column>
         <template v-slot:left>
           <g-image src="~/assets/images/kafa-logo.svg" alt="logo"></g-image>
         </template>
         <template v-slot:middle>
           <a to="/">Políticas de Privacidad</a>
           <a to="/">Términos y Condiciones</a>
         </template>
         <template v-slot:right>
           <span>Derechos Reservados ®2020</span>
         </template>
      </triplet-column>
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
  footer {
    .triplets {
      &-section {
        &--end {
          .triplets {
            &-column {
              &--end {
                justify-self: center;
                span {
                  text-align: right;
                }
              }
            }
          }
        }
      }
    }
    a {
      padding-right: rem(16px);
      @include respond-to("small and down") {
        display: block;
      }
    }
  }
}
</style>