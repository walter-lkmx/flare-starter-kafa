<template>
  <default-layout>
    <base-page>

        <!--Single Column / Text-->
        <section class="contact">
            <slim-column>
                <section class="text">
                    <h1 class="title">Contacto</h1>
                    <p><span>Teléfono</span>(646) 135 8240</p>
                    <p><span>Correo electrónico</span>info@kafa-logistics.com</p>
                    <p><span>Dirección</span>Calle 2da y Granada Local #9. Ensenada, Baja California. CP 22830</p>
                    <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3388.789272573247!2d-116.6095194128525!3d31.85794906980314!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x80d893bd404a0153%3A0xa49701c532dd79c9!2sKafa%20Logistics!5e0!3m2!1sen!2smx!4v1596568762935!5m2!1sen!2smx" width="710" height="283" frameborder="0" style="border:0;" allowfullscreen="" aria-hidden="false" tabindex="0"></iframe>
                </section>
            </slim-column>
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
    .contact {
        background-color: $brand-blue-5;
        padding: $gutter-xxlarge 0;
        .slim-column {
            color: white;
            iframe {
                margin-bottom: $gutter-large;
            }
            .title {
                color: white;
                font-size: 48px;
                font-weight: 900;
                text-transform: uppercase;
                text-shadow: 0px 2px 4px rgba(0, 0, 0, 0.51);
            }
            p {
                span {
                    color: white;
                    font-weight: 900;
                    text-transform: uppercase;
                    font-size: rem(21px);
                    display: block;
                    margin-bottom: $gutter-small;
                }
            }
            ul {
                margin-bottom: $gutter;
            }
        }
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
