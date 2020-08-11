<template>
  <default-layout>
    <base-page>
        <!-- SimpleHero -->
        <section class="ferro-intro">
            <simple-hero>
            <h1 class="title">Ferroviario</h1>
            </simple-hero>
        </section>

        <!--TextBanner-->
        <section class="ferro-description">
            <text-banner>
                <h2>Para envío de grande volúmenes de cualquier tipo de mercancía a México y Estados Unidos.</h2>
            </text-banner>
        </section>

        <!--Single Column / FeaturesGrid-->
        <section class="features">
            <single-column>
                <section class="features-grid">
                    <div class="feature">
                        <h2 class="service__name">Destinos</h2>
                        <p class="service__description">Terminales en la Ciudad de México, Silao, Gudalajara, Culiacán, Cd. Obregón, Hermosillo, Mexicali, Monterrey y todo Estados Unidos.</p>
                    </div>
                    <div class="feature">
                        <h2 class="service__name">Ruta</h2>
                        <p class="service__description">Servicio Intermodal Interpacífico.</p>
                    </div>
                    <div class="feature">
                        <h2 class="service__name">Equipo Disponible</h2>
                        <ul class="service__description">
                            <li>20' y 40' DC.</li>
                            <li>40' HC.</li>
                            <li>53' HC.</li>
                        </ul>
                    </div>
                    <div class="feature">
                        <h2 class="service__name">Tipo de Carga</h2>
                        <ul class="service__description">
                            <li>Seca.</li>
                            <li>Peligrosa.</li>
                        </ul>
                    </div>
                    <div class="feature">
                        <h2 class="service__name">Carga Mínima</h2>
                        <p class="service__description">Desde 1 contenedor.</p>
                    </div>
                    <div class="feature">
                        <h2 class="service__name">Cálculo del Costo</h2>
                        <p class="service__description">Por ruta y tipo de carga.</p>
                    </div>
                    <div class="feature">
                        <h2 class="service__name">Tiempo de Entrega</h2>
                        <p class="service__description">Días.</p>
                    </div>
                    <div class="feature">
                        <h2 class="service__name">Horarios</h2>
                        <ul class="service__description">
                            <li>Horario flexible para la carga / descarga del contenedor.</li>
                            <li>Llegadas y salidas diarias.</li>
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
    .ferro-intro {
        .simple-hero {
            background-image: url('../../assets/images/services/hero-ferro.jpg');
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
    .ferro-description {
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
