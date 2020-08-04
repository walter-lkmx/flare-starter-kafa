<template>
  <default-layout>
    <base-page>

        <!--Single Column / Text-->
        <section class="legal">
            <slim-column>
                <section class="text">
                    <g-image src="~/assets/images/freight.jpg" alt="Freight"></g-image>
                    <h1 class="title">Aviso de privacidad</h1>
                    <p>Última actualización: <strong>4 de agosto, 2020</strong></p>
                    <p>De conformidad con lo establecido en la Ley Federal de Protección de Datos Personales en Posesión de los Particulares, <strong>Kafá Logistics, S.A de C.V.</strong> pone a su disposición el siguiente aviso de privacidad.</p>
                    <p><strong>Kafá Logistics, S.A de C.V.</strong>, es responsable del uso y protección de sus datos personales, en este sentido y atendiendo las obligaciones legales establecidas en la Ley Federal de Protección de Datos Personales en Posesión de los Particulares, a través de este instrumento se informa a los titulares de los datos, la información que de ellos se recaba y los fines que se le darán a dicha información.</p>
                    <p>Además de lo anterior, informamos a usted que <strong>Kafá Logistics, S.A de C.V.</strong>, tiene su domicilio ubicado en: Calle 2da y Granada Local #9. Ensenada, Baja California. CP 22830.</p>
                    <p>Los datos personales que recabamos de usted serán utilizados para las siguientes finalidades, las cuales son necesarias para concretar nuestra relación con usted, así como para atender los servicios y/o pedidos que solicite: dar soluciones logísticas en el transporte aéreo, marítimo y terrestre de mercancías desde y hacia cualquier parte del mundo; Trabajar como facilitadores en las cadenas de suministro de nuestros clientes y socios comerciales, proporcionando de manera oportuna soluciones logísticas</p>
                    <p>Para llevar a cabo las finalidades descritas en el presente aviso de privacidad, utilizaremos los siguientes datos personales:</p>
                    <ul>
                        <li>a) Nombre</li>
                        <li>b) Razón Social</li>
                        <li>c) Teléfono</li>
                        <li>d) Dirección</li>
                    </ul>
                    <p>Por otra parte, informamos a usted, que sus datos personales no serán compartidos con ninguna autoridad, empresa, organización o persona distintas a nosotros y serán utilizados exclusivamente para los fines señalados.</p>
                    <p>Usted tiene en todo momento el derecho a conocer qué datos personales tenemos de usted, para qué los utilizamos y las condiciones del uso que les damos (Acceso). Asimismo, es su derecho solicitar la corrección de su información personal en caso de que esté desactualizada, sea inexacta o incompleta (Rectificación); de igual manera, tiene derecho a que su información se elimine de nuestros registros o bases de datos cuando considere que la misma no está siendo utilizada adecuadamente (Cancelación); así como también a oponerse al uso de sus datos personales para fines específicos (Oposición). Estos derechos se conocen como derechos ARCO.</p>
                    <p>Para el ejercicio de cualquiera de los derechos ARCO, se deberá presentar la solicitud respectiva a través de los formatos que estarán a su disposición en: Calle 2da y Granada Local #9. Ensenada, Baja California. CP 22830</p>
                    <p>Lo anterior también servirá para conocer el procedimiento y requisitos para el ejercicio de los derechos ARCO.</p>
                    <p>En todo caso la respuesta a la solicitud se dará en un plazo de 72 horas.</p>
                    <p>Los datos de contacto de la persona o departamento de datos personales, que está a cargo de dar trámite a las solicitudes de derechos ARCO, son los siguientes:</p>
                    <ul>
                        <li>a) Nombre del responsable: Departamento Jurídico</li>
                        <li>b) Domicilio: Calle 2da y Granada Local #9. Ensenada, Baja California. CP 22830</li>
                        <li>c) Teléfono: (646) 135 8240</li>
                    </ul>

                    <p>Cabe mencionar, que en cualquier momento usted puede revocar su consentimiento para el uso de sus datos personales. Del mismo modo, usted puede revocar el consentimiento que, en su caso, nos haya otorgado para el tratamiento de sus datos personales. Asimismo, usted deberá considerar que para ciertos fines la revocación de su consentimiento implicará que no podamos seguir prestando el servicio que nos solicitó, o la conclusión de su relación con nosotros.</p>
                    <p>Para revocar el consentimiento que usted otorga en este acto o para limitar su divulgación, se deberá presentar la solicitud respectiva a través de los formatos que estarán a su disposición en: Calle 2da y Granada Local #9. Ensenada, Baja California. CP 22830</p>
                    <p>Del mismo modo, podrá solicitar la información para conocer el procedimiento y requisitos para la revocación del consentimiento, así como limitar el uso y divulgación de su información personal. En cualquier caso, la respuesta a las peticiones se dará a conocer en un plazo de 72 horas.</p>
                    <p>De cambios en nuestro modelo de negocio, o por otras causas, por lo cual, nos comprometemos a mantenerlo informado sobre los cambios que pueda sufrir el presente aviso de privacidad, sin embargo, usted puede solicitar información sobre si el mismo ha sufrido algún cambio a través de la siguiente dirección electrónica: <strong>www.kafa-logistics.com/privacidad</strong></p>
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
    .legal {
        background-color: $brand-blue-5;
        padding: $gutter-xxlarge 0;
        .slim-column {
            color: white;
            img {
                margin-bottom: $gutter-large;
            }
            .title {
                color: white;
                font-size: 48px;
                font-weight: 900;
                text-transform: uppercase;
                text-shadow: 0px 2px 4px rgba(0, 0, 0, 0.51);
            }
            h2 {
                color: white;
                font-weight: 900;
            }
            ul {
                margin-bottom: $gutter;
            }
        }
    }

}
</style>
