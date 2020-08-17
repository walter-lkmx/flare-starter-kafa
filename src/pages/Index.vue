<template>
  <default-layout>
    <base-page>
      <!-- SimpleHero -->
      <section class="intro">
        <simple-hero>
          <h1 class="title">Tu enlace global<br>con operación local</h1>
          <p class="description">Ofrecemos la red de servicios más robusta y flexible.</p>
          <a href="#services" class="our-services">Nuestros servicios</a>
        </simple-hero>
      </section>

      <!-- TripletColumns / Stats -->
      <section class="stats">
          <triplet-column>
            <template v-slot:left>
                <span class="first__number">10K</span>
                <span class="first__text">Envíos</span>
            </template>
            <template v-slot:middle>
                <span class="second__number">100K</span>
                <span class="second__text">Toneladas</span>
                <span class="second__text">enviadas</span>
            </template>
            <template v-slot:right>
                <span class="third__text">Todo tipo de carga</span>
                <div class="third__grid">
                  <span>Seca</span>
                  <span>Peligrosa</span>
                  <span>Refrigerada</span>
                  <span>Valiosa</span>
                </div>
            </template>
          </triplet-column>
      </section>

      <!-- TripletColumns / Service Row 1 -->
      <section class="service-row-1" id="services">
          <triplet-column>
            <template v-slot:left>
                <h2 class="service__name">Marítimo FCL</h2>
                <p class="service__description">Mayor rentabilidad por volumen, seguridad y flexibilidad en la entrega de tu mercancía de importación y exportación.</p>
                <g-link to="/services/maritime-fcl" class="service__button">Leer Más</g-link>
            </template>
            <template v-slot:middle>
            </template>
            <template v-slot:right>
                <h2 class="service__name">Marítimo LCL</h2>
                <p class="service__description">Ideal para emprendedores y empresas que requieren el servicio marítimo sin la necesidad de enviar un contenedor completo.</p>
                <g-link to="/services/maritime-lcl" class="service__button">Leer Más</g-link>
            </template>
          </triplet-column>
      </section>

      <!-- TripletColumns / Service Row 2 -->
      <section class="service-row-2">
          <triplet-column>
            <template v-slot:left>
            </template>
            <template v-slot:middle>
                <h2 class="service__name">Terrestre</h2>
                <p class="service__description">Total flexibilidad en rutas, equipo y tiempo de carga y descarga.</p>
                <g-link to="/services/terrestrial" class="service__button">Leer Más</g-link>
            </template>
            <template v-slot:right>
            </template>
          </triplet-column>
      </section>

      <!-- TripletColumns / Service Row 3 -->
      <section class="service-row-3">
          <triplet-column>
            <template v-slot:left>
                <h2 class="service__name">Ferroviario</h2>
                <p class="service__description">Para envío de grandes volúmenes de cualquier tipo de mercancía a México y Estados Unidos.</p>
                <g-link to="/services/ferro" class="service__button">Leer Más</g-link>
            </template>
            <template v-slot:middle>
            </template>
            <template v-slot:right>
                <h2 class="service__name">Aéreo</h2>
                <p class="service__description">El mejor tiempo de entrega en envíos de carga seca y refrigerada a México y el mundo.</p>
                <g-link to="/services/aerial" class="service__button">Leer Más</g-link>
            </template>
          </triplet-column>
      </section>
      
      <!--TextBanner / Contact Us-->
      <section class="contact-us">
        <text-banner>
          <h1>CONTAMOS SOLUCIONES PARA EL MANEJO DE TU CARGA <span>EN REPOSO Y EN MOVIMIENTO</span></h1>
          <g-link to="/Contact" class="contact-btn">Contáctanos</g-link>
        </text-banner>
      </section>

      <!-- TwinColumns / Warehousing -->
      <section class="warehousing">
        <twin-columns>
          <template v-slot:left>
            <h2 class="service__name">Almacenes</h2>
            <p class="service__description">Mayor rentabilidad por volumen, seguridad y flexibilidad en la entrega de tu mercancía de importación y exportación. </p>
            <g-link to="/services/warehouse" class="service__button">Leer Más</g-link>
          </template>
          <template v-slot:right>
          </template>
        </twin-columns>
      </section>

      <!-- TwinColumns / Patio -->
      <section class="patio">
        <twin-columns>
          <template v-slot:left>
          </template>
          <template v-slot:right>
            <h1 class="service__name">Patio</h1>
            <p class="service__description">Mayor rentabilidad por volumen, seguridad y flexibilidad en la entrega de tu mercancía de importación y exportación.</p>
            <g-link to="/services/patio" class="service__button">Leer Más</g-link>
          </template>
        </twin-columns>
      </section>
    </base-page>
  </default-layout>
</template>


<script>
export default {
  metaInfo: {
    title: 'Flare Starter'
  }
}
</script>

