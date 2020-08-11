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
        <section class="maritime-fcl-description">
            <text-banner>
                <h2>Este tipo de flete te garantiza mayor rentabilidad por volumen, seguridad y flexibilidad en la entrega de tu mercancía de importación y exportación. Envía tus productos al otro lado del mundo con la asesoría de nuestros expertos en logística y recibe tu mercancía de importación mediante el método más confiable, seguro y eficiente.</h2>
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
                            <ul class="service__description">
                                <li>20' y 40' DC.</li>
                                <li>40' HC.</li>
                                <li>40' RF.</li>
                                <li>20' y 40' FR.</li>
                                <li>20' y 40' OT.</li>
                            </ul>
                    </div>
                    <div class="feature">
                        <h2 class="service__name">Tipo de Carga</h2>
                        <ul class="service__description">
                            <li>Seca.</li>
                            <li>Refrigerada.</li>
                            <li>Peligrosa.</li>
                        </ul>
                    </div>
                    <div class="feature">
                        <h2 class="service__name">Carga Mínima</h2>
                        <p class="service__description">Desde 1 contenedor.</p>
                    </div>
                    <div class="feature">
                        <h2 class="service__name">Cálculo del Costo</h2>
                        <p class="service__description">Por contenedor.</p>
                    </div>
                    <div class="feature">
                        <h2 class="service__name">Tiempo de Entrega</h2>
                        <p class="service__description">Semanas.</p>
                    </div>
                    <div class="feature">
                        <h2 class="service__name">Monitoreo</h2>
                        <p class="service__description">A través de nuestra plataforma.</p>
                    </div>
                    <div class="feature">
                        <h2 class="service__name">Alianzas</h2>
                        <ul class="service__description">
                            <li>Cosco</li>
                            <li>APL</li>
                            <li>ONE</li>
                            <li>CMA-CGM</li>
                            <li>Hapag Lloyd</li>
                            <li>MSC</li>
                        </ul>
                    </div>
                    <div class="feature">
                        <h2 class="service__name">Servicios Adicionales</h2>
                        <ul class="service__description">
                            <li>Servicio de resguardo en patio o almacén.</li>
                            <li>Etiquetado de mercancía para importación / exportación.</li>
                            <li>Conexiones para contenedor refrigerado.</li>
                            <li>“Cross Docking”.</li>
                        </ul>
                    </div>
                    <div class="feature">
                        <h2 class="service__name">Horarios</h2>
                        <ul class="service__description">
                            <li>Horario flexible para la carga/descarga del contenedor.</li>
                            <li>Arribos y zarpes calendarizados semanales.</li>
                        </ul>
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
                    @include respond-to('small and down') {
                        font-size: rem(34px);
                    }
                    @include respond-to('medium') {
                        font-size: rem(34px);
                    }
                }
                &>* {
                    position: unset;
                }
            }
        }
    }
    .maritime-fcl-description {
        background-color: $brand-blue-6;
        .text-banner {
            padding: rem(48px);
            .slim-column {
                @include respond-to("large and up") {
                    width: rem(815px);
                }
                h2 {
                    color: white;
                    line-height: 1.5;
                }
            }
        }
    }
    .features {
        background-color: $brand-blue-5;
        padding-bottom: $gutter-xxlarge;
        .single-column {
            .features-grid {
                @include gridline(4, 0, top);
                .feature {
                    color: white;
                    padding: rem(24px);
                    min-height: rem(292px);
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
                            li {
                                padding-bottom: $gutter-small;
                                &:before {
                                    content: "- ";
                                    position: absolute;
                                    margin-left: - $gutter-small;
                                }
                            }
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
                @include respond-to("small and down") {
                    @include gridline(1, 0, top);
                    .feature {
                        &:nth-child(even) {
                            background-color: $brand-blue-7;
                        }
                        &:nth-child(odd) {
                            background-color: $brand-blue-3;
                        }
                        &:first-child, &:last-child {
                            background-color: $brand-blue-4;
                        }
                    }
                }
            }
        }
    }

}
</style>
