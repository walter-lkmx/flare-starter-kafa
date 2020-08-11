<template>
  <default-layout>
    <base-page>
        <!-- SimpleHero -->
        <section class="warehouse-intro">
            <simple-hero>
            <h1 class="title">Almacenes</h1>
            </simple-hero>
        </section>

        <!--TextBanner-->
        <section class="warehouse-description">
        </section>

        <!--Single Column / FeaturesGrid-->
        <section class="features">
            <single-column>
                <section class="features-grid">
                    <div class="feature">
                        <h2 class="service__name">Almacenes</h2>
                        <ul class="service__description">
                            <li>Ensenada - 800 m².</li>
                            <li>Tijuana Otay - 2,000 m².</li>
                            <li>Otay, CA (EE.UU.) - 2,000 m².</li>
                        </ul>
                    </div>
                    <div class="feature">
                        <h2 class="service__name">Equipamiento</h2>
                        <ul class="service__description">
                            <li>Racks.</li>
                            <li>Unidades para distribución de la mercancía.</li>
                        </ul>
                    </div>
                    <div class="feature">
                        <h2 class="service__name">Sistemas de seguridad</h2>
                        <ul class="service__description">
                            <li>Guardia y alarma.</li>
                            <li>Video-vigilancia.</li>
                            <li>Registro de entradas y salidas.</li>
                        </ul>
                    </div>
                    <div class="feature">
                        <h2 class="service__name">Servicios Adicionales</h2>
                        <ul class="service__description">
                            <li>Maniobras de consolidación y desconsolidación.</li>
                            <li>Etiquetado de mercancía.</li>
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
    .warehouse-intro {
        .simple-hero {
            background-image: url('../../assets/images/warehouse.jpg');
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
    .warehouse-description {
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
