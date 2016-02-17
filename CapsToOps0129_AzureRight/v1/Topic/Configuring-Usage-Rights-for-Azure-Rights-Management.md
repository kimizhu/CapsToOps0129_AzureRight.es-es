---
title: Configuraci&#243;n de los derechos de uso para Azure Rights Management
ms.custom: na
ms.reviewer: na
ms.service: rights-management
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 97ddde38-b91b-42a5-8eb4-3ce6ce15393d
---
# Configuraci&#243;n de los derechos de uso para Azure Rights Management
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="es-ES">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="9001f94c8a37421a3a33f4e050d3966b" id="tgt1" class="tgtSentence">Cuando establece la protección en archivos o correos electrónicos con Azure Rights Management (Azure RMS) y no usa ninguna plantilla, debe configurar los derechos de uso usted mismo.</caps:sentence>
          <caps:sentence sentenceid="4759eaa3722455ba5ca2cb73f65d63f6" id="tgt2" class="tgtSentence"> Además, al configurar plantillas personalizadas para Azure RMS, se seleccionan los derechos de uso que se aplicarán automáticamente cuando los usuarios, administradores o servicios configurados seleccionen la plantilla.</caps:sentence>
          <caps:sentence sentenceid="4ea7cec50b2c9f5249319dd04b8e1887" id="tgt3" class="tgtSentence"> Por ejemplo, en el Portal de Azure clásico, puede seleccionar los roles que configuran una agrupación lógica de derechos de uso o puede configurar los derechos individuales.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="7d1427422be15d3a6063602c3740f8b8" id="tgt4" class="tgtSentence">Use este tema para ayudarlo a configurar los derechos de uso que desea para la aplicación que esté usando y para entender cómo las aplicaciones interpretan estos derechos.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="815697d92fb3752fa447b8741a1776b7" id="tgt5" class="tgtSentence">Derechos de uso y descripciones</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="2d87cb9296e7c3669458efdff1c4c3fe" id="tgt6" class="tgtSentence">En la tabla siguiente se enumeran y se describen los derechos de uso que admite Rights Management y cómo se usan y se interpretan.</caps:sentence>
            <caps:sentence sentenceid="02cf72f05a25b6b5b971902046dfd1a3" id="tgt7" class="tgtSentence"> En esta tabla, el <embeddedLabel>Nombre común</embeddedLabel> es normalmente cómo se muestra o se referencia el derecho de uso, como una versión más descriptiva del valor de una sola palabra que se usa en el código (el valor <embeddedLabel>Codificación en la directiva</embeddedLabel>).</caps:sentence>
            <caps:sentence sentenceid="7267040c9198a4f62a4d6a357be066e5" id="tgt8" class="tgtSentence">
              <embeddedLabel>Constante o valor de API</embeddedLabel> es el nombre de SDK para una llamada de API de MSIPC, que se usa al escribir una aplicación habilitada para RMS que comprueba un derecho de uso o agrega un derecho de uso a una directiva.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3f2b150f808bc3e27a2f440ab2d8a3c6" id="tgt9" class="tgtSentence">Nombre común</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e098a007db915530bd25d77dc8d3f54d" id="tgt10" class="tgtSentence">Codificación en la directiva</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt11" class="tgtSentence">Descripción</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="49ef69f8b3ee502870d6227498bb5d2b" id="tgt12" class="tgtSentence">Implementación en los derechos personalizados de Office</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0e7868a90e9963ffb3b5295713654994" id="tgt13" class="tgtSentence">Nombre en el Portal de Azure clásico</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ed28d7972fd33bdb7711f43036cf6293" id="tgt14" class="tgtSentence">Nombre en las plantillas de AD RMS</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="23af13cadd1a1a64d87310e11f2714df" id="tgt15" class="tgtSentence">Constante o valor de API</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4eec452dee7d15acfb78a023b487bf19" id="tgt16" class="tgtSentence">Información adicional</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="50a95a046ffd80714b66e6dea211fb90" id="tgt17" class="tgtSentence">Editar contenido, Editar</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="34bbec02468fdd1d22c63223d7332980" id="tgt18" class="tgtSentence">DOCEDIT</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="90f860aa3a6a80ee2cbed9ddd6d3fea8" id="tgt19" class="tgtSentence">Permite al usuario modificar, reorganizar, formatear o filtrar el contenido dentro de la aplicación.</caps:sentence>
                    <caps:sentence sentenceid="a0cb76638dfbefe26866b2f14d650e77" id="tgt20" class="tgtSentence"> No concede el derecho a guardar la copia modificada.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="42575dfa334afff5826737c7b8ab2c33" id="tgt21" class="tgtSentence">Como parte de las opciones <ui>Cambiar</ui> y <ui>Control total</ui>.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence sentenceid="8f054fa7f49178bcd816144add2cc802" id="tgt22" class="tgtSentence">Editar contenido</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence sentenceid="de95b43bceeb4b998aed4aed5cef1ae7" id="tgt23" class="tgtSentence">Editar</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4b99c13013f59eb4aa6fc87d531d9c24" id="tgt24" class="tgtSentence">No aplicable</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ed3e20ca3597bc508f69682a7c5c80bf" id="tgt25" class="tgtSentence">En las aplicaciones de Office, este derecho también permite al usuario guardar el documento.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="43781db5c40ecc39fd718685594f0956" id="tgt26" class="tgtSentence">Guardar</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="de95b43bceeb4b998aed4aed5cef1ae7" id="tgt27" class="tgtSentence">EDITAR</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6dbcffbab9a5f161795c1926c3e8672a" id="tgt28" class="tgtSentence">Permite al usuario guardar el documento en su ubicación actual.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="42575dfa334afff5826737c7b8ab2c33" id="tgt29" class="tgtSentence">Como parte de las opciones <ui>Cambiar</ui> y <ui>Control total</ui>.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence sentenceid="0a896fa018624b7d79f7e4d17df857e4" id="tgt30" class="tgtSentence">Guardar archivo</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence sentenceid="43781db5c40ecc39fd718685594f0956" id="tgt31" class="tgtSentence">Guardar</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d22020c2cd3e6df0dac6ffa74b4a9528" id="tgt32" class="tgtSentence">IPC_GENERIC_WRITEL"EDIT"</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="9171f0bcaf17994ee24c580206bb9cb9" id="tgt33" class="tgtSentence">En las aplicaciones de Office, este derecho también permite al usuario modificar el documento.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="06d4cd63bde972fc66a0aed41d2f5c51" id="tgt34" class="tgtSentence">Comentario</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="06d4cd63bde972fc66a0aed41d2f5c51" id="tgt35" class="tgtSentence">COMMENT</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c289835c60607ea6f5902d02c66f572c" id="tgt36" class="tgtSentence">Habilita la opción para agregar anotaciones o comentarios al contenido.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2d57d21f35e060a4c5e81c03aea3efa8" id="tgt37" class="tgtSentence">No implementado</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2d57d21f35e060a4c5e81c03aea3efa8" id="tgt38" class="tgtSentence">No implementado</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2d57d21f35e060a4c5e81c03aea3efa8" id="tgt39" class="tgtSentence">No implementado</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6533547f2c151282fd0bba476e453cbc" id="tgt40" class="tgtSentence">IPC_GENERIC_COMMENTL"COMMENT"</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="acd04afb2dc7cea6508345df4899cca9" id="tgt41" class="tgtSentence">Este derecho está disponible en el SDK como directiva ad hoc en el módulo de protección de RMS para Windows PowerShell y se implementó en algunas aplicaciones de proveedores de software.</caps:sentence>
                    <caps:sentence sentenceid="fbaefbbef0b3a46d5895fd9d3491843c" id="tgt42" class="tgtSentence"> Sin embargo, no se usa extensamente y no es compatible actualmente con las aplicaciones de Office.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="08a07d2c1d92407b018f9bf30abddb8c" id="tgt43" class="tgtSentence">Guardar como, Exportar</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b2507468f95156358fa490fd543ad2f0" id="tgt44" class="tgtSentence">EXPORTAR</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="84f26f1c3b70699c287ffd6c049c6656" id="tgt45" class="tgtSentence">Habilita la opción para guardar el contenido con un nombre de archivo diferente (Guardar como).</caps:sentence>
                    <caps:sentence sentenceid="f35507f54b97b58a083b618c3f9d7233" id="tgt46" class="tgtSentence"> Según la aplicación, el archivo puede guardarse sin protección.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e47cdababf8a1af829a6f8d9851398e2" id="tgt47" class="tgtSentence">Como parte de las opciones <ui>Cambiar</ui> y <ui>Control total</ui>.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence sentenceid="2e8491abe629384137fa7bb24bd72a19" id="tgt48" class="tgtSentence">Exportar contenido (Guardar como)</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence sentenceid="e80a671026f8b9ff8662e4b6cefbc97b" id="tgt49" class="tgtSentence">Exportar (Guardar como)</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="aaeb2a6bec649ce5c75cbda605028a76" id="tgt50" class="tgtSentence">IPC_GENERIC_EXPORTL"EXPORT"</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1ee1cd1bbe5d49b786c003108cd223b5" id="tgt51" class="tgtSentence">Este derecho también permite al usuario realizar otras opciones de exportación en las aplicaciones, como <ui>Enviar a OneNote</ui>.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="965dbaac085fc891bfbbd4f9d145bbc8" id="tgt52" class="tgtSentence">Reenviar</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="965dbaac085fc891bfbbd4f9d145bbc8" id="tgt53" class="tgtSentence">REENVIAR</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="75f7490a090c6fc45ad2f36ee345fac4" id="tgt54" class="tgtSentence">Habilita la opción para reenviar un mensaje de correo electrónico y agregar destinatarios a las líneas <ui>Para</ui> y <ui>CO</ui>.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2b398174dd581ed3cdaae11335cae83e" id="tgt55" class="tgtSentence">Se deniega al usar la directiva estándar <ui>No reenviar</ui>.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence sentenceid="965dbaac085fc891bfbbd4f9d145bbc8" id="tgt56" class="tgtSentence">Reenviar</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence sentenceid="965dbaac085fc891bfbbd4f9d145bbc8" id="tgt57" class="tgtSentence">Reenviar</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8e54ca3b6d5bb021a491d2152b98277f" id="tgt58" class="tgtSentence">IPC_EMAIL_FORWARDL"FORWARD"</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8b70669740859f11898bb5cdb98fe565" id="tgt59" class="tgtSentence">No permite que el reenviador conceda derechos a otros usuarios como parte de la acción de reenvío.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b3fd7f50a632febc1f19586b0faec74b" id="tgt60" class="tgtSentence">Control total</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="72122ce96bfec66e2396d2e25225d70a" id="tgt61" class="tgtSentence">OWNER</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f649982f6d96240956517b8f8863a66e" id="tgt62" class="tgtSentence">Concede todos los derechos para el documento; se pueden realizar todas las acciones disponibles.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="bfcd34fbc5a4f90c7104bceef78f2a3e" id="tgt63" class="tgtSentence">Como la opción personalizada <ui>Control total</ui>.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence sentenceid="b3fd7f50a632febc1f19586b0faec74b" id="tgt64" class="tgtSentence">Control total</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence sentenceid="b3fd7f50a632febc1f19586b0faec74b" id="tgt65" class="tgtSentence">Control total</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="98c267f72699d2f6806cdfb2ba0e51ac" id="tgt66" class="tgtSentence">IPC_GENERIC_ALLL"OWNER"</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f6333f8d3b769a94d2c4183db73e9dec" id="tgt67" class="tgtSentence">Incluye la capacidad de quitar la protección.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f7531e2d0ea27233ce00b5f01c5bf335" id="tgt68" class="tgtSentence">Imprimir</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f7531e2d0ea27233ce00b5f01c5bf335" id="tgt69" class="tgtSentence">PRINT</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8775666f54983cca66cdb608124504a5" id="tgt70" class="tgtSentence">Habilita las opciones para imprimir el contenido.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1b13886d6d97aacb574987cd54f17a26" id="tgt71" class="tgtSentence">Como la opción <ui>Imprimir contenido</ui> en los permisos personalizados.</caps:sentence>
                    <caps:sentence sentenceid="8eb9eaeea8e1cf6c8421ab917de92023" id="tgt72" class="tgtSentence"> No se trata de un valor por destinatario.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence sentenceid="f7531e2d0ea27233ce00b5f01c5bf335" id="tgt73" class="tgtSentence">Imprimir</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence sentenceid="f7531e2d0ea27233ce00b5f01c5bf335" id="tgt74" class="tgtSentence">Imprimir</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="bbf63f718ea596e7b562078238fc546d" id="tgt75" class="tgtSentence">IPC_GENERIC_PRINTL"PRINT"</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e8e4c7d13f41b356ba7390b9d6355c3e" id="tgt76" class="tgtSentence">Sin información adicional</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e84afaab83ecb301b3d97ce4174d2773" id="tgt77" class="tgtSentence">Responder</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e84afaab83ecb301b3d97ce4174d2773" id="tgt78" class="tgtSentence">RESPONDER</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3ade94d36dcd6a17ea86d0b8ce89c61c" id="tgt79" class="tgtSentence">Habilita la opción Respuesta en un cliente de correo electrónico, sin permitir que se realicen cambios en las líneas <ui>Para</ui> o <ui>CO</ui>.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4b99c13013f59eb4aa6fc87d531d9c24" id="tgt80" class="tgtSentence">No aplicable</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence sentenceid="e84afaab83ecb301b3d97ce4174d2773" id="tgt81" class="tgtSentence">Responder</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence sentenceid="e84afaab83ecb301b3d97ce4174d2773" id="tgt82" class="tgtSentence">Responder</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1ed15b06a1e5e9a6558bb86c4f7171fd" id="tgt83" class="tgtSentence">IPC_EMAIL_REPLY</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e8e4c7d13f41b356ba7390b9d6355c3e" id="tgt84" class="tgtSentence">Sin información adicional</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="031d46c4d346f6539a2fd367d169e82e" id="tgt85" class="tgtSentence">Responder a todos</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0d56fa2e9f47acbd7d309398ceaeafd8" id="tgt86" class="tgtSentence">REPLYALL</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e734f6ee0c0535b150b6e5a2c2c90af7" id="tgt87" class="tgtSentence">Habilita la opción <ui>Responder a todos</ui> en un cliente de correo electrónico, pero no permite al usuario agregar a destinatarios a las líneas <ui>Para</ui> o <ui>CO</ui>.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4b99c13013f59eb4aa6fc87d531d9c24" id="tgt88" class="tgtSentence">No aplicable</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence sentenceid="031d46c4d346f6539a2fd367d169e82e" id="tgt89" class="tgtSentence">Responder a todos</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence sentenceid="031d46c4d346f6539a2fd367d169e82e" id="tgt90" class="tgtSentence">Responder a todos</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="faf614ab7a26aadd48e76afdc8fe0337" id="tgt91" class="tgtSentence">IPC_EMAIL_REPLYALLL"REPLYALL"</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e8e4c7d13f41b356ba7390b9d6355c3e" id="tgt92" class="tgtSentence">Sin información adicional</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4770c9e40fe2ceeee8fc23a8f6ae7076" id="tgt93" class="tgtSentence">Ver, Abrir, Leer</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1bda80f2be4d3658e0baa43fbe7ae8c1" id="tgt94" class="tgtSentence">VER</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e5135d824218166e2523c0fa5ad155dc" id="tgt95" class="tgtSentence">Permite al usuario abrir el documento y ver el contenido.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8143c5a35619288c0e81b6682637bea2" id="tgt96" class="tgtSentence">Como la opción <ui>Ver</ui> de la directiva personalizada <ui>Leer</ui>.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence sentenceid="bf9310f79455738321e8fb6f5f17994b" id="tgt97" class="tgtSentence">Ver contenido</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence sentenceid="1bda80f2be4d3658e0baa43fbe7ae8c1" id="tgt98" class="tgtSentence">Vista</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="75f25384784235642fbb2d01cf3439c2" id="tgt99" class="tgtSentence">IPC_GENERIC_READL"VIEW"</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e8e4c7d13f41b356ba7390b9d6355c3e" id="tgt100" class="tgtSentence">Sin información adicional</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="12cba3ee81cf4a793796a51b6327c678" id="tgt101" class="tgtSentence">Copiar</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3e40063e25753005ccb971c164035b1a" id="tgt102" class="tgtSentence">EXTRACT</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c38e8ea018e847b3df7e411015cd9c12" id="tgt103" class="tgtSentence">Habilita las opciones para copiar los datos del documento en el mismo documento o en otro documento.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3d05fca2a1b9f47aab98942b6bb49238" id="tgt104" class="tgtSentence">Como la opción de directiva personalizada <ui>Permitir a los usuarios con acceso de lectura copiar contenido</ui>.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence sentenceid="72f001626ceb5d8aaf9a1e5c332a4100" id="tgt105" class="tgtSentence">Copiar y Extraer contenido</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence sentenceid="3e40063e25753005ccb971c164035b1a" id="tgt106" class="tgtSentence">Extracción</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="9d292af68a54a5f6176e554f1220b19a" id="tgt107" class="tgtSentence">IPC_GENERIC_EXTRACTL"EXTRACT"</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="be85965ef4ecab57f3b48a0b959ac2db" id="tgt108" class="tgtSentence">En algunas aplicaciones, también permite que todo el documento se guarde en sin protección.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f32ad6570e1c9601ba9520cfd85d9b2b" id="tgt109" class="tgtSentence">Ver derechos</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e56c658eff7d914ebcc5e8372e7d47f7" id="tgt110" class="tgtSentence">VIEWRIGHTSDATA</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ce07262b9f8fea781604e0b1480fa6c0" id="tgt111" class="tgtSentence">Permite al usuario ver la directiva que se aplica al documento.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2d57d21f35e060a4c5e81c03aea3efa8" id="tgt112" class="tgtSentence">No implementado</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence sentenceid="a161d2714713b2f8320680221beec56e" id="tgt113" class="tgtSentence">Ver derechos asignados</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence sentenceid="f32ad6570e1c9601ba9520cfd85d9b2b" id="tgt114" class="tgtSentence">Ver derechos</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="59b3310efce98daa4a02147123a51127" id="tgt115" class="tgtSentence">IPC_READ_RIGHTSL"VIEWRIGHTSDATA"</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b7fd7192c13a89688a4a47554e4b7752" id="tgt116" class="tgtSentence">Algunas aplicaciones no lo tienen en cuenta.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="56675b99c752602e649fb6d41863b436" id="tgt117" class="tgtSentence">Cambiar derechos</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ca159992d71a9c580e6eaf6a64c91913" id="tgt118" class="tgtSentence">EDITRIGHTSDATA</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="dbfe5aeeb009d452c331f81ed82c4c9c" id="tgt119" class="tgtSentence">Permite al usuario cambiar la directiva que se aplica al documento.</caps:sentence>
                    <caps:sentence sentenceid="721d77637b6ff0aba40da5287299fc80" id="tgt120" class="tgtSentence"> Incluye la eliminación de la protección.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2d57d21f35e060a4c5e81c03aea3efa8" id="tgt121" class="tgtSentence">No implementado</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence sentenceid="56675b99c752602e649fb6d41863b436" id="tgt122" class="tgtSentence">Cambiar derechos</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence sentenceid="1029778c8ad930e73a554ee36b5ea0c4" id="tgt123" class="tgtSentence">Editar derechos</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="815df98bb31fa02102a7365a1f418a77" id="tgt124" class="tgtSentence">IPC_WRITE_RIGHTSL"EDITRIGHTSDATA"</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e8e4c7d13f41b356ba7390b9d6355c3e" id="tgt125" class="tgtSentence">Sin información adicional</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="57f85f148884da85833540f4593ca5cd" id="tgt126" class="tgtSentence">Permitir macros</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ef1686f9b42b5f39b35f3d82da0d09a5" id="tgt127" class="tgtSentence">OBJMODEL</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="48ed6687fad5e0bf4b2bc28085d17fbc" id="tgt128" class="tgtSentence">Habilita la opción para ejecutar macros u obtener acceso remoto o mediante programación al contenido de un documento.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="69c4ce4e1238ff94b457fe6da63a4346" id="tgt129" class="tgtSentence">Como la opción de directiva personalizada <ui>Permitir el acceso mediante programación</ui>.</caps:sentence>
                    <caps:sentence sentenceid="8eb9eaeea8e1cf6c8421ab917de92023" id="tgt130" class="tgtSentence"> No se trata de un valor por destinatario.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence sentenceid="57f85f148884da85833540f4593ca5cd" id="tgt131" class="tgtSentence">Permitir macros</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence sentenceid="57f85f148884da85833540f4593ca5cd" id="tgt132" class="tgtSentence">Permitir macros</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4b99c13013f59eb4aa6fc87d531d9c24" id="tgt133" class="tgtSentence">No aplicable</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e8e4c7d13f41b356ba7390b9d6355c3e" id="tgt134" class="tgtSentence">Sin información adicional</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="27be548e880c9f92197e89235e0e84c6" id="tgt135" class="tgtSentence">Derechos incluidos en los niveles de permisos</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="5e575628abededf9d562ad8cd33bc03c" id="tgt136" class="tgtSentence">Algunas aplicaciones agrupan derechos de uso en niveles de permisos para facilitar la selección de derechos de uso que suelen utilizarse de forma conjunta.</caps:sentence>
            <caps:sentence sentenceid="df8a60bade3a4010543c280322534547" id="tgt137" class="tgtSentence"> Estos niveles de permisos ayudan a resumir un nivel de complejidad de los usuarios para que puedan elegir opciones basadas en roles.</caps:sentence>
            <caps:sentence sentenceid="cf68492f09e7318d51a74d3ffef3fbae" id="tgt138" class="tgtSentence">  Por ejemplo, <embeddedLabel>Revisor</embeddedLabel> y <embeddedLabel>Coautor</embeddedLabel>.</caps:sentence>
            <caps:sentence sentenceid="f9ed17fc58d9ab622a8fe86a35743e0d" id="tgt139" class="tgtSentence"> Aunque estas opciones suelen mostrar a los usuarios un resumen de los derechos, puede que no incluyan todos los derechos enumerados en la tabla anterior.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="9771712e71b8150923f2e4d51607e54b" id="tgt140" class="tgtSentence">Utilice la tabla siguiente para ver una lista de estos niveles de permisos y una lista completa de los derechos que contienen.</caps:sentence>
          </para>
          <table border="1">
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a47e77ee2cd4cadc6d90a878c14ded6f" id="tgt141" class="tgtSentence">Nivel de permisos</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b5fba9ff24d0045d1377a05a46b32f68" id="tgt142" class="tgtSentence">Aplicaciones</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1300f623b4eb0bbfaab059fe0804e1de" id="tgt143" class="tgtSentence">Derechos incluidos (nombre común)</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4b2a1529867b8d697685b1722ccd0149" id="tgt144" class="tgtSentence">Visor</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1ea0594b653fbf0789494176a84894d3" id="tgt145" class="tgtSentence">Portal de Azure clásico</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="16038aecce8801279d1271a1934963dd" id="tgt146" class="tgtSentence">Aplicación de uso compartido Rights Management para Windows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4770c9e40fe2ceeee8fc23a8f6ae7076" id="tgt147" class="tgtSentence">Ver, Abrir, Leer</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="e84afaab83ecb301b3d97ce4174d2773" id="tgt148" class="tgtSentence">Responder</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="031d46c4d346f6539a2fd367d169e82e" id="tgt149" class="tgtSentence">Responder a todos</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7ba917e4e5158c8a9ed6eda08a6ec572" id="tgt150" class="tgtSentence">Revisor</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1ea0594b653fbf0789494176a84894d3" id="tgt151" class="tgtSentence">Portal de Azure clásico</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="16038aecce8801279d1271a1934963dd" id="tgt152" class="tgtSentence">Aplicación de uso compartido Rights Management para Windows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4770c9e40fe2ceeee8fc23a8f6ae7076" id="tgt153" class="tgtSentence">Ver, Abrir, Leer</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="43781db5c40ecc39fd718685594f0956" id="tgt154" class="tgtSentence">Guardar</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="50a95a046ffd80714b66e6dea211fb90" id="tgt155" class="tgtSentence">Editar contenido, Editar</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="faceb5fc0befbee2c154b949291a8a8f" id="tgt156" class="tgtSentence">Responder<superscript>*</superscript></caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="183be7aee825c4834c8e97b3dc60d865" id="tgt157" class="tgtSentence">Responder a todos<superscript>*</superscript></caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="22fef890a762e90210ac982938b8187f" id="tgt158" class="tgtSentence">Reenviar<superscript>*</superscript></caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6397f49a39cad2d01f7aa31440514285" id="tgt159" class="tgtSentence">Coautor</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1ea0594b653fbf0789494176a84894d3" id="tgt160" class="tgtSentence">Portal de Azure clásico</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="16038aecce8801279d1271a1934963dd" id="tgt161" class="tgtSentence">Aplicación de uso compartido Rights Management para Windows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4770c9e40fe2ceeee8fc23a8f6ae7076" id="tgt162" class="tgtSentence">Ver, Abrir, Leer</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="43781db5c40ecc39fd718685594f0956" id="tgt163" class="tgtSentence">Guardar</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="334d477b638b0a90bdbc816491bb4e7a" id="tgt164" class="tgtSentence">Editar contenido, Editar
</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="12cba3ee81cf4a793796a51b6327c678" id="tgt165" class="tgtSentence">Copiar</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="f32ad6570e1c9601ba9520cfd85d9b2b" id="tgt166" class="tgtSentence">Ver derechos</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="56675b99c752602e649fb6d41863b436" id="tgt167" class="tgtSentence">Cambiar derechos</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="57f85f148884da85833540f4593ca5cd" id="tgt168" class="tgtSentence">Permitir macros</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="08a07d2c1d92407b018f9bf30abddb8c" id="tgt169" class="tgtSentence">Guardar como, Exportar</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="f7531e2d0ea27233ce00b5f01c5bf335" id="tgt170" class="tgtSentence">Imprimir</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="faceb5fc0befbee2c154b949291a8a8f" id="tgt171" class="tgtSentence">Responder<superscript>*</superscript></caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="183be7aee825c4834c8e97b3dc60d865" id="tgt172" class="tgtSentence">Responder a todos<superscript>*</superscript></caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="22fef890a762e90210ac982938b8187f" id="tgt173" class="tgtSentence">Reenviar<superscript>*</superscript></caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8602733155c8ad0dc232d58685c12b8d" id="tgt174" class="tgtSentence">Copropietario</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1ea0594b653fbf0789494176a84894d3" id="tgt175" class="tgtSentence">Portal de Azure clásico</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="16038aecce8801279d1271a1934963dd" id="tgt176" class="tgtSentence">Aplicación de uso compartido Rights Management para Windows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4770c9e40fe2ceeee8fc23a8f6ae7076" id="tgt177" class="tgtSentence">Ver, Abrir, Leer</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="43781db5c40ecc39fd718685594f0956" id="tgt178" class="tgtSentence">Guardar</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="334d477b638b0a90bdbc816491bb4e7a" id="tgt179" class="tgtSentence">Editar contenido, Editar
</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="12cba3ee81cf4a793796a51b6327c678" id="tgt180" class="tgtSentence">Copiar</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="f32ad6570e1c9601ba9520cfd85d9b2b" id="tgt181" class="tgtSentence">Ver derechos</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="56675b99c752602e649fb6d41863b436" id="tgt182" class="tgtSentence">Cambiar derechos</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="57f85f148884da85833540f4593ca5cd" id="tgt183" class="tgtSentence">Permitir macros</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="08a07d2c1d92407b018f9bf30abddb8c" id="tgt184" class="tgtSentence">Guardar como, Exportar</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="f7531e2d0ea27233ce00b5f01c5bf335" id="tgt185" class="tgtSentence">Imprimir</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="faceb5fc0befbee2c154b949291a8a8f" id="tgt186" class="tgtSentence">Responder<superscript>*</superscript></caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="183be7aee825c4834c8e97b3dc60d865" id="tgt187" class="tgtSentence">Responder a todos<superscript>*</superscript></caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="22fef890a762e90210ac982938b8187f" id="tgt188" class="tgtSentence">Reenviar<superscript>*</superscript></caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="b3fd7f50a632febc1f19586b0faec74b" id="tgt189" class="tgtSentence">Control total</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <caps:sentence sentenceid="97845ddafca1baa49a93ecad221d7661" id="tgt190" class="tgtSentence">
              <superscript>*</superscript> No aplicable a la aplicación de uso compartido Rights Management para Windows</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="1d8d58a3b523e1338eb4db96dea81fad" id="tgt191" class="tgtSentence">Derechos incluidos en las plantillas predeterminadas</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="f83efc5b04976d445b3cb8276ac78e8a" id="tgt192" class="tgtSentence">Los derechos que se incluyen con las plantillas predeterminadas son los siguientes:</caps:sentence>
          </para>
          <table border="1">
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c6e8002007aa1e8639005d3f83436283" id="tgt193" class="tgtSentence">Nombre para mostrar</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="815936bf6221a13d68b8a9443161448b" id="tgt194" class="tgtSentence">Derechos incluidos (nombre común) </caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e077074c9f6cde84d6730b603611b0cb" id="tgt195" class="tgtSentence">&lt;nombreDeOrganización&gt;- Solo vista confidencial</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4770c9e40fe2ceeee8fc23a8f6ae7076" id="tgt196" class="tgtSentence">Ver, Abrir, Leer</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <caps:sentence sentenceid="c47576c448d33e39dbff14a38f8aeda0" id="tgt197" class="tgtSentence"> <para>&lt;nombreDeOrganización&gt; - Confidencial</para></caps:sentence>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4770c9e40fe2ceeee8fc23a8f6ae7076" id="tgt198" class="tgtSentence">Ver, Abrir, Leer</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="43781db5c40ecc39fd718685594f0956" id="tgt199" class="tgtSentence">Guardar</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="50a95a046ffd80714b66e6dea211fb90" id="tgt200" class="tgtSentence">Editar contenido, Editar</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="f32ad6570e1c9601ba9520cfd85d9b2b" id="tgt201" class="tgtSentence">Ver derechos</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="57f85f148884da85833540f4593ca5cd" id="tgt202" class="tgtSentence">Permitir macros</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="965dbaac085fc891bfbbd4f9d145bbc8" id="tgt203" class="tgtSentence">Reenviar</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="e84afaab83ecb301b3d97ce4174d2773" id="tgt204" class="tgtSentence">Responder</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="031d46c4d346f6539a2fd367d169e82e" id="tgt205" class="tgtSentence">Responder a todos</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="206a0bfe-0912-4e0e-aa15-484b000b264c">Configuring Azure Rights Management</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">When you set protection on files or emails by using Azure Rights Management (Azure RMS) and you do not use a template, you must configure the usage rights yourself.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> In addition, when you configure custom templates for Azure RMS, you select the usage rights that will then be automatically applied when the template is selected by users, administrators, or configured services.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> For example, in the Azure  classic portal you can select roles that configure a logical grouping of usage rights, or you can configure the individual rights.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src4" class="srcSentence">Use this topic to help you configure the usage rights you want for the application you’re using and understand how these rights are interpreted by applications.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src5" class="srcSentence">Usage Rights and Descriptions</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src6" class="srcSentence">The following table lists and describes the usage rights that Rights Management supports, and how they are used and interpreted.</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> In this table, the <embeddedLabel>Common name</embeddedLabel> is typically how you might see the usage right displayed or referenced, as a more friendly version of the single-word value that is used in the code (the <embeddedLabel>Encoding in policy</embeddedLabel> value).</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> The <embeddedLabel>API Constant or Value</embeddedLabel> is the SDK name for an MSIPC API call, used when you write an RMS-enlightened application that checks for a usage right, or adds a usage right to a policy.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src9" class="srcSentence">Common name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src10" class="srcSentence">Encoding in policy</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src11" class="srcSentence">Description</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src12" class="srcSentence">Implementation in Office custom rights</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src13" class="srcSentence">Name in the Azure  classic portal</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src14" class="srcSentence">Name in AD RMS templates</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src15" class="srcSentence">API constant or value</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src16" class="srcSentence">Additional information</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src17" class="srcSentence">Edit Content, Edit</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src18" class="srcSentence">DOCEDIT</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src19" class="srcSentence">Allows the user to modify, rearrange, format or filter the content inside the application.</caps:sentence>
                    <caps:sentence id="src20" class="srcSentence"> It does not grant the right to save the edited copy.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src21" class="srcSentence">As part of the <ui>Change</ui> and <ui>Full Control</ui> options.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence id="src22" class="srcSentence">Edit Content</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence id="src23" class="srcSentence">Edit</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src24" class="srcSentence">Not applicable</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src25" class="srcSentence">In Office applications, this right also allows the user to save the document.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src26" class="srcSentence">Save</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src27" class="srcSentence">EDIT</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src28" class="srcSentence">Allows the user to save the document in its current location.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src29" class="srcSentence">As part of the <ui>Change</ui> and <ui>Full Control</ui> options.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence id="src30" class="srcSentence">Save File</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence id="src31" class="srcSentence">Save</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src32" class="srcSentence">IPC_GENERIC_WRITEL"EDIT"</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src33" class="srcSentence">In Office applications, this right also allows the user to modify the document.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src34" class="srcSentence">Comment</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src35" class="srcSentence">COMMENT</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src36" class="srcSentence">Enables the option to add annotations or comments to the content.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src37" class="srcSentence">Not implemented</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src38" class="srcSentence">Not implemented</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src39" class="srcSentence">Not implemented</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src40" class="srcSentence">IPC_GENERIC_COMMENTL"COMMENT"</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src41" class="srcSentence">This right is available in the SDK, is available as an ad-hoc policy in the RMS Protection module for Windows PowerShell, and has been implemented in some software vendor applications.</caps:sentence>
                    <caps:sentence id="src42" class="srcSentence"> However, it is not widely used and is not currently supported by Office applications.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src43" class="srcSentence">Save As, Export</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src44" class="srcSentence">EXPORT</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src45" class="srcSentence">Enables the option to save the content to a different file name (Save As).</caps:sentence>
                    <caps:sentence id="src46" class="srcSentence"> Depending on the application, the file might be saved without protection.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src47" class="srcSentence">As part of the <ui>Change</ui> and<ui> Full Control</ui> options.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence id="src48" class="srcSentence">Export Content (Save As)</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence id="src49" class="srcSentence">Export (Save As)</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src50" class="srcSentence">IPC_GENERIC_EXPORTL"EXPORT"</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src51" class="srcSentence">This right also allows the user to perform other export options in applications, such as <ui>Send to OneNote</ui>.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src52" class="srcSentence">Forward</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src53" class="srcSentence">FORWARD</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src54" class="srcSentence">Enables the option to forward an email message and to add recipients to the <ui>To</ui> and <ui>Cc</ui> lines.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src55" class="srcSentence">Denied when using the <ui>Do Not Forward</ui> standard policy.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence id="src56" class="srcSentence">Forward</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence id="src57" class="srcSentence">Forward</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src58" class="srcSentence">IPC_EMAIL_FORWARDL"FORWARD"</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src59" class="srcSentence">Does not allow the forwarder to grant rights to other users as part of the forward action.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src60" class="srcSentence">Full Control</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src61" class="srcSentence">OWNER</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src62" class="srcSentence">Grants all rights to the document and all available actions can be performed.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src63" class="srcSentence">As the <ui>Full Control</ui> custom option.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence id="src64" class="srcSentence">Full Control</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence id="src65" class="srcSentence">Full Control</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src66" class="srcSentence">IPC_GENERIC_ALLL"OWNER"</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src67" class="srcSentence">Includes the ability to remove protection.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src68" class="srcSentence">Print</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src69" class="srcSentence">PRINT</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src70" class="srcSentence">Enables the options to print the content.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src71" class="srcSentence">As the <ui>Print Content </ui>option in custom permissions.</caps:sentence>
                    <caps:sentence id="src72" class="srcSentence"> Not a per-recipient setting.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence id="src73" class="srcSentence">Print</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence id="src74" class="srcSentence">Print</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src75" class="srcSentence">IPC_GENERIC_PRINTL"PRINT</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src76" class="srcSentence">No additional information</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src77" class="srcSentence">Reply</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src78" class="srcSentence">REPLY</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src79" class="srcSentence">Enables the Reply option in an email client, without allowing changes in the <ui>To</ui> or<ui> Cc</ui> lines.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src80" class="srcSentence">Not applicable</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence id="src81" class="srcSentence">Reply</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence id="src82" class="srcSentence">Reply</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src83" class="srcSentence">IPC_EMAIL_REPLY</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src84" class="srcSentence">No additional information</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src85" class="srcSentence">Reply All</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src86" class="srcSentence">REPLYALL</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src87" class="srcSentence">Enables the <ui>Reply All</ui> option in an email client, but doesn’t allow the user to add recipients to the <ui>To</ui> or <ui>Cc</ui> lines.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src88" class="srcSentence">Not applicable</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence id="src89" class="srcSentence">Reply All</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence id="src90" class="srcSentence">Reply All</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src91" class="srcSentence">IPC_EMAIL_REPLYALLL"REPLYALL"</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src92" class="srcSentence">No additional information</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src93" class="srcSentence">View, Open, Read</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src94" class="srcSentence">VIEW</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src95" class="srcSentence">Allows the user to open the document and see the content.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src96" class="srcSentence">As the <ui>Read</ui> custom policy, <ui>View</ui> option.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence id="src97" class="srcSentence">View Content</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence id="src98" class="srcSentence">View</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src99" class="srcSentence">IPC_GENERIC_READL"VIEW"</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src100" class="srcSentence">No additional information</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src101" class="srcSentence">Copy</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src102" class="srcSentence">EXTRACT</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src103" class="srcSentence">Enables options to copy data from the document into the same or another document.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src104" class="srcSentence">As the <ui>Allow users with Read access to copy content</ui> custom policy option.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence id="src105" class="srcSentence">Copy and Extract content</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence id="src106" class="srcSentence">Extract</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src107" class="srcSentence">IPC_GENERIC_EXTRACTL"EXTRACT"</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src108" class="srcSentence">In some applications it also allows the whole document to be saved in unprotected form.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src109" class="srcSentence">View Rights</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src110" class="srcSentence">VIEWRIGHTSDATA</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src111" class="srcSentence">Allows the user to see the policy that is applied to the document.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src112" class="srcSentence">Not implemented</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence id="src113" class="srcSentence">View Assigned Rights</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence id="src114" class="srcSentence">View Rights</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src115" class="srcSentence">IPC_READ_RIGHTSL"VIEWRIGHTSDATA"</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src116" class="srcSentence">Ignored by some applications.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src117" class="srcSentence">Change Rights</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src118" class="srcSentence">EDITRIGHTSDATA</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src119" class="srcSentence">Allows the user to change the policy that is applied to the document.</caps:sentence>
                    <caps:sentence id="src120" class="srcSentence"> Includes including removing protection.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src121" class="srcSentence">Not implemented</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence id="src122" class="srcSentence">Change Rights</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence id="src123" class="srcSentence">Edit Rights</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src124" class="srcSentence">IPC_WRITE_RIGHTSL"EDITRIGHTSDATA"</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src125" class="srcSentence">No additional information</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src126" class="srcSentence">Allow Macros</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src127" class="srcSentence">OBJMODEL</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src128" class="srcSentence">Enables the option to run macros or perform other programmatic or remote access to the content in a document.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src129" class="srcSentence">As the <ui>Allow Programmatic Access</ui> custom policy option.</caps:sentence>
                    <caps:sentence id="src130" class="srcSentence"> Not a per-recipient setting.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence id="src131" class="srcSentence">Allow Macros</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence id="src132" class="srcSentence">Allow Macros</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src133" class="srcSentence">Not applicable</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src134" class="srcSentence">No additional information</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src135" class="srcSentence">Rights included in permissions  levels</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src136" class="srcSentence">Some applications group usage rights together into permissions levels, to make it easier to select usage rights that are typically used together.</caps:sentence>
            <caps:sentence id="src137" class="srcSentence"> These permisisons levels help to abstract a level of complexity from users, so they can choose options that are role-based.</caps:sentence>
            <caps:sentence id="src138" class="srcSentence">  For example, <embeddedLabel>Reviewer</embeddedLabel> and <embeddedLabel>Co-Author</embeddedLabel>.</caps:sentence>
            <caps:sentence id="src139" class="srcSentence"> Although these options often show users a summary of the rights, they might not include every right that is listed in the previous table.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src140" class="srcSentence">Use the following table for a list of these permissions levels and a complete list of the rights that they contain.</caps:sentence>
          </para>
          <table border="1">
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src141" class="srcSentence">Permissions Level</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src142" class="srcSentence">Applications</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src143" class="srcSentence">Rights included (common name)</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src144" class="srcSentence">Viewer</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src145" class="srcSentence">Azure classic portal</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src146" class="srcSentence">Rights Management sharing application for Windows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src147" class="srcSentence">View, Open, Read</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src148" class="srcSentence">Reply</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src149" class="srcSentence">Reply All</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src150" class="srcSentence">Reviewer</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src151" class="srcSentence">Azure classic portal</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src152" class="srcSentence">Rights Management sharing application for Windows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src153" class="srcSentence">View, Open, Read</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src154" class="srcSentence">Save</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src155" class="srcSentence">Edit Content, Edit</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src156" class="srcSentence">Reply<superscript>*</superscript></caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src157" class="srcSentence">Reply All<superscript>*</superscript></caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src158" class="srcSentence">Forward<superscript>*</superscript></caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src159" class="srcSentence">Co-Author</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src160" class="srcSentence">Azure classic portal</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src161" class="srcSentence">Rights Management sharing application for Windows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src162" class="srcSentence">View, Open, Read</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src163" class="srcSentence">Save</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src164" class="srcSentence">Edit Content, Edit
</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src165" class="srcSentence">Copy</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src166" class="srcSentence">View Rights</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src167" class="srcSentence">Change Rights</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src168" class="srcSentence">Allow Macros</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src169" class="srcSentence">Save As, Export</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src170" class="srcSentence">Print</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src171" class="srcSentence">Reply<superscript>*</superscript></caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src172" class="srcSentence">Reply All<superscript>*</superscript></caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src173" class="srcSentence">Forward<superscript>*</superscript></caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src174" class="srcSentence">Co-Owner</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src175" class="srcSentence">Azure classic portal</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src176" class="srcSentence">Rights Management sharing application for Windows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src177" class="srcSentence">View, Open, Read</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src178" class="srcSentence">Save</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src179" class="srcSentence">Edit Content, Edit
</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src180" class="srcSentence">Copy</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src181" class="srcSentence">View Rights</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src182" class="srcSentence">Change Rights</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src183" class="srcSentence">Allow Macros</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src184" class="srcSentence">Save As, Export</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src185" class="srcSentence">Print</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src186" class="srcSentence">Reply<superscript>*</superscript></caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src187" class="srcSentence">Reply All<superscript>*</superscript></caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src188" class="srcSentence">Forward<superscript>*</superscript></caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src189" class="srcSentence">Full Control</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <caps:sentence id="src190" class="srcSentence">
              <superscript>*</superscript> Not applicable to the Rights Management sharing application for Windows</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src191" class="srcSentence">Rights included in the default templates</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src192" class="srcSentence">The rights that are included with the default templates are as follows:</caps:sentence>
          </para>
          <table border="1">
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src193" class="srcSentence">Display Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src194" class="srcSentence">Rights included (common name) </caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src195" class="srcSentence">&lt;organization name&gt; - Confidential View Only</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src196" class="srcSentence">View, Open, Read</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <caps:sentence id="src197" class="srcSentence"> <para>&lt;organization name&gt; - Confidential</para></caps:sentence>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src198" class="srcSentence">View, Open, Read</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src199" class="srcSentence">Save</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src200" class="srcSentence">Edit Content, Edit</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src201" class="srcSentence">View Rights</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src202" class="srcSentence">Allow Macros</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src203" class="srcSentence">Forward</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src204" class="srcSentence">Reply</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src205" class="srcSentence">Reply All</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="206a0bfe-0912-4e0e-aa15-484b000b264c">Configuring Azure Rights Management</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>