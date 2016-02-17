---
title: C&#243;mo son compatibles las aplicaciones con Azure Rights Management
ms.custom: na
ms.reviewer: na
ms.service: rights-management
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2cdc7bde-4044-4021-b887-11476f99afd9
---
# C&#243;mo son compatibles las aplicaciones con Azure Rights Management
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="es-ES">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="2bcc2de8ce59618404fc0df9369171a5" id="tgt1" class="tgtSentence">Use la información siguiente para tratar de comprender cómo las aplicaciones de usuario final (como las aplicaciones de Office, Word, Excel, PowerPoint y Outlook) y los servicios (como Exchange y SharePoint) pueden utilizar Microsoft <token>aad_rightsmanagement_1</token> con la idea de proteger los datos de su organización:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <link xlink:href="2cdc7bde-4044-4021-b887-11476f99afd9#BKMK_SharingAppIntro">RMS sharing application for Windows and mobile platforms</link>
            </para>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="2cdc7bde-4044-4021-b887-11476f99afd9#BKMK_OfficeAppsIntro">Office applications: Word, Excel, PowerPoint, Outlook</link>
            </para>
            <list class="bullet">
              <listItem>
                <para>
                  <link xlink:href="2cdc7bde-4044-4021-b887-11476f99afd9#BKMK_ExchangeIntro">Exchange Online and Exchange Server</link>
                </para>
              </listItem>
              <listItem>
                <para>
                  <link xlink:href="2cdc7bde-4044-4021-b887-11476f99afd9#BKMK_SharePointIntro">SharePoint Online and SharePoint Server</link>
                </para>
              </listItem>
            </list>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="2cdc7bde-4044-4021-b887-11476f99afd9#BKMK_FCIIntro">File servers that run Windows Server and use File Classification Infrastructure (FCI)</link>
            </para>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="2cdc7bde-4044-4021-b887-11476f99afd9#BKMK_APIAppsIntro">Other applications that support the RMS APIs</link>
            </para>
          </listItem>
        </list>
        <alert class="note">
          <para>
            <caps:sentence sentenceid="8c9f46310166e027b352ce0c3c2c573b" id="tgt2" class="tgtSentence">Para comprobar las aplicaciones y versiones que son compatibles con <token>aad_rightsmanagement_1</token> (Azure RMS), consulte <link xlink:href="dc78321d-d759-4653-8818-80da74b6cdeb">Requirements for Azure Rights Management</link>.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence sentenceid="a939cf5b90f330679b74eda704a74a2a" id="tgt3" class="tgtSentence">En algunos casos, la protección de la información se aplica de manera automática, según lo previsto en las directivas que tú mismo configuras.</caps:sentence>
          <caps:sentence sentenceid="d9f9cc689fc84f4139db76ae8c620182" id="tgt4" class="tgtSentence"> Por ejemplo, este es el caso con bibliotecas de SharePoint, archivos clasificados y reglas de transporte de Exchange.</caps:sentence>
          <caps:sentence sentenceid="7d505a1b797eb9004a5090d00fc4d235" id="tgt5" class="tgtSentence"> En otros casos, los usuarios deben aplicar ellos mismos la protección de la información desde sus aplicaciones, ya sea seleccionando una plantilla o unas opciones específicas.</caps:sentence>
          <caps:sentence sentenceid="cf5389cd798d49b035f49af4b3a61fd6" id="tgt6" class="tgtSentence"> Por ejemplo, este es el caso cuando los usuarios comparten un archivo por correo electrónico, o protegen un archivo in situ restringiendo el acceso o el uso a usuarios seleccionados o a usuarios externos a la organización.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="2069038249ee40a1074eac95aba018e1" id="tgt7" class="tgtSentence">Las plantillas facilitan a los usuarios (y a los administradores que configuran las directivas) la aplicación del nivel de protección adecuado y restringen el acceso a personas de dentro de la organización.</caps:sentence>
          <caps:sentence sentenceid="e0cac67edb86895c0e8c22171a698617" id="tgt8" class="tgtSentence"> Aunque <token>aad_rightsmanagement_1</token> viene con dos plantillas predeterminadas, es probable que quiera crear plantillas personalizadas para reducir las veces que se tienen que especificar opciones individuales.</caps:sentence>
          <caps:sentence sentenceid="8c4d3ab3c104606371f8a7abab8d11d7" id="tgt9" class="tgtSentence"> Para obtener más información, vea <link xlink:href="1775d8d0-9a59-42c8-914f-ce285b71ac1c">Configuring Custom Templates for Azure Rights Management</link>.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="c62e29cade752dd82a469ce01f55d682" id="tgt10" class="tgtSentence">Para los casos en que los usuarios deban aplicar ellos mismos la protección de información, asegúrate de proporcionarles las instrucciones y las directrices sobre cómo y cuándo deben hacerlo.</caps:sentence>
          <caps:sentence sentenceid="a96dc4e5fc951bc693affb056185d9dc" id="tgt11" class="tgtSentence"> Las instrucciones deberían ser específicas para la aplicación y las versiones que usan y sobre cómo usarlas, y las directrices sobre cuándo y cómo es apropiado para tu negocio aplicar la protección de información.</caps:sentence>
          <caps:sentence sentenceid="6d4b28b3d093b0bd0346992db18b13f2" id="tgt12" class="tgtSentence"> Para obtener más información, vea <link xlink:href="58f9a6ff-4121-4c8c-9865-1bb290604ad2">Instruct Users How to Protect Files by using Azure Rights Management</link>.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="1babb5e8bf37a458e910863a3f2e1b08" id="tgt13" class="tgtSentence">Para obtener información sobre cómo configurar estas aplicaciones para Azure RMS, consulte <link xlink:href="ea09cbc5-b98b-444e-8b60-5bc3cb199c36">Configuring Applications for Azure Rights Management</link>.</caps:sentence>
        </para>
        <alert class="tip">
          <para>
            <caps:sentence sentenceid="479ed5748c3958da3329d24af42f647d" id="tgt14" class="tgtSentence">Para consultar ejemplos y capturas de pantalla de aplicaciones que usan Azure RMS, consulte la sección <link xlink:href="aeeebcd7-6646-4405-addf-ee1cc74df5df#BKMK_RMSpictures">Azure RMS in action: What administrators and users see</link> del tema <link xlink:href="aeeebcd7-6646-4405-addf-ee1cc74df5df">What is Azure Rights Management?</link>.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <section address="BKMK_SharingAppIntro">
        <title>
          <caps:sentence sentenceid="8fd6704f8167322156faf50718f02152" id="tgt15" class="tgtSentence">Aplicación de uso compartido RMS para Windows y plataformas móviles</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="fd0b72a29488e67ffcbcf27f2ef04deb" id="tgt16" class="tgtSentence">La aplicación de uso compartido RMS es una aplicación gratuita y descargable que es necesaria para admitir Office 2010, pero también se recomienda para equipos con Windows, equipos con Mac y dispositivos móviles.</caps:sentence>
            <caps:sentence sentenceid="4781b992747afea8287ee484f6966a54" id="tgt17" class="tgtSentence"> Una de sus ventajas es que puede aplicar protección genérica para aplicaciones y archivos que no admiten <token>aad_rightsmanagement_2</token> de forma nativa, lo que significa que se pueden proteger todos los archivos.</caps:sentence>
            <caps:sentence sentenceid="3d35b34f7ad6573b10ba8fa067d107c7" id="tgt18" class="tgtSentence"> Para obtener más información acerca de los diferentes niveles de protección, consulte la sección <externalLink><linkText>Niveles de protección: nativo y genérico</linkText><linkUri>http://technet.microsoft.com/library/dn339003.aspx#BKMK_LevelsofProtection</linkUri></externalLink> en la <externalLink><linkText>Guía del administrador de la aplicación de uso compartido de Rights Management</linkText><linkUri>http://technet.microsoft.com/library/dn339003.aspx</linkUri></externalLink>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="6aa90e52909c533510b6821027685f23" id="tgt19" class="tgtSentence">Cuando los usuarios protegen sus archivos mediante la aplicación de uso compartido de RMS, también pueden realizar el seguimiento de los documentos que han protegido y, si es necesario, revocar el acceso a ellos.</caps:sentence>
            <caps:sentence sentenceid="49b99554838ce1c5318171be9db4a381" id="tgt20" class="tgtSentence"> Para ello, pueden utilizar el <externalLink><linkText>sitio de seguimiento de documentos</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=529562</linkUri></externalLink>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="4e0eeffbbcafe9cf44bca0caa805ecd7" id="tgt21" class="tgtSentence">Para ordenadores con Windows, la aplicación de uso compartido RMS se integra de forma discreta con las aplicaciones que los usuarios ya usan y las mejora: </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="0be37b6164a02efa383d5b8763fb562f" id="tgt22" class="tgtSentence">Se instala un completo de Office para Word, Excel, PowerPoint y Outlook.</caps:sentence>
                <caps:sentence sentenceid="cb17f7f9ce80920af64245cb755055ed" id="tgt23" class="tgtSentence"> De este modo, los usuarios disponen del botón <ui>Compartir protegido</ui> en la cinta de opciones, que abre un sencillo cuadro de diálogo de configuración que se usa normalmente para proteger archivos que se enviarán por correo electrónico.</caps:sentence>
                <caps:sentence sentenceid="9c466cfa6fd5a1edc29094431b2d93cb" id="tgt24" class="tgtSentence"> Este botón también proporciona una forma rápida de obtener acceso al sitio de seguimiento de documentos.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="1ecc769afb277fabf142f7c0ecc4352b" id="tgt25" class="tgtSentence">Una nueva opción con un clic en el botón secundario para el Explorador de archivos.</caps:sentence>
                <caps:sentence sentenceid="eab799640fa67fe22a62e5d8b2d1fb87" id="tgt26" class="tgtSentence"> De este modo, los usuarios disponen de la opción <ui>Proteger en contexto</ui>, que abre un sencillo cuadro de diálogo de configuración que se usa normalmente para proteger archivos almacenados en un disco.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="9e25d2cfbf4e233f2e8f7aab5a9b1db4" id="tgt27" class="tgtSentence">Un visor para abrir archivos que se hayan protegido con <token>aad_rightsmanagement_2</token>.</caps:sentence>
                <caps:sentence sentenceid="45e20352474135fd480a5176e747dc67" id="tgt28" class="tgtSentence"> Este visor de invoca automáticamente cuando no hay otra aplicación instalada que pueda abrir el archivo protegido.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="6cfc5a40613976d89295f1aabd040c28" id="tgt29" class="tgtSentence">Configuración de back-end para Office 2010 que permite que Word, Excel, PowerPoint y Outlook funcionen sin problemas con <token>aad_rightsmanagement_1</token>.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="217c4536042de77eb64a6fabbffe624e" id="tgt30" class="tgtSentence">Aunque la aplicación para uso compartido de RMS para Windows puede descargarse e instalarse en un solo equipo desde la <externalLink><linkText>página de Microsoft Rights Management</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=303970</linkUri></externalLink>, también admite una implementación empresarial para la instalación silenciosa y la configuración personalizada.</caps:sentence>
            <caps:sentence sentenceid="d3d094e25e7ac14a4098802b5757e141" id="tgt31" class="tgtSentence"> Para obtener más información, vea los recursos siguientes:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <externalLink>
                  <linkText>
                    <caps:sentence sentenceid="45fd73cece8c888a3560a65a749417d4" id="tgt32" class="tgtSentence">Guía de administrador de la aplicación de uso compartido Rights Management</caps:sentence>
                  </linkText>
                  <linkUri>http://technet.microsoft.com/library/dn339003.aspx</linkUri>
                </externalLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <externalLink>
                  <linkText>
                    <caps:sentence sentenceid="5a82d1d6328fcf4e332c7353808716e6" id="tgt33" class="tgtSentence">Guía de usuario de la aplicación de uso compartido Rights Management</caps:sentence>
                  </linkText>
                  <linkUri>http://technet.microsoft.com/library/dn339006.aspx</linkUri>
                </externalLink>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="376f96fbe49dacb622794e28acf9f6f0" id="tgt34" class="tgtSentence">La aplicación de uso compartido RMS para dispositivos móviles admite los dispositivos móviles más usados, como iPad e iPhone, Android, Windows Phone y Windows RT.</caps:sentence>
            <caps:sentence sentenceid="b3fbb20184c6d3871728fbe36ba36cad" id="tgt35" class="tgtSentence"> Los usuarios pueden descargar esta aplicación desde la tienda pertinente, y se pueden encontrar enlaces a estas desde la <externalLink><linkText>página de Rights Management de Microsoft</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=303970</linkUri></externalLink>.</caps:sentence>
          </para>
        </content>
      </section>
      <section address="BKMK_OfficeAppsIntro">
        <title>
          <caps:sentence sentenceid="c34ae920feec696b27cfd3b100ae6a72" id="tgt36" class="tgtSentence">Aplicaciones de Office: Word, Excel, PowerPoint, Outlook</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="cfc201439612ce748c1ec3f1f3d86dd5" id="tgt37" class="tgtSentence">Estas aplicaciones admiten de forma nativa Rights Management mediante Information Rights Management (IRM) y permiten a los usuarios aplicar protección a un documento guardado o a un mensaje de correo electrónico que se enviará.</caps:sentence>
            <caps:sentence sentenceid="1718a8c16ac552e71ccbb9eec5b54f3f" id="tgt38" class="tgtSentence"> Los usuarios pueden aplicar plantillas o elegir configuraciones muy personalizadas para restricciones de acceso, derechos y uso.</caps:sentence>
            <caps:sentence sentenceid="9b8e7d0f7d0935ea5a46a19be7710ebd" id="tgt39" class="tgtSentence"> Por ejemplo, los usuarios pueden configurar un archivo para que solamente pueda acceder a él gente de tu organización, o controlar si se puede editar el archivo o si se restringe a solo lectura, o si se impide que se pueda imprimir.</caps:sentence>
            <caps:sentence sentenceid="dc28da06aa5a2671b8f829e3ed76f54f" id="tgt40" class="tgtSentence"> Para archivos sujetos a limitación temporal, se puede configurar una fecha de caducidad (directamente por parte de los usuarios o aplicando una plantilla) en la que ya no se podrá acceder al archivo.</caps:sentence>
            <caps:sentence sentenceid="0d8cdb3d65f2ba67d56b3353092a1534" id="tgt41" class="tgtSentence"> Para Outlook, los usuarios también pueden elegir la opción <ui>No reenviar</ui> con el fin de evitar la fuga de datos.</caps:sentence>
          </para>
        </content>
        <sections>
          <section address="BKMK_ExchangeIntro">
            <title>
              <caps:sentence sentenceid="67f7404f1323c5a892421c8c12d68e94" id="tgt42" class="tgtSentence">Exchange Online y Exchange Server</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="2ea4c69dac443e59bc9ae5b0f170eefe" id="tgt43" class="tgtSentence">Cuando usas Exchange Online o Exchange Server, puedes utilizar la integración de Information Rights Management (IRM), que proporciona más soluciones de protección de la información:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="f33a3b9b98aadda6025a701d32090df1" id="tgt44" class="tgtSentence">
                      <legacyBold>Exchange ActiveSync IRM</legacyBold> para que los dispositivos móviles puedan proteger y consumir mensajes de correo electrónico protegidos.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="a4686c6b248df30022830ea65c0020b6" id="tgt45" class="tgtSentence">Compatibilidad de RMS con <legacyBold>Outlook Web App</legacyBold>, que se implementa de forma similar al cliente de Outlook, para que los usuarios puedan proteger mensajes de correo electrónico mediante plantillas o especificando opciones individuales. Y los usuarios pueden leer y usar los mensajes de correo electrónico protegidos que se les hayan enviado.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="c54417980f511632a46dda8dc5eb5bc0" id="tgt46" class="tgtSentence">
                      <legacyBold>Reglas de protección</legacyBold> para clientes de Outlook que un administrador configura para aplicar automáticamente plantillas RMS a mensajes de correo electrónico para destinatarios concretos.</caps:sentence>
                    <caps:sentence sentenceid="a255ba072deb5d2699736fd0910bcbe3" id="tgt47" class="tgtSentence"> Por ejemplo, cuando se envían correos electrónicos internos a tu departamento legal, solo los miembros del departamento legal pueden leerlos y no se pueden reenviar.</caps:sentence>
                    <caps:sentence sentenceid="84ba63ce5a27d7348e4a2798bd41f483" id="tgt48" class="tgtSentence"> Los usuarios consultan la protección que se aplicará al mensaje de correo electrónico antes de enviarlo y, de forma predeterminada, pueden quitarla si deciden que no es necesaria.</caps:sentence>
                    <caps:sentence sentenceid="823755670240569244e044ad2505f966" id="tgt49" class="tgtSentence"> Los correos electrónicos se cifran antes de enviarlos.</caps:sentence>
                    <caps:sentence sentenceid="cee670589668f40a9677b9906b7dc8e1" id="tgt50" class="tgtSentence"> Para obtener más información, consulte <externalLink><linkText>Reglas de protección de Outlook</linkText><linkUri>http://technet.microsoft.com/library/dd638178(v=exchg.150).aspx</linkUri></externalLink> y <externalLink><linkText>Crear una regla de protección de Outlook</linkText><linkUri>http://technet.microsoft.com/library/dd638196(v=exchg.150).aspx</linkUri></externalLink> en la biblioteca de Exchange.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="14d907c7af830c95f099bb4fcf9fb24d" id="tgt51" class="tgtSentence">
                      <legacyBold>Reglas de transporte</legacyBold> que un administrador configura para aplicar automáticamente plantillas de RMS a mensajes de correo electrónico en función de propiedades como el remitente, el destinatario, el asunto del mensaje y el contenido.</caps:sentence>
                    <caps:sentence sentenceid="dcb4186ec20acb80780e40dce7156053" id="tgt52" class="tgtSentence"> Dichas reglas son similares en concepto a las reglas de protección, pero no permiten a los usuarios quitar la protección. Se pueden aplicar a Outlook Web Access y a correos electrónicos enviados mediante dispositivos móviles, y no cifra mensajes de correo electrónico antes de que el cliente los envíe.</caps:sentence>
                    <caps:sentence sentenceid="d3852a14f2f8f05e57524c2924aa71bf" id="tgt53" class="tgtSentence"> Para obtener más información, consulte <externalLink><linkText>Crear una regla de protección de transporte</linkText><linkUri>http://technet.microsoft.com/library/dd302432.aspx</linkUri></externalLink> en la biblioteca de Exchange.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="cf9485118fecb38d3fede142dc6d13ef" id="tgt54" class="tgtSentence">
                      <legacyBold>Directivas de prevención de la pérdida de datos (DLP)</legacyBold> que contienen conjuntos de condiciones para filtrar mensajes de correo electrónico y tomar medidas para tratar de evitar la pérdida de contenido confidencial (por ejemplo, información personal o de tarjetas de crédito).</caps:sentence>
                    <caps:sentence sentenceid="da85c29db1f099c0e441560b7d91e8ae" id="tgt55" class="tgtSentence"> Las sugerencias de las directivas se pueden usar cuando se detectan datos sensibles, para alertar a los usuarios de que es posible que sea necesario aplicar protección de la información, en función de la información del mensaje de correo electrónico.</caps:sentence>
                    <caps:sentence sentenceid="8f43d296537db8c47b0ef0be7eca51ad" id="tgt56" class="tgtSentence"> Para obtener más información, consulte <externalLink><linkText>Prevención de pérdida de datos</linkText><linkUri>http://technet.microsoft.com/library/jj150527(v=exchg.150).aspx</linkUri></externalLink> en la biblioteca de Exchange.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="594b90fa9387906baa0ee3e5a1bd45c4" id="tgt57" class="tgtSentence">
                      <legacyBold>Cifrado de mensajes de Office 365</legacyBold> que usa reglas de transporte para enviar correos electrónicos cifrados a personas que están fuera de su compañía y que leen el correo en un explorador con una interfaz similar a la de Outlook Web App.</caps:sentence>
                    <caps:sentence sentenceid="8d4a2008bddc59432f7148a63be55a69" id="tgt58" class="tgtSentence"> Puedes personalizar el texto de aviso y el texto de cabecera en los correos electrónicos cifrados de tu compañía e, incluso, agregar el logotipo de la compañía.</caps:sentence>
                    <caps:sentence sentenceid="561b2ed14f7bee4ed84915783640ec5d" id="tgt59" class="tgtSentence"> Para obtener más información, consulte <externalLink><linkText>Cifrado de mensajes de Office 365</linkText><linkUri>http://office.microsoft.com/o365-message-encryption-FX104179182.aspx</linkUri></externalLink> en el sitio web de Office.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="1ff587366417803d247d0427204f8122" id="tgt60" class="tgtSentence">Si usa Exchange Server, puede utilizar las características de protección de la información con <token>aad_rightsmanagement_1</token> si implementa el conector RMS, que actúa como un transmisor entre sus servidores locales y el servicio en la nube de RMS.</caps:sentence>
                <caps:sentence sentenceid="cf0ed32eae86ca30fb9c194696705fa8" id="tgt61" class="tgtSentence"> Para obtener más información, vea <link xlink:href="90e7e33f-9ecc-497b-89c5-09205ffc5066">Deploying the Azure Rights Management Connector</link>.</caps:sentence>
              </para>
            </content>
          </section>
          <section address="BKMK_SharePointIntro">
            <title>
              <caps:sentence sentenceid="8e0cd9ed0afa0870825b16ce70a4dd8f" id="tgt62" class="tgtSentence">SharePoint Online y SharePoint Server</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="11306bf874b80c12c3247fd908151ca7" id="tgt63" class="tgtSentence">Cuando usas SharePoint Online y SharePoint Server, puedes utilizar la integración Information Rights Management (IRM), que permite a los administradores proteger listas o bibliotecas para que cuando un usuario consulte un documento, el archivo esté protegido para que solo personas autorizadas puedan verlo y usarlo según las directivas de protección de la información que hayas especificado.</caps:sentence>
                <caps:sentence sentenceid="87f2d68ebe63b9e14760ad4494a10db6" id="tgt64" class="tgtSentence"> Por ejemplo, el archivo podría ser de solo lectura, deshabilitar el copiado del texto, evitar que se guarde una copia local e impedir que se pueda imprimir.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="ac58e3868c93af0d71a146c5418eff47" id="tgt65" class="tgtSentence">Para listas y bibliotecas, la protección de la información siempre se aplica por un administrador, nunca por un usuario final.</caps:sentence>
                <caps:sentence sentenceid="75a917d19256af7f867dc3c5fb2400c2" id="tgt66" class="tgtSentence"> Y se aplica en el nivel de la lista o la biblioteca para todos los documentos de ese contenedor, en lugar de en archivos individuales.</caps:sentence>
                <caps:sentence sentenceid="56db1e6eb4802caa6d010e0430aa8f13" id="tgt67" class="tgtSentence">  Si utiliza SharePoint Online, los usuarios también pueden aplicar IRM a su biblioteca de OneDrive para la Empresa.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="e60a59662173d63f008158c393b35aac" id="tgt68" class="tgtSentence">En primer lugar, el servicio IRM se debe habilitar para SharePoint.</caps:sentence>
                <caps:sentence sentenceid="2159e92963440c41a292a010b9a5d489" id="tgt69" class="tgtSentence"> A continuación, especifique Information Rights Management para una biblioteca.</caps:sentence>
                <caps:sentence sentenceid="9c7370f94dd3022c3e2ee49721c41bf7" id="tgt70" class="tgtSentence"> En el caso de SharePoint Online y OneDrive para la Empresa, los usuarios pueden especificar también Information Rights Management para su biblioteca de OneDrive para la Empresa.</caps:sentence>
                <caps:sentence sentenceid="b7a1f410b77350f8d6137a88cfcad960" id="tgt71" class="tgtSentence"> SharePoint no usa plantillas de directiva de derechos, aunque hay valores de configuración de SharePoint que se pueden seleccionar que coinciden estrechamente con la configuración que se puede especificar en las plantillas.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="14433f57cdf8cefd01b5d3c2449e8404" id="tgt72" class="tgtSentence">Si usas SharePoint Server, puedes utilizar las funciones de protección de la información con <token>aad_rightsmanagement_1</token> implementando el conector RMS, que actúa como una retransmisión entre tus servidores locales y el servicio en la nube de RMS.</caps:sentence>
                <caps:sentence sentenceid="cf0ed32eae86ca30fb9c194696705fa8" id="tgt73" class="tgtSentence"> Para obtener más información, vea <link xlink:href="90e7e33f-9ecc-497b-89c5-09205ffc5066">Deploying the Azure Rights Management Connector</link>.</caps:sentence>
              </para>
              <alert class="note">
                <para>
                  <caps:sentence sentenceid="33c18a321ba13e1200c1d8c1ecb70c79" id="tgt74" class="tgtSentence">Actualmente, hay algunas limitaciones al utilizar IRM con SharePoint:</caps:sentence>
                </para>
                <list class="bullet">
                  <listItem>
                    <para>
                      <caps:sentence sentenceid="a7bf445eab0ac67103e642fc6b2133b0" id="tgt75" class="tgtSentence">No puede usar las plantillas predeterminadas o personalizadas que se administran en el Portal de Azure clásico.</caps:sentence>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <caps:sentence sentenceid="926b48b0499febb2d39fa4b63e5c3f8a" id="tgt76" class="tgtSentence">Los archivos que tienen una extensión de nombre de archivo .PPDF para archivos PDF protegidos no se admiten.</caps:sentence>
                      <caps:sentence sentenceid="781c671e997e3f4dc1db09aba8f48176" id="tgt77" class="tgtSentence"> Los archivos que tienen una extensión de nombre de archivo .PDF y que han sido protegidos forma nativa por RMS se admiten cuando se utiliza un lector PDF que admita RMS de forma nativa.</caps:sentence>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <caps:sentence sentenceid="1034024627fd79b72907a8bb0a8f0244" id="tgt78" class="tgtSentence"> Dado que Office en dispositivos móviles no admite aún RMS, estos dispositivos deben utilizar un explorador para ver los archivos que han sido protegidos con RMS, y los archivos son de solo lectura.</caps:sentence>
                    </para>
                  </listItem>
                </list>
              </alert>
              <para>
                <caps:sentence sentenceid="5b1283e08025c47323a453cb8a89ac41" id="tgt79" class="tgtSentence">Azure RMS aplica el uso de restricciones y cifrado de datos para documentos cuando se descargan de SharePoint y no cuando el documento se crea primero en SharePoint o se carga en la biblioteca.</caps:sentence>
                <caps:sentence sentenceid="1590d014c78e81ccd79cff5197366b62" id="tgt80" class="tgtSentence"> Para obtener información sobre cómo se protegen los documentos antes de descargarse, consulte <externalLink><linkText>Cifrado de datos en OneDrive para la Empresa y SharePoint Online</linkText><linkUri>https://technet.microsoft.com/library/dn905447.aspx</linkUri></externalLink> en la documentación de SharePoint.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="97e80bf6a341ee8d1a64e231ba1ed1d2" id="tgt81" class="tgtSentence">Para obtener más información acerca del uso de Azure RMS con SharePoint, vea la siguiente entrada del blog de Office: <externalLink><linkText>What’s New with Information Rights Management in SharePoint and SharePoint Online</linkText><linkUri>http://blogs.office.com/2012/11/09/whats-new-with-information-rights-management-in-sharepoint-and-sharepoint-online/</linkUri></externalLink> (Novedades de Information Rights Management en SharePoint y SharePoint Online)</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </section>
      <section address="BKMK_FCIIntro">
        <title>
          <caps:sentence sentenceid="cf4019b714b3ac39dcc146f936037bd6" id="tgt82" class="tgtSentence">Servidores de archivos que ejecutan Windows Server y usan Infraestructura de clasificación de archivos (FCI)</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="d908b46655c04cb2e35d69dd6488ceb4" id="tgt83" class="tgtSentence">Cuando configuras Windows Server para usar Infraestructura de clasificación de archivos, esta característica del administrador de recursos del servidor de archivos puede examinar archivos locales y determinar si contienen datos sensibles.</caps:sentence>
            <caps:sentence sentenceid="4961f30cb50d823b5d00f874631e9f6a" id="tgt84" class="tgtSentence"> Para archivos que cumplan este criterio, se etiquetan con propiedades de clasificación que define un administrador.</caps:sentence>
            <caps:sentence sentenceid="4aa3dcae3af9ff68edfd186b27b01fdb" id="tgt85" class="tgtSentence"> Entonces, la Infraestructura de clasificación de archivos puede tomar medidas, según lo estipulado en la clasificación.</caps:sentence>
            <caps:sentence sentenceid="21a272e8bb60ecf04904ced67dd08138" id="tgt86" class="tgtSentence"> Una de estas acciones es aplicar la protección de la información mediante <token>aad_rightsmanagement_1</token> y la implementación del conector Rights Management (también conocido como conector RMS).</caps:sentence>
            <caps:sentence sentenceid="a37daa5cd46e9ab0673d063ae2a407a8" id="tgt87" class="tgtSentence"> Los archivos de Office se protegen así automáticamente con Azure RMS.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="533800c07abaf868092c675560d105ed" id="tgt88" class="tgtSentence">Para proteger todos los tipos de archivo, no utilice el conector RMS sino que, en su lugar, ejecute un script de Windows PowerShell, usando cmdlets de la <externalLink><linkText>herramienta de protección de RMS</linkText><linkUri>https://www.microsoft.com/en-us/download/details.aspx?id=47256</linkUri></externalLink>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="e0588fb42cce3108a9e33302579446b5" id="tgt89" class="tgtSentence">Las directivas de clasificación se pueden configurar completamente y son enormemente ampliables para que puedas prevenir la pérdida potencial de datos de usuarios autorizados y no autorizados.</caps:sentence>
            <caps:sentence sentenceid="f58ed9a22eda60004e56bd62c86d3cce" id="tgt90" class="tgtSentence"> Incluso pueden ayudar a reducir el riesgo de que los administradores de la red pierdan datos, ya que se pueden configurar directivas que no requieran que dichos administradores tengan acceso a los archivos.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="51e85c8999e9b6b6bea2ca83080c4493" id="tgt91" class="tgtSentence">Para obtener instrucciones acerca de la instalación y configuración del conector de RMS para archivos de Office, consulte <link xlink:href="90e7e33f-9ecc-497b-89c5-09205ffc5066">Deploying the Azure Rights Management Connector</link>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="3f2c7e6de0f49d0be85c5c8b52d1571a" id="tgt92" class="tgtSentence">Para obtener instrucciones acerca del uso del de Windows PowerShell para todos los tipos de archivo, consulte <link xlink:href="9aa693db-9727-4284-9f64-867681e114c9">RMS Protection with Windows Server File Classification Infrastructure (FCI)</link>.</caps:sentence>
          </para>
        </content>
      </section>
      <section address="BKMK_APIAppsIntro">
        <title>
          <caps:sentence sentenceid="b8c31eeb7e365689f25cc0defcdab212" id="tgt93" class="tgtSentence">Otras aplicaciones compatibles con las API de RMS</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="dc20573b78c8144bfc406ce243d9698c" id="tgt94" class="tgtSentence">Con RMS SDK, sus desarrolladores internos pueden escribir aplicaciones de línea de negocio que admitan <token>aad_rightsmanagement_1</token> de forma nativa.</caps:sentence>
            <caps:sentence sentenceid="946270a3df45ea8b1523cac3309d9c66" id="tgt95" class="tgtSentence"> Cómo se integre la protección de la información con estas aplicaciones depende del modo en que estén escritas.</caps:sentence>
            <caps:sentence sentenceid="855aa387257d2b17f6c702a660d64fe6" id="tgt96" class="tgtSentence"> Por ejemplo, la integración se podría aplicar automáticamente con un requisito mínimo de interacción del usuario o, para una experiencia más personalizada, los usuarios podrían recibir un aviso para configurar los valores a fin de aplicar la protección de la información a los archivos.</caps:sentence>
            <caps:sentence sentenceid="36301f1ecba89db1daec34624650d341" id="tgt97" class="tgtSentence"> Para obtener más información sobre el SDK, consulte <externalLink><linkText>Microsoft Rights Management SDK</linkText><linkUri>http://msdn.microsoft.com/library/hh552972(v=vs.85).aspx</linkUri></externalLink>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="162976d03051109b1fa902eb1235c8d3" id="tgt98" class="tgtSentence">De forma parecida, muchos proveedores de software suministran aplicaciones que ofrecen soluciones para la protección de la información, también conocidos como productos de Enterprise Rights Management (ERM).</caps:sentence>
            <caps:sentence sentenceid="6ec697a9b179de9b59c8eaafda2e902b" id="tgt99" class="tgtSentence"> Un ejemplo habitual es un lector de PDF que admita <token>aad_rightsmanagement_2</token> para plataformas concretas.</caps:sentence>
            <caps:sentence sentenceid="2c8ce62067418eb76953a428754b558f" id="tgt100" class="tgtSentence"> Puede usar la tabla en la sección <link xlink:href="dc78321d-d759-4653-8818-80da74b6cdeb#BKMK_ClientCapabilities">Client device capabilities</link> del tema <link xlink:href="dc78321d-d759-4653-8818-80da74b6cdeb">Requirements for Azure Rights Management</link> para identificar las aplicaciones que son compatibles con RMS (aplicaciones preparadas para RMS) y, a continuación, realizar una búsqueda web para adquirir o descargar la aplicación.</caps:sentence>
          </para>
          <alert class="tip">
            <para>
              <caps:sentence sentenceid="8ae7d2fdec419843a7af394110e5f459" id="tgt101" class="tgtSentence">Para estar al tanto de las aplicaciones publicadas recientemente, consulte los canales de la comunidad de RMS, que se enumeran en <link xlink:href="7cc73d92-27d6-49ff-a8ab-2fae73519b4b">Information and Support for Azure Rights Management</link>.</caps:sentence>
            </para>
          </alert>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="5214667c-ec69-42ca-8bbf-8cb22da8c62e">Getting started with Azure Rights Management</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Use the following information to help you understand how your end-user applications (such as the Office applications, Word, Excel, PowerPoint, and Outlook) and services (such as Exchange and SharePoint) can use Microsoft <token>aad_rightsmanagement_1</token> to help protect your organization’s data:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <link xlink:href="2cdc7bde-4044-4021-b887-11476f99afd9#BKMK_SharingAppIntro">RMS sharing application for Windows and mobile platforms</link>
            </para>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="2cdc7bde-4044-4021-b887-11476f99afd9#BKMK_OfficeAppsIntro">Office applications: Word, Excel, PowerPoint, Outlook</link>
            </para>
            <list class="bullet">
              <listItem>
                <para>
                  <link xlink:href="2cdc7bde-4044-4021-b887-11476f99afd9#BKMK_ExchangeIntro">Exchange Online and Exchange Server</link>
                </para>
              </listItem>
              <listItem>
                <para>
                  <link xlink:href="2cdc7bde-4044-4021-b887-11476f99afd9#BKMK_SharePointIntro">SharePoint Online and SharePoint Server</link>
                </para>
              </listItem>
            </list>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="2cdc7bde-4044-4021-b887-11476f99afd9#BKMK_FCIIntro">File servers that run Windows Server and use File Classification Infrastructure (FCI)</link>
            </para>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="2cdc7bde-4044-4021-b887-11476f99afd9#BKMK_APIAppsIntro">Other applications that support the RMS APIs</link>
            </para>
          </listItem>
        </list>
        <alert class="note">
          <para>
            <caps:sentence id="src2" class="srcSentence">To verify the applications and versions that <token>aad_rightsmanagement_1</token> (Azure RMS) supports, see <link xlink:href="dc78321d-d759-4653-8818-80da74b6cdeb">Requirements for Azure Rights Management</link>.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence id="src3" class="srcSentence">In some cases, information protection is automatically applied, according to policies that you configure.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> For example, this is the case with SharePoint libraries, classified files, and Exchange transport rules.</caps:sentence>
          <caps:sentence id="src5" class="srcSentence"> In other cases, users must apply information protection themselves from their applications, either by selecting a template or by selecting specific options.</caps:sentence>
          <caps:sentence id="src6" class="srcSentence"> For example, this is the case when users share a file by email, or protect a file in-place by restricting access or usage to selected users or to users outside the organization.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src7" class="srcSentence">Templates make it easier for users (and administrators who configure policies) to apply the correct level of protection and restrict access to people inside your organization.</caps:sentence>
          <caps:sentence id="src8" class="srcSentence"> Although <token>aad_rightsmanagement_1</token> comes with two default templates, you will probably want to create custom templates to reduce the times when they have to specify individual options.</caps:sentence>
          <caps:sentence id="src9" class="srcSentence"> For more information, see <link xlink:href="1775d8d0-9a59-42c8-914f-ce285b71ac1c">Configuring Custom Templates for Azure Rights Management</link>.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src10" class="srcSentence">For the cases where users must apply information protection themselves, be sure to provide them with instructions and guidance how and when to do this.</caps:sentence>
          <caps:sentence id="src11" class="srcSentence"> The instructions should be specific for the application and versions that they use and how they use them, and the guidance for when and how to apply information protection should be appropriate for your business.</caps:sentence>
          <caps:sentence id="src12" class="srcSentence"> For more information, see <link xlink:href="58f9a6ff-4121-4c8c-9865-1bb290604ad2">Instruct Users How to Protect Files by using Azure Rights Management</link>.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src13" class="srcSentence">For information about how to configure these applications for Azure RMS, see <link xlink:href="ea09cbc5-b98b-444e-8b60-5bc3cb199c36">Configuring Applications for Azure Rights Management</link>.</caps:sentence>
        </para>
        <alert class="tip">
          <para>
            <caps:sentence id="src14" class="srcSentence">For examples and screenshots of applications using Azure RMS, see the <link xlink:href="aeeebcd7-6646-4405-addf-ee1cc74df5df#BKMK_RMSpictures">Azure RMS in action: What administrators and users see</link> section from the <link xlink:href="aeeebcd7-6646-4405-addf-ee1cc74df5df">What is Azure Rights Management?</link> topic.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <section address="BKMK_SharingAppIntro">
        <title>
          <caps:sentence id="src15" class="srcSentence">RMS sharing application for Windows and mobile platforms</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src16" class="srcSentence">The RMS sharing application is a free, downloadable application that is required to support Office 2010, but also recommended for Windows computers, Mac computers, and mobile devices.</caps:sentence>
            <caps:sentence id="src17" class="srcSentence"> One of its benefits is that it can apply generic protection for applications and files that do not natively support <token>aad_rightsmanagement_2</token>, which means that all files can be protected.</caps:sentence>
            <caps:sentence id="src18" class="srcSentence"> For more information about the different protection levels, see the <externalLink><linkText>Level of protection – native and generic</linkText><linkUri>http://technet.microsoft.com/library/dn339003.aspx#BKMK_LevelsofProtection</linkUri></externalLink> section from the <externalLink><linkText>Rights Management sharing application administrator guide</linkText><linkUri>http://technet.microsoft.com/library/dn339003.aspx</linkUri></externalLink>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src19" class="srcSentence">When users protect their files by using the RMS sharing application, they can also track the documents that they protected, and if necessary, revoke access to them.</caps:sentence>
            <caps:sentence id="src20" class="srcSentence"> They do this by using the <externalLink><linkText>document tracking site</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=529562</linkUri></externalLink>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src21" class="srcSentence">For Windows computers, the RMS sharing application unobtrusively integrates with and enhances the  applications that users already use: </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src22" class="srcSentence">An Office add-in for Word, Excel, PowerPoint, and Outlook is installed.</caps:sentence>
                <caps:sentence id="src23" class="srcSentence"> This provides users with a <ui>Share Protected</ui> button on the ribbon, which invokes an easy-to-use dialog box of settings that are most commonly used to protect files to be emailed.</caps:sentence>
                <caps:sentence id="src24" class="srcSentence"> This button also provides a quick way to access the document tracking site.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src25" class="srcSentence">A new right-click option for File Explorer.</caps:sentence>
                <caps:sentence id="src26" class="srcSentence"> This provides users with a <ui>Protect in-place</ui> option, which invokes an easy-to-use dialog box of settings that are most commonly used to protect files stored on a disk.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src27" class="srcSentence">A viewer to open files that have been protected by <token>aad_rightsmanagement_2</token>.</caps:sentence>
                <caps:sentence id="src28" class="srcSentence"> This viewer is automatically invoked when there is no other application installed that could open the protected file.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src29" class="srcSentence">Backend configuration for Office 2010 that lets Word, Excel, PowerPoint, and Outlook from this suite work seamlessly with <token>aad_rightsmanagement_1</token>.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src30" class="srcSentence">Although the RMS sharing application for Windows can be downloaded and installed for a single computer by using the <externalLink><linkText>Microsoft Rights Management page</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=303970</linkUri></externalLink>, it also supports an enterprise deployment for silent installation and custom configuration.</caps:sentence>
            <caps:sentence id="src31" class="srcSentence"> For more information, see the following resources:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <externalLink>
                  <linkText>
                    <caps:sentence id="src32" class="srcSentence">Rights Management sharing application administrator guide</caps:sentence>
                  </linkText>
                  <linkUri>http://technet.microsoft.com/library/dn339003.aspx</linkUri>
                </externalLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <externalLink>
                  <linkText>
                    <caps:sentence id="src33" class="srcSentence">Rights Management sharing application user guide</caps:sentence>
                  </linkText>
                  <linkUri>http://technet.microsoft.com/library/dn339006.aspx</linkUri>
                </externalLink>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src34" class="srcSentence">The RMS sharing application for mobile devices supports the most commonly used mobile devices, such as iPad and iPhone, Android, Windows Phone, and Windows RT.</caps:sentence>
            <caps:sentence id="src35" class="srcSentence"> Users can download this app from the relevant store, and there are links to these from the <externalLink><linkText>Microsoft Rights Management page</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=303970</linkUri></externalLink>.</caps:sentence>
          </para>
        </content>
      </section>
      <section address="BKMK_OfficeAppsIntro">
        <title>
          <caps:sentence id="src36" class="srcSentence">Office applications: Word, Excel, PowerPoint, Outlook</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src37" class="srcSentence">These applications natively support Rights Management by using information rights management (IRM) and let users apply protection to a saved document or to an email message to be sent.</caps:sentence>
            <caps:sentence id="src38" class="srcSentence"> Users can apply templates or choose very customized settings for access, rights, and usage restrictions.</caps:sentence>
            <caps:sentence id="src39" class="srcSentence"> For example, users can configure a file so that it can be accessed only by people in your organization, or control whether the file can be edited, or restricted to read-only, or prevent it from being printed.</caps:sentence>
            <caps:sentence id="src40" class="srcSentence"> For time-sensitive files, an expiration time can be configured (directly by users or by applying a template) for when the file can no longer be accessed.</caps:sentence>
            <caps:sentence id="src41" class="srcSentence"> For Outlook, users can also choose the <ui>Do Not Forward</ui> option to help prevent data leakage.</caps:sentence>
          </para>
        </content>
        <sections>
          <section address="BKMK_ExchangeIntro">
            <title>
              <caps:sentence id="src42" class="srcSentence">Exchange Online and Exchange Server</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src43" class="srcSentence">When you use Exchange Online or Exchange Server, you can use information rights management (IRM) integration, which provides additional information protection solutions:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src44" class="srcSentence">
                      <legacyBold>Exchange ActiveSync IRM</legacyBold> so that mobile devices can protect and consume protected email messages.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src45" class="srcSentence">RMS support for the <legacyBold>Outlook Web App</legacyBold>, implemented similarly to the Outlook client, so that users can protect email messages by templates or by specifying individual options, and users can read and use protected email messages that are sent to them.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src46" class="srcSentence">
                      <legacyBold>Protection rules</legacyBold> for Outlook clients that an administrator configures to automatically apply RMS templates to email messages for specified recipients.</caps:sentence>
                    <caps:sentence id="src47" class="srcSentence"> For example, when internal emails are sent to your legal department, they can only be read by members of the legal department and cannot be forwarded.</caps:sentence>
                    <caps:sentence id="src48" class="srcSentence"> Users see the protection applied to the email message before sending it, and by default, they can remove it if they decide it is not necessary.</caps:sentence>
                    <caps:sentence id="src49" class="srcSentence"> Emails are encrypted before they are sent.</caps:sentence>
                    <caps:sentence id="src50" class="srcSentence"> For more information, see <externalLink><linkText>Outlook Protection Rules</linkText><linkUri>http://technet.microsoft.com/library/dd638178(v=exchg.150).aspx</linkUri></externalLink> and <externalLink><linkText>Create an Outlook Protection Rule</linkText><linkUri>http://technet.microsoft.com/library/dd638196(v=exchg.150).aspx</linkUri></externalLink> in the Exchange library.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src51" class="srcSentence">
                      <legacyBold>Transport rules</legacyBold> that an administrator configures to automatically apply RMS templates to email messages based on properties such as sender, recipient, message subject, and content.</caps:sentence>
                    <caps:sentence id="src52" class="srcSentence"> These are similar in concept to protection rules but do not let users remove the protection, can be applied to Outlook Web Access and emails sent by mobile devices, and do not encrypt email messages before they are sent from the client.</caps:sentence>
                    <caps:sentence id="src53" class="srcSentence"> For more information, see <externalLink><linkText>Create a Transport Protection Rule</linkText><linkUri>http://technet.microsoft.com/library/dd302432.aspx</linkUri></externalLink> in the Exchange library.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src54" class="srcSentence">
                      <legacyBold>Data loss prevention (DLP) policies</legacyBold> that contain sets of conditions to filter email messages, and take actions to help prevent data loss for confidential or sensitive content (for example, personal information or credit card information).</caps:sentence>
                    <caps:sentence id="src55" class="srcSentence"> Policy Tips can be used when sensitive data is detected, to alert users that they might need to apply information protection, based on the information in the email message.</caps:sentence>
                    <caps:sentence id="src56" class="srcSentence"> For more information, see <externalLink><linkText>Data Loss Prevention</linkText><linkUri>http://technet.microsoft.com/library/jj150527(v=exchg.150).aspx</linkUri></externalLink> in the Exchange library.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src57" class="srcSentence">
                      <legacyBold>Office 365 Message Encryption</legacyBold> that uses transport rules to send encrypted emails to people outside your company, and the email is read in a browser with an interface similar to the Outlook Web App.</caps:sentence>
                    <caps:sentence id="src58" class="srcSentence"> You can customize the disclaimer text and header text in your company’s encrypted emails, and even add your company logo.</caps:sentence>
                    <caps:sentence id="src59" class="srcSentence"> For more information, see <externalLink><linkText>Office 365 Message Encryption</linkText><linkUri>http://office.microsoft.com/o365-message-encryption-FX104179182.aspx</linkUri></externalLink> from the Office website.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src60" class="srcSentence">If you use Exchange Server, you can use the information protection features with <token>aad_rightsmanagement_1</token> by deploying the RMS connector, which acts as a relay between your on-premises servers and the RMS cloud service.</caps:sentence>
                <caps:sentence id="src61" class="srcSentence"> For more information, see <link xlink:href="90e7e33f-9ecc-497b-89c5-09205ffc5066">Deploying the Azure Rights Management Connector</link>.</caps:sentence>
              </para>
            </content>
          </section>
          <section address="BKMK_SharePointIntro">
            <title>
              <caps:sentence id="src62" class="srcSentence">SharePoint Online and SharePoint Server</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src63" class="srcSentence">When you use SharePoint Online or SharePoint Server, you can use information rights management (IRM) integration, which lets administrators protect lists or libraries so that when a user checks-out a document, the file is protected so that only authorized people can view and use the file according to the information protection policies that you specify.</caps:sentence>
                <caps:sentence id="src64" class="srcSentence"> For example, the file might be read-only, disable the copying of text, prevent saving a local copy, and prevent printing the file.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src65" class="srcSentence">For lists and libraries,  information protection is always applied by an administrator, never an end user.</caps:sentence>
                <caps:sentence id="src66" class="srcSentence"> And it is applied at the list or library level for all documents in that container, rather than on individual files.</caps:sentence>
                <caps:sentence id="src67" class="srcSentence">  If you use SharePoint Online, users can also apply IRM to their OneDrive for Business library.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src68" class="srcSentence">The IRM service must first be enabled for SharePoint.</caps:sentence>
                <caps:sentence id="src69" class="srcSentence"> Then, you specify Information Rights Management for a library.</caps:sentence>
                <caps:sentence id="src70" class="srcSentence"> In the case of SharePoint Online and OneDrive for Business, users can also specify Information Rights Management for their OneDrive for Business library.</caps:sentence>
                <caps:sentence id="src71" class="srcSentence"> SharePoint does not use rights policy templates, although there are SharePoint configuration settings that you can select that closely match the settings that you can specify in templates.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src72" class="srcSentence">If you use SharePoint Server, you can use the information protection features with <token>aad_rightsmanagement_1</token> by deploying the RMS connector, which acts as a relay between your on-premises servers and the RMS cloud service.</caps:sentence>
                <caps:sentence id="src73" class="srcSentence"> For more information, see <link xlink:href="90e7e33f-9ecc-497b-89c5-09205ffc5066">Deploying the Azure Rights Management Connector</link>.</caps:sentence>
              </para>
              <alert class="note">
                <para>
                  <caps:sentence id="src74" class="srcSentence">Currently, there are some limitations when you use IRM with SharePoint:</caps:sentence>
                </para>
                <list class="bullet">
                  <listItem>
                    <para>
                      <caps:sentence id="src75" class="srcSentence">You cannot use the default or custom templates that you manage in the Azure classic portal.</caps:sentence>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <caps:sentence id="src76" class="srcSentence">Files that have a .PPDF file name extension for protected PDF files are not supported.</caps:sentence>
                      <caps:sentence id="src77" class="srcSentence"> Files that have .PDF file name extension and that have been natively protected by RMS are supported when you use a PDF reader that natively supports RMS.</caps:sentence>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <caps:sentence id="src78" class="srcSentence"> Because Office on mobile devices does not yet support RMS, these devices must use a browser to view files that have been protected with RMS, and the files are read-only.</caps:sentence>
                    </para>
                  </listItem>
                </list>
              </alert>
              <para>
                <caps:sentence id="src79" class="srcSentence">Azure RMS applies usage restrictions and data encryption for documents when they are downloaded from SharePoint, and not when the document is first created in SharePoint or uploaded to the library.</caps:sentence>
                <caps:sentence id="src80" class="srcSentence"> For information about how documents are protected before they are downloaded, see <externalLink><linkText>Data Encryption in OneDrive for Business and SharePoint Online</linkText><linkUri>https://technet.microsoft.com/library/dn905447.aspx</linkUri></externalLink> from the SharePoint documentation.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src81" class="srcSentence">For more information about using Azure RMS with SharePoint, see the following  post from the Office blog: <externalLink><linkText>What’s New with Information Rights Management in SharePoint and SharePoint Online</linkText><linkUri>http://blogs.office.com/2012/11/09/whats-new-with-information-rights-management-in-sharepoint-and-sharepoint-online/</linkUri></externalLink></caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </section>
      <section address="BKMK_FCIIntro">
        <title>
          <caps:sentence id="src82" class="srcSentence">File servers that run Windows Server and use File Classification Infrastructure (FCI)</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src83" class="srcSentence">When you configure Windows Server to use File Classification Infrastructure, this File Server Resource Manager feature can scan local files and determine whether they contain sensitive data.</caps:sentence>
            <caps:sentence id="src84" class="srcSentence"> For files that meet this criteria, they are tagged with classification properties that an administrator defines.</caps:sentence>
            <caps:sentence id="src85" class="srcSentence"> The File Classification Infrastructure can then take automatic action, according to the classification.</caps:sentence>
            <caps:sentence id="src86" class="srcSentence"> One of these actions include applying information protection by using <token>aad_rightsmanagement_1</token> and the deployment of the Rights Management connector (also known as the RMS connector).</caps:sentence>
            <caps:sentence id="src87" class="srcSentence"> Office files are then automatically protected by Azure RMS.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src88" class="srcSentence">To protect all file types, you would not use the RMS connector, but instead, run a Windows PowerShell script, using cmdlets from the <externalLink><linkText>RMS Protection tool</linkText><linkUri>https://www.microsoft.com/en-us/download/details.aspx?id=47256</linkUri></externalLink>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src89" class="srcSentence">The classification policies are fully configurable and highly extensible so that you can prevent potential data leakage from unauthorized and authorized users.</caps:sentence>
            <caps:sentence id="src90" class="srcSentence"> It can even help to reduce the risk of data leakage by network administrators because you can configure policies that don’t require these administrators to have access to the files.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src91" class="srcSentence">For instructions to deploy and configure the RMS connector for Office files, see <link xlink:href="90e7e33f-9ecc-497b-89c5-09205ffc5066">Deploying the Azure Rights Management Connector</link>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src92" class="srcSentence">For instructions to use the Windows PowerShell script for all file types, see <link xlink:href="9aa693db-9727-4284-9f64-867681e114c9">RMS Protection with Windows Server File Classification Infrastructure (FCI)</link>.</caps:sentence>
          </para>
        </content>
      </section>
      <section address="BKMK_APIAppsIntro">
        <title>
          <caps:sentence id="src93" class="srcSentence">Other applications that support the RMS APIs</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src94" class="srcSentence">By using the RMS SDK, your internal developers can write line-of-business applications to natively support <token>aad_rightsmanagement_1</token>.</caps:sentence>
            <caps:sentence id="src95" class="srcSentence"> How information protection is integrated with these applications depends on how they are written.</caps:sentence>
            <caps:sentence id="src96" class="srcSentence"> For example, the integration might be automatically applied with minimal user interaction required, or for a more customized experience, users might be prompted to configure settings to apply information protection to files.</caps:sentence>
            <caps:sentence id="src97" class="srcSentence"> For more information about the SDK, see the <externalLink><linkText>Microsoft Rights Management SDK</linkText><linkUri>http://msdn.microsoft.com/library/hh552972(v=vs.85).aspx</linkUri></externalLink>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src98" class="srcSentence">Similarly, many software vendors provide applications to provide  information protection solutions, also known as enterprise rights management (ERM) products.</caps:sentence>
            <caps:sentence id="src99" class="srcSentence"> A popular example is a PDF reader that supports <token>aad_rightsmanagement_2</token> for specific platforms.</caps:sentence>
            <caps:sentence id="src100" class="srcSentence"> You can use the table in the <link xlink:href="dc78321d-d759-4653-8818-80da74b6cdeb#BKMK_ClientCapabilities">Client device capabilities</link> section of the <link xlink:href="dc78321d-d759-4653-8818-80da74b6cdeb">Requirements for Azure Rights Management</link> topic to identify applications that support RMS (RMS-enlightened applications), and then use a web search to purchase or download the application.</caps:sentence>
          </para>
          <alert class="tip">
            <para>
              <caps:sentence id="src101" class="srcSentence">For newly released applications, check the RMS community channels, listed in <link xlink:href="7cc73d92-27d6-49ff-a8ab-2fae73519b4b">Information and Support for Azure Rights Management</link>.</caps:sentence>
            </para>
          </alert>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="5214667c-ec69-42ca-8bbf-8cb22da8c62e">Getting started with Azure Rights Management</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>