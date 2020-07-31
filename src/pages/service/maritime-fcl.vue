<template>
  <default-layout>
    <base-page>
        <!-- SimpleHero -->
        <section class="maritime-fcl-intro">
            <simple-hero>
            <h1 class="title">Marítimo FCL</h1>
            </simple-hero>
        </section>

        <!--TextBanner-->
        <section class="maritime-description">
            <text-banner>
                <p>Este tipo de flete te garantiza mayor rentabilidad por volumen, seguridad y flexibilidad en la entrega de tu mercancía de importación y exportación. Envía tus productos al otro lado del mundo con la asesoría de nuestros expertos en logística y recibe tu mercancía de importación mediante el método más confiable, seguro y eficiente.</p>
            </text-banner>
        </section>

        <!--Single Column / FeaturesGrid-->
        <section class="features">
            <single-column>
                <section class="features-grid">
                    <div class="feature">
                        <h2 class="service__name">Destinos</h2>
                        <p class="service__description">Principales puertos en México, Asia, Europa, América y todo el mundo.</p>
                    </div>
                    <div class="feature">
                        <h2 class="service__name">Equipo Disponible</h2>
                        <p class="service__description">20' y 40' DC<br>40' HC<br>40' RF<br>20' y 40' FR<br>20' y 40' OT</p>
                    </div>
                    <div class="feature">
                        <h2 class="service__name">Tipo de Carga</h2>
                        <p class="service__description">Seca<br>Refrigerada y<br>Peligrosa</p>
                    </div>
                    <div class="feature">
                        <h2 class="service__name">Carga Mínima</h2>
                        <p class="service__description">Desde 1 contenedor</p>
                    </div>
                    <div class="feature">
                        <h2 class="service__name">Cálculo del Costo</h2>
                        <p class="service__description">Por contenedor</p>
                    </div>
                    <div class="feature">
                        <h2 class="service__name">Tiempo de Entrega</h2>
                        <p class="service__description">Semanas</p>
                    </div>
                    <div class="feature">
                        <h2 class="service__name">Monitoreo</h2>
                        <p class="service__description">A través de nuestra plataforma</p>
                    </div>
                    <div class="feature">
                        <h2 class="service__name">Alianzas</h2>
                        <p class="service__description">Cosco<br>APL<br>ONE</p>
                    </div>
                    <div class="feature">
                        <h2 class="service__name">Servicios Adicionales</h2>
                        <p class="service__description">Servicio de resguardo en patio o almacén</p>
                        <p class="service__description">Etiquetado de mercancía para importación / exportación</p>
                    </div>
                    <div class="feature">
                        <h2 class="service__name">Horarios</h2>
                        <p class="service__description">Horario flexible para la carga/descarga del contenedor</p>
                        <p class="service__description">Arribos y zarpes calendarizados semanales</p>
                    </div>
                </section>
            </single-column>
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
    .maritime-fcl-intro {
        .simple-hero {
            background-image: url('../../assets/images/services/hero-maritime-fcl.jpg');
            background-size: cover;
            &__content {
                color: white;
                padding-top: rem(145px);
                .title {
                    color: white;
                    font-size: 60px;
                    font-weight: 900;
                    text-transform: uppercase;
                    text-shadow: 0px 2px 4px rgba(0, 0, 0, 0.51);
                }
                &>* {
                    position: unset;
                }
            }
        }
    }
    .maritime-description {
        background-color: $brand-blue-6;
        .text-banner {
            padding: rem(48px);
            .slim-column {
                width: rem(815px);
                p {
                    color: white;
                    line-height: 1.5;
                }
            }
        }
    }
    .features {
        background-color: $brand-blue-5;
        .single-column {
            .features-grid {
                @include gridline(4, 0, top);
                .feature {
                    color: white;
                    padding: rem(24px);
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
                            @include respond-to('large and up') {
                            width: 85%;
                            }
                        }
                    }
                    &:first-child, &:nth-of-type(8), &:nth-of-type(9) {
                        background-color: $brand-blue-4;
                    }
                    &:nth-of-type(2), &:nth-of-type(4), &:nth-of-type(5), &:nth-of-type(7), &:nth-of-type(10), &:nth-of-type(12) {
                        background-color: $brand-blue-7;
                    }
                    &:nth-of-type(3), &:nth-of-type(6), &:nth-of-type(11) {
                        background-color: $brand-blue-3;
                    }
                }
                @include respond-to("medium") {
                    @include gridline(3, 0, top);
                    .feature {
                        &:first-child, &:nth-of-type(6), &:nth-of-type(7) {
                            background-color: $brand-blue-4;
                        }
                        &:nth-of-type(2), &:nth-of-type(4), &:nth-of-type(6), &:nth-of-type(8), &:nth-of-type(10), &:nth-of-type(12) {
                            background-color: $brand-blue-7;
                        }
                        &:nth-of-type(3), &:nth-of-type(5), &:nth-of-type(11) {
                            background-color: $brand-blue-3;
                        }
                    }
                }
            }
        }
    }

}
</style>
