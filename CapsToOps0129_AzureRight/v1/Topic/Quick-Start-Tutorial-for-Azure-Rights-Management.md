---
title: Tutorial de inicio r&#225;pido de Azure Rights Management
ms.custom: na
ms.reviewer: na
ms.service: rights-management
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1db923bf-7d19-4fdd-a413-bfeb58af5e03
---
# Tutorial de inicio r&#225;pido de Azure Rights Management
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="es-ES">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="940649db38ed2d3f79877c600095a330" id="tgt1" class="tgtSentence">Use este tutorial para probar rápidamente Microsoft Azure Rights Management (también conocido como Azure RMS) para su organización en solo 5 pasos que deberían tomarle menos de 15 minutos.</caps:sentence>
          <caps:sentence sentenceid="0920179cc231cc0a3c9bbdfd9bc8fc91" id="tgt2" class="tgtSentence"> Podrá activar el servicio, enviar de forma segura un documento confidencial por correo electrónico a alguien de otra organización y luego hacer un seguimiento para saber cuándo se abre ese documento.</caps:sentence>
          <caps:sentence sentenceid="bdc778f379d69a0ea23b374ac6062c56" id="tgt3" class="tgtSentence"> Cuando el documento confidencial se envía, se cifra durante el tránsito y solo lo puede leer la persona a la que se envía, mediante los permisos que establece el remitente.</caps:sentence>
        </para>
        <para>
          <mediaLinkInline>
            <image xlink:href="3c893b16-6b7c-44e5-91e2-057ef42a9932"></image>
          </mediaLinkInline>
        </para>
        <para>
          <caps:sentence sentenceid="3be089740944bc19a9c18936f5f933dc" id="tgt4" class="tgtSentence">Este tutorial está destinado a los administradores y consultores de TI a fin de ayudarles a evaluar Azure Rights Management como una solución de protección de información para una organización.</caps:sentence>
          <caps:sentence sentenceid="fb074e7efe93746706819829f0e83518" id="tgt5" class="tgtSentence"> En un entorno de producción, las instrucciones para activar el servicio están a cargo del administrador, mientras que las instrucciones para enviar el documento son responsabilidad de los usuarios finales.</caps:sentence>
          <caps:sentence sentenceid="c1c6641e1bc841168ba85af28d1f6a2e" id="tgt6" class="tgtSentence"> En este tutorial se incluyen ambos conjuntos de instrucciones para demostrar el escenario completo del envío seguro de un documento confidencial a alguien de otra organización.</caps:sentence>
          <caps:sentence sentenceid="9e0d2706c1a6d82a35efa855bbe1eb89" id="tgt7" class="tgtSentence"> Si tiene problemas para completar este tutorial, envíe un mensaje de correo electrónico a <externalLink><linkText>AskIPTeam</linkText><linkUri>mailto:askipteam@microsoft.com?subject=Having%20problems%20with%20the%20Quick%20Start%20tutorial</linkUri></externalLink> y le ayudaremos.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="18f8f4b00a8fc67143c8dca5cd642100" id="tgt8" class="tgtSentence">Para completar este tutorial, necesitará lo siguiente:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="06409497b42cc1d884270754c6f51fe7" id="tgt9" class="tgtSentence">Una suscripción que admita Azure Rights Management.</caps:sentence>
              <caps:sentence sentenceid="95ad92b9d9e75065d09a01f9d237ffaf" id="tgt10" class="tgtSentence"> Esta puede ser una suscripción de pago o una suscripción de prueba.</caps:sentence>
              <caps:sentence sentenceid="88bffdcfb2a69f3d5ebc4498af03da3a" id="tgt11" class="tgtSentence"> Si quiere usar el seguimiento de documentos, que es un requisito en el paso 5 de este tutorial, su suscripción debe ser compatible con esta característica.</caps:sentence>
              <caps:sentence sentenceid="b74c3d4fef0797313d24ee039ef7cc0e" id="tgt12" class="tgtSentence"> Para obtener más información sobre las opciones de suscripción y los vínculos a las pruebas gratuitas, vea la sección <link xlink:href="dc78321d-d759-4653-8818-80da74b6cdeb#BKMK_SupportedSubscriptions">Cloud subscriptions that support Azure RMS</link> del tema <link xlink:href="dc78321d-d759-4653-8818-80da74b6cdeb">Requirements for Azure Rights Management</link>.</caps:sentence>
            </para>
            <para>
              <caps:sentence sentenceid="4f28c0ce2496de27b40e7b8cb488571c" id="tgt13" class="tgtSentence">Sugerencia: Si necesita obtener una suscripción, hágalo con anticipación porque el proceso puede durar varios minutos en completarse.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="dd88e5ba3a73482d9babc20a680490ba" id="tgt14" class="tgtSentence">Una cuenta de administrador para iniciar sesión en el centro de administración de Office 365 o en el Portal de Azure clásico para poder activar el servicio Rights Management.</caps:sentence>
              <caps:sentence sentenceid="73362d72867645e5af7a61c63d7138ca" id="tgt15" class="tgtSentence"> Esta cuenta también debe tener una dirección de correo electrónico y un servicio de correo electrónico de trabajo (por ejemplo, Exchange Online o Exchange Server).</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="076c6001b57aa7abb308c5143aec1689" id="tgt16" class="tgtSentence">Un equipo que ejecute Windows (a partir de Windows 7 SP1) y que tenga instalado Office 2016, Office 2013 u Office 2010.</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence sentenceid="3b3764e5a9a94133e8d50e55941852ab" id="tgt17" class="tgtSentence">Comencemos.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="cc8c0b753ed15fec45135ea95934ae80" id="tgt18" class="tgtSentence">Paso 1: Activación del servicio Rights Management</caps:sentence>
        </title>
        <content>
          <para>
            <mediaLinkInline>
              <image xlink:href="6b066564-3b43-43eb-999a-ce0c0cf7d25b"></image>
            </mediaLinkInline>
          </para>
          <para>
            <caps:sentence sentenceid="e3ba7687d02de29fde1527b5dfced3d8" id="tgt19" class="tgtSentence">Aunque es posible que tenga una suscripción que admita la Azure Rights Management, el servicio viene desactivado de forma predeterminada.</caps:sentence>
            <caps:sentence sentenceid="e3609809d3665769a43efa8a4aa04fac" id="tgt20" class="tgtSentence"> Para activarlo, puede usar el Centro de administración de Office 365 o el Portal de Azure clásico:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="7a57387850b2dbb6a001396c1e151091" id="tgt21" class="tgtSentence">Si tiene una suscripción de Office 365 que incluya Azure Rights Management o una suscripción de Office 365 que excluya Azure Rights Management, pero tiene una suscripción de Azure RMS Premium: <embeddedLabel>Use el Centro de administración de Office 365</embeddedLabel>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="048439426341140da780409fc948fb91" id="tgt22" class="tgtSentence">Si no tiene una suscripción de Office 365: <embeddedLabel>Use el Portal de Azure clásico</embeddedLabel>.</caps:sentence>
              </para>
            </listItem>
          </list>
          <mediaLink>
            <image xlink:href="4c4e5cad-e22a-4bcb-81b8-4048187357f1"></image>
          </mediaLink>
          <procedure>
            <title>
              <caps:sentence sentenceid="448a932b5daf8b0098f4c07c904ee0af" id="tgt23" class="tgtSentence">Para activar Rights Management desde el centro de administración de Office 365</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="1f15ac0171f52117607e1009d82daa8e" id="tgt24" class="tgtSentence">Vaya al <externalLink><linkText>portal de Office 365</linkText><linkUri>https://portal.office.com/</linkUri></externalLink> e inicie sesión con su cuenta profesional o educativa.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="1c2c7a763af00927f8a4dbe30e91903f" id="tgt25" class="tgtSentence">Si el Centro de administración de Office 365 no se muestra automáticamente, seleccione el icono del iniciador de la aplicación en la parte superior izquierda y elija <ui>Admin</ui>.</caps:sentence>
                    <caps:sentence sentenceid="df0360a0ab29f93fe3cc801c4c156415" id="tgt26" class="tgtSentence"> El icono <ui>Administrador</ui> aparece únicamente para los administradores de Office 365.</caps:sentence>
                  </para>
                  <alert class="tip">
                    <para>
                      <caps:sentence sentenceid="4a2dad5c56aa3e5f6c105c5263b4ffff" id="tgt27" class="tgtSentence">Para obtener ayuda con el centro de administración, consulte <externalLink><linkText>Sobre el Centro de administración de Office 365: ayuda para el administrador</linkText><linkUri>https://support.office.com/article/About-the-Office-365-admin-center-Admin-Help-58537702-d421-4d02-8141-e128e3703547</linkUri></externalLink>.</caps:sentence>
                    </para>
                  </alert>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="e30515d2d6ca28b427f4d525b17b0478" id="tgt28" class="tgtSentence">En el panel izquierdo, expanda <ui>CONFIGURACIÓN DEL SERVICIO</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="e06d209f1190c5a647829af121ed03a5" id="tgt29" class="tgtSentence">Haga clic en <ui>Rights Management</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="324eef6f9a207320f6b6fa26017475af" id="tgt30" class="tgtSentence">En la página <ui>RIGHTS MANAGEMENT</ui>, haga clic en <ui>Administrar</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="9bcf8edc7b8cfb36966189c69a30c23e" id="tgt31" class="tgtSentence">En la página <ui>Rights Management</ui>, haga clic en <ui>Activar</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="cb3dbd0c84b54d66efc08ecf6d4f0d34" id="tgt32" class="tgtSentence">Cuando el sistema le pregunte <ui>¿Desea activar Rights Management?</ui>, haga clic en <ui>Activar</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence sentenceid="76600d257ec2d32fd9c164ad85df0f70" id="tgt33" class="tgtSentence">Ahora debería ver el texto <ui>Rights Management está activada</ui> y la opción para desactivarla (es posible que deba actualizar la página manualmente).</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="14828b316c3cc1ed229a80d40f6db4bd" id="tgt34" class="tgtSentence">Por el momento, no haga clic en <ui>Características avanzadas</ui>.</caps:sentence>
                  <caps:sentence sentenceid="a2349b8f30dcf0a92bc9794c4fa9647d" id="tgt35" class="tgtSentence"> Esto le llevará al Portal de Azure clásico, donde podrá configurar las plantillas, que no son necesarias en este tutorial.</caps:sentence>
                  <caps:sentence sentenceid="62da051cafafd321dd9d6db9c240e9ed" id="tgt36" class="tgtSentence"> En su lugar, puede cerrar el centro de administración de Office 365.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
          <procedure>
            <title>
              <caps:sentence sentenceid="5377d3bbb754ec4b89ea810b7974f3d0" id="tgt37" class="tgtSentence">Para activar Rights Management desde el portal de Azure</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="6fd5b3b562a3f94b92b4db3351631379" id="tgt38" class="tgtSentence">Vaya al <externalLink><linkText>Portal de Azure clásico</linkText><linkUri>http://go.microsoft.com/fwlink/p/?LinkID=275081</linkUri></externalLink> e inicie sesión.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="754a9e159cb4f6ee8e17958f8431ca5b" id="tgt39" class="tgtSentence">En el panel izquierdo, haga clic en <ui>ACTIVE DIRECTORY</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="0a119846f95f1b3e868eae5ffcdd23f4" id="tgt40" class="tgtSentence">En la página <ui>Active Directory</ui>, haga clic en <ui>RIGHTS MANAGEMENT</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="a37a7ea60df661543c16c5bd4b2f8665" id="tgt41" class="tgtSentence">Seleccione el directorio que desea administrar para <token>aad_rightsmanagement_2</token>, haga clic en <ui>ACTIVAR</ui> y confirme la acción.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence sentenceid="5dd372e9e38fe1fec576e30c2c0bda7a" id="tgt42" class="tgtSentence">El <ui>ESTADO DE RIGHTS MANAGEMENT</ui> debe indicar ahora <ui>Activo</ui> y la opción <ui>ACTIVAR</ui> debe aparecer reemplazada por <ui>DESACTIVAR</ui>.</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="a3007566b05d1bce8572c8ee408df81a" id="tgt43" class="tgtSentence">Aunque puede configurar otras opciones de Rights Management en el portal, en este tutorial no es necesario, así que puede cerrar el Portal de Azure clásico.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
          <para>
            <caps:sentence sentenceid="7336afa5bd557a56736dfcf11d128e34" id="tgt44" class="tgtSentence">Eso es todo lo que necesita hacer en este primer paso.</caps:sentence>
            <caps:sentence sentenceid="08e4786f7ebfbf32720556445cf8c6a1" id="tgt45" class="tgtSentence"> El servicio está activado para que todos los usuarios de su organización puedan empezar a proteger los documentos importantes y confidenciales.</caps:sentence>
            <caps:sentence sentenceid="124041334946a8fab343a0c8ecdd46f4" id="tgt46" class="tgtSentence"> En un entorno de producción, es posible que desee restringir quién puede hacer esto al inicio a fin de llevar a cabo una implementación por fases.</caps:sentence>
            <caps:sentence sentenceid="b5f46da1bc79a0a2d8c6c5b39723a685" id="tgt47" class="tgtSentence"> Sin embargo, esto no es necesario para este tutorial.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="3a32eb87f38f4bc71c98b6ea47ad8e49" id="tgt48" class="tgtSentence">Aunque las plantillas personalizadas no se incluyen aquí, probablemente desee configurar algunas en una implementación de producción.</caps:sentence>
            <caps:sentence sentenceid="21aa1cdacf8582b9c9065bf5facc1ded" id="tgt49" class="tgtSentence"> Las plantillas permiten a los usuarios aplicar rápida y fácilmente la configuración de derechos cuando necesitan proteger archivos.</caps:sentence>
            <caps:sentence sentenceid="8ed4fb1a651d5e7ddb6a0d190d1fdff3" id="tgt50" class="tgtSentence"> Al activar Rights Management, obtendrá automáticamente 2 plantillas predeterminadas, que probablemente desee complementar con sus propias plantillas personalizadas en un entorno de producción.</caps:sentence>
            <caps:sentence sentenceid="fc76b095107642f0ca25f26a635c0ff4" id="tgt51" class="tgtSentence"> Sin embargo, las plantillas no son necesarias para este tutorial, así que ya puede ir al paso siguiente.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3595f5ce672f7f50c9aed66fb85c26d6" id="tgt52" class="tgtSentence">Si desea obtener más información</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4eec452dee7d15acfb78a023b487bf19" id="tgt53" class="tgtSentence">Información adicional</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1a5b1978cfe523b64bc27b5d993aa6f0" id="tgt54" class="tgtSentence">Acerca de la activación de Rights Management y el control de quién puede proteger archivos y correo electrónico cuando el servicio está activado   →</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="f8707e01-b239-4d1a-a1ea-0d1cf9a8d214">Activating Azure Rights Management</link>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="df561e4fb1699a8e2c2eafac28794afc" id="tgt55" class="tgtSentence">Acerca de las plantillas predeterminadas y del modo de crear nuevas plantillas personalizadas   →</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="1775d8d0-9a59-42c8-914f-ce285b71ac1c">Configuring Custom Templates for Azure Rights Management</link>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="9d0326859653ad60d213770a943d75be" id="tgt56" class="tgtSentence">Paso 2: Instalación de la aplicación de uso compartido Rights Management</caps:sentence>
        </title>
        <content>
          <para>
            <mediaLinkInline>
              <image xlink:href="56ac1537-75ba-453b-b65a-ff12ebe1f468"></image>
            </mediaLinkInline>
          </para>
          <para>
            <caps:sentence sentenceid="309ef3a79b3ad1ec018931a0c503c1bd" id="tgt57" class="tgtSentence">La aplicación de uso compartido Rights Management (también conocida como “aplicación de uso compartido RMS”) no es un requisito para Azure Rights Management, pero se recomienda para todos los equipos y dispositivos móviles compatibles con Azure Rights Management.</caps:sentence>
            <caps:sentence sentenceid="e0ef3721a07cfd0fbcd46eed9494d671" id="tgt58" class="tgtSentence"> La aplicación de uso compartido RMS se integra con aplicaciones de Office mediante la instalación de un complemento de Office para que los usuarios puedan proteger fácilmente los archivos directamente desde la cinta.</caps:sentence>
            <caps:sentence sentenceid="e17093f9e55ba9730e6ca7252ff79ce1" id="tgt59" class="tgtSentence"> También permite proteger todos los tipos de archivos mediante la aplicación de la protección genérica para los archivos que no son compatibles de forma nativa con Azure Rights Management y un sitio de seguimiento de documentos para que los usuarios controlen y revoquen los archivos que hayan protegido.</caps:sentence>
            <caps:sentence sentenceid="8e4759049decbb8cb4e664199d9c2e5c" id="tgt60" class="tgtSentence"> Usaremos el sitio de seguimiento de documentos más tarde en este tutorial.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="8630ad71c26f4a3dddfa6823fa6d1a3c" id="tgt61" class="tgtSentence">Esta aplicación se descarga de forma gratuita y ofrece una instalación con script para entornos de producción.</caps:sentence>
            <caps:sentence sentenceid="60e99bafe4b630e513fb2d8e1ef3a10b" id="tgt62" class="tgtSentence"> Sin embargo, en este tutorial la instalaremos de forma local.</caps:sentence>
          </para>
          <mediaLink>
            <image xlink:href="01e1ff01-4bca-4690-b8f1-9e8fe2a784b1"></image>
          </mediaLink>
          <procedure>
            <title>
              <caps:sentence sentenceid="3cf4cc52a998b14c5c7984a40033c719" id="tgt63" class="tgtSentence">Para descargar e instalar la aplicación Rights Management sharing</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="899369be6455fb30645fecfd0a8e727f" id="tgt64" class="tgtSentence">Vaya a la página de <externalLink><linkText>Microsoft Rights Management</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=303970</linkUri></externalLink> en el sitio web de Microsoft.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="41165b3f4b7357740133d3b9029f14a2" id="tgt65" class="tgtSentence">En la sección <ui>Equipos</ui>, haga clic en el icono de la <ui>Aplicación RMS para Windows</ui> y guarde el archivo <ui>Setup.exe</ui> para instalar la aplicación de uso compartido Microsoft Rights Management.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="19541cec65c563b2a81abd4f25b5cfc1" id="tgt66" class="tgtSentence">Para realizar una instalación local, debe usar una cuenta de administrador para ejecutar el archivo Setup.exe que se descargó.</caps:sentence>
                    <caps:sentence sentenceid="0167027de0dbe004ace43d2ed2a2f550" id="tgt67" class="tgtSentence"> Si el sistema le pregunta si desea continuar, haga clic en <ui>Sí</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="abacc694f0d29dee144cf040dbc3e3ed" id="tgt68" class="tgtSentence">En la página <ui>Instalar Microsoft RMS</ui>, haga clic en <ui>Siguiente</ui> y espere a que finalice la instalación.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="025542cb5e7b499000d6265d9329efe1" id="tgt69" class="tgtSentence">Cuando finalice la instalación, haga clic en <ui>Reiniciar</ui> si se le pide que reinicie el equipo, o en <ui>Cerrar</ui> para completar la instalación.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence sentenceid="61b9d2e9fec05c79a2530e1e7c2d9300" id="tgt70" class="tgtSentence">Ya está listo para empezar a proteger los archivos que contienen la información que desea compartir solo con las personas que especifique.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3595f5ce672f7f50c9aed66fb85c26d6" id="tgt71" class="tgtSentence">Si desea obtener más información</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4eec452dee7d15acfb78a023b487bf19" id="tgt72" class="tgtSentence">Información adicional</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c12bbfe2430f0c1b13805dce370dd79b" id="tgt73" class="tgtSentence">Acerca de una instalación local de la aplicación de uso compartido Rights Management para Windows y las instrucciones de usuario   →</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <externalLink>
                      <linkText>
                        <caps:sentence sentenceid="5a82d1d6328fcf4e332c7353808716e6" id="tgt74" class="tgtSentence">Guía de usuario de la aplicación de uso compartido Rights Management</caps:sentence>
                      </linkText>
                      <linkUri>http://technet.microsoft.com/library/dn339006.aspx</linkUri>
                    </externalLink>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d6cb8af2e8a6ad24853418285ccacf0a" id="tgt75" class="tgtSentence">Acerca de la instalación con scripts de la aplicación de uso compartido Rights Management para Windows y más información técnica   →</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <externalLink>
                      <linkText>
                        <caps:sentence sentenceid="45fd73cece8c888a3560a65a749417d4" id="tgt76" class="tgtSentence">Guía de administrador de la aplicación de uso compartido Rights Management</caps:sentence>
                      </linkText>
                      <linkUri>http://technet.microsoft.com/library/dn339003.aspx</linkUri>
                    </externalLink>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="30a40f5b787f839eb427ce1bd224b165" id="tgt77" class="tgtSentence">Para comprender la diferencia entre la protección nativa y la protección genérica   →</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="bbbb7aa95d80547c793bc460821fdf86" id="tgt78" class="tgtSentence">
                      <externalLink>
                        <linkText>¿Cuál es la diferencia entre la protección genérica y la protección incorporada (nativa)?</linkText>
                        <linkUri>https://technet.microsoft.com/library/dn574738.aspx</linkUri>
                      </externalLink> </caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="dae3cc7b2a8ab82b58e3a9260fa3f23a" id="tgt79" class="tgtSentence">Paso 3: Enviar el documento que desea proteger por correo electrónico</caps:sentence>
        </title>
        <content>
          <para>
            <mediaLinkInline>
              <image xlink:href="5faba8d1-045d-4caa-b34d-b408a61e6a3b"></image>
            </mediaLinkInline>
          </para>
          <para>
            <caps:sentence sentenceid="2691f512371dbfa5a5f7e3c205356abb" id="tgt80" class="tgtSentence">Para este paso, primero use Word para crear y guardar el documento que desea proteger y asígnele un nombre<system>Confidential.docx</system>.</caps:sentence>
            <caps:sentence sentenceid="f0c8a130b00ad2808cc262607a411ab2" id="tgt81" class="tgtSentence"> Para este tutorial, lo que importa no es el texto en concreto, si no el hecho de que haya texto para confirmar más fácilmente si el recipiente autorizado puede leerlo.</caps:sentence>
            <caps:sentence sentenceid="898a4c8bbd38e276cd0fed75906ce287" id="tgt82" class="tgtSentence"> Por ejemplo, puede escribir: <userInputLocalizable>Si puede leer esto en los datos adjuntos del correo electrónico, el remitente ha compartido correctamente un archivo protegido con Azure RMS.</userInputLocalizable></caps:sentence> </para>
          <para>
            <caps:sentence sentenceid="5cb437e4d9f3a6da6c201ce03109975c" id="tgt83" class="tgtSentence">A continuación, estará listo para compartir de forma segura este documento por correo electrónico.</caps:sentence>
          </para>
          <mediaLink>
            <image xlink:href="4243c4fb-517d-4f4a-a80a-c0ff470947aa"></image>
          </mediaLink>
          <procedure>
            <title>
              <caps:sentence sentenceid="bcb13b7c8b46696e92a923ed291328d2" id="tgt84" class="tgtSentence">Para compartir de forma segura el documento por correo electrónico</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="034dbf0405a7eebedf1777787602cfb3" id="tgt85" class="tgtSentence">En Outlook, cree un mensaje nuevo y adjunte el archivo que acaba de crear.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="207894a0ff96f65b95c39144fba73cfd" id="tgt86" class="tgtSentence">En el cuadro <ui>Para</ui>, escriba una o más direcciones de correo electrónico empresarial.</caps:sentence>
                    <caps:sentence sentenceid="f89c2cdd8dbc6f8c15b98ffa69516641" id="tgt87" class="tgtSentence"> Asegúrese de especificar una dirección de correo electrónico empresarial, como <userInput>janetm@contoso.com</userInput> o <userInput>p.dover@fabrikam.com</userInput>, porque, actualmente, Azure Rights Management no es compatible con las direcciones de correo electrónico personales que se usan en casa con el proveedor de Internet.</caps:sentence>
                    <caps:sentence sentenceid="5bc3e9009ccb35ae4a97658b485ddf2f" id="tgt88" class="tgtSentence"> No se preocupe por saber si la persona a la que envía el archivo también tiene Azure Rights Management o no.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="4a0e58ee2997cf2294a087b77c7a0b0f" id="tgt89" class="tgtSentence">Escriba un asunto, como <userInputLocalizable>Documento confidencial</userInputLocalizable> y, a continuación, escriba un mensaje breve para el correo electrónico, como <userInputLocalizable>Lea este documento confidencial y no lo comparta con otros.</userInputLocalizable></caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="e5d7648686a23b14b7f96688cec5f9ef" id="tgt90" class="tgtSentence">A continuación, en la pestaña <ui>Mensaje</ui> del grupo <ui>RMS</ui>, haga clic en <ui>Uso compartido seguro</ui> y luego haga clic en <ui>Uso compartido seguro</ui> nuevamente:</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="e8ccd91259b03901e6e5ef1cbb1103e5" id="tgt91" class="tgtSentence">En el cuadro de diálogo <ui>Uso compartido seguro</ui>:</caps:sentence>
                  </para>
                  <list class="ordered">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="72a6668baea3c97faf482e0c7ed58223" id="tgt92" class="tgtSentence">Seleccione <ui>Visor – Solo ver</ui>.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="c8617a6ec5cd1f4b8bb1305b9e6fa54d" id="tgt93" class="tgtSentence">Esto significa que los destinatarios podrán ver el documento pero no editarlo ni imprimirlo.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="42e46920ecfa6a404c662b44ad25319e" id="tgt94" class="tgtSentence">Seleccione <ui>Enviarme un correo electrónico cuando alguien trate de abrir estos documentos</ui>.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="a4d002603767dc3ffee4b81d295924e1" id="tgt95" class="tgtSentence">Recibirá una notificación por correo electrónico cada vez que los destinatarios intenten abrir el archivo adjunto, y también si alguien más intenta abrirlo (por ejemplo, cuando el destinatario reenvía el correo electrónico a un compañero de trabajo.</caps:sentence>
                        <caps:sentence sentenceid="6aca58314a95c1d66a9732674611f219" id="tgt96" class="tgtSentence"> En este último caso, verá que se deniega el acceso y, a partir de los detalles del usuario, podrá decidir si enviar a esa persona una copia del documento que puede abrir.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="67ffc9c6fd8065b6fe53ebe2bd37858a" id="tgt97" class="tgtSentence">Seleccione <ui>Permítame revocar el acceso a estos documentos de forma instantánea</ui>.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="317dc6bc9d9a0929dc75fe1f759ca37c" id="tgt98" class="tgtSentence">Esta opción requiere que los destinatarios tengan una conexión a Internet cada vez que abran el archivo adjunto, pero con el beneficio de que si más adelante se revoca el documento, la próxima vez que intenten abrirlo, no podrán hacerlo.</caps:sentence>
                        <caps:sentence sentenceid="2d678561414d7eb3f9e42f9ab631c4e8" id="tgt99" class="tgtSentence"> Si no selecciona esta opción, es posible que los destinatarios puedan abrirlo incluso sin una conexión a Internet, pero con la desventaja de que si más adelante se revoca el documento, puede producirse una demora para que esto tenga efecto.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="2dc0fed1d52620bc408d2cfb08d7478d" id="tgt100" class="tgtSentence">Haga clic en <ui>Enviar ahora</ui>.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="c608f94063c8cd9710c1af26bc67e4c0" id="tgt101" class="tgtSentence">El correo electrónico con datos adjuntos se envía a las direcciones de correo electrónico que especificó.</caps:sentence>
                        <caps:sentence sentenceid="e3202adc8887884e5790b333916f512a" id="tgt102" class="tgtSentence"> Además del mensaje de correo electrónico, verán instrucciones sobre cómo leer el documento adjunto que está protegido con Azure Rights Management.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </content>
              </step>
            </steps>
          </procedure>
          <para>
            <caps:sentence sentenceid="fd227d01baa0b756476a5e55c55cd841" id="tgt103" class="tgtSentence">Ahora que ha enviado el documento protegido, está listo para pedir a los destinatarios que esperen a que llegue para luego abrirlo.</caps:sentence>
            <caps:sentence sentenceid="6edd3e6faf9adecfa1ea51744b54c4a6" id="tgt104" class="tgtSentence"> Sin embargo, no debe cerrar Outlook, porque lo volveremos a usar en el último paso para realizar un seguimiento de los datos adjuntos.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3595f5ce672f7f50c9aed66fb85c26d6" id="tgt105" class="tgtSentence">Si desea obtener más información</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4eec452dee7d15acfb78a023b487bf19" id="tgt106" class="tgtSentence">Información adicional</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d7ff14043f5dd045a491ffaee66fcec2" id="tgt107" class="tgtSentence">Todas las instrucciones y los métodos alternativos para proteger los archivos que comparte por correo electrónico   →</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <externalLink>
                      <linkText>
                        <caps:sentence sentenceid="c3f04f5507167fd0366fa7d88b0c1ad2" id="tgt108" class="tgtSentence">Proteger un archivo que comparte por correo electrónico mediante la aplicación de uso compartido Rights Management.</caps:sentence>
                      </linkText>
                      <linkUri>https://technet.microsoft.com/library/dn574735.aspx</linkUri>
                    </externalLink>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="819726e26e4dafb8e9d910b6e2618c59" id="tgt109" class="tgtSentence">Acerca de las opciones del cuadro de diálogo <ui>Uso compartido seguro</ui>   →</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <externalLink>
                      <linkText>
                        <caps:sentence sentenceid="13cef8b13123a7c436788f60855c4248" id="tgt110" class="tgtSentence">Opciones del cuadro de diálogo para la aplicación de uso compartido Rights Management</caps:sentence>
                      </linkText>
                      <linkUri>https://technet.microsoft.com/library/dn574738.aspx</linkUri>
                    </externalLink>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="abd3311922c5dca4140aeccbc679ce20" id="tgt111" class="tgtSentence">Paso 4: Pedir a los destinatarios que abran el documento por correo electrónico</caps:sentence>
        </title>
        <content>
          <para>
            <mediaLinkInline>
              <image xlink:href="a0705091-4f9d-4d41-897b-b99e6000e006"></image>
            </mediaLinkInline>
          </para>
          <para>
            <caps:sentence sentenceid="e4b87e713ac76a7489edf6e71d1d252c" id="tgt112" class="tgtSentence">Los destinatarios pueden usar muchos dispositivos para leer el documento protegido que envía como datos adjuntos por correo electrónico.</caps:sentence>
            <caps:sentence sentenceid="f293df5c84168f5317a26f965fd34e8a" id="tgt113" class="tgtSentence"> Entre los dispositivos, se encuentran el iPad, el iPhone, tabletas y teléfonos Android, y equipos Mac, así como los equipos Windows.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="37212e4d35d929941350285ae004355f" id="tgt114" class="tgtSentence">Pídales que lean el mensaje de correo electrónico que ha enviado.</caps:sentence>
            <caps:sentence sentenceid="428cf1f28216fd28b82ce04473cae3de" id="tgt115" class="tgtSentence"> Verán el mensaje de correo electrónico con el siguiente texto delante:</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="63d54c49bfbcd77ffc6487a038e4e3a8" id="tgt116" class="tgtSentence">
              <ui>El remitente ha protegido los datos adjuntos con Microsoft RMS. Debe</ui> <externalLink><linkText>iniciar sesión</linkText><linkUri>http://aka.ms/rms</linkUri></externalLink> <ui>para abrirlos.</ui> </caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="25851d87b86378a5f9a0dc12c1bd63d2" id="tgt117" class="tgtSentence">Cuando hacen clic en el vínculo, este los lleva a las instrucciones para instalar la aplicación de uso compartido RMS y, si es necesario, suscribirse a una cuenta gratuita.</caps:sentence>
            <caps:sentence sentenceid="831f9947c2f3082b73f8bf72f06a6fa4" id="tgt118" class="tgtSentence"> La cuenta gratuita les concede una suscripción de RMS para individuos, que garantiza que los usuarios autorizados siempre puedan leer un documento protegido, incluso si su organización no dispone de Azure RMS.</caps:sentence>
            <caps:sentence sentenceid="c6ea192ef05750cbfd52acd943ae5a4c" id="tgt119" class="tgtSentence"> A continuación, están preparados para leer los datos adjuntos protegidos siguiendo las instrucciones a continuación.</caps:sentence>
          </para>
          <mediaLink>
            <image xlink:href="f370d881-a296-417a-8905-c32a8d8ac9bb"></image>
          </mediaLink>
          <procedure>
            <title>
              <caps:sentence sentenceid="5dd3fb02a42121176525edd1a9e5dfd9" id="tgt120" class="tgtSentence">Para ver los datos adjuntos del documento protegido</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="940507240ca116990a45520084144e68" id="tgt121" class="tgtSentence">Debido a que Azure Rights Management protegió un documento de Word, hay dos elementos adjuntos en el mensaje de correo electrónico.</caps:sentence>
                    <caps:sentence sentenceid="58e24f2a3eec8a1ae54a7bc603f09ded" id="tgt122" class="tgtSentence"> Estos son en realidad dos versiones del mismo archivo, pero con extensiones de nombre de archivo diferentes.</caps:sentence>
                    <caps:sentence sentenceid="e9f2fa9eeaa7e50cc24affb45ff6034a" id="tgt123" class="tgtSentence"> Abra la versión que tiene la extensión de nombre de archivo <system>.ppdf</system> (<system>Confidential.ppdf</system>).</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="d268403a2f27459c1858e3cf8d508876" id="tgt124" class="tgtSentence">Si tiene una versión de <externalLink><linkText>Office en el dispositivo que admite Rights Management</linkText><linkUri>https://technet.microsoft.com/library/dn655136.aspx#BKMK_SupportedApplications</linkUri></externalLink>, puede abrir la otra versión del archivo (<system>Confidential.docx</system>) para que se ejecute en Word.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="2bb0ad84150e128501de2fc72cb401ce" id="tgt125" class="tgtSentence">Si se le pide su nombre de usuario y contraseña, escriba su nombre de usuario en el mismo formato que la dirección de correo electrónico que se usó para enviarle el correo electrónico y los datos adjuntos.</caps:sentence>
                    <caps:sentence sentenceid="e11ed849b7603a1fa2fc5ad21972022a" id="tgt126" class="tgtSentence"> Por ejemplo, <userInput>janetm@contoso.com</userInput> o <userInput>p.dover@fabrikam.com</userInput>.</caps:sentence>
                    <caps:sentence sentenceid="53b9bd351140021d2610e63d8ebbb96a" id="tgt127" class="tgtSentence"> Para la contraseña, escriba la contraseña que proporcionó al suscribirse a RMS para usuarios.</caps:sentence>
                    <caps:sentence sentenceid="e2b4f294763a716d07225abcdf2f2ec0" id="tgt128" class="tgtSentence"> O bien, si su organización tiene Azure RMS, debe escribir la contraseña de trabajo habitual.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence sentenceid="fdf3b3a333944e357a5ab268357c7e5a" id="tgt129" class="tgtSentence">En este momento, se abre el documento y puede leer el contenido.</caps:sentence>
                  <caps:sentence sentenceid="318fe9e51adb6a79715eb3a06b269b5f" id="tgt130" class="tgtSentence"> Por ejemplo, puede decir <userInputLocalizable>Si puede leer esto en los datos adjuntos del correo electrónico, el remitente ha compartido correctamente un archivo protegido con Azure RMS.</userInputLocalizable> Debido a que es de solo lectura, no puede cambiar el contenido.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
          <para>
            <caps:sentence sentenceid="e73262e68fb7fcb96df76692b6d3a88e" id="tgt131" class="tgtSentence">Como paso opcional, puede pedir el destinatario que reenvíe el correo electrónico a otras personas que no incluyó en el correo electrónico original.</caps:sentence>
            <caps:sentence sentenceid="d90b403e84515bacfd9a02d80c9c15da" id="tgt132" class="tgtSentence"> Incluso si las otras personas trabajan para una organización como Azure Rights Management o solicitan su propia suscripción de RMS para usuarios, no podrán abrir el archivo adjunto.</caps:sentence>
            <caps:sentence sentenceid="6461861f4baec8190ac6153053a070fb" id="tgt133" class="tgtSentence"> Cuando se les pide el nombre de usuario, se deniega el acceso al documento.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="e6c8ec70c679659fff8526017e0f53bf" id="tgt134" class="tgtSentence">Ahora que el destinatario ha abierto el archivo adjunto y lo ha enviado de forma opcional a alguien más, espere la notificación por correo electrónico que informa de esta actividad.</caps:sentence>
            <caps:sentence sentenceid="d3b2402b65c7a730c1db650c8b5e873e" id="tgt135" class="tgtSentence"> Sin embargo, los mensajes de correo electrónico son fáciles de perder con el tiempo, así que una mejor manera de realizar un seguimiento de quién tuvo acceso al documento es usar el sitio de seguimiento de documentos, que se explica en el paso final.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3595f5ce672f7f50c9aed66fb85c26d6" id="tgt136" class="tgtSentence">Si desea obtener más información</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4eec452dee7d15acfb78a023b487bf19" id="tgt137" class="tgtSentence">Información adicional</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="bc48e37909f8c825f0eced9bf688c455" id="tgt138" class="tgtSentence">Instrucciones completas para ver archivos protegidos con Azure Rights Management   →</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <externalLink>
                      <linkText>
                        <caps:sentence sentenceid="5027005987755a9b1503b04f02dab7d8" id="tgt139" class="tgtSentence">Ver y usar archivos que han sido protegidos con Rights Management</caps:sentence>
                      </linkText>
                      <linkUri>https://technet.microsoft.com/library/dn574741.aspx</linkUri>
                    </externalLink>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d114ce5efd05466e03b15e0bd0208813" id="tgt140" class="tgtSentence">Acerca de la suscripción gratuita, RMS para usuarios   →</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="2efcb440-fefd-45e9-872b-f471573aadf2">RMS for Individuals and Azure Rights Management</link>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e0271e7fc8aa8c7997a4262e12d26b45" id="tgt141" class="tgtSentence">Acerca de las dos versiones del archivo que ve adjunto al mensaje de correo electrónico   →</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <externalLink>
                      <linkText>
                        <caps:sentence sentenceid="2b34d2d7b1575556df73d94c4d931762" id="tgt142" class="tgtSentence">¿Qué es el archivo .ppdf que se crea automáticamente?</caps:sentence>
                      </linkText>
                      <linkUri>https://technet.microsoft.com/library/dn574738.aspx</linkUri>
                    </externalLink>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="283e27696cc8a6f684c81f9a3dceb07f" id="tgt143" class="tgtSentence">Paso 5: Hacer un seguimiento del documento protegido</caps:sentence>
        </title>
        <content>
          <para>
            <mediaLinkInline>
              <image xlink:href="3d1ce494-490f-4493-8158-523ecda40fae"></image>
            </mediaLinkInline>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="2a6afe33ce452b7635c80e7642551f2a" id="tgt144" class="tgtSentence">Para este paso, debe tener una suscripción que admita el seguimiento de documentos.</caps:sentence>
              <caps:sentence sentenceid="40484a73b64876b08fbb008038329c7a" id="tgt145" class="tgtSentence"> Para comprobar si la suscripción incluye el seguimiento de documentos, vea <externalLink><linkText>Comparación de ofertas de Rights Management Services (RMS)</linkText><linkUri>https://technet.microsoft.com/dn858608.aspx</linkUri></externalLink>.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence sentenceid="ec84999fa8b806b91646d2526da5858c" id="tgt146" class="tgtSentence">Este paso es opcional, pero a la mayoría de las personas les gusta saber si se ha abierto el archivo adjunto que enviaron a los usuarios. Si es así, cuándo e incluso desde dónde.</caps:sentence>
            <caps:sentence sentenceid="4be0bb25039056347740ae85bcda324d" id="tgt147" class="tgtSentence"> Por ejemplo:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="873504c32f68ebb54eb9cd7ffabe1b1e" id="tgt148" class="tgtSentence">Espera una respuesta de una persona en un tiempo especificado y puede ver en el sitio de seguimiento de documentos que el archivo no se ha abierto, incluso cerca de la fecha límite.</caps:sentence>
                <caps:sentence sentenceid="09d9cfcfdaab5180c143d6717908ed8b" id="tgt149" class="tgtSentence"> Le envía un correo electrónico de seguimiento o la llama por teléfono como recordatorio puntual.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="0802a85de9177a132199b8720de5dad7" id="tgt150" class="tgtSentence">Después de ver que alguien ha abierto el documento, le pregunta si tiene dudas o si necesita información adicional.</caps:sentence>
              </para>
            </listItem>
          </list>
          <mediaLink>
            <image xlink:href="5b799166-171f-45dc-91b8-3f4c3c2992a8"></image>
          </mediaLink>
          <procedure>
            <title>
              <caps:sentence sentenceid="99209045ec0bd1e1d5007c5649ebf3bd" id="tgt151" class="tgtSentence">Para hacer un seguimiento de un documento protegido</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="94d1699322180c782a1d08f16bd37823" id="tgt152" class="tgtSentence">En Outlook, en la pestaña <ui>Inicio</ui> del grupo <ui>RMS</ui>, haga clic en <ui>Hacer seguimiento de uso</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="53c8e813b741f1f8dd0aa7b4a3853dd5" id="tgt153" class="tgtSentence">Si ve la página <ui>Proteger y compartir en sus términos</ui>, haga clic en <ui>Iniciar sesión</ui> y proporcione su nombre de usuario y contraseña de nuevamente.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="9884048d5ddce8ca0977e6bf58c27046" id="tgt154" class="tgtSentence">En la página <ui>Sus documentos compartidos</ui>, verá el documento que adjuntó al correo electrónico, <system>Confidential.docx</system>.</caps:sentence>
                    <caps:sentence sentenceid="f3af7f349f69efe702dbf4e531cf20d5" id="tgt155" class="tgtSentence"> En este punto, es el único archivo que aparece, pero a medida que comparta más documentos protegidos, la lista aumentará.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="aec33280b797530e720e2c9b9792de01" id="tgt156" class="tgtSentence">En esta página, verá la fecha en la que compartió el documento (cuándo envió el correo electrónico con el archivo adjunto protegido), la fecha de la última actividad y el nombre del destinatario al que envía el correo electrónico.</caps:sentence>
                    <caps:sentence sentenceid="431e7f5e4d2334ab658b0529a1c50bd9" id="tgt157" class="tgtSentence"> Haga clic en el nombre del documento para obtener detalles adicionales.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="d9aba71277dcaa8fc64bf86b7aa4d7ae" id="tgt158" class="tgtSentence">En la página nueva, que tiene el nombre del archivo en el que hizo clic, verá los detalles de resumen solo para ese documento y una lista de otras opciones que están disponibles para el documento (<ui>Lista</ui><ui>Escala de tiempo</ui><ui>Mapa</ui><ui>Configuración</ui>).</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="758b4c85fdd069358f6b639f6ce7f655" id="tgt159" class="tgtSentence">Haga clic en cada opción para explorar maneras diferentes para hacer un seguimiento de un documento protegido.</caps:sentence>
                    <caps:sentence sentenceid="b00aca6e6baea78892b7d3a061fa61e6" id="tgt160" class="tgtSentence"> O bien, también en la página <ui>Resumen</ui>, haga clic en<ui>Abrir en Excel</ui> para exportar la información a una hoja de cálculo o en <ui>Revocar acceso</ui> para dejar de compartir el documento.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence sentenceid="c5cf16c86c527b1005890671dd108d57" id="tgt161" class="tgtSentence">Puede volver a este sitio para realizar un seguimiento de más actividad relacionada con su documento protegido o revocar el acceso si es necesario.</caps:sentence>
                  <caps:sentence sentenceid="eeb66cb556d22f70ecd74924f3410c07" id="tgt162" class="tgtSentence"> Incluso puede acceder al sitio desde su dispositivo móvil o tableta mediante un explorador con este vínculo: <externalLink><linkText>seguimiento de documentos</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=529562</linkUri></externalLink></caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3595f5ce672f7f50c9aed66fb85c26d6" id="tgt163" class="tgtSentence">Si desea obtener más información</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4eec452dee7d15acfb78a023b487bf19" id="tgt164" class="tgtSentence">Información adicional</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c356f6bf8a346c0e7cb6483ddb57f1b4" id="tgt165" class="tgtSentence">Todas las instrucciones para realizar el seguimiento de los documentos   →</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <externalLink>
                      <linkText>
                        <caps:sentence sentenceid="08e07c08a82f9e8ba0aa6af551660dd1" id="tgt166" class="tgtSentence">Realizar un seguimiento de los documentos o revocarlos con la aplicación de uso compartido RMS</caps:sentence>
                      </linkText>
                      <linkUri>https://technet.microsoft.com/library/dn986611.aspx</linkUri>
                    </externalLink>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b2ea99effd4ed45b46b1b29377c18ef7" id="tgt167" class="tgtSentence">Vídeo de dos minutos en el que se explica y muestra el seguimiento de documentos   →</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <externalLink>
                      <linkText>
                        <caps:sentence sentenceid="359f977b97a00d540b44bcfc1c2c01f7" id="tgt168" class="tgtSentence">Revocación y seguimiento de documentos de Azure RMS</caps:sentence>
                      </linkText>
                      <linkUri>http://channel9.msdn.com/Series/Information-Protection/Azure-RMS-Document-Tracking-and-Revocation</linkUri>
                    </externalLink>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a0c75e43ab29adce4875806462967e5c" id="tgt169" class="tgtSentence">Para la solución de problemas y las preguntas de los clientes   →</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <externalLink>
                      <linkText>
                        <caps:sentence sentenceid="1ea15bf16350f6bd7bee6a3388afa295" id="tgt170" class="tgtSentence">Preguntas más frecuentes sobre seguimiento de documentos</caps:sentence>
                      </linkText>
                      <linkUri>https://technet.microsoft.com/dn947488</linkUri>
                    </externalLink>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="0a4f90ce90fc062c4fc00532513d86da" id="tgt171" class="tgtSentence">Pasos siguientes</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="b54608b6581cf4e69aee32f02473f011" id="tgt172" class="tgtSentence">En este tutorial se repasó un caso de cómo Azure RMS puede ayudar a proteger los datos.</caps:sentence>
            <caps:sentence sentenceid="dc850cdbd1fd888dc8eed8f0f3feacdc" id="tgt173" class="tgtSentence"> Para ver otros usos comunes, vea la sección <externalLink><linkText>Azure RMS en acción</linkText><linkUri>https://technet.microsoft.com/library/jj585026.aspx#BKMK_RMSpictures</linkUri></externalLink> en el artículo <link xlink:href="aeeebcd7-6646-4405-addf-ee1cc74df5df">What is Azure Rights Management?</link>.</caps:sentence>
            <caps:sentence sentenceid="8f110d2b6c26a7c4deaf5743edaf6076" id="tgt174" class="tgtSentence"> Hay otras secciones en este artículo que también pueden ser útiles, por ejemplo, la que explica cómo funciona Azure RMS y qué problemas empresariales puede resolver.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="a3dad2e66efd6d3eb67c416b8a0883d9" id="tgt175" class="tgtSentence">Si está listo para comenzar a implementar Azure RMS, use el <link xlink:href="086600c2-c5d8-47ec-a4c0-c782e1797486">Azure Rights Management Deployment Roadmap</link> para ver los pasos de implementación y los vínculos con instrucciones de los procedimientos.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="5214667c-ec69-42ca-8bbf-8cb22da8c62e">Getting Started with Azure Rights Management</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Use this tutorial to quickly try out Microsoft Azure Rights Management (also known as Azure RMS) for your organization with just 5 steps that should take you less than 15 minutes.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> You’ll activate the service, securely send a confidential document by email to somebody in another organization, and then be able to track when that document is opened.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> When the confidential document is emailed, it is encrypted while in transit and can be read only by the person it is sent to, using the permissions that are set by the sender.</caps:sentence>
        </para>
        <para>
          <mediaLinkInline>
            <image xlink:href="3c893b16-6b7c-44e5-91e2-057ef42a9932"></image>
          </mediaLinkInline>
        </para>
        <para>
          <caps:sentence id="src4" class="srcSentence">This tutorial is aimed at IT administrators and consultants, to help them evaluate Azure Rights Management as an information protection solution for an organization.</caps:sentence>
          <caps:sentence id="src5" class="srcSentence"> In a production environment, the instructions to activate the service would be done by an administrator and the instructions to send the document would be done by end users.</caps:sentence>
          <caps:sentence id="src6" class="srcSentence"> Both sets of instructions are included in this tutorial, to demonstrate the end-to-end scenario of securely sending a confidential document to somebody in another organization.</caps:sentence>
          <caps:sentence id="src7" class="srcSentence"> If you have any problems completing this tutorial, send an email message to <externalLink><linkText>AskIPTeam</linkText><linkUri>mailto:askipteam@microsoft.com?subject=Having%20problems%20with%20the%20Quick%20Start%20tutorial</linkUri></externalLink> and we will help you out.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src8" class="srcSentence">To complete this tutorial, you will need the following:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src9" class="srcSentence">A subscription that supports Azure Rights Management .</caps:sentence>
              <caps:sentence id="src10" class="srcSentence"> This can be a paid subscription or a trial subscription.</caps:sentence>
              <caps:sentence id="src11" class="srcSentence"> If you want to use document tracking, which is required for step 5 in this tutorial, your subscription must support document tracking.</caps:sentence>
              <caps:sentence id="src12" class="srcSentence"> For more information about the subscription options and links to free trials, see the <link xlink:href="dc78321d-d759-4653-8818-80da74b6cdeb#BKMK_SupportedSubscriptions">Cloud subscriptions that support Azure RMS</link> section in the <link xlink:href="dc78321d-d759-4653-8818-80da74b6cdeb">Requirements for Azure Rights Management</link> topic.</caps:sentence>
            </para>
            <para>
              <caps:sentence id="src13" class="srcSentence">Tip: If you need to get a subscription, do this in advance because this process can sometimes take a while to complete.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src14" class="srcSentence">An administrator account to sign in to the Office 365 admin center or the Azure classic portal, so that you can activate the Rights Management service.</caps:sentence>
              <caps:sentence id="src15" class="srcSentence"> This account must also have an email address and a working email service (for example, Exchange Online or Exchange Server).</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src16" class="srcSentence">A computer running Windows (minimum of Windows 7 SP1), and which has installed either Office 2016, Office 2013, or Office 2010.</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence id="src17" class="srcSentence">Let’s get started.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src18" class="srcSentence">Step 1: Activate the Rights Management service</caps:sentence>
        </title>
        <content>
          <para>
            <mediaLinkInline>
              <image xlink:href="6b066564-3b43-43eb-999a-ce0c0cf7d25b"></image>
            </mediaLinkInline>
          </para>
          <para>
            <caps:sentence id="src19" class="srcSentence">Even though you might have a subscription that supports Azure Rights Management, the service is disabled by default.</caps:sentence>
            <caps:sentence id="src20" class="srcSentence"> To activate it, you can use either the Office 365 admin center, or the Azure classic portal:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src21" class="srcSentence">If you have an Office 365 subscription that includes Azure Rights Management, or an Office 365 subscription that excludes Azure Rights Management but you have a subscription for Azure RMS Premium: <embeddedLabel>Use the Office 365 admin center</embeddedLabel>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src22" class="srcSentence">If you do not have an Office 365 subscription: <embeddedLabel>Use the Azure classic portal</embeddedLabel>.</caps:sentence>
              </para>
            </listItem>
          </list>
          <mediaLink>
            <image xlink:href="4c4e5cad-e22a-4bcb-81b8-4048187357f1"></image>
          </mediaLink>
          <procedure>
            <title>
              <caps:sentence id="src23" class="srcSentence">To activate Rights Management from the Office 365 admin center</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src24" class="srcSentence">Go to the <externalLink><linkText>Office 365 portal</linkText><linkUri>https://portal.office.com/</linkUri></externalLink> and sign in with your work or school account.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src25" class="srcSentence">If the Office 365 admin center does not automatically display, select the app launcher icon in the upper-left and choose <ui>Admin</ui>.</caps:sentence>
                    <caps:sentence id="src26" class="srcSentence"> The <ui>Admin</ui> tile appears only to Office 365 administrators.</caps:sentence>
                  </para>
                  <alert class="tip">
                    <para>
                      <caps:sentence id="src27" class="srcSentence">For admin center help, see <externalLink><linkText>About the Office 365 admin center - Admin Help</linkText><linkUri>https://support.office.com/article/About-the-Office-365-admin-center-Admin-Help-58537702-d421-4d02-8141-e128e3703547</linkUri></externalLink>.</caps:sentence>
                    </para>
                  </alert>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src28" class="srcSentence">In the left pane, expand <ui>SERVICE SETTINGS</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src29" class="srcSentence">Click <ui>Rights Management</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src30" class="srcSentence">On the <ui>RIGHTS MANAGEMENT</ui> page, click <ui>Manage</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src31" class="srcSentence">On the <ui>rights management</ui> page, click <ui>activate</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src32" class="srcSentence">When prompted <ui>Do you want to activate Rights Management?</ui>, click <ui>activate</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence id="src33" class="srcSentence">You should now see <ui>Rights management is activated</ui> and the option to deactivate (you might need to manually refresh the page)</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src34" class="srcSentence">At this time, do not click <ui>advanced features</ui>.</caps:sentence>
                  <caps:sentence id="src35" class="srcSentence"> This takes you to the Azure classic portal where you can configure templates, which are not needed for this tutorial.</caps:sentence>
                  <caps:sentence id="src36" class="srcSentence"> Instead, you can close the Office 365 admin center.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
          <procedure>
            <title>
              <caps:sentence id="src37" class="srcSentence">To activate Rights Management from the Azure portal</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src38" class="srcSentence">Go to the <externalLink><linkText>Azure classic portal</linkText><linkUri>http://go.microsoft.com/fwlink/p/?LinkID=275081</linkUri></externalLink> and sign in.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src39" class="srcSentence">In the left pane, click <ui>ACTIVE DIRECTORY</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src40" class="srcSentence">From the <ui>active directory</ui> page, click <ui>RIGHTS MANAGEMENT</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src41" class="srcSentence">Select the directory to manage for <token>aad_rightsmanagement_2</token>, click <ui>ACTIVATE</ui>, and then confirm your action.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence id="src42" class="srcSentence">The <ui>RIGHTS MANAGEMENT STATUS</ui> should now display <ui>Active</ui> and the <ui>ACTIVATE</ui> option is replaced with <ui>DEACTIVATE</ui>.</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src43" class="srcSentence">Although you can configure other options for Rights Management in the portal, these are not needed for this tutorial, so you can close the Azure classic portal.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
          <para>
            <caps:sentence id="src44" class="srcSentence">That’s all you need to do for this first step.</caps:sentence>
            <caps:sentence id="src45" class="srcSentence"> The service is activated so all users in your organization can now start to protect important and sensitive documents.</caps:sentence>
            <caps:sentence id="src46" class="srcSentence"> In a production environment, you might want to restrict who can do this initially, for a phased rollout.</caps:sentence>
            <caps:sentence id="src47" class="srcSentence"> But it’s not necessary for this tutorial.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src48" class="srcSentence">Although not included here, for a production deployment, you probably will also probably want to configure custom templates.</caps:sentence>
            <caps:sentence id="src49" class="srcSentence"> Templates make it easier for users to quickly apply the right settings when they need to protect files.</caps:sentence>
            <caps:sentence id="src50" class="srcSentence"> When you activate Rights Management, you automatically get 2 default templates and it’s likely you will want to supplement these with your own custom templates in a production environment.</caps:sentence>
            <caps:sentence id="src51" class="srcSentence"> But templates are not needed for this tutorial, so you’re ready to go to the next step.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src52" class="srcSentence">If you want more information</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src53" class="srcSentence">Additional information</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src54" class="srcSentence">About activating Rights Management and controlling who can protect files and email when the service is activated   →</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="f8707e01-b239-4d1a-a1ea-0d1cf9a8d214">Activating Azure Rights Management</link>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src55" class="srcSentence">About the default templates and how to create new, custom templates   →</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="1775d8d0-9a59-42c8-914f-ce285b71ac1c">Configuring Custom Templates for Azure Rights Management</link>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src56" class="srcSentence">Step 2: Install the Rights Management sharing application</caps:sentence>
        </title>
        <content>
          <para>
            <mediaLinkInline>
              <image xlink:href="56ac1537-75ba-453b-b65a-ff12ebe1f468"></image>
            </mediaLinkInline>
          </para>
          <para>
            <caps:sentence id="src57" class="srcSentence">The Rights Management sharing application (also known as the “RMS sharing app”) isn’t a requirement for Azure Rights Management, but we recommend it for all computers and mobile devices that support Azure Rights Management.</caps:sentence>
            <caps:sentence id="src58" class="srcSentence"> The RMS sharing application integrates with Office applications by installing an Office add-in so that users can easily protect files directly from the ribbon.</caps:sentence>
            <caps:sentence id="src59" class="srcSentence"> It also makes it possible to protect all files types by applying generic protection for files that are not natively supported by Azure Rights Management, and a document tracking site for users to track and revoke files that they have protected.</caps:sentence>
            <caps:sentence id="src60" class="srcSentence"> We’ll be using the document tracking site later in this tutorial.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src61" class="srcSentence">This application is free to download and offers a scripted install for production environments.</caps:sentence>
            <caps:sentence id="src62" class="srcSentence"> But for this tutorial, we’ll install it locally.</caps:sentence>
          </para>
          <mediaLink>
            <image xlink:href="01e1ff01-4bca-4690-b8f1-9e8fe2a784b1"></image>
          </mediaLink>
          <procedure>
            <title>
              <caps:sentence id="src63" class="srcSentence">To download and install the Rights Management sharing application</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src64" class="srcSentence">Go to the <externalLink><linkText>Microsoft Rights Management</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=303970</linkUri></externalLink> page on the Microsoft website.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src65" class="srcSentence">In the <ui>Computers</ui> section, click the icon for the <ui>RMS app for Windows</ui> and save the <ui>Setup.exe</ui> file to install the Microsoft Rights Management sharing application.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src66" class="srcSentence">For a local install, you must use an administrator account to run the Setup.exe file that was downloaded.</caps:sentence>
                    <caps:sentence id="src67" class="srcSentence"> If you are prompted to continue, click <ui>Yes</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src68" class="srcSentence">On the <ui>Setup Microsoft RMS</ui> page, click <ui>Next</ui>, and wait for the installation to finish.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src69" class="srcSentence">When the installation finishes, click <ui>Restart</ui> if prompted to restart your computer, or click  <ui>Close</ui> to complete the installation.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence id="src70" class="srcSentence">You’re now ready to start protecting files that contain information that you want to share but only with the people that you specify.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src71" class="srcSentence">If you want more information</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src72" class="srcSentence">Additional information</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src73" class="srcSentence">About a local installation of the Rights Management sharing application for Windows and user instructions   →</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <externalLink>
                      <linkText>
                        <caps:sentence id="src74" class="srcSentence">Rights Management sharing application user guide</caps:sentence>
                      </linkText>
                      <linkUri>http://technet.microsoft.com/library/dn339006.aspx</linkUri>
                    </externalLink>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src75" class="srcSentence">About the scripted installation of the Rights Management sharing application for Windows and more technical information   →</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <externalLink>
                      <linkText>
                        <caps:sentence id="src76" class="srcSentence">Rights Management sharing application administrator guide</caps:sentence>
                      </linkText>
                      <linkUri>http://technet.microsoft.com/library/dn339003.aspx</linkUri>
                    </externalLink>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src77" class="srcSentence">To understand the difference between native protection and generic protection   →</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src78" class="srcSentence">
                      <externalLink>
                        <linkText>What’s the difference between generic protection and built-in (native) protection?</linkText>
                        <linkUri>https://technet.microsoft.com/library/dn574738.aspx</linkUri>
                      </externalLink> </caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src79" class="srcSentence">Step 3: Email your document that you want to protect</caps:sentence>
        </title>
        <content>
          <para>
            <mediaLinkInline>
              <image xlink:href="5faba8d1-045d-4caa-b34d-b408a61e6a3b"></image>
            </mediaLinkInline>
          </para>
          <para>
            <caps:sentence id="src80" class="srcSentence">For this step, first create and save a document using Word that will represent your document that you want to protect, and name it <system>Confidential.docx</system>.</caps:sentence>
            <caps:sentence id="src81" class="srcSentence"> For this tutorial, it doesn’t matter what text it actually contains, but you will want it to contain some text so you can more easily confirm that the authorized recipient could read it.</caps:sentence>
            <caps:sentence id="src82" class="srcSentence"> For example, you might type: <userInputLocalizable>If you can read this from your email attachment, the sender has successfully shared a file that was protected with Azure RMS.</userInputLocalizable></caps:sentence> </para>
          <para>
            <caps:sentence id="src83" class="srcSentence">You’re then ready to safely share this document by email.</caps:sentence>
          </para>
          <mediaLink>
            <image xlink:href="4243c4fb-517d-4f4a-a80a-c0ff470947aa"></image>
          </mediaLink>
          <procedure>
            <title>
              <caps:sentence id="src84" class="srcSentence">To safely share your document by email</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src85" class="srcSentence">Using Outlook, create a new message and attach the file that you just created.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src86" class="srcSentence">In the <ui>To</ui> box, type one or more business email addresses.</caps:sentence>
                    <caps:sentence id="src87" class="srcSentence"> Make sure you specify a business email address, such as <userInput>janetm@contoso.com</userInput> or <userInput>p.dover@fabrikam.com</userInput> because currently, Azure Rights Management doesn’t support personal email addresses that you might use at home from your Internet provider.</caps:sentence>
                    <caps:sentence id="src88" class="srcSentence"> Don’t worry about whether the person you’re sending it to also has Azure Rights Management or not.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src89" class="srcSentence">Type a subject, such as  <userInputLocalizable>Confidential document</userInputLocalizable> and then type a short message for the email, such as <userInputLocalizable>Please read this confidential document and do not share it with others.</userInputLocalizable></caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src90" class="srcSentence">Then, on the <ui>Message</ui> tab, in the <ui>RMS</ui> group, click <ui>Share Protected</ui> and then click <ui>Share Protected</ui> again:</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src91" class="srcSentence">In the <ui>share protected</ui> dialog box:</caps:sentence>
                  </para>
                  <list class="ordered">
                    <listItem>
                      <para>
                        <caps:sentence id="src92" class="srcSentence">Select <ui>Viewer – View Only</ui>.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src93" class="srcSentence">This means our recipients will be able to view the document but not edit or print it.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src94" class="srcSentence">Select <ui>Email me when somebody tries to open these documents</ui>.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src95" class="srcSentence">You’ll get an email notification each time the recipients try to open the attachment, and also if somebody else tries to open it—for example, your recipient forwards the email to co-worker.</caps:sentence>
                        <caps:sentence id="src96" class="srcSentence"> In this last scenario, you’ll see that access was denied and from the user details, you can decide whether to send that person a copy of the document that they can open.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src97" class="srcSentence">Select <ui>Allow me to instantly revoke access to these documents</ui>.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src98" class="srcSentence">This option requires the recipients to have an Internet connection each time they open the attachment but with the benefit that if you later revoke the document, the next time they try to open it, they will not be able to.</caps:sentence>
                        <caps:sentence id="src99" class="srcSentence"> If you do not select this option, the recipients might be able to open it even without an Internet connection but with the disadvantage that if you later revoke the document, there might be a delay for when that takes effect.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src100" class="srcSentence">Click <ui>Send Now</ui>.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src101" class="srcSentence">The email with attachment is sent to the email addresses that you specified.</caps:sentence>
                        <caps:sentence id="src102" class="srcSentence"> In addition to your email message, they will see instructions how to read the attached document that is protected by Azure Rights Management.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </content>
              </step>
            </steps>
          </procedure>
          <para>
            <caps:sentence id="src103" class="srcSentence">Now you’ve sent your protected document, you’re ready to ask your recipients to wait for it to arrive and then open it.</caps:sentence>
            <caps:sentence id="src104" class="srcSentence"> But don’t close Outlook, because we’ll use it again in our final step to track the attachment.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src105" class="srcSentence">If you want more information</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src106" class="srcSentence">Additional information</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src107" class="srcSentence">Full instructions and alternative methods for protecting files that you share by email   →</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <externalLink>
                      <linkText>
                        <caps:sentence id="src108" class="srcSentence">Protect a file that you share by email by using the Rights Management sharing application</caps:sentence>
                      </linkText>
                      <linkUri>https://technet.microsoft.com/library/dn574735.aspx</linkUri>
                    </externalLink>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src109" class="srcSentence">About the options in the <ui>share protected</ui> dialog box   →</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <externalLink>
                      <linkText>
                        <caps:sentence id="src110" class="srcSentence">Dialog box options for the Rights Management sharing application</caps:sentence>
                      </linkText>
                      <linkUri>https://technet.microsoft.com/library/dn574738.aspx</linkUri>
                    </externalLink>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src111" class="srcSentence">Step 4: Ask your recipients to open the emailed document</caps:sentence>
        </title>
        <content>
          <para>
            <mediaLinkInline>
              <image xlink:href="a0705091-4f9d-4d41-897b-b99e6000e006"></image>
            </mediaLinkInline>
          </para>
          <para>
            <caps:sentence id="src112" class="srcSentence">Your recipients can use many devices to read the protected document that you sent as an email attachment.</caps:sentence>
            <caps:sentence id="src113" class="srcSentence"> The devices include iPads, iPhones, Android tablets and phones, Mac computers, as well as Windows computers.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src114" class="srcSentence">Ask them to read the email message that you sent.</caps:sentence>
            <caps:sentence id="src115" class="srcSentence"> They will see your email message and before that, the following text:</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src116" class="srcSentence">
              <ui>The sender has protected the attachments with Microsoft RMS. You must</ui> <externalLink><linkText>sign in</linkText><linkUri>http://aka.ms/rms</linkUri></externalLink> <ui>to open them.</ui> </caps:sentence>
          </para>
          <para>
            <caps:sentence id="src117" class="srcSentence">When they click the link, it takes them to instructions to install the RMS sharing app and if necessary, sign up for a free account.</caps:sentence>
            <caps:sentence id="src118" class="srcSentence"> The free account grants them a subscription for RMS for individuals, which ensures that authorized users can always read a protected document, even if their organization does not have Azure RMS.</caps:sentence>
            <caps:sentence id="src119" class="srcSentence"> They are then ready to read the protected attachment by using the following instructions.</caps:sentence>
          </para>
          <mediaLink>
            <image xlink:href="f370d881-a296-417a-8905-c32a8d8ac9bb"></image>
          </mediaLink>
          <procedure>
            <title>
              <caps:sentence id="src120" class="srcSentence">To view the protected document attachment</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src121" class="srcSentence">Because Azure Rights Management protected a Word document, there are two attachments for the email message.</caps:sentence>
                    <caps:sentence id="src122" class="srcSentence"> These are actually two versions of the same file but with different file name extensions.</caps:sentence>
                    <caps:sentence id="src123" class="srcSentence"> Open the version that has the <system>.ppdf</system> file name extension (<system>Confidential.ppdf</system>).</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src124" class="srcSentence">If you have a version of <externalLink><linkText>Office on your device that supports Rights Management</linkText><linkUri>https://technet.microsoft.com/library/dn655136.aspx#BKMK_SupportedApplications</linkUri></externalLink>, you can open the other version of the file (<system>Confidential.docx</system>), so that it opens in Word.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src125" class="srcSentence">If you are prompted for your user name and password, enter your user name in the same format as the email address that was used to send you the email and attachment.</caps:sentence>
                    <caps:sentence id="src126" class="srcSentence"> For example, <userInput>janetm@contoso.com</userInput> or <userInput>p.dover@fabrikam.com</userInput>.</caps:sentence>
                    <caps:sentence id="src127" class="srcSentence"> For your password, type the password that you supplied when you signed up for RMS for individuals.</caps:sentence>
                    <caps:sentence id="src128" class="srcSentence"> Or, if your organization has Azure RMS, enter your usual work password.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence id="src129" class="srcSentence">The document opens and you can now read the contents.</caps:sentence>
                  <caps:sentence id="src130" class="srcSentence"> For example, it might say <userInputLocalizable>If you can read this from your email attachment, the sender has successfully shared a file that was protected with Azure RMS.</userInputLocalizable> Because it’s read-only, you cannot change the contents.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
          <para>
            <caps:sentence id="src131" class="srcSentence">As an optional step, you could ask your recipient to forward the email to other people that you didn’t include in your original email.</caps:sentence>
            <caps:sentence id="src132" class="srcSentence"> Even if those other people work for an organization that has Azure Rights Management or they apply for their own RMS for individuals subscription, they won’t be able to open the attachment.</caps:sentence>
            <caps:sentence id="src133" class="srcSentence"> When they are promoted for their user name, access to the document will be denied.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src134" class="srcSentence">Now that the recipient has opened the attachment and optionally, forwarded it to somebody else, expect to get an email notification that reports this activity.</caps:sentence>
            <caps:sentence id="src135" class="srcSentence"> But email messages are easy to lose over time, so a better way to track who accessed your document is to use the document tracking site, which is covered in the final step.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src136" class="srcSentence">If you want more information</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src137" class="srcSentence">Additional information</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src138" class="srcSentence">Full instructions for viewing files that are protected by Azure Rights Management   →</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <externalLink>
                      <linkText>
                        <caps:sentence id="src139" class="srcSentence">View and use files that have been protected by Rights Management</caps:sentence>
                      </linkText>
                      <linkUri>https://technet.microsoft.com/library/dn574741.aspx</linkUri>
                    </externalLink>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src140" class="srcSentence">About the free subscription, RMS for individuals   →</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="2efcb440-fefd-45e9-872b-f471573aadf2">RMS for Individuals and Azure Rights Management</link>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src141" class="srcSentence">About the two versions of the file that you see attached to the email message   →</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <externalLink>
                      <linkText>
                        <caps:sentence id="src142" class="srcSentence">What’s the .ppdf file that’s automatically created?</caps:sentence>
                      </linkText>
                      <linkUri>https://technet.microsoft.com/library/dn574738.aspx</linkUri>
                    </externalLink>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src143" class="srcSentence">Step 5: Track your protected document</caps:sentence>
        </title>
        <content>
          <para>
            <mediaLinkInline>
              <image xlink:href="3d1ce494-490f-4493-8158-523ecda40fae"></image>
            </mediaLinkInline>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src144" class="srcSentence">For this step, you must have a subscription that supports document tracking.</caps:sentence>
              <caps:sentence id="src145" class="srcSentence"> To check whether your subscription includes document tracking, see <externalLink><linkText>Comparison of Rights Management Services (RMS) Offerings</linkText><linkUri>https://technet.microsoft.com/dn858608.aspx</linkUri></externalLink>.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence id="src146" class="srcSentence">This step is optional, but most people like to know if the attachment they sent to people has been opened, when, and even from where.</caps:sentence>
            <caps:sentence id="src147" class="srcSentence"> For example:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src148" class="srcSentence">You’re expecting a response from somebody by a specified time and you can see from the document tracking site that she hasn’t opened the document even though the deadline is approaching.</caps:sentence>
                <caps:sentence id="src149" class="srcSentence"> You send her a follow-up email or telephone her as a timely reminder.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src150" class="srcSentence">After seeing that somebody has opened the document, you follow up to ask her if she has any questions or requires additional information.</caps:sentence>
              </para>
            </listItem>
          </list>
          <mediaLink>
            <image xlink:href="5b799166-171f-45dc-91b8-3f4c3c2992a8"></image>
          </mediaLink>
          <procedure>
            <title>
              <caps:sentence id="src151" class="srcSentence">To track your protected document</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src152" class="srcSentence">Using Outlook, on the <ui>Home</ui> tab, in the <ui>RMS</ui> group, click <ui>Track Usage</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src153" class="srcSentence">If you see the <ui>Protect and share on your terms</ui> page, click <ui>Sign in</ui> and supply your user name and password again.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src154" class="srcSentence">On the <ui>Your shared documents</ui> page, you’ll see the document that you attached to the email, <system>Confidential.docx</system>.</caps:sentence>
                    <caps:sentence id="src155" class="srcSentence"> At this point, it’s the only file displayed but as you share additional protected documents, the list will grow.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src156" class="srcSentence">From this page, you’ll see when you shared the document (when you sent the email with the protected attachment), the date of the last activity, and the name of the recipient you sent the email to.</caps:sentence>
                    <caps:sentence id="src157" class="srcSentence"> Click the document name for additional details.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src158" class="srcSentence">On the new page, which has the name of the file that you clicked, you’ll see summary details for that document only, and a list of other options that are available for the document (<ui>List</ui>, <ui>Timeline</ui>, <ui>Map</ui>, <ui>Settings</ui>).</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src159" class="srcSentence">Click each option to explore different ways to track your protected document.</caps:sentence>
                    <caps:sentence id="src160" class="srcSentence"> Or, still on the <ui>Summary</ui> page, click <ui>Open in Excel</ui> to export the information to a spreadsheet, or click <ui>Revoke access</ui> to stop sharing the document.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence id="src161" class="srcSentence">You can return to this site to track further activity for your protected document, or revoke access if necessary.</caps:sentence>
                  <caps:sentence id="src162" class="srcSentence"> You can even access the site from your mobile device or tablet, by using a browser with this link: <externalLink><linkText>document tracking</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=529562</linkUri></externalLink></caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src163" class="srcSentence">If you want more information</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src164" class="srcSentence">Additional information</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src165" class="srcSentence">Full instructions for tracking your documents   →</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <externalLink>
                      <linkText>
                        <caps:sentence id="src166" class="srcSentence">Track and revoke your documents when you use the RMS sharing application</caps:sentence>
                      </linkText>
                      <linkUri>https://technet.microsoft.com/library/dn986611.aspx</linkUri>
                    </externalLink>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src167" class="srcSentence">Two minute video that explains and shows document tracking   →</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <externalLink>
                      <linkText>
                        <caps:sentence id="src168" class="srcSentence">Azure RMS Document Tracking and Revocation</caps:sentence>
                      </linkText>
                      <linkUri>http://channel9.msdn.com/Series/Information-Protection/Azure-RMS-Document-Tracking-and-Revocation</linkUri>
                    </externalLink>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src169" class="srcSentence">For troubleshooting and customer questions   →</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <externalLink>
                      <linkText>
                        <caps:sentence id="src170" class="srcSentence">FAQ for Document Tracking</caps:sentence>
                      </linkText>
                      <linkUri>https://technet.microsoft.com/dn947488</linkUri>
                    </externalLink>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src171" class="srcSentence">Next Steps</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src172" class="srcSentence">This tutorial stepped you through just one scenario for how Azure RMS can help protect your data.</caps:sentence>
            <caps:sentence id="src173" class="srcSentence"> To see other common uses, see the <externalLink><linkText>Azure RMS in action</linkText><linkUri>https://technet.microsoft.com/library/jj585026.aspx#BKMK_RMSpictures</linkUri></externalLink> section from the <link xlink:href="aeeebcd7-6646-4405-addf-ee1cc74df5df">What is Azure Rights Management?</link> article.</caps:sentence>
            <caps:sentence id="src174" class="srcSentence"> There are other sections in this article that you might also find useful, such as how Azure RMS works and what business problems it can solve.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src175" class="srcSentence">If you’re ready to start deploying Azure RMS, use the <link xlink:href="086600c2-c5d8-47ec-a4c0-c782e1797486">Azure Rights Management Deployment Roadmap</link> for your deployment steps and links for how-to instructions.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="5214667c-ec69-42ca-8bbf-8cb22da8c62e">Getting Started with Azure Rights Management</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>