<style lang="scss">
body {
  .intro {
    .simple-hero {
      background-image: url('../assets/images/hero-image.jpg');
      background-size: cover;
      &__content {
        color: white;
        padding-top: rem(195px);
        span {
          text-transform: uppercase;
          letter-spacing: 2.4px;
        }
        .title {
          color: white;
          font-size: 60px;
          font-weight: 900;
          text-transform: uppercase;
          text-shadow: 0px 2px 4px rgba(0, 0, 0, 0.51);
          @include respond-to('small and down') {
              font-size: rem(28px);
          }
          @include respond-to('medium') {
              font-size: rem(34px);
          }
        }
        .our-services {
          @include button($brand-yellow, black);
          width: rem(250px);
          text-transform: uppercase;
          text-align: center;
          text-decoration: none;
          font-weight: 900;
        }
        &>* {
          position: unset;
        }
        @include respond-to("small and down") {
          padding-top: rem(89px);
        }
        @include respond-to("medium") {
          padding-top: rem(89px);
        }
      }
    }
  }
  .stats {
    background-color: $brand-blue-6;
    .triplets {
      padding: rem(28px) 0;
      &-section {
        &--start, &--middle, &--end {
          .triplets {
            &-column {
              align-self: center;
              &--start, &--middle, &--end {
                span {
                  display: block;
                  color: white;
                  text-transform: uppercase;
                  font-size: rem(25px);
                  font-weight: 900;
                  vertical-align: middle;
                  &.first {
                    &__number {
                      font-size: rem(60px);
                    }
                    &__text {
                      font-size: rem(28px);
                    }
                  }
                  &.second {
                    &__number {
                      font-size: rem(68px);
                      text-align: center;
                    }
                    &__text {
                      text-align: center;
                      font-size: rem(25px);
                      &:last-child {
                        font-size: rem(30px);
                      }
                    }
                  }
                  &.third {
                    &__text {
                      margin-bottom: rem(16px);
                      font-size: rem(23px);
                      display: inline-block;
                      width: auto;
                      padding: 0 rem(16px);
                    }
                  }
                  @include respond-to("small and down") {
                    line-height: 1.2;
                  }
                  @include respond-to("medium") {
                    line-height: 1.2;
                  }
                }
                .third {
                  &__grid {
                    display: grid;
                    grid-template-columns: repeat(2, 1fr);
                    grid-template-rows: repeat(2, 1fr);
                    grid-row-gap: rem(8px);
                    grid-column-gap: rem(8px);
                    padding: 0 rem(5px);
                    span {
                      font-size: rem(16px);
                    }
                  }
                }
              }
            }
          }
        }
      }
      @include respond-to("small and down") {
        grid-row-gap: rem(34px);
        &-section {
          &--start, &--middle, &--end {
            .triplets {
              &-column {
                align-self: center;
                &--start, &--middle, &--end {
                  span {
                    text-align: center;
                    &.third {
                      &__text {
                        display: block;
                        padding: 0;
                        margin-bottom: rem(8px);
                      }
                    }
                  }
                  .third {
                    &__grid {
                      grid-template-columns: repeat(1, 1fr);
                      grid-template-rows: repeat(1, 1fr);
                      grid-row-gap: rem(8px);
                    }
                  }
                }
              }
            }
          }
        }
      }
      @include respond-to("medium") {
        grid-row-gap: rem(34px);
        &-section {
          &--start, &--middle, &--end {
            .triplets {
              &-column {
                align-self: center;
                &--start, &--middle, &--end {
                  span {
                    text-align: center;
                    &.third {
                      &__text {
                        display: block;
                        padding: 0;
                        margin-bottom: rem(8px);
                      }
                    }
                  }
                  .third {
                    &__grid {
                      grid-template-columns: repeat(1, 1fr);
                      grid-template-rows: repeat(1, 1fr);
                      grid-row-gap: rem(8px);
                    }
                  }
                }
              }
            }
          }
        }
      }
    }
  }
  .service-row-1, .service-row-2, .service-row-3 {
    .triplets {
      &-section {
        &--start, &--middle, &--end {
          .triplets {
            &-column {
              &--start, &--middle, &--end {
                .service {
                  &__name {
                    color: white;
                    text-transform: uppercase;
                    font-weight: 900;
                    border-bottom: 3px solid $brand-orange;
                    padding-bottom: rem(16px);
                    display: inline-block;
                  }
                  &__description {
                    color: white;
                    @include respond-to("large and up") {
                      width: 85%;
                    }
                  }
                  &__button {
                    @include button($brand-yellow, black);
                    width: auto;
                    padding: rem(12px);
                    text-transform: uppercase;
                    text-align: center;
                    text-decoration: none;
                    font-weight: 900;
                  }
                }
              }
            }
          }
        }
      }
    }
  }
  .service-row-1, .service-row-3 {
    background-color: $brand-blue-5;
    .triplets {
      &-section {
        &--start {
          .triplets {
            &-column {
              &--start {
                padding: rem(24px);
              }
            }
          }
        }
        &--middle {
          height: rem(400px);
          .triplets {
            &-column {
              &--middle {
                padding: 0;
              }
            }
          }
        }
        &--end {
          .triplets {
            &-column {
              &--end {
                padding: rem(24px);
              }
            }
          }
        }
      }
    }
  }
  .service-row-1 {
    background-color: $brand-blue-5;
    .triplets {
      &-section {
        &--start {
          .triplets {
            &-column {
              &--start {
                background-color: $brand-blue-4;
              }
            }
          }
        }
        &--middle {
          background-image: url('../assets/images/home-grid-1.jpg');
          background-size: cover;
        }
        &--end {
          .triplets {
            &-column {
              &--end {
                background-color: $brand-blue-7;
              }
            }
          }
        }
      }
    }
  }
  .service-row-2 {
    background-color: $brand-blue-7;
    .triplets {
      &-section {
        &--start {
          height: rem(400px);
          .triplets {
            &-column {
              &--start {
                padding: 0;
                background-image: url('../assets/images/home-grid-2.jpg');
                background-size: cover;
              }
            }
          }
        }
        &--middle {
          .triplets {
            &-column {
              &--middle {
                padding: rem(24px);
                background-color: $brand-blue-3;
              }
            }
          }
        }
        &--end {
          height: rem(400px);
          .triplets {
            &-column {
              &--end {
                padding: 0;
                background-image: url('../assets/images/home-grid-3.jpg');
                background-size: cover;
              }
            }
          }
        }
      }
    }
  }
  .service-row-3 {
    .triplets {
      &-section {
        &--start {
          .triplets {
            &-column {
              &--start {
                background-color: $brand-blue-2;
              }
            }
          }
        }
        &--middle {
          background-image: url('../assets/images/home-grid-4.jpg');
          background-size: cover;
        }
        &--end {
          .triplets {
            &-column {
              &--end {
                background-color: $brand-blue-3;
              }
            }
          }
        }
      }
    }
  }
  .contact-us {
    background-color: $brand-blue-6;
    .text-banner {
      padding: rem(124px) 0;
      h1 {
        color: white;
        font-weight: 900;
        margin-bottom: rem(30px);
        span {
          display: block;
          margin-top: rem(24px);
          font-size: rem(40px);
          line-height: 1;
        }
      }
      .contact-btn {
        @include button($brand-yellow, black);
        width: auto;
        margin: 0 auto;
        padding: rem(12px);
        text-transform: uppercase;
        text-align: center;
        text-decoration: none;
        font-weight: 900;
      }
    }
  }
  
  .warehousing {
    background-color: $brand-blue-4;
    .twin-columns {
      .twins {
        &-section {
          &--start {
            .twins {
              &-column {
                &--start {
                  width: rem(336px);
                  justify-self: center;
                  padding: rem(24px);
                  @include respond-to("small and down") {
                    justify-self: left;
                  }
                  @include respond-to("medium") {
                    justify-self: left;
                  }
                }
              }
            }
          }
          &--end {
            background-image: url('../assets/images/warehouse.jpg');
            background-size: cover;
            .twins {
              &-column {
                &--end {
                  //width: 100%;
                  padding: 0;
                }
              }
            }
          }
        }
      }
    }
  }
  .patio {
    background-color: $brand-blue-6;
    .twin-columns {
      .twins {
        &-section {
          &--start {
            background-image: url('../assets/images/patio.jpg');
            background-size: cover;
            .twins {
              &-column {
                &--start {
                  //width: 100%;
                  padding: 0;
                }
              }
            }
          }
          &--end {
            .twins {
              &-column {
                &--end {
                  width: rem(336px);
                  justify-self: left;
                  padding: rem(24px);
                }
              }
            }
          }
        }
      }
    }
  }
    .warehousing, .patio {
    .twin-columns {
      height: rem(336px);
      @include respond-to("small and down") {
        height: unset;
      }
      @include respond-to("medium") {
        height: unset;
      }
      .twins {
        &-section {
          &--start, &--end {
            @include respond-to("small and down") {
              height: rem(336px);
            }
            @include respond-to("medium") {
              height: rem(336px);
            }
            .twins {
              &-column {
                &--start, &--end {
                  .service {
                    &__name {
                      color: white;
                      text-transform: uppercase;
                      font-weight: 900;
                      border-bottom: 3px solid $brand-orange;
                      padding-bottom: rem(16px);
                      display: inline-block;
                    }
                    &__description {
                      color: white;
                      @include respond-to("large and up") {
                        width: 85%;
                      }
                    }
                    &__button {
                      @include button($brand-yellow, black);
                      width: auto;
                      padding: rem(12px);
                      text-transform: uppercase;
                      text-align: center;
                      text-decoration: none;
                      font-weight: 900;
                    }
                  }
                  img {
                    height: rem(336px);
                    @include respond-to("small and down") {
                      height: unset;
                    }
                    @include respond-to("medium") {
                      height: unset;
                    }
                  }
                }
              }
            }
          }
        }
      }
    }
  }
}
</style>