---
title: Migraci&#243;n desde AD RMS a Azure Rights Management
ms.custom: na
ms.reviewer: na
ms.service: rights-management
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 828cf1f7-d0e7-4edf-8525-91896dbe3172
---
# Migraci&#243;n desde AD RMS a Azure Rights Management
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="es-ES">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="7e1093f11a5de031bec12bda815bee57" id="tgt1" class="tgtSentence">Use el siguiente conjunto de instrucciones para migrar su implementación de Active Directory Rights Management Services (AD RMS) en Azure Rights Management (Azure RMS).</caps:sentence>
          <caps:sentence sentenceid="1fc10734b5a495bb1694a544301201c5" id="tgt2" class="tgtSentence"> Después de la migración, los usuarios seguirán teniendo acceso a documentos y mensajes de correo electrónico que su organización protege mediante AD RMS, mientras que el contenido protegido recientemente usará Azure RMS.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="f1f77b5de4e8083120506a9394617442" id="tgt3" class="tgtSentence">¿No está seguro de si esta migración de AD RMS es conveniente para su organización?</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="1b4cba74d699f78e0dee21550f909cdb" id="tgt4" class="tgtSentence">Para obtener una introducción a Azure RMS, los problemas empresariales que puede resolver, cómo lo ven administradores y usuarios y cómo funciona, consulte <link xlink:href="aeeebcd7-6646-4405-addf-ee1cc74df5df">What is Azure Rights Management?</link></caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="0450240d9c722338056c9ad6de10cb77" id="tgt5" class="tgtSentence">Para obtener una comparación entre Azure RMS y AD RMS, consulte <link xlink:href="8123bd62-1814-4d79-b306-e20c1a00e264">Comparing Azure Rights Management and AD RMS</link>.</caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="5628de21bd65d29e43995c98b581fb4c" id="tgt6" class="tgtSentence">Requisitos previos para la migración desde AD RMS a Azure RMS.</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="464db707f8d458530d2faa8267ef40f9" id="tgt7" class="tgtSentence">Antes de iniciar la migración a Azure RMS, asegúrese de que se cumplen los siguientes requisitos previos y de que conoce las limitaciones.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ba12fb48e2d23bb2bd2819f64d02ec7e" id="tgt8" class="tgtSentence">Requisito</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5dc731e46ae38b87ff3e3e2eaf459db2" id="tgt9" class="tgtSentence">Más información</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8c09c4ba1af9e8b2527a29a424486a91" id="tgt10" class="tgtSentence">Una implementación de RMS compatible</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a4618ccf08306a67fc9a8df7c8d82827" id="tgt11" class="tgtSentence">Todas las versiones de Windows Server 2008 a Windows Server 2012 R2 de AD RMS admiten una migración a Azure RMS:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="b33d517673e01450cdc5dd68f42d526f" id="tgt12" class="tgtSentence">Windows Server 2008 (x86 o x64)</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="5b49d77d595e430fb98a078e8af23ff9" id="tgt13" class="tgtSentence">Windows Server 2008 R2 (x64)</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="8c3656681a6763ef49ffe59d9ae8208b" id="tgt14" class="tgtSentence">Windows Server 2012 (x64)</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="cfb81116c57d2d5bbe86aaadd996b205" id="tgt15" class="tgtSentence">Windows Server 2012 R2 (x64)</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <alert class="note">
                    <para>
                      <caps:sentence sentenceid="2ae22f44d0fa5149950d578528edfc21" id="tgt16" class="tgtSentence">Si está ejecutando Windows RMS en Windows Server 2003, esta versión del sistema operativo quedará fuera del soporte técnico durante 2015.</caps:sentence>
                      <caps:sentence sentenceid="70981c284a7509c571c31779289ffe68" id="tgt17" class="tgtSentence"> Puede migrar esta versión de RMS a Azure RMS, pero este proceso solo se admite si todavía se admite el sistema operativo.</caps:sentence>
                      <caps:sentence sentenceid="93fadfc4f84f023636c830010449d31c" id="tgt18" class="tgtSentence"> Como alternativa, puede importar el dominio de publicación de confianza (TPD) a una versión de AD RMS que es compatible y, a continuación, volver a importar el TPD sin la opción de compatibilidad de RMS 1.0.</caps:sentence>
                      <caps:sentence sentenceid="1f5f606b4ae46273756548ceeb471e8d" id="tgt19" class="tgtSentence"> Para obtener más información sobre TPD, consulte <externalLink><linkText>Dominio de publicación de confianza</linkText><linkUri>http://technet.microsoft.com/library/dd996639(v=ws.10).aspx</linkUri></externalLink></caps:sentence>
                    </para>
                  </alert>
                  <para>
                    <caps:sentence sentenceid="7ac523a739204bc8a0fd195097224b76" id="tgt20" class="tgtSentence">Se admiten todas las topologías de AD RMS válidas:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="aa541a950d7c0be5f5379fdb4e3688a6" id="tgt21" class="tgtSentence">Bosque único, un solo clúster de RMS</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="9d6c47c780c3c79f7de85d5bedaef053" id="tgt22" class="tgtSentence">Bosque único, varios clústeres de RMS solo con licencias</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="9e0660df87010fc22772e4272acd7dbd" id="tgt23" class="tgtSentence">Varios bosques, varios clústeres de RMS</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <alert class="note">
                    <para>
                      <caps:sentence sentenceid="55f86f0427e122442e1af8fb7c177d8c" id="tgt24" class="tgtSentence">De forma predeterminada, varios clústeres de RMS se migran a un solo inquilino de Azure RMS.</caps:sentence>
                      <caps:sentence sentenceid="937f9b4b6b4a8e446bbde7d3a82237c6" id="tgt25" class="tgtSentence"> Si desea distintos inquilinos de RMS, debe tratarlos como migraciones diferentes.</caps:sentence>
                      <caps:sentence sentenceid="c46d3d0f13b0b4cc7c8c46ca341dbee1" id="tgt26" class="tgtSentence"> No se puede importar una clave de un clúster de RMS a más de un inquilino de Azure RMS.</caps:sentence>
                    </para>
                  </alert>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1b8f14374bc6cd88798b18d698fa0ec5" id="tgt27" class="tgtSentence">Todos los requisitos para ejecutar Azure RMS, lo que incluye un inquilino de Azure RMS (no activado)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4462659de4d522ffbc363a78e3f7fd9f" id="tgt28" class="tgtSentence">Consulte <link xlink:href="dc78321d-d759-4653-8818-80da74b6cdeb">Requirements for Azure Rights Management</link>.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="5b4aedae3914c0fb85692e4739501835" id="tgt29" class="tgtSentence">Aunque debe tener un inquilino de Azure RMS para poder migrar desde AD RMS, se recomienda que no active el servicio Rights Management antes de la migración.</caps:sentence>
                    <caps:sentence sentenceid="b1dc2ea89658fb844cc7318be2badd36" id="tgt30" class="tgtSentence"> El proceso de migración incluye este paso después de exportar las claves y plantillas de AD RMS e importarlas en Azure RMS.</caps:sentence>
                    <caps:sentence sentenceid="ab77b94551487a9d00c1995e82f86b5a" id="tgt31" class="tgtSentence"> Sin embargo, aunque esté activado Azure RMS, puede migrar desde AD RMS.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="09189aa7fb0d0b633f119604b093ac0d" id="tgt32" class="tgtSentence">Preparación para Azure RMS:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="8ecd274a2b3ef0b0fe4ec034bcc2d721" id="tgt33" class="tgtSentence">Sincronización de directorios entre el directorio local y Azure Active Directory</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="d03d4eeeaaf82ae4ba6349c1c3822ada" id="tgt34" class="tgtSentence">Grupos habilitados para correo en Azure Active Directory</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4462659de4d522ffbc363a78e3f7fd9f" id="tgt35" class="tgtSentence">Consulte <link xlink:href="afbca2d6-32a7-4bda-8aaf-9f93f5da5abc">Preparing for Azure Rights Management</link>.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cf6da7690e2f4fcbcbd33fe6bf65bef3" id="tgt36" class="tgtSentence">Si ha usado la funcionalidad Information Rights Management (IRM) de Exchange Server (por ejemplo, las reglas de transporte y Outlook Web Access) o SharePoint Server con AD RMS:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="69194a3ca7b97af28634a43befc9823f" id="tgt37" class="tgtSentence">Plan durante un breve período de tiempo si IRM no estará disponible en estos servidores</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2c4963a25e25da3add0b0250dbf40fba" id="tgt38" class="tgtSentence">Aún puede utilizar IRM en estos servidores con Azure RMS después de la migración.</caps:sentence>
                    <caps:sentence sentenceid="5886b7adf35c4d8a1bd656b8d330ca17" id="tgt39" class="tgtSentence"> Sin embargo, uno de los pasos de migración es deshabilitar temporalmente el servicio IRM, instalar y configurar un conector, volver a configurar los servidores y, a continuación, volver a habilitar IRM.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="05d67ef2b02b32aa29c30c2019652b18" id="tgt40" class="tgtSentence">Se trata de la única interrupción del servicio durante el proceso de migración.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <caps:sentence sentenceid="d2f2ded167a3bc2d5846271643e6d4a3" id="tgt41" class="tgtSentence">Limitaciones:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="7045979f47814ad634a33b1d72db2c10" id="tgt42" class="tgtSentence">Aunque el proceso de migración permite migrar la clave del certificado de licencias del servidor (SLC) a un módulo de seguridad de hardware (HSM) para Azure RMS, Exchange Online actualmente no admite esta configuración. Si desea usar Exchange Online con Azure RMS, la clave del inquilino de Azure RMS debe estar <externalLink><linkText>administrada por Microsoft</linkText><linkUri>http://technet.microsoft.com/library/dn440580.aspx</linkUri></externalLink>. Como alternativa, puede ejecutar IRM con funcionalidad reducida en Exchange Online cuando sea el usuario quien  administre el inquilino de Azure RMS (BYOK). Para obtener más información acerca del uso de Exchange Online con Azure RMS, vea <link xlink:href="#BKMK_Step6Migration">Step 6. Configure IRM integration for Exchange Online</link> en estas instrucciones.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="c76c74fb4f3e617b7225abe3010aa8e8" id="tgt43" class="tgtSentence">Si tiene software y clientes que no son compatibles con Azure RMS, no podrá proteger o consumir contenido protegido por Azure RMS.</caps:sentence>
                <caps:sentence sentenceid="76d643a5ba1bea30bd2d0ca3c797f33f" id="tgt44" class="tgtSentence"> Asegúrese de consultar la sección de clientes y aplicaciones compatibles en el tema <link xlink:href="dc78321d-d759-4653-8818-80da74b6cdeb">Requirements for Azure Rights Management</link>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="ad5dedaa2ff99bbc93331604a5108441" id="tgt45" class="tgtSentence">Si importa su clave de local a Azure RMS como archivada (sin establecer el TPD como activo durante el proceso de importación) y migra los usuarios en lotes en una migración por fases, el contenido protegido recientemente por los usuarios migrados no será accesible para los usuarios que permanecen en AD RMS.</caps:sentence>
                <caps:sentence sentenceid="04c11e9d679e974b49006806631654f4" id="tgt46" class="tgtSentence"> En este escenario, siempre que sea posible, mantenga un tiempo de migración corto y migre los usuarios en lotes lógicos, de forma que si colaboran entre sí se miren juntos.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="533ed82f5209cbd53fca1f8b47f50dd6" id="tgt47" class="tgtSentence">Esta limitación no se aplica cuando se establece el TPD como activo durante el proceso de importación, porque todos los usuarios protegerán el contenido con la misma clave.</caps:sentence>
                <caps:sentence sentenceid="b7bf882340f8fa084276a093aded0906" id="tgt48" class="tgtSentence"> Se recomienda esta configuración, ya que le permite migrar todos los usuarios de forma independiente y a su propio ritmo.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="59650ba2910c3f7cd10aa37a53ebd08e" id="tgt49" class="tgtSentence">Si colabora con asociados externos (por ejemplo, mediante el uso de la federación o de dominios de usuario de confianza), estos también deberán migrar a Azure RMS al mismo tiempo o tan pronto como sea posible una vez haya completado la migración.</caps:sentence>
                <caps:sentence sentenceid="feb97bb633dea67a239709ac84eba4b9" id="tgt50" class="tgtSentence"> Para seguir teniendo acceso al contenido previamente protegido por su organización con AD RMS, se deberán realizar cambios en la configuración del cliente similares a los que realice el usuario, incluidos en este documento.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="2d97b5d730b78206f98044c79e7725e4" id="tgt51" class="tgtSentence">Debido a las posibles variaciones de configuración de los asociados, las instrucciones exactas para este cambio de configuración están fuera del ámbito de este documento.</caps:sentence>
                <caps:sentence sentenceid="d5cb703e9c63be2d9e5d0cfe3d7ff4f5" id="tgt52" class="tgtSentence"> Para obtener ayuda, póngase en contacto con los servicios de soporte al cliente de Microsoft (CSS).</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="c44752dc608ae1486f687465ec71380b" id="tgt53" class="tgtSentence">Pasos para la migración desde AD RMS a Azure RMS</caps:sentence>
        </title>
        <content>
          <para></para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="249b1959ad300e46d244c63b635f7194" id="tgt54" class="tgtSentence">Pasos del proceso de migración</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5dc731e46ae38b87ff3e3e2eaf459db2" id="tgt55" class="tgtSentence">Más información</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <embeddedLabel>
                      <caps:sentence sentenceid="5dd1c2055143474357639df5f5a3b070" id="tgt56" class="tgtSentence">1. Descargue las herramientas de administración de Azure RMS.</caps:sentence>
                    </embeddedLabel>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f1bcbb94613d91032d33beb396e5a9fb" id="tgt57" class="tgtSentence">Para obtener instrucciones, consulte <link xlink:href="828cf1f7-d0e7-4edf-8525-91896dbe3172#BKMK_Step1Migration">Step 1: Download the Azure Rights Management Administration Tool</link>.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <embeddedLabel>
                      <caps:sentence sentenceid="ba0e05024c12ef76be258f2e2d4cf1db" id="tgt58" class="tgtSentence">2. Exporte los datos de configuración de AD RMS e impórtelos en Azure RMS.</caps:sentence>
                    </embeddedLabel>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c15b04b43569b8a19349feab7c3cd90a" id="tgt59" class="tgtSentence">Exporte los datos de configuración (claves, plantillas y direcciones URL) de AD RMS a un archivo XML y, luego, cargue ese archivo en Azure RMS mediante el cmdlet Import-AadrmTPD de Windows PowerShell.</caps:sentence>
                    <caps:sentence sentenceid="c6d836a701d21e2d9cc18234cd4140dc" id="tgt60" class="tgtSentence"> Podrían ser necesarios pasos adicionales, dependiendo de la configuración de claves de AD RMS:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="083c7bb86d0bca53c5b02e9406b21056" id="tgt61" class="tgtSentence">Migración entre claves protegidas de software: De claves basadas en contraseña administradas centralmente en AD RMS a clave de inquilino de Azure RMS administrada por Microsoft.</caps:sentence>
                        <caps:sentence sentenceid="248cf34360a22dba69726af20714a564" id="tgt62" class="tgtSentence"> Esta es la ruta de migración más sencilla y no se necesita ningún paso adicional.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="b79366ad4da5a2a9b7e9bc00604c4616" id="tgt63" class="tgtSentence">Migración entre claves protegidas por HSM: De claves almacenadas por un módulo de seguridad de hardware (HSM) para AD RMS a clave de inquilino de Azure RMS administrada por el cliente (el escenario "aporte su propia clave" o BYOK).</caps:sentence>
                        <caps:sentence sentenceid="151d3e02771181e35d02c16b561d0231" id="tgt64" class="tgtSentence"> Esto requiere pasos adicionales para transferir la clave de HSM de Thales local a HSM de Azure RMS.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="847ea4b718777808c8e1dc9711ea2e87" id="tgt65" class="tgtSentence">Migración de clave protegida por software a clave protegida por HSM: Claves basadas en contraseña administradas centralmente en AD RMS para la clave del inquilino de Azure RMS administrada por clientes (el escenario "bring your own key" o "BYOK").</caps:sentence>
                        <caps:sentence sentenceid="c815745846edb8cef716ed34bde85a7e" id="tgt66" class="tgtSentence"> Aquí es necesario realizar la mayor parte de la configuración, porque debe extraer primero la clave de software e importarla a un HSM local y, a continuación, realizar los pasos adicionales para transferir la clave del HSM local de Thales al HSM de Azure RMS.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence sentenceid="f1bcbb94613d91032d33beb396e5a9fb" id="tgt67" class="tgtSentence">Para obtener instrucciones, consulte <link xlink:href="828cf1f7-d0e7-4edf-8525-91896dbe3172#BKMK_Step2Migration">Step 2. Export configuration data from AD RMS and import it to Azure RMS</link>.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <embeddedLabel>
                      <caps:sentence sentenceid="5a3f6c2098cb9f7e242273dd7923e245" id="tgt68" class="tgtSentence">3. Active el inquilino de RMS.</caps:sentence>
                    </embeddedLabel>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2c680cdefdce9364458747ce841533cb" id="tgt69" class="tgtSentence">Si es posible, realice este paso después del proceso de importación y no antes.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="3dad81dd51d8bde90a1e99c299ce2323" id="tgt70" class="tgtSentence">Para obtener más información e instrucciones sobre este tema, consulte <link xlink:href="828cf1f7-d0e7-4edf-8525-91896dbe3172#BKMK_Step3Migration">Step 3. Activate your RMS tenant</link>.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <embeddedLabel>
                      <caps:sentence sentenceid="8ce4d085869ea294d3fcebb64c17136a" id="tgt71" class="tgtSentence">4. Configure las plantillas importadas.</caps:sentence>
                    </embeddedLabel>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="08c2ba72e673a3e9402928261199ddd9" id="tgt72" class="tgtSentence">Al importar las plantillas de directiva de derechos, su estado se archiva.</caps:sentence>
                    <caps:sentence sentenceid="8aaca0e3f9f4c7fecf1d94bb31db19cb" id="tgt73" class="tgtSentence"> Si quiere que los usuarios puedan verla y usarla, debe cambiar el estado de la plantilla a publicada en el Portal de Azure clásico.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="f1bcbb94613d91032d33beb396e5a9fb" id="tgt74" class="tgtSentence">Para obtener instrucciones, consulte <link xlink:href="828cf1f7-d0e7-4edf-8525-91896dbe3172#BKMK_Step4Migration">Step 4. Configure imported templates</link>.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <embeddedLabel>
                      <caps:sentence sentenceid="36bc033d5901e8e02c5002d980d60330" id="tgt75" class="tgtSentence">5. Vuelva a configurar los clientes para usar Azure RMS.</caps:sentence>
                    </embeddedLabel>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d790da94e39cb677936e6eeb11395b79" id="tgt76" class="tgtSentence">Debe volver a configurar los equipos de Windows existentes para utilizar el servicio de Azure RMS en lugar de AD RMS.</caps:sentence>
                    <caps:sentence sentenceid="355b2210f20722b85725ea57fa3f1f41" id="tgt77" class="tgtSentence"> Este paso se aplica a los equipos de su organización y en los equipos de las organizaciones asociadas si ha colaborado con ellas al ejecutar AD RMS.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="7ad5d9d2cdac24f0ee616a66e1c39ea0" id="tgt78" class="tgtSentence">Además, si ha implementado las <externalLink><linkText>extensiones para dispositivos móviles</linkText><linkUri>http://technet.microsoft.com/library/dn673574.aspx</linkUri></externalLink> para admitir dispositivos móviles como iPads y teléfonos iOS, teléfonos y tabletas Android, Windows Phone y equipos Mac, debe quitar los registros SRV en DNS que redirigen estos clientes para usar AD RMS.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="f1bcbb94613d91032d33beb396e5a9fb" id="tgt79" class="tgtSentence">Para obtener instrucciones, consulte <link xlink:href="828cf1f7-d0e7-4edf-8525-91896dbe3172#BKMK_Step5Migration">Step 5. Reconfigure clients to use Azure RMS</link>.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <embeddedLabel>
                      <caps:sentence sentenceid="f2632949f5cb705ab557a07f0a1b2e55" id="tgt80" class="tgtSentence">6. Configure la integración de IRM con Exchange Online.</caps:sentence>
                    </embeddedLabel>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="94ed4585c34b26e1c82a821e74d23a22" id="tgt81" class="tgtSentence">Este paso es necesario si desea usar Exchange Online con Azure RMS.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="f1bcbb94613d91032d33beb396e5a9fb" id="tgt82" class="tgtSentence">Para obtener instrucciones, consulte <link xlink:href="#BKMK_Step6Migration">Step 6. Configure IRM integration for Exchange Online</link>.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <embeddedLabel>
                      <caps:sentence sentenceid="140da34a0e8f8faf3106d69800ecc7d5" id="tgt83" class="tgtSentence">7. Implemente el conector RMS.</caps:sentence>
                    </embeddedLabel>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="89a43e63b6d3568dbbea9c788ac5356a" id="tgt84" class="tgtSentence">Este paso es necesario si desea utilizar cualquiera de los siguientes servicios locales con Azure RMS:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="3dda89d997b4887b0621a65c9276e65f" id="tgt85" class="tgtSentence">Exchange Server (por ejemplo, las reglas de transporte y Outlook Web Access)</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="7d2daf2c6bc276a6baf2ca2f452c6496" id="tgt86" class="tgtSentence">Servidor de SharePoint </caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="0f9d889aedcac973e41b8531c65b8b2d" id="tgt87" class="tgtSentence">Windows Server que se ejecuta la infraestructura de clasificación de archivos</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence sentenceid="f1bcbb94613d91032d33beb396e5a9fb" id="tgt88" class="tgtSentence">Para obtener instrucciones, consulte <link xlink:href="#BKMK_Step7Migration">Step 7. Deploy the RMS connector</link>.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt89" class="tgtSentence">
                      <embeddedLabel>8. Retire AD RMS</embeddedLabel>. </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cffedc4ac3b2e3b4f1bfd1908f34fb0c" id="tgt90" class="tgtSentence">Cuando haya confirmado que todos los clientes usan Azure RMS y ya no obtienen acceso a los servidores de AD RMS, puede retirar la implementación de AD RMS.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="f1bcbb94613d91032d33beb396e5a9fb" id="tgt91" class="tgtSentence">Para obtener instrucciones, consulte <link xlink:href="#BKMK_Step8Migration">Step 8. Decommission AD RMS</link>.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <embeddedLabel>
                      <caps:sentence sentenceid="e44252b7e2b0818adae058a8f50bed7c" id="tgt92" class="tgtSentence">9. Vuelva a escribir su clave de inquilino de Azure RMS.</caps:sentence>
                    </embeddedLabel>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="64d64f2292c30071e0b54747793b151c" id="tgt93" class="tgtSentence">Este paso es necesario si no estaba realizando la ejecución en modo criptográfico 2 antes de la migración y es opcional pero recomendado para que todas las migraciones ayuden a proteger la seguridad de la clave de inquilino de Azure RMS.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="f1bcbb94613d91032d33beb396e5a9fb" id="tgt94" class="tgtSentence">Para obtener instrucciones, consulte <link xlink:href="#BKMK_Step9Migration">Step 9. Re-key your Azure RMS tenant key</link>.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
        <sections>
          <section address="BKMK_Step1Migration">
            <title>
              <caps:sentence sentenceid="7805b4aef1ee01bb46d3e3066c48c22c" id="tgt95" class="tgtSentence">Paso 1: Descargue la herramienta de administración de Azure Rights Management</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="569fffc045110bd6191896e6504d5ee6" id="tgt96" class="tgtSentence">Vaya al Centro de descarga de Microsoft y descargue la <externalLink><linkText>herramienta de administración de Azure Rights Management</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=257721</linkUri></externalLink>, que contiene el módulo de administración de Azure RMS para Windows PowerShell.</caps:sentence>
              </para>
            </content>
          </section>
          <section address="BKMK_Step2Migration">
            <title>
              <caps:sentence sentenceid="bbda0a46b68df43bb2a6abe0b891d724" id="tgt97" class="tgtSentence">Paso 2.</caps:sentence>
              <caps:sentence sentenceid="3a70e246ce81a5a8263af846eafd4519" id="tgt98" class="tgtSentence"> Exporte los datos de configuración de AD RMS e impórtelos en Azure RMS.</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="514542f0d85c4624fe4ddbd36177d435" id="tgt99" class="tgtSentence">Este paso es un proceso de dos fases:</caps:sentence>
              </para>
              <list class="ordered">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="0e3f916eef8ead3f8780cebc0df6fa84" id="tgt100" class="tgtSentence">Exporte los datos de configuración de AD RMS mediante la exportación de los dominios de publicación de confianza (TPD) a un archivo .xml.</caps:sentence>
                    <caps:sentence sentenceid="6a848f8ebb16d9f58d2a7ea4d2c61742" id="tgt101" class="tgtSentence"> Este proceso es el mismo para todas las migraciones.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="8c9d05771a9c8c5d9fb961ea6455f684" id="tgt102" class="tgtSentence">Importe los datos de configuración a Azure RMS.</caps:sentence>
                    <caps:sentence sentenceid="f48cec05328a3a3092c6a88f6d3fd85d" id="tgt103" class="tgtSentence"> Hay diferentes procesos para este paso, según la configuración de la implementación de AD RMS actual y la topología preferida para su clave de inquilino de Azure RMS.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
            <sections>
              <section>
                <title>
                  <caps:sentence sentenceid="a927df83adb490dccc1e9c178b4b52ea" id="tgt104" class="tgtSentence">Exportar los datos de configuración de AD RMS</caps:sentence>
                </title>
                <content>
                  <para>
                    <caps:sentence sentenceid="c6c0f805f214b635d7b303be0955fb3a" id="tgt105" class="tgtSentence">Siga este procedimiento en todos los clústeres de AD RMS, para todos los dominios de publicación confianza que tienen contenido protegido de su organización.</caps:sentence>
                    <caps:sentence sentenceid="d41c234d6ccf9e3b52dea221094a80b2" id="tgt106" class="tgtSentence"> No es necesario ejecutar esto en clústeres solo para licencias.</caps:sentence>
                  </para>
                  <alert class="note">
                    <para>
                      <caps:sentence sentenceid="938561b99440632029af4d54e4ee67fa" id="tgt107" class="tgtSentence">Si utiliza Windows Server 2003 Rights Management, en lugar de estas instrucciones, siga el procedimiento <externalLink><linkText>Exportar clave privada de SLC, TUD, TPD y RMS</linkText><linkUri>http://technet.microsoft.com/library/jj835767(v=ws.10).aspx</linkUri></externalLink> desde el tema <externalLink><linkText>Migración desde Windows RMS a AD RMS en una estructura distinta</linkText><linkUri>http://technet.microsoft.com/library/jj835767(v=ws.10).aspx</linkUri></externalLink>.</caps:sentence>
                    </para>
                  </alert>
                  <procedure>
                    <title>
                      <caps:sentence sentenceid="96b8c7cc965fba3b6e5ae99fc1f084e1" id="tgt108" class="tgtSentence">Para exportar los datos de configuración (información del dominio de publicación de confianza)</caps:sentence>
                    </title>
                    <steps class="ordered">
                      <step>
                        <content>
                          <para>
                            <caps:sentence sentenceid="754c08bccb0f094ae7a6da26b52c1c5a" id="tgt109" class="tgtSentence">Inicie sesión en el clúster de AD RMS como un usuario con permisos de administración de AD RMS.</caps:sentence>
                          </para>
                        </content>
                      </step>
                      <step>
                        <content>
                          <para>
                            <caps:sentence sentenceid="952d3e6193558e6b9cf79493fafae4a7" id="tgt110" class="tgtSentence">Desde la consola de administración de AD RMS (<ui>Active Directory Rights Management Services</ui>), expanda el nombre del clúster de AD RMS, expanda <ui>Directivas de confianza</ui> y luego haga clic en <ui>Dominios de publicación de confianza</ui>.</caps:sentence>
                          </para>
                        </content>
                      </step>
                      <step>
                        <content>
                          <para>
                            <caps:sentence sentenceid="1ac874db7a207ce084ea06f3d2c4ccb2" id="tgt111" class="tgtSentence">En el panel de resultados, seleccione el dominio de publicación de confianza y luego, en el panel Acciones, haga clic en <ui>Exportar dominio de publicación de confianza</ui>.</caps:sentence>
                          </para>
                        </content>
                      </step>
                      <step>
                        <content>
                          <para>
                            <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt112" class="tgtSentence">En el cuadro de diálogo <ui>Exportar dominio de publicación de confianza</ui>: </caps:sentence>
                          </para>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="ccbe2a6c96a5df5e1966988e40064061" id="tgt113" class="tgtSentence">Haga clic en <ui>Guardar como</ui> y guárdelo en la ruta de acceso con un nombre de archivo de su elección.</caps:sentence>
                                <caps:sentence sentenceid="94326ec278af6643af1d92bfa45d7a0c" id="tgt114" class="tgtSentence"> Asegúrese de especificar <userInput>.xml</userInput> como la extensión de nombre de archivo (no se adjunta automáticamente).</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="f2cbdf8071427b0d9f28809710ce3c21" id="tgt115" class="tgtSentence">Especifique y confirme una contraseña segura.</caps:sentence>
                                <caps:sentence sentenceid="01960238fe98c1a575c1cff4c51fad09" id="tgt116" class="tgtSentence"> Recuerde esta contraseña, porque la necesitará más adelante, al importar los datos de configuración a Azure RMS.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="93043851f494b0f5951a50628b8b220a" id="tgt117" class="tgtSentence">No seleccione la casilla para guardar el archivo de dominio de confianza en RMS 1.0.</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </content>
                      </step>
                    </steps>
                    <conclusion>
                      <content>
                        <para>
                          <caps:sentence sentenceid="80db68cac396143711c135bff9c4904b" id="tgt118" class="tgtSentence">Cuando se exportan todos los dominios de publicación de confianza, está listo para empezar el procedimiento para importar estos datos en Azure RMS.</caps:sentence>
                        </para>
                      </content>
                    </conclusion>
                  </procedure>
                </content>
              </section>
              <section>
                <title>
                  <caps:sentence sentenceid="68e772f492c3ebc8b7a3f29b2fb84376" id="tgt119" class="tgtSentence">Importar los datos de configuración a Azure RMS</caps:sentence>
                </title>
                <content>
                  <para>
                    <caps:sentence sentenceid="f3fa2011be807b30894fe8895bfe595c" id="tgt120" class="tgtSentence">Los procedimientos exactos para este paso dependen de la configuración actual de la implementación de AD RMS y de la topología preferida para su clave de inquilino de Azure RMS.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="22834af228ea32cbd0ff163a5e9b6331" id="tgt121" class="tgtSentence">La implementación de AD RMS actual usará una de las siguientes configuraciones con la clave del certificado emisor de licencias de servidor (SLC):</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="a95a6f19e6157f4b93df09df5b6edcf8" id="tgt122" class="tgtSentence">Protección con contraseña de la base de datos de AD RMS.</caps:sentence>
                        <caps:sentence sentenceid="32d0aeb2cbb512efc1db0c2d91b22d05" id="tgt123" class="tgtSentence"> Se trata de la configuración predeterminada.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="8495b16466dcd05f59a7eafb503e325a" id="tgt124" class="tgtSentence">Protección de HSM mediante el uso de un módulo de seguridad de hardware (HSM) de Thales.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="fb54f72e2ce58ea366653d0e0f5762a8" id="tgt125" class="tgtSentence">Protección de HSM mediante un módulo de seguridad de hardware (HSM) desde un proveedor distinto de Thales.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="c2eb35576d4bdaaf85e56ded33b3f45d" id="tgt126" class="tgtSentence">Contraseña protegida mediante un proveedor criptográfico externo.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <alert class="note">
                    <para>
                      <caps:sentence sentenceid="4a4ed69a5659a845b02f4807627c230c" id="tgt127" class="tgtSentence">Para obtener más información acerca del uso de módulos de seguridad de hardware con AD RMS, consulte <externalLink><linkText>Uso de AD RMS con módulos de seguridad de hardware</linkText><linkUri>http://technet.microsoft.com/library/jj651024.aspx</linkUri></externalLink>.</caps:sentence>
                    </para>
                  </alert>
                  <para>
                    <caps:sentence sentenceid="47287a38c1798822432c179a565636c1" id="tgt128" class="tgtSentence">Las dos opciones de topología de clave de inquilino de Azure RMS son: Microsoft administra su clave de inquilino (<embeddedLabel>administrada por Microsoft</embeddedLabel>), o bien es el usuario quien se encarga de ello (<embeddedLabel>administrada por el cliente</embeddedLabel>).</caps:sentence>
                    <caps:sentence sentenceid="50be791a7cb39cce9b952df378a3730d" id="tgt129" class="tgtSentence"> Cuando administra su propia clave de inquilino de Azure RMS, esto se conoce a veces como "aporte su propia clave" (BYOK) y requiere un módulo de seguridad de hardware (HSM) de Thales.</caps:sentence>
                    <caps:sentence sentenceid="be021ab36c2c99a549fc25f5fcee238c" id="tgt130" class="tgtSentence"> Para obtener más información, consulte la sección <link xlink:href="f0d33c5f-a6a6-44a1-bdec-5be1bc8e1e14#BKMK_ChooseTenantKey">Choose your tenant key topology: Managed by Microsoft (the default) or managed by you (BYOK)</link> en el tema <link xlink:href="f0d33c5f-a6a6-44a1-bdec-5be1bc8e1e14">Planning and Implementing Your Azure Rights Management Tenant Key</link>.</caps:sentence>
                  </para>
                  <alert class="important">
                    <para>
                      <caps:sentence sentenceid="75d863f411e139d0a683b954fe84aa85" id="tgt131" class="tgtSentence"> Actualmente, BYOK de Azure RMS no es compatible con Exchange Online.</caps:sentence>
                      <caps:sentence sentenceid="0e96c6c6fe380419563490e0d5843430" id="tgt132" class="tgtSentence">  Si desea usar BYOK después de la migración y planea usar Exchange Online, asegúrese de que comprende de qué forma esta configuración reduce la funcionalidad IRM para Exchange Online.</caps:sentence>
                      <caps:sentence sentenceid="876b8591adaaf6947b953603981b230a" id="tgt133" class="tgtSentence"> Revise la información de la sección <link xlink:href="f0d33c5f-a6a6-44a1-bdec-5be1bc8e1e14#BKMK_Pricing">BYOK pricing and restrictions</link> del tema <link xlink:href="f0d33c5f-a6a6-44a1-bdec-5be1bc8e1e14">Planning and Implementing Your Azure Rights Management Tenant Key</link> para ayudarle a elegir la mejor topología de clave de inquilino de Azure RMS para la migración.</caps:sentence>
                    </para>
                  </alert>
                  <para>
                    <caps:sentence sentenceid="d9fb47d43d938970982d27ef116e1927" id="tgt134" class="tgtSentence">Utilice la tabla siguiente para identificar qué procedimiento se utilizará para la migración.</caps:sentence>
                    <caps:sentence sentenceid="a0cd56ea813cdfd0fdce182e4c17b1f3" id="tgt135" class="tgtSentence"> No se admiten las combinaciones que no aparecen.</caps:sentence>
                  </para>
                  <table>
                    <thead>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="55bcf4aa8c710228c1687091120c1f8e" id="tgt136" class="tgtSentence">Implementación de AD RMS actual</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="42b6eea116fe2f5c1c1ec42ac067573f" id="tgt137" class="tgtSentence">Topología de clave de inquilino de Azure RMS elegida</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="635c0bbff8d67282bf2607b2dc797c4f" id="tgt138" class="tgtSentence">Instrucciones de migración</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </thead>
                    <tbody>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="7a27d6340f65f47727bf6a7923f48571" id="tgt139" class="tgtSentence">Protección con contraseña de la base de datos de AD RMS</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="c5fb0d393ff6dd6a4e8740a507704f5a" id="tgt140" class="tgtSentence">Administrada por Microsoft:</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="abda7877548e2693387fce7b54bf4008" id="tgt141" class="tgtSentence">Consulte el procedimiento <embeddedLabel>Migración entre claves protegidas por software</embeddedLabel> después de esta tabla.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence sentenceid="1cf2ec56d8c98b2d3dff7a9e80d74358" id="tgt142" class="tgtSentence">Esta es la ruta de migración más sencilla y solo requiere que transfiera los datos de configuración a Azure RMS.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="a2038560ad20a765998daa21a9ba9a90" id="tgt143" class="tgtSentence">Protección de HSM mediante el uso de un módulo de seguridad de hardware (HSM) de Thales nShield</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="bb42b180ba57d0d33beaafa4ec1de882" id="tgt144" class="tgtSentence">Administrada por el cliente (BYOK)</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="abda7877548e2693387fce7b54bf4008" id="tgt145" class="tgtSentence">Consulte el procedimiento <embeddedLabel>Migración entre claves protegidas por HSM</embeddedLabel> después de esta tabla.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence sentenceid="49cdd820f8e663f23c1fee45b68a8214" id="tgt146" class="tgtSentence">Esto requiere el conjunto de herramientas BYOK y dos conjuntos de pasos para transferir la clave del HSM local al HSM de Azure RMS y, a continuación, transferir los datos de configuración a Azure RMS.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="7a27d6340f65f47727bf6a7923f48571" id="tgt147" class="tgtSentence">Protección con contraseña de la base de datos de AD RMS</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="bb42b180ba57d0d33beaafa4ec1de882" id="tgt148" class="tgtSentence">Administrada por el cliente (BYOK)</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="abda7877548e2693387fce7b54bf4008" id="tgt149" class="tgtSentence">Consulte el procedimiento <embeddedLabel>Migración de clave protegida por software a clave protegida por HSM</embeddedLabel> después de esta tabla.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence sentenceid="e6208ea50baab5801f04a600ddcccdea" id="tgt150" class="tgtSentence">Esto requiere el conjunto de herramientas BYOK y tres conjuntos de pasos para, primero, extraer la clave de software e importarla en un HSM local, después transferir la clave del HSM local al HSM de Azure RMS y, por último, transferir los datos de configuración a Azure RMS.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="1cccf4e07e7352ab837a0c52cc12bcf5" id="tgt151" class="tgtSentence">Protección de HSM mediante un módulo de seguridad de hardware (HSM) desde un proveedor distinto de Thales.</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="bb42b180ba57d0d33beaafa4ec1de882" id="tgt152" class="tgtSentence">Administrada por el cliente (BYOK)</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="0fbbef83992d74ba964154c296f2b7d1" id="tgt153" class="tgtSentence">Póngase en contacto con el proveedor de HSM para obtener instrucciones sobre cómo transferir su clave de este HSM a un módulo de seguridad de hardware (HSM) de Thales nShield.</caps:sentence>
                            <caps:sentence sentenceid="a4c97bd314b44cc9ee64777264117bf4" id="tgt154" class="tgtSentence"> A continuación, siga las instrucciones del procedimiento <embeddedLabel>Migración entre claves protegidas por HSM</embeddedLabel> después de esta tabla.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="fbf74c8a30e188f501f77cce6b17f673" id="tgt155" class="tgtSentence">Contraseña protegida mediante un proveedor criptográfico externo.</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="bb42b180ba57d0d33beaafa4ec1de882" id="tgt156" class="tgtSentence">Administrada por el cliente (BYOK)</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="c133b46736ecd35151ad19d805c089ec" id="tgt157" class="tgtSentence">Póngase en contacto con el proveedor criptográfico para obtener instrucciones sobre cómo transferir su clave a un módulo de seguridad de hardware (HSM) de Thales nShield.</caps:sentence>
                            <caps:sentence sentenceid="a4c97bd314b44cc9ee64777264117bf4" id="tgt158" class="tgtSentence"> A continuación, siga las instrucciones del procedimiento <embeddedLabel>Migración entre claves protegidas por HSM</embeddedLabel> después de esta tabla.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </tbody>
                  </table>
                  <para>
                    <caps:sentence sentenceid="2b99df0603fbc3ab0b245064051af3da" id="tgt159" class="tgtSentence">Antes de iniciar estos procedimientos, asegúrese de que puede tener acceso a los archivos .xml que creó anteriormente cuando exportó los dominios de publicación de confianza.</caps:sentence>
                    <caps:sentence sentenceid="bf3769f079784f5b46c3cd09f212bfad" id="tgt160" class="tgtSentence"> Por ejemplo, estos podrían estar guardados en una unidad USB que se transfiere desde el servidor de AD RMS a la estación de trabajo conectada a Internet.</caps:sentence>
                  </para>
                  <alert class="security note">
                    <para>
                      <caps:sentence sentenceid="78c4993d05d81a47dfcb2bfcb645029e" id="tgt161" class="tgtSentence">Independientemente de cómo almacene estos datos, aplique las prácticas de seguridad recomendadas para protegerlos, ya que estos incluyen la clave privada.</caps:sentence>
                    </para>
                  </alert>
                </content>
                <sections>
                  <section expanded="false">
                    <title>
                      <caps:sentence sentenceid="43a577cfe853156c7b9287f847f8fa60" id="tgt162" class="tgtSentence">Migración entre claves protegidas por software</caps:sentence>
                    </title>
                    <content>
                      <para>
                        <caps:sentence sentenceid="dc891f09233b1692de4d142e20c73b14" id="tgt163" class="tgtSentence">Utilice este procedimiento para importar la configuración de AD RMS a Azure RMS, que resulta en que la clave del inquilino de Azure RMS la administre Microsoft.</caps:sentence>
                      </para>
                      <procedure>
                        <title>
                          <caps:sentence sentenceid="e080f04ad82c2e0822ae16145b991993" id="tgt164" class="tgtSentence">Para importar los datos de configuración a Azure RMS</caps:sentence>
                        </title>
                        <steps class="ordered">
                          <step>
                            <content>
                              <para>
                                <caps:sentence sentenceid="1a58a0749a5ef4600f28cc3abc7ed4ee" id="tgt165" class="tgtSentence">En una estación de trabajo conectada a Internet, descargue e instale el módulo de Windows PowerShell para Azure RMS (versión mínima 2.1.0.0), que incluye el cmdlet <externalLink><linkText>Import-AadrmTpd</linkText><linkUri>http://msdn.microsoft.com/library/azure/dn857523.aspx</linkUri></externalLink>.</caps:sentence>
                              </para>
                              <alert class="tip">
                                <para>
                                  <caps:sentence sentenceid="ad9de9badcaf0c18cff82a61c9291579" id="tgt166" class="tgtSentence">Si ya descargó e instaló el módulo, compruebe el número de versión. Para ello, ejecute: <codeInline>(Get-Module aadrm -ListAvailable).Version</codeInline></caps:sentence>
                                </para>
                              </alert>
                              <para>
                                <caps:sentence sentenceid="9b8b89d25f443ebfc7497fedc34ed4ca" id="tgt167" class="tgtSentence">Para conocer las instrucciones de instalación, consulte <link xlink:href="0d665ed6-b1de-4d63-854a-bc57c1c49844">Installing Windows PowerShell for Azure Rights Management</link>.</caps:sentence>
                              </para>
                            </content>
                          </step>
                          <step>
                            <content>
                              <para>
                                <caps:sentence sentenceid="986a1e9cf69d28fc407425532bc33082" id="tgt168" class="tgtSentence">Inicie Windows PowerShell con la opción <ui>Ejecutar como administrador</ui> y use el cmdlet <externalLink><linkText>Connect-AadrmService</linkText><linkUri>http://msdn.microsoft.com/library/azure/dn629415.aspx</linkUri></externalLink> para conectarse al servicio de Azure RMS:</caps:sentence>
                              </para>
                              <code>Connect-AadrmService</code>
                              <para>
                                <caps:sentence sentenceid="4029bc06e3eeccb6ce05b9512cc14d97" id="tgt169" class="tgtSentence">Cuando se le pida, escriba las credenciales de administrador de inquilinos de <token>aad_rightsmanagement_1</token> (normalmente, usará una cuenta de administrador global de Office 365 o Azure Active Directory).</caps:sentence>
                              </para>
                            </content>
                          </step>
                          <step>
                            <content>
                              <para>
                                <caps:sentence sentenceid="16859c9da62799922bc88b1c7de34fc3" id="tgt170" class="tgtSentence">Use el cmdlet <externalLink><linkText>Import-AadrmTpd</linkText><linkUri>http://msdn.microsoft.com/library/azure/dn857523.aspx</linkUri></externalLink> para cargar el primer archivo del dominio de publicación de confianza (.xml) exportado.</caps:sentence>
                                <caps:sentence sentenceid="14a9730d980469ea1785fc40d3011ad4" id="tgt171" class="tgtSentence"> Si tiene más de un archivo .xml porque tenía varios dominios de publicación de confianza, elija el archivo que contenga el dominio de publicación de confianza exportado que desee usar en Azure RMS para proteger el contenido después de la migración.</caps:sentence>
                                <caps:sentence sentenceid="8b30551c6f81bc11c5e9502037601555" id="tgt172" class="tgtSentence"> Use el siguiente comando:</caps:sentence>
                              </para>
                              <code>Import-AadrmTpd -TpdFile &lt;PathToTpdPackageFile&gt; -ProtectionPassword -Active $True -Verbose 
</code>
                              <para>
                                <caps:sentence sentenceid="d05370276e06291b048268558cc39bee" id="tgt173" class="tgtSentence">Por ejemplo: <userInput>Import-AadrmTpd -TpdFile E:\contosokey1.xml -ProtectionPassword -Active $true -Verbose</userInput></caps:sentence>
                              </para>
                              <para>
                                <caps:sentence sentenceid="bdf90db64bc835dde7ee09fe0c01bd71" id="tgt174" class="tgtSentence">Cuando se le pida, escriba la contraseña que especificó anteriormente y confirme que desea realizar esta acción.</caps:sentence>
                              </para>
                            </content>
                          </step>
                          <step>
                            <content>
                              <para>
                                <caps:sentence sentenceid="8afeeaa5d17a9f91abb0fcc38cecfbb6" id="tgt175" class="tgtSentence">Cuando se haya completado el comando, repita el paso 3 en cada archivo .xml restante que se creó mediante la exportación de los dominios de publicación de confianza.</caps:sentence>
                                <caps:sentence sentenceid="84b5ba88804238a7fab867f8f0ae13d5" id="tgt176" class="tgtSentence"> Pero en el caso de estos archivos, establezca <userInput>-Active</userInput> en <userInput>false</userInput> al ejecutar el comando Import.</caps:sentence>
                                <caps:sentence sentenceid="407e8379b5443b7c0092c35c8bab7f29" id="tgt177" class="tgtSentence"> Por ejemplo: <userInput>Import-AadrmTpd -TpdFile E:\contosokey2.xml -ProtectionPassword -Active $false -Verbose</userInput></caps:sentence>
                              </para>
                            </content>
                          </step>
                          <step>
                            <content>
                              <para>
                                <caps:sentence sentenceid="16859c9da62799922bc88b1c7de34fc3" id="tgt178" class="tgtSentence">Use el cmdlet <externalLink><linkText>Disconnect-AadrmService</linkText><linkUri>http://msdn.microsoft.com/library/azure/dn629416.aspx</linkUri></externalLink> para desconectarse del servicio Azure RMS:</caps:sentence>
                              </para>
                              <code>Disconnect-AadrmService</code>
                            </content>
                          </step>
                        </steps>
                        <conclusion>
                          <content>
                            <para>
                              <caps:sentence sentenceid="e8393e916064352781cb463d173cc280" id="tgt179" class="tgtSentence">Ahora puede ir al <link xlink:href="828cf1f7-d0e7-4edf-8525-91896dbe3172#BKMK_Step3Migration">Step 3. Activate your RMS tenant</link>.</caps:sentence>
                            </para>
                          </content>
                        </conclusion>
                      </procedure>
                    </content>
                  </section>
                  <section expanded="false">
                    <title>
                      <caps:sentence sentenceid="79d770e64ba910a7d3a1919258322d15" id="tgt180" class="tgtSentence">Migración entre claves protegidas por HSM</caps:sentence>
                    </title>
                    <content>
                      <para>
                        <caps:sentence sentenceid="7fc31851698774585cee1419d3e4fbf0" id="tgt181" class="tgtSentence">Es un procedimiento de dos partes para importar la clave HSM y la configuración de AD RMS a Azure RMS, que tiene como resultado la clave de inquilino de Azure RMS que administra el propio usuario (BYOK).</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="7307f9fbc74ce9ad6a544238b4f83f47" id="tgt182" class="tgtSentence">Primero debe empaquetar su clave HSM para prepararla para transferirla a Azure RMS y, luego, importarla con los datos de configuración.</caps:sentence>
                      </para>
                      <procedure>
                        <title>
                          <caps:sentence sentenceid="1568a99c9922711ef507dce608aeef93" id="tgt183" class="tgtSentence">Parte 1: Empaquetar la clave HSM para que esté preparada para transferirla a Azure RMS</caps:sentence>
                        </title>
                        <steps class="ordered">
                          <step>
                            <content>
                              <para>
                                <caps:sentence sentenceid="1ce48bdd76c7b3edd2f11eb0283fe381" id="tgt184" class="tgtSentence">Siga los pasos descritos en la sección <link xlink:href="f0d33c5f-a6a6-44a1-bdec-5be1bc8e1e14#BKMK_ImplementBYOK">Implementing bring your own key (BYOK)</link> de <link xlink:href="f0d33c5f-a6a6-44a1-bdec-5be1bc8e1e14">Planning and Implementing Your Azure Rights Management Tenant Key</link>; para ello, use el procedimiento <embeddedLabel>Generar y transferir su clave de inquilino a través de Internet</embeddedLabel> con la excepción siguiente:</caps:sentence>
                              </para>
                              <list class="bullet">
                                <listItem>
                                  <para>
                                    <caps:sentence sentenceid="034d95d731d57d6b533537bbc00fb872" id="tgt185" class="tgtSentence">No siga los pasos que se indican en <embeddedLabel>Generar su clave de inquilino</embeddedLabel>, porque ya tiene el equivalente por su implementación de AD RMS.</caps:sentence>
                                    <caps:sentence sentenceid="546dfa9ba2d608126cf2bfcc448bf164" id="tgt186" class="tgtSentence"> Debe identificar la clave utilizada por el servidor de AD RMS de la instalación de Thales y usar esta clave durante la migración.</caps:sentence>
                                    <caps:sentence sentenceid="854d132d1b3341bceb61d290ca83fa92" id="tgt187" class="tgtSentence"> Los archivos de claves cifradas de Thales suelen denominarse <ui>key_(keyAppName)_(keyIdentifier)</ui> de forma local en el servidor.</caps:sentence>
                                  </para>
                                </listItem>
                                <listItem>
                                  <para>
                                    <caps:sentence sentenceid="034d95d731d57d6b533537bbc00fb872" id="tgt188" class="tgtSentence">No siga los pasos para <embeddedLabel>Transferir su clave de inquilino a Azure RMS</embeddedLabel>, que usa el comando Add-AadrmKey.</caps:sentence>
                                    <caps:sentence sentenceid="bb1a16ebb8482461d33a9081c7ce4233" id="tgt189" class="tgtSentence">  En su lugar, transferirá la clave HSM preparada cuando se cargue el dominio de publicación de confianza exportado, mediante el comando Import-AadrmTpd.</caps:sentence>
                                  </para>
                                </listItem>
                              </list>
                            </content>
                          </step>
                          <step>
                            <content>
                              <para>
                                <caps:sentence sentenceid="92b256a028ba1ac9ab443940bbae1e90" id="tgt190" class="tgtSentence">En la estación de trabajo conectada a Internet, en la sesión de Windows PowerShell, vuelva a conectar con el servicio de Azure RMS.</caps:sentence>
                              </para>
                            </content>
                          </step>
                        </steps>
                        <conclusion>
                          <content>
                            <para>
                              <caps:sentence sentenceid="6b711d337027506973104e4c461927a7" id="tgt191" class="tgtSentence">Ahora que ha preparado su clave HSM para Azure RMS, está listo para importar el archivo de clave HSM y los datos de configuración de AD RMS.</caps:sentence>
                            </para>
                          </content>
                        </conclusion>
                      </procedure>
                      <procedure>
                        <title>
                          <caps:sentence sentenceid="a77dc71f92c3decdd8206e8fcffa89b8" id="tgt192" class="tgtSentence">Part 2: Importar la clave HSM y los datos de configuración a Azure RMS</caps:sentence>
                        </title>
                        <steps class="ordered">
                          <step>
                            <content>
                              <para>
                                <caps:sentence sentenceid="1983fc332527e4f1b93ca306553c042a" id="tgt193" class="tgtSentence">En la estación de trabajo conectada a Internet y en la sesión de Windows PowerShell, cargue el primer archivo del dominio de publicación de confianza exportado (.xml).</caps:sentence>
                                <caps:sentence sentenceid="dac6d0c09c16fbd0c73804284e571477" id="tgt194" class="tgtSentence"> Si tiene más de un archivo .xml porque tenía varios dominios de publicación de confianza, elija el archivo que contenga el dominio de publicación de confianza exportado que corresponda a la clave HSM que desee usar en Azure RMS para proteger el contenido después de la migración.</caps:sentence>
                                <caps:sentence sentenceid="8b30551c6f81bc11c5e9502037601555" id="tgt195" class="tgtSentence"> Use el siguiente comando:</caps:sentence>
                              </para>
                              <code>Import-AadrmTpd -TpdFile &lt;PathToTpdPackageFile&gt; -ProtectionPassword -HsmKeyFile &lt;PathToBYOKPackage&gt; -Active $True -Verbose</code>
                              <para>
                                <caps:sentence sentenceid="d05370276e06291b048268558cc39bee" id="tgt196" class="tgtSentence">Por ejemplo: <userInput>Import -TpdFile E:\no_key_tpd_contosokey1.xml  -HsmKeyFile E:\KeyTransferPackage-contosokey.byok -ProtectionPassword -Active $true -Verbose</userInput></caps:sentence>
                              </para>
                              <para>
                                <caps:sentence sentenceid="bdf90db64bc835dde7ee09fe0c01bd71" id="tgt197" class="tgtSentence">Cuando se le pida, escriba la contraseña que especificó anteriormente y confirme que desea realizar esta acción.</caps:sentence>
                              </para>
                            </content>
                          </step>
                          <step>
                            <content>
                              <para>
                                <caps:sentence sentenceid="304c3a82083750773bf4fa16c248bea7" id="tgt198" class="tgtSentence">Cuando se haya completado el comando, repita el paso 1 en cada archivo .xml restante que se creó mediante la exportación de los dominios de publicación de confianza.</caps:sentence>
                                <caps:sentence sentenceid="84b5ba88804238a7fab867f8f0ae13d5" id="tgt199" class="tgtSentence"> Pero en el caso de estos archivos, establezca <userInput>-Active</userInput> en <userInput>false</userInput> al ejecutar el comando Import.</caps:sentence>
                                <caps:sentence sentenceid="969122afb7e203ce34ae3ffc285d83e5" id="tgt200" class="tgtSentence">  Por ejemplo: <userInput>Import -TpdFile E:\contosokey2.xml -HsmKeyFile E:\KeyTransferPackage-contosokey.byok -ProtectionPassword -Active $false -Verbose</userInput></caps:sentence>
                              </para>
                            </content>
                          </step>
                          <step>
                            <content>
                              <para>
                                <caps:sentence sentenceid="16859c9da62799922bc88b1c7de34fc3" id="tgt201" class="tgtSentence">Use el cmdlet <externalLink><linkText>Disconnect-AadrmService</linkText><linkUri>http://msdn.microsoft.com/library/windowsazure/dn629416.aspx</linkUri></externalLink> para desconectarse del servicio Azure RMS:</caps:sentence>
                              </para>
                              <code>Disconnect-AadrmService</code>
                            </content>
                          </step>
                        </steps>
                        <conclusion>
                          <content>
                            <para>
                              <caps:sentence sentenceid="e8393e916064352781cb463d173cc280" id="tgt202" class="tgtSentence">Ahora puede ir al <link xlink:href="828cf1f7-d0e7-4edf-8525-91896dbe3172#BKMK_Step3Migration">Step 3. Activate your RMS tenant</link>.</caps:sentence>
                            </para>
                          </content>
                        </conclusion>
                      </procedure>
                    </content>
                  </section>
                  <section expanded="false">
                    <title>
                      <caps:sentence sentenceid="e449bff9e10c98b1a91495f05606d77c" id="tgt203" class="tgtSentence">Migración de clave protegida por software a clave protegida por HSM</caps:sentence>
                    </title>
                    <content>
                      <para>
                        <caps:sentence sentenceid="d400abc307e43a60c9fb7b6a47454cef" id="tgt204" class="tgtSentence">Es un procedimiento de tres partes para importar la configuración de AD RMS a Azure RMS, que resulta en que la clave del inquilino de Azure RMS la administre el propio usuario (BYOK).</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="9ba71160e9807c77cf11bfb30ec09012" id="tgt205" class="tgtSentence">Debe extraer la clave del primer certificado emisor de licencias de servidor (SLC) de los datos de configuración y transferir la clave a un HSM de Thales local, empaquetar y transferir la clave de HSM a Azure RMS y, a continuación, importe los datos de configuración.</caps:sentence>
                      </para>
                      <procedure>
                        <title>
                          <caps:sentence sentenceid="c4313a333fe6f83b450cb5698458a23d" id="tgt206" class="tgtSentence">Parte 1: Extraer el SLC de los datos de configuración e importar la clave al HSM local</caps:sentence>
                        </title>
                        <steps class="ordered">
                          <step>
                            <content>
                              <para>
                                <caps:sentence sentenceid="2564f9d4990abdb6c8406c2678526798" id="tgt207" class="tgtSentence">Siga los pasos siguientes que aparecen en la sección <link xlink:href="f0d33c5f-a6a6-44a1-bdec-5be1bc8e1e14#BKMK_ImplementBYOK">Implementing bring your own key (BYOK)</link> del tema <link xlink:href="f0d33c5f-a6a6-44a1-bdec-5be1bc8e1e14">Planning and Implementing Your Azure Rights Management Tenant Key</link>:</caps:sentence>
                              </para>
                              <list class="bullet">
                                <listItem>
                                  <para>
                                    <caps:sentence sentenceid="e265492707dd0595fd1f399bb8a2690e" id="tgt208" class="tgtSentence">
                                      <embeddedLabel>Generar y transferir su clave de inquilino a través de Internet</embeddedLabel>: <embeddedLabel>Preparar la estación de trabajo conectada a Internet</embeddedLabel></caps:sentence>
                                  </para>
                                </listItem>
                                <listItem>
                                  <para>
                                    <caps:sentence sentenceid="e265492707dd0595fd1f399bb8a2690e" id="tgt209" class="tgtSentence">
                                      <embeddedLabel>Generar y transferir su clave de inquilino a través de Internet</embeddedLabel>: <embeddedLabel>Prepare su estación de trabajo desconectada.</embeddedLabel></caps:sentence>
                                  </para>
                                </listItem>
                              </list>
                              <para>
                                <caps:sentence sentenceid="5a805607a590f53bd5c9d48ac363568b" id="tgt210" class="tgtSentence">Debe seguir los pasos para generar la clave de inquilino, puesto que ya tiene el equivalente en el archivo de datos de configuración exportado (.xml).</caps:sentence>
                                <caps:sentence sentenceid="7914923580376d1d1f2635fb1da8c681" id="tgt211" class="tgtSentence"> En su lugar, se ejecutará un comando para extraer esta clave del archivo e importarla en el HSM local.</caps:sentence>
                              </para>
                            </content>
                          </step>
                          <step>
                            <content>
                              <para>
                                <caps:sentence sentenceid="9016ee10dbce7c06044a304e2f389ba6" id="tgt212" class="tgtSentence">En la estación de trabajo desconectada, ejecute el siguiente comando:</caps:sentence>
                              </para>
                              <code>KeyTransferRemote.exe -ImportRmsCentrallyManagedKey -TpdFilePath &lt;TPD&gt; -ProtectionPassword -KeyIdentifier &lt;KeyID&gt; -ExchangeKeyPackage &lt;BYOK-KEK-pka-Region&gt; -NewSecurityWorldPackage &lt;BYOK-SecurityWorld-pkg-Region&gt;</code>
                              <para>
                                <caps:sentence sentenceid="6767ded2b561c516fe3b5e56f147abb2" id="tgt213" class="tgtSentence">Por ejemplo, para Norteamérica: <userInput>KeyTransferRemote.exe -ImportRmsCentrallyManagedKey -TpdFilePath E:\contosokey1.xml -ProtectionPassword -KeyIdentifier contosorms1key –- -ExchangeKeyPackage &lt;BYOK-KEK-pka-NA-1&gt; -NewSecurityWorldPackage &lt;BYOK-SecurityWorld-pkg-NA-1&gt;</userInput></caps:sentence>
                              </para>
                              <para>
                                <caps:sentence sentenceid="c80e9d4e4171ecff41ff04fe5ffb6917" id="tgt214" class="tgtSentence">Información adicional:</caps:sentence>
                              </para>
                              <list class="bullet">
                                <listItem>
                                  <para>
                                    <caps:sentence sentenceid="2c3e87f07013ef0a820ba4ac0a783bf6" id="tgt215" class="tgtSentence">El parámetro ImportRmsCentrallyManagedKey indica que la operación es importar la clave de SLC.</caps:sentence>
                                  </para>
                                </listItem>
                                <listItem>
                                  <para>
                                    <caps:sentence sentenceid="4e5876f46a374c209a1e8c7efd766687" id="tgt216" class="tgtSentence">Si no especifica la contraseña en el comando, se le pedirá que la especifique.</caps:sentence>
                                  </para>
                                </listItem>
                                <listItem>
                                  <para>
                                    <caps:sentence sentenceid="f35edd5674fb649f724c48b7fc8d0e0d" id="tgt217" class="tgtSentence">El parámetro KeyIdentifier es un nombre descriptivo de clave que crea el nombre del archivo de clave.</caps:sentence>
                                    <caps:sentence sentenceid="cd4bb580bcc724e7dc7935c08d1f4c74" id="tgt218" class="tgtSentence"> Debe utilizar únicamente caracteres en minúsculas ASCII.</caps:sentence>
                                  </para>
                                </listItem>
                                <listItem>
                                  <para>
                                    <caps:sentence sentenceid="f4c9e89632c9d7b293e21cf54b05a895" id="tgt219" class="tgtSentence">El parámetro ExchangeKeyPackage especifica un paquete de claves de intercambio de claves (KEK) específico de la región cuyo nombre comienza por BYOK-KEK-pkg-.</caps:sentence>
                                  </para>
                                </listItem>
                                <listItem>
                                  <para>
                                    <caps:sentence sentenceid="54a153639be36aa861863090c1177601" id="tgt220" class="tgtSentence">El parámetro NewSecurityWorldPackage especifica un paquete internacional de seguridad específico de la región cuyo nombre comienza por BYOK-SecurityWorld-pkg-.</caps:sentence>
                                  </para>
                                </listItem>
                              </list>
                              <para>
                                <caps:sentence sentenceid="e5594da2d2abc1ae7ca06668f59a1137" id="tgt221" class="tgtSentence">Este comando genera lo siguiente:</caps:sentence>
                              </para>
                              <list class="bullet">
                                <listItem>
                                  <para>
                                    <caps:sentence sentenceid="e8a38bb7eea904f2107c52e55618741e" id="tgt222" class="tgtSentence">Un archivo de clave de HSM: %NFAST_KMDATA%\local\key_mscapi_&lt;KeyID&gt;</caps:sentence>
                                  </para>
                                </listItem>
                                <listItem>
                                  <para>
                                    <caps:sentence sentenceid="191abb451b135925ecdd57fbdaa14073" id="tgt223" class="tgtSentence">Archivo de datos de configuración de RMS con el SLC quitado: %NFAST_KMDATA%\local\no_key_tpd_&lt;KeyID&gt;.xml</caps:sentence>
                                  </para>
                                </listItem>
                              </list>
                            </content>
                          </step>
                          <step>
                            <content>
                              <para>
                                <caps:sentence sentenceid="8b29675e8a1f53d8c8bb17a9b75f49cd" id="tgt224" class="tgtSentence">Si tiene más de un archivo de datos de configuración de RMS, repita el paso 2 para el resto de estos archivos.</caps:sentence>
                              </para>
                            </content>
                          </step>
                        </steps>
                        <conclusion>
                          <content>
                            <para>
                              <caps:sentence sentenceid="dee04f3f6ad3a9c25d19ee34a0df0c9f" id="tgt225" class="tgtSentence">Ahora que se ha extraído el SLC para que sea una clave de HSM, está listo para empaquetar y transferirla a Azure RMS.</caps:sentence>
                            </para>
                          </content>
                        </conclusion>
                      </procedure>
                      <procedure>
                        <title>
                          <caps:sentence sentenceid="2feaabefc7c24d6f622cb7dca95621bf" id="tgt226" class="tgtSentence">Part 2: Empaquetar y transferir su clave de HSM a Azure RMS</caps:sentence>
                        </title>
                        <steps class="ordered">
                          <step>
                            <content>
                              <para>
                                <caps:sentence sentenceid="e70e56cdb9cdcd5fb91a2d69e891961f" id="tgt227" class="tgtSentence">Siga los pasos siguientes que aparecen en la sección <link xlink:href="f0d33c5f-a6a6-44a1-bdec-5be1bc8e1e14#BKMK_ImplementBYOK">Implementing bring your own key (BYOK)</link> de <link xlink:href="f0d33c5f-a6a6-44a1-bdec-5be1bc8e1e14">Planning and Implementing Your Azure Rights Management Tenant Key</link>:</caps:sentence>
                              </para>
                              <list class="bullet">
                                <listItem>
                                  <para>
                                    <caps:sentence sentenceid="e265492707dd0595fd1f399bb8a2690e" id="tgt228" class="tgtSentence">
                                      <embeddedLabel>Generar y transferir su clave de inquilino a través de Internet</embeddedLabel>: <embeddedLabel>Preparar su clave de inquilino para transferirla</embeddedLabel></caps:sentence>
                                  </para>
                                </listItem>
                                <listItem>
                                  <para>
                                    <caps:sentence sentenceid="e265492707dd0595fd1f399bb8a2690e" id="tgt229" class="tgtSentence">
                                      <embeddedLabel>Generar y transferir su clave de inquilino a través de Internet</embeddedLabel>: <embeddedLabel>Transferir su clave de inquilino a Azure RMS</embeddedLabel></caps:sentence>
                                  </para>
                                </listItem>
                              </list>
                            </content>
                          </step>
                        </steps>
                        <conclusion>
                          <content>
                            <para>
                              <caps:sentence sentenceid="bc050b6d0f973332c1adf193ac13fd8b" id="tgt230" class="tgtSentence">Ahora que ha transferido su clave de HSM a Azure RMS, está listo para importar los datos de configuración de AD RMS, que contienen solo un puntero a la clave del inquilino recién transferido.</caps:sentence>
                            </para>
                          </content>
                        </conclusion>
                      </procedure>
                      <procedure>
                        <title>
                          <caps:sentence sentenceid="630383ca2e18816108cce9cc20ec87c8" id="tgt231" class="tgtSentence">Part 3: Importar los datos de configuración a Azure RMS</caps:sentence>
                        </title>
                        <steps class="ordered">
                          <step>
                            <content>
                              <para>
                                <caps:sentence sentenceid="52dde1ac053f9367b40671e8c20eb102" id="tgt232" class="tgtSentence">Aún en la estación de trabajo conectada a Internet y en la sesión de Windows PowerShell, copie los archivos de configuración de RMS con el SLC quitado (desde la estación de trabajo desconectada, %NFAST_KMDATA%\local\no_key_tpd_&lt;KeyID&gt;.xml)</caps:sentence>
                              </para>
                            </content>
                          </step>
                          <step>
                            <content>
                              <para>
                                <caps:sentence sentenceid="202bd58572981ff5eeb24c2b1e3cf44b" id="tgt233" class="tgtSentence">Cargue el primer archivo.</caps:sentence>
                                <caps:sentence sentenceid="dac6d0c09c16fbd0c73804284e571477" id="tgt234" class="tgtSentence"> Si tiene más de un archivo .xml porque tenía varios dominios de publicación de confianza, elija el archivo que contenga el dominio de publicación de confianza exportado que corresponda a la clave HSM que desee usar en Azure RMS para proteger el contenido después de la migración.</caps:sentence>
                                <caps:sentence sentenceid="8b30551c6f81bc11c5e9502037601555" id="tgt235" class="tgtSentence"> Use el siguiente comando:</caps:sentence>
                              </para>
                              <code>Import-AadrmTpd -TpdFile &lt;PathToNoKeyTpdPackageFile&gt; -ProtectionPassword -HsmKeyFile &lt;PathToKeyTransferPackage&gt; -Active $true -Verbose </code>
                              <para>
                                <caps:sentence sentenceid="d05370276e06291b048268558cc39bee" id="tgt236" class="tgtSentence">Por ejemplo: <userInput>Import -TpdFile E:\no_key_tpd_contosorms1key.xml -ProtectionPassword -HsmKeyFile E:\KeyTransferPackage-contosorms1key.byok -Active $true -Verbose </userInput></caps:sentence>
                              </para>
                              <para>
                                <caps:sentence sentenceid="bdf90db64bc835dde7ee09fe0c01bd71" id="tgt237" class="tgtSentence">Cuando se le pida, escriba la contraseña que especificó anteriormente y confirme que desea realizar esta acción.</caps:sentence>
                              </para>
                            </content>
                          </step>
                          <step>
                            <content>
                              <para>
                                <caps:sentence sentenceid="ac0901fe2044dcb2cc068b7524667831" id="tgt238" class="tgtSentence">Cuando se haya completado el comando, repita el paso 2 en cada archivo .xml restante que se creó mediante la exportación de los dominios de publicación de confianza.</caps:sentence>
                                <caps:sentence sentenceid="84b5ba88804238a7fab867f8f0ae13d5" id="tgt239" class="tgtSentence"> Pero en el caso de estos archivos, establezca <userInput>-Active</userInput> en <userInput>false</userInput> al ejecutar el comando Import.</caps:sentence>
                                <caps:sentence sentenceid="407e8379b5443b7c0092c35c8bab7f29" id="tgt240" class="tgtSentence"> Por ejemplo: <userInput>Import -TpdFile E:\no_key_tpd_contosorms2key.xml -ProtectionPassword -HsmKeyFile E:\KeyTransferPackage-contosorms1key.byok -Active $false -Verbose </userInput></caps:sentence>
                              </para>
                            </content>
                          </step>
                          <step>
                            <content>
                              <para>
                                <caps:sentence sentenceid="16859c9da62799922bc88b1c7de34fc3" id="tgt241" class="tgtSentence">Use el cmdlet <externalLink><linkText>Disconnect-AadrmService</linkText><linkUri>http://msdn.microsoft.com/library/windowsazure/dn629416.aspx</linkUri></externalLink> para desconectarse del servicio Azure RMS:</caps:sentence>
                              </para>
                              <code>Disconnect-AadrmService</code>
                            </content>
                          </step>
                        </steps>
                        <conclusion>
                          <content>
                            <para>
                              <caps:sentence sentenceid="e8393e916064352781cb463d173cc280" id="tgt242" class="tgtSentence">Ahora puede ir al <link xlink:href="828cf1f7-d0e7-4edf-8525-91896dbe3172#BKMK_Step3Migration">Step 3. Activate your RMS tenant</link>.</caps:sentence>
                            </para>
                          </content>
                        </conclusion>
                      </procedure>
                    </content>
                  </section>
                </sections>
              </section>
            </sections>
          </section>
          <section address="BKMK_Step3Migration">
            <title>
              <caps:sentence sentenceid="109514fd8cd9e2015190a63d21e7c991" id="tgt243" class="tgtSentence">Paso 3:</caps:sentence>
              <caps:sentence sentenceid="ffa6ca6573c72d8f004b6b25226f1468" id="tgt244" class="tgtSentence"> Active el inquilino de RMS.</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="3fa616e8d09f47e4613a608a5ab40b61" id="tgt245" class="tgtSentence">Las instrucciones de este paso se tratan íntegramente en el tema <link xlink:href="f8707e01-b239-4d1a-a1ea-0d1cf9a8d214">Activating Azure Rights Management</link>.</caps:sentence>
              </para>
              <alert class="tip">
                <para>
                  <caps:sentence sentenceid="9a3fec79df6d035db9bf50b7636f1e25" id="tgt246" class="tgtSentence">Si tiene una suscripción de Office 365, puede activar Azure RMS desde el centro de administración de Office 365 o el Portal de Azure clásico.</caps:sentence>
                  <caps:sentence sentenceid="af78cd8483c136c8b7fc88eda98f497b" id="tgt247" class="tgtSentence"> Se recomienda usar el Portal de Azure clásico, ya que usará este portal de administración para completar el paso siguiente.</caps:sentence>
                </para>
              </alert>
              <para>
                <caps:sentence sentenceid="62576c444793c839ecacd1bae075cafd" id="tgt248" class="tgtSentence">
                  <embeddedLabel>¿Qué ocurre si ya está activado el inquilino de Azure RMS?</embeddedLabel> Si el servicio de Azure RMS ya está activado en su organización, es posible que los usuarios ya hayan usado Azure RMS para proteger el contenido con una clave de inquilino generada automáticamente (y las plantillas predeterminadas) en lugar de las claves (y plantillas) existentes de AD RMS.</caps:sentence>
                <caps:sentence sentenceid="0ed02c45af6fb8a877cd0de9328b63b7" id="tgt249" class="tgtSentence"> Esto es improbable que ocurra en equipos que estén bien administrados en la intranet, ya que se configuran automáticamente para su infraestructura de AD RMS.</caps:sentence>
                <caps:sentence sentenceid="c65d1ddccf3401da27a54736965d9b50" id="tgt250" class="tgtSentence"> Pero esto puede suceder en equipos de grupo de trabajo o equipos que se conectan con poca frecuencia a la intranet.</caps:sentence>
                <caps:sentence sentenceid="61a9c88a9e631bef540eede6fd229823" id="tgt251" class="tgtSentence"> Desafortunadamente, también es difícil identificar estos equipos, motivo por el que se recomienda no activar el servicio antes de importar los datos de configuración de AD RMS.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="587749ba1f609ee7f51650ee509c8a99" id="tgt252" class="tgtSentence">Si ya está activado el inquilino de Azure RMS y puede identificar estos equipos, asegúrese de que ejecuta el script CleanUpRMS_RUN_Elevated.cmd en estos equipos, tal como se describe en el paso 5.</caps:sentence>
                <caps:sentence sentenceid="202ffab1a468fd4607ec7254f9a2d368" id="tgt253" class="tgtSentence"> La ejecución de este script les obliga a reinicializar el entorno de usuario, así descargan la clave de inquilino y las plantillas importadas actualizadas.</caps:sentence>
              </para>
            </content>
          </section>
          <section address="BKMK_Step4Migration">
            <title>
              <caps:sentence sentenceid="323241aef2be0c46e26a80632199dfb4" id="tgt254" class="tgtSentence">Paso 4.</caps:sentence>
              <caps:sentence sentenceid="dec2d8c6239478bcc3df92273496f727" id="tgt255" class="tgtSentence"> Configure las plantillas importadas.</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="789e297da3c8f43f2e89dfb802da264a" id="tgt256" class="tgtSentence">Dado que las plantillas que importó tienen un estado predeterminado de <ui>Archivada</ui>, debe cambiar este estado a <ui>Publicada</ui> si desea que los usuarios puedan utilizar estas plantillas con Azure RMS.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="790354c8613148f9f8cfd8a6b3f0df3c" id="tgt257" class="tgtSentence">Además, si sus plantillas de AD RMS usaban el grupo <ui>TODOS</ui>, este grupo desaparecerá automáticamente al importar las plantillas a Azure RMS; debe agregar manualmente el grupo o usuarios equivalentes y los mismos derechos a las plantillas importadas.</caps:sentence>
                <caps:sentence sentenceid="4680928f50076c8a650c95ec8f5882a5" id="tgt258" class="tgtSentence"> El grupo equivalente de Azure RMS se llama <system>AllStaff-&lt;tenant_GUID&gt;@&lt;tenant_name&gt;.onmicrosoft.com</system>.</caps:sentence>
                <caps:sentence sentenceid="4f2a8e43314a42a39d01921595a49e66" id="tgt259" class="tgtSentence"> Por ejemplo, este grupo puede tener un aspecto similar al siguiente para Contoso: <system>AllStaff-9c11c87a-ac8b-46a3-8d5c-f4d0b72ee29a@contoso.onmicrosoft.com</system>.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="5e74cf089e636e7ec5b7c1259ccb81ac" id="tgt260" class="tgtSentence">Si no está seguro de si las plantillas de AD RMS incluyen el grupo CUALQUIERA, expanda la sección <link xlink:href="#BKMK_ScriptForANYONE">PowerShell script to identify AD RMS templates that include the ANYONE group</link> en este paso para copiar y usar el script de PowerShell de ejemplo para identificar estas plantillas.</caps:sentence>
                <caps:sentence sentenceid="c67985e4e4ceb311ab268f8f6998e0f8" id="tgt261" class="tgtSentence"> Para más información sobre el uso de Windows PowerShell con AD RMS, consulte <externalLink><linkText>Uso de Windows PowerShell para administrar AD RMS</linkText><linkUri>https://technet.microsoft.com/library/ee221079(v=ws.10).aspx</linkUri></externalLink>.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="8d85b35bc3605b384c6479e039a283e2" id="tgt262" class="tgtSentence">Puede ver el grupo creado automáticamente de su organización si copia una de las plantillas de directiva de permisos predeterminadas en el Portal de Azure clásico e identifica el <ui>NOMBRE DE USUARIO</ui> en la página <ui>PERMISOS</ui>.</caps:sentence>
                <caps:sentence sentenceid="80c94e27704f7aff98c5dd1f0780e712" id="tgt263" class="tgtSentence"> Sin embargo, no puede usar el portal clásico para agregar este grupo a una plantilla que se creó o importó manualmente; en su lugar, debe usar una de las siguientes opciones de Azure RMS PowerShell:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="16859c9da62799922bc88b1c7de34fc3" id="tgt264" class="tgtSentence">Use el cmdlet <externalLink><linkText>New-AadrmRightsDefinition</linkText><linkUri>https://msdn.microsoft.com/library/azure/dn727080.aspx</linkUri></externalLink> de PowerShell para definir el grupo "AllStaff" y los derechos como un objeto de definición de derechos, y ejecute de nuevo este comando para cada uno de los demás grupos o usuarios a los que ya se les ha otorgado derechos en la plantilla original además de para el grupo CUALQUIERA.</caps:sentence>
                    <caps:sentence sentenceid="68d40b9728b4c4ee251a6967c171233b" id="tgt265" class="tgtSentence"> A continuación, agregue estos objetos de definición de derechos a las plantillas mediante el cmdlet <externalLink><linkText>Set-AadrmTemplateProperty</linkText><linkUri>https://msdn.microsoft.com/en-us/library/azure/dn727076.aspx</linkUri></externalLink>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="16859c9da62799922bc88b1c7de34fc3" id="tgt266" class="tgtSentence">Use el cmdlet <externalLink><linkText>Export-AadrmTemplate</linkText><linkUri>https://msdn.microsoft.com/library/azure/dn727078.aspx</linkUri></externalLink> para exportar la plantilla a un archivo .XML que puede editar para agregar el grupo "AllStaff" y los derechos a los grupos y derechos existentes y, a continuación, use el cmdlet <externalLink><linkText>Import-AadrmTemplate</linkText><linkUri>https://msdn.microsoft.com/library/azure/dn727077.aspx</linkUri></externalLink> para importar este cambio de nuevo en Azure RMS.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <alert class="note">
                <para>
                  <caps:sentence sentenceid="66bce28c3c39e3aa13ce91c1bbe60528" id="tgt267" class="tgtSentence">Este grupo equivalente "AllStaff" no es exactamente igual que el grupo TODOS de AD RMS:  el grupo "AllStaff" incluye todos los usuarios de su inquilino de Azure, mientras que el grupo TODOS incluye todos los usuarios autenticados, que podrían estar fuera de su organización.</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="9236e27d78a4cab57bb74db879ef4d2d" id="tgt268" class="tgtSentence">Debido a esta diferencia entre los dos grupos, puede que tenga que agregar también usuarios externos además del grupo "AllStaff".</caps:sentence>
                  <caps:sentence sentenceid="7b8435a7e049840b390e4e8eb4c4d168" id="tgt269" class="tgtSentence"> Actualmente no se admiten direcciones de correo electrónico externas para grupos.</caps:sentence>
                </para>
              </alert>
              <para>
                <caps:sentence sentenceid="c252fbbfeb7650309546988a57b464e1" id="tgt270" class="tgtSentence">Las plantillas que se importan de AD RMS tienen el mismo aspecto y comportamiento que las plantillas personalizadas que se pueden crear en el Portal de Azure clásico.</caps:sentence>
                <caps:sentence sentenceid="bdc1d87d3013b77c09cecc8c14c73adc" id="tgt271" class="tgtSentence"> Para cambiar las plantillas importadas para publicarlas de modo que los usuarios puedan verlas y seleccionarlas desde las aplicaciones o para realizar otros cambios en las plantillas, consulte <link xlink:href="1775d8d0-9a59-42c8-914f-ce285b71ac1c">Configuring Custom Templates for Azure Rights Management</link>.</caps:sentence>
              </para>
              <alert class="tip">
                <para>
                  <caps:sentence sentenceid="a6583b5544e5b6aa76107950d5dc4169" id="tgt272" class="tgtSentence">Para obtener una experiencia más coherente para los usuarios durante el proceso de migración, no realice cambios en las plantillas importadas aparte de estos dos y no publique las dos plantillas predeterminadas que vienen con Azure RMS ni cree plantillas nuevas en este momento.</caps:sentence>
                  <caps:sentence sentenceid="33114e4183694206ed98efd7df18d911" id="tgt273" class="tgtSentence"> En su lugar, espere hasta que se complete el proceso de migración y haya dado de baja los servidores de AD RMS.</caps:sentence>
                </para>
              </alert>
            </content>
            <sections>
              <section expanded="false" address="BKMK_ScriptForANYONE">
                <title>
                  <caps:sentence sentenceid="c9417a4f464a216ccd9380ac080132e5" id="tgt274" class="tgtSentence">Script de ejemplo de Windows PowerShell para identificar plantillas de AD RMS que incluyen el grupo CUALQUIERA</caps:sentence>
                </title>
                <content>
                  <para>
                    <caps:sentence sentenceid="6a63ca9096ce03b685acda780220a557" id="tgt275" class="tgtSentence">Esta sección contiene el script de ejemplo que le ayuda a identificar plantillas de AD RMS que tienen definido el grupo CUALQUIERA, tal como se ha descrito en la sección anterior.</caps:sentence>
                  </para>
                  <para>
                    <legacyItalic>
                      <caps:sentence sentenceid="291039e00dd33ca07dd04e988654da22" id="tgt276" class="tgtSentence">
                        <embeddedLabel>Aviso de declinación de responsabilidades</embeddedLabel>: Este script de ejemplo no es compatible en ningún servicio o programa de soporte estándar de Microsoft.</caps:sentence>
                      <caps:sentence sentenceid="c62eb79717d2870aba23b3fa99ed9aa4" id="tgt277" class="tgtSentence"> Este script de ejemplo se proporciona TAL CUAL sin garantía de ningún tipo.</caps:sentence>
                    </legacyItalic>
                  </para>
                  <code>import-module adrmsadmin New-PSDrive -Name MyRmsAdmin -PsProvider AdRmsAdmin -Root https://localhost -Force $ListofTemplates=dir MyRmsAdmin:\RightsPolicyTemplate foreach($Template in $ListofTemplates) { $templateID=$Template.id $rights = dir MyRmsAdmin:\RightsPolicyTemplate\$Templateid\userright $templateName=$Template.DefaultDisplayName if ($rights.usergroupname -eq "anyone") { $templateName = $Template.defaultdisplayname write-host "Template " -NoNewline write-host -NoNewline $templateName -ForegroundColor Red write-host " contains rights for " -NoNewline write-host ANYONE  -ForegroundColor Red } } Remove-PSDrive MyRmsAdmin -force
</code>
                </content>
              </section>
            </sections>
          </section>
          <section address="BKMK_Step5Migration">
            <title>
              <caps:sentence sentenceid="b07068230cd9957fd61de6376c46207a" id="tgt278" class="tgtSentence">Paso 5.</caps:sentence>
              <caps:sentence sentenceid="4211c7ea703db35fd23d534f8f4b4547" id="tgt279" class="tgtSentence"> Vuelva a configurar los clientes para usar Azure RMS.</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="cfd608dfbc0540950dcbd6b3dcd30e82" id="tgt280" class="tgtSentence">Para los clientes de Windows:</caps:sentence>
              </para>
              <list class="ordered">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="e265492707dd0595fd1f399bb8a2690e" id="tgt281" class="tgtSentence">
                      <externalLink>
                        <linkText>Descargue los scripts de migración</linkText>
                        <linkUri>http://go.microsoft.com/fwlink/?LinkId=524619</linkUri>
                      </externalLink>: </caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="c540add67544ede964e67cf3d7a93dd2" id="tgt282" class="tgtSentence">CleanUpRMS_RUN_Elevated.cmd</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="4ba5c672db6295a1c089c027a3803da3" id="tgt283" class="tgtSentence">Redirect_OnPrem.cmd</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence sentenceid="5d5c6c7d62e65db194f21a564bfa2e19" id="tgt284" class="tgtSentence">Estos scripts restablecen la configuración en los equipos de Windows para que usen el servicio de Azure RMS en lugar de AD RMS.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="d4a9a5cb446ccbb5c67aedfd03a926a4" id="tgt285" class="tgtSentence">Siga las instrucciones del script de redirección (Redirect_OnPrem.cmd) para modificarlo de forma que señale al nuevo inquilino de Azure RMS.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="5323f31a189c997652d5a3a0ed5fb256" id="tgt286" class="tgtSentence">En los equipos Windows, ejecute estos scripts con privilegios elevados en el contexto del usuario.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="6e449c2c59a1e1e8912452b875d45e5f" id="tgt287" class="tgtSentence">Para clientes de dispositivos móviles y equipos Mac:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="37794107207a9e8a9ac8109c11aeee74" id="tgt288" class="tgtSentence">Quite los registros de DNS SRV que creó cuando implementó la <externalLink><linkText>extensión de AD RMS para dispositivos móviles</linkText><linkUri>http://technet.microsoft.com/library/dn673574.aspx</linkUri></externalLink>.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
            <sections>
              <section expanded="false">
                <title>
                  <caps:sentence sentenceid="73990d4d365d797e9b6da85d325975a9" id="tgt289" class="tgtSentence">Cambios realizados por los scripts de migración</caps:sentence>
                </title>
                <content>
                  <para>
                    <caps:sentence sentenceid="5cae975640e774b0ec1a50e5cbbcdecc" id="tgt290" class="tgtSentence">En esta sección se documentan los cambios que hacen los scripts de migración.</caps:sentence>
                    <caps:sentence sentenceid="7e0092d6290c6a143e8205e7d783bf90" id="tgt291" class="tgtSentence"> Puede utilizar esta información sólo con fines de referencia o para solucionar problemas o si prefiere hacer estos cambios usted mismo.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="a5ec859cfc6dca2f0377fe527ae4ccde" id="tgt292" class="tgtSentence">CleanUpRMS_RUN_Elevated.cmd:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="19fc8030eb87b6a393d10d5c8767e2d6" id="tgt293" class="tgtSentence">Elimine el contenido de las carpetas %userprofile%\AppData\Local\Microsoft\DRM y %userprofile%\AppData\Local\Microsoft\MSIPC, incluidas todas las subcarpetas y los archivos con nombres de archivo largos.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="b722a91a8467d1fb862ece0d3ba416e3" id="tgt294" class="tgtSentence">Elimine el contenido de las claves del Registro siguientes:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="7a43cfee3d40f2d2b9074c8fcb1d9923" id="tgt295" class="tgtSentence">HKEY_LOCAL_MACHINE\Software\Microsoft\Office\(11.0|12.0|14.0)\Common\DRM</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="eafa82a559f1413fe776f53dfc3b4137" id="tgt296" class="tgtSentence">HKEY_CURRENT_USER\Software\Microsoft\Office\(11.0|12.0|14.0)\Common\DRM</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="c7f38463861e65ee71515aebf39769fb" id="tgt297" class="tgtSentence">HKEY_LOCAL_MACHINE\Software\WoW6432Node\Microsoft\Office\(11.0|12.0|14.0)\Common\DRM</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="a43c9e4d926e4a1d36f630272b378c35" id="tgt298" class="tgtSentence">HKEY_CURRENT_USER\Software\WoW6432Node\Microsoft\Office\(11.0|12.0|14.0)\Common\DRM</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="3b029246c53d388da4cdced405deea46" id="tgt299" class="tgtSentence">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MSIPC\ServiceLocation</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="66712671dae4821cb4c97211bf62133a" id="tgt300" class="tgtSentence">HKEY_LOCAL_MACHINE\SOFTWARE\WoW6432Node\Microsoft\MSIPC\ServiceLocation</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="9e38087a294154bad98452ad73430016" id="tgt301" class="tgtSentence">HKEY_LOCAL_MACHINE\Software\Microsoft\MSDRM\ServiceLocation</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="7285873bc66bd51ab54618f5108e69e7" id="tgt302" class="tgtSentence">Elimine los siguientes valores del Registro:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="41ab5dbb0aa718831126a06e17a48842" id="tgt303" class="tgtSentence">HKEY_CURRENT_USER\Software\Microsoft\Office\15.0\Common\DRM\DefaultServerURL</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="1eaa9bffc767d3f5c991d4adda593b80" id="tgt304" class="tgtSentence">HKEY_CURRENT_USER\Software\Microsoft\Office\15.0\Common\DRM\DefaultServer</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence sentenceid="b60e278d76351e700cac68621743b526" id="tgt305" class="tgtSentence">Redirect_OnPrem.cmd:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="59a3ee9cceaa5043e6203a402300b83b" id="tgt306" class="tgtSentence">Cree los siguientes valores del Registro para cada dirección URL proporcionada como un parámetro en cada una de las siguientes ubicaciones:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="22819938d1af49b9a662ddef60fc5885" id="tgt307" class="tgtSentence">HKEY_CURRENT_USER\Software\Microsoft\Office\(11.0|12.0|14.0)\Common\DRM\LicenseServerRedirection</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="c8985d1d050d5973ebab9c4201209411" id="tgt308" class="tgtSentence">HKEY_CURRENT_USER\Software\WoW6432Node\Microsoft\Office\(11.0|12.0|14.0)\Common\DRM\LicenseServerRedirection</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="24879e3cb182f3c99abe21c4ee9eca9a" id="tgt309" class="tgtSentence">HKEY_LOCAL_MACHINE\Software\Microsoft\Office\(11.0|12.0|14.0)\Common\DRM\LicenseServerRedirection</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="406df330896cd3c0794920f46cd938fd" id="tgt310" class="tgtSentence">HKEY_LOCAL_MACHINE\Software\WoW6432Node\Microsoft\Office\(11.0|12.0|14.0)\Common\DRM\LicenseServerRedirection</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="02a964ee4a12efdb687ad0d436119760" id="tgt311" class="tgtSentence">HKEY_CURRENT_USER\Software\Classes\Local Settings\Software\Microsoft\MSIPC\LicensingRedirection</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                      <para>
                        <caps:sentence sentenceid="3bbdc6d5a2543bdf56ad63364f55a174" id="tgt312" class="tgtSentence">Cada entrada tiene un valor REG_SZ de <ui>https://OldRMSserverURL/_wmcs/licensing</ui> con los datos en el siguiente formato: <ui>https://&lt;YourTenantURL&gt;/_wmcs/licensing</ui>.</caps:sentence>
                      </para>
                      <alert class="note">
                        <para>
                          <caps:sentence sentenceid="80305a496e1bd4363b3917c9b5acd933" id="tgt313" class="tgtSentence">
                            <placeholder>&lt;YourTenantURL&gt;</placeholder> tiene el formato siguiente: <ui>{GUID}.rms.[Region].aadrm.com</ui>.</caps:sentence>
                        </para>
                        <para>
                          <caps:sentence sentenceid="b922f2b29ac449fbea90ff49fbc782c0" id="tgt314" class="tgtSentence">Por ejemplo:  5c6bb73b-1038-4eec-863d-49bded473437.rms.na.aadrm.com</caps:sentence>
                        </para>
                        <para>
                          <caps:sentence sentenceid="1c2c13a341ef0efefe79e91fb5532568" id="tgt315" class="tgtSentence">Para encontrar este valor, identifique el valor <ui>RightsManagementServiceId</ui> cuando ejecute el cmdlet <externalLink><linkText>Get-AadrmConfiguration</linkText><linkUri>http://msdn.microsoft.com/library/windowsazure/dn629410.aspx</linkUri></externalLink> para Azure RMS.</caps:sentence>
                        </para>
                      </alert>
                    </listItem>
                  </list>
                </content>
              </section>
            </sections>
          </section>
          <section address="BKMK_Step6Migration">
            <title>
              <caps:sentence sentenceid="f908b923db8fd9da757a6e8223a5a8fc" id="tgt316" class="tgtSentence">Paso 6.</caps:sentence>
              <caps:sentence sentenceid="36a0d72df947da56074f640aa8a226bd" id="tgt317" class="tgtSentence"> Configure la integración de IRM en Exchange Online.</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="7cdefa985f73cfe79da57362b0e94de9" id="tgt318" class="tgtSentence">Si ha importado anteriormente el TDP desde AD RMS a Exchange Online, debe quitarlo para evitar conflictos de plantillas y directivas después de haber migrado a Azure RMS.</caps:sentence>
                <caps:sentence sentenceid="8c1b10166db1b06c63557d94794bc5bc" id="tgt319" class="tgtSentence"> Para ello, use el cmdlet <externalLink><linkText>Remove-RMSTrustedPublishingDomain</linkText><linkUri>https://technet.microsoft.com/en-us/library/jj200720(v=exchg.150).aspx</linkUri></externalLink> de Exchange Online.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="a729f647b41ab0ae3990e2d2787356c6" id="tgt320" class="tgtSentence">Si eligió una topología de clave de inquilino de Azure RMS de <embeddedLabel>administrada por Microsoft</embeddedLabel>:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="abda7877548e2693387fce7b54bf4008" id="tgt321" class="tgtSentence">Vea la sección <link xlink:href="ea09cbc5-b98b-444e-8b60-5bc3cb199c36#BKMK_ExchangeOnline">Exchange Online: IRM Configuration</link> del tema <link xlink:href="ea09cbc5-b98b-444e-8b60-5bc3cb199c36">Configuring Applications for Azure Rights Management</link>.</caps:sentence>
                    <caps:sentence sentenceid="f0bf7dea8f5e087cb78dfa16ecb7991d" id="tgt322" class="tgtSentence"> Esta sección incluye la ejecución de comandos típicos que conectan con el servicio de Exchange Online, importan la clave de inquilino de Azure RMS y habilitan la funcionalidad IRM para Exchange Online.</caps:sentence>
                    <caps:sentence sentenceid="00f4cc711369136298c1cb7344b12769" id="tgt323" class="tgtSentence"> Después de completar estos pasos, tendrá la funcionalidad completa de RMS con Exchange Online.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="a729f647b41ab0ae3990e2d2787356c6" id="tgt324" class="tgtSentence">Si ha elegido una topología de clave de inquilino de Azure RMS <embeddedLabel>administrada por el cliente (BYOK)</embeddedLabel>:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="146f9fe0969ee405166209fc122b7c07" id="tgt325" class="tgtSentence"> Habrá reducido la funcionalidad de RMS con Exchange Online, como se describe en la sección <link xlink:href="f0d33c5f-a6a6-44a1-bdec-5be1bc8e1e14#BKMK_Pricing">BYOK pricing and restrictions</link> del tema <link xlink:href="f0d33c5f-a6a6-44a1-bdec-5be1bc8e1e14">Planning and Implementing Your Azure Rights Management Tenant Key</link>.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
          <section address="BKMK_Step7Migration">
            <title>
              <caps:sentence sentenceid="82b70be280a638b7b2939b8f72fff4d1" id="tgt326" class="tgtSentence">Paso 7.</caps:sentence>
              <caps:sentence sentenceid="c215284fc4d7fd29381f8f3286d3f9e1" id="tgt327" class="tgtSentence"> Implemente el conector RMS.</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="4a01051fd06342e667c04e3200d092b9" id="tgt328" class="tgtSentence">Si ha utilizado la funcionalidad Information Rights Management (IRM) de Exchange Server o SharePoint Server con AD RMS, primero debe deshabilitar IRM en estos servidores y quitar la configuración de AD RMS.</caps:sentence>
                <caps:sentence sentenceid="e66d9816131b27122114e5328c323428" id="tgt329" class="tgtSentence"> A continuación, implemente el conector de Rights Management (RMS), que actúa como interfaz de comunicaciones (una retransmisión) entre los servidores locales y Azure RMS.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="206af5939efcb63715156bee2aa2b580" id="tgt330" class="tgtSentence">Por último, para este paso, si ha importado varios TPD en Azure RMS que se usaron para proteger los mensajes de correo electrónico, debe editar manualmente el registro en los equipos de Exchange Server para redirigir todas las direcciones URL de TPD al conector RMS.</caps:sentence>
              </para>
              <alert class="note">
                <para>
                  <caps:sentence sentenceid="3e9efa01b5a0b590b4b23f45c0807b3f" id="tgt331" class="tgtSentence">Antes de empezar, compruebe las versiones admitidas de los servidores locales que son compatibles con el conector RMS en "Servidores locales compatibles con Azure RMS" <link xlink:href="dc78321d-d759-4653-8818-80da74b6cdeb#BKMK_SupportedApplications">Applications that support Azure RMS</link> del tema <link xlink:href="dc78321d-d759-4653-8818-80da74b6cdeb">Requirements for Azure Rights Management</link>.</caps:sentence>
                </para>
              </alert>
              <procedure>
                <title>
                  <caps:sentence sentenceid="4cb1f0643b31ab6707fd50d284154dff" id="tgt332" class="tgtSentence">Deshabilitar IRM en servidores de Exchange y quitar la configuración de AD RMS</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="b945916b620db993b5b16a140be8714d" id="tgt333" class="tgtSentence">En cada servidor de Exchange, busque la carpeta siguiente y elimine todas las entradas de esa carpeta: \ProgramData\Microsoft\DRM\Server\S-1-5-18</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="20c089aa8f08762007eb2b71e0adcfa6" id="tgt334" class="tgtSentence">Desde uno de los servidores de Exchange, use el cmdlet <externalLink><linkText>Set_IRMConfiguration</linkText><linkUri>http://technet.microsoft.com/library/dd979792.aspx</linkUri></externalLink> de Exchange para deshabilitar primero las características de IRM para los mensajes enviados a destinatarios internos: </caps:sentence>
                      </para>
                      <code>Set-IRMConfiguration -InternalLicensingEnabled $false</code>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="6ae07daf41a6a2c4dcbec8711a5a9c82" id="tgt335" class="tgtSentence">A continuación, utilice el mismo cmdlet para deshabilitar las características de IRM para los mensajes enviados a destinatarios externos:</caps:sentence>
                      </para>
                      <code>Set-IRMConfiguration -ExternalLicensingEnabled $false</code>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="fd6ff6360c0e7a850f960a26269700b7" id="tgt336" class="tgtSentence">A continuación, use el mismo cmdlet para deshabilitar IRM en Microsoft Office Outlook Web App y en Microsoft Exchange ActiveSync:</caps:sentence>
                      </para>
                      <code>Set-IRMConfiguration -ClientAccessServerEnabled $false</code>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="98cf0c7145d90ac7991609db3ce37057" id="tgt337" class="tgtSentence">Por último, use el mismo cmdlet para borrar los certificados almacenados en la memoria caché:</caps:sentence>
                      </para>
                      <code>Set-IRMConfiguration -RefreshServerCertificates</code>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="8d3e2a4c29ff51e7a7767129532d2cda" id="tgt338" class="tgtSentence">En cada Exchange Server, restablezca ahora IIS, por ejemplo, mediante la ejecución de un símbolo del sistema como administrador y escriba <userInput>iisreset</userInput>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
              <procedure>
                <title>
                  <caps:sentence sentenceid="275b5b52b6f28df41b12437e7216b8ee" id="tgt339" class="tgtSentence">Deshabilitar IRM en servidores de SharePoint y quitar la configuración de AD RMS</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="80d713860e5cbaf688244278ebaeaf25" id="tgt340" class="tgtSentence">Asegúrese de que no hay ningún documento desprotegido desde bibliotecas protegidas con RMS.</caps:sentence>
                        <caps:sentence sentenceid="ddfe5764cd983e85e68912f4bed899bb" id="tgt341" class="tgtSentence"> Si hay, quedarán inaccesibles al final de este procedimiento.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="6cdcc6ef76d8d81a6874cb91d62efb5c" id="tgt342" class="tgtSentence">En el sitio web de Administración central de SharePoint, en la sección <ui>Inicio rápido</ui>, haga clic en <ui>Seguridad</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt343" class="tgtSentence">En la página <ui>Seguridad</ui>, en la página <ui>Directiva de información</ui>, haga clic en <ui>Configurar Information Rights Management</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt344" class="tgtSentence">En la página <ui>Information Rights Management</ui>, en la sección <ui>Information Rights Management</ui>, seleccione <ui>No use IRM en este servidor</ui> y luego haga clic en <ui>Aceptar</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="49c6a2f12f1769ccb4dfbc7840e3425e" id="tgt345" class="tgtSentence">En cada uno de los equipos de SharePoint Server, elimine el contenido de la carpeta \ProgramData\Microsoft\MSIPC\Server\<placeholder>&lt;SID de la cuenta que ejecuta SharePoint Server&gt;</placeholder>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
              <procedure>
                <title>
                  <caps:sentence sentenceid="5f8cb0a4420a79f1c6c0e9c89404dd36" id="tgt346" class="tgtSentence">Instalar y configurar el conector RMS</caps:sentence>
                </title>
                <steps class="bullet">
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="235ed0a4f8aa910730d1f6941a38502b" id="tgt347" class="tgtSentence">Use las instrucciones del tema <link xlink:href="90e7e33f-9ecc-497b-89c5-09205ffc5066">Deploying the Azure Rights Management Connector</link>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
              <procedure>
                <title>
                  <caps:sentence sentenceid="45b9132d6a804689d624987ff64d2707" id="tgt348" class="tgtSentence">En Exchange solo y varios TPD: Editar el registro</caps:sentence>
                </title>
                <steps class="bullet">
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="d3aa9434a1a3f112f1065166ec769d1e" id="tgt349" class="tgtSentence">En cada servidor Exchange, agregue manualmente las claves del Registro siguientes para cada TPD adicional que ha importado, para redirigir las direcciones URL de los TPD al conector RMS.</caps:sentence>
                        <caps:sentence sentenceid="37c3a328b94d5b92973ffd92a6bfe5f5" id="tgt350" class="tgtSentence"> Estas entradas del Registro son específicas para la migración y no se agregan mediante la herramienta de configuración de servidor para el conector RMS de Microsoft.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="cbc9cb4a5151b6bbd82dd788a4b03e96" id="tgt351" class="tgtSentence">Al realizar estas modificaciones del registro, utilice las siguientes instrucciones:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="05d18373e30d5a4c6a58e6f3b2e3e7ab" id="tgt352" class="tgtSentence">Reemplace <placeholder>ConnectorFQDN</placeholder> por el nombre que definió en el DNS para el conector.</caps:sentence>
                            <caps:sentence sentenceid="4eee3758f1bf4073d94deae936dd0a13" id="tgt353" class="tgtSentence"> Por ejemplo, <ui>rmsconnector.contoso.com</ui>.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="525aa5b6a77435179938bcb6a80c3748" id="tgt354" class="tgtSentence">Use el prefijo HTTP o HTTPS para la dirección URL del conector, en función de si ha configurado el conector para usar HTTP o HTTPS para comunicarse con los servidores locales.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                      <para> </para>
                      <para>
                        <embeddedLabel>
                          <caps:sentence sentenceid="88138f7ee93a43414511f38caed9e21f" id="tgt355" class="tgtSentence">Para Exchange 2013:</caps:sentence>
                        </embeddedLabel>
                      </para>
                      <table>
                        <thead>
                          <tr>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="b75ba2542571d3ceaab9c5d83c92075c" id="tgt356" class="tgtSentence">Ruta de acceso del registro</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="599dcce2998a6b40b1e38e8c6006cb0a" id="tgt357" class="tgtSentence">Tipo</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="2063c1608d6e0baf80249c42e2be5804" id="tgt358" class="tgtSentence">Valor</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="8d777f385d3dfec8815d20f7496026dc" id="tgt359" class="tgtSentence">Datos</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                        </thead>
                        <tbody>
                          <tr>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="51bd899ad0b193c2861a83d1d8f8c447" id="tgt360" class="tgtSentence">HKLM\SOFTWARE\Microsoft\ExchangeServer\v15\IRM\LicenseServerRedirection</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="2b1bda4361069cdf7a4437824c22893c" id="tgt361" class="tgtSentence">Reg_SZ</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="c3d957a855225df0e45cb87b34facd88" id="tgt362" class="tgtSentence">https://&lt;AD RMS Intranet Licensing URL&gt;/_wmcs/licensing</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="5e9f115816f9a71685775cd8d7bf469f" id="tgt363" class="tgtSentence">Una de las siguientes, en función de si usas HTTP o HTTPS desde tu servidor Exchange al conector RMS:</caps:sentence>
                              </para>
                              <list class="bullet">
                                <listItem>
                                  <para>
                                    <caps:sentence sentenceid="199c6265e21e51538d2129bb847d8773" id="tgt364" class="tgtSentence">http://&lt;connectorFQDN&gt;/_wmcs/licensing</caps:sentence>
                                  </para>
                                </listItem>
                                <listItem>
                                  <para>
                                    <caps:sentence sentenceid="fb67fe12165a832ef54d0fde1c564982" id="tgt365" class="tgtSentence">https://&lt;connectorName&gt;/_wmcs/licensing</caps:sentence>
                                  </para>
                                </listItem>
                              </list>
                            </TD>
                          </tr>
                          <tr>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="47a5fe058dba39acbc92107d29512f94" id="tgt366" class="tgtSentence">HKLM\SOFTWARE\Microsoft\ExchangeServer\v15\IRM\LicenseServerRedirection </caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="2b1bda4361069cdf7a4437824c22893c" id="tgt367" class="tgtSentence">Reg_SZ</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="c59e0643dded1f67b95dc4bd20e91159" id="tgt368" class="tgtSentence">https://&lt;AD RMS Extranet Licensing URL&gt;/_wmcs/licensing</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="5e9f115816f9a71685775cd8d7bf469f" id="tgt369" class="tgtSentence">Una de las siguientes, en función de si usas HTTP o HTTPS desde tu servidor Exchange al conector RMS:</caps:sentence>
                              </para>
                              <list class="bullet">
                                <listItem>
                                  <para>
                                    <caps:sentence sentenceid="199c6265e21e51538d2129bb847d8773" id="tgt370" class="tgtSentence">http://&lt;connectorFQDN&gt;/_wmcs/licensing</caps:sentence>
                                  </para>
                                </listItem>
                                <listItem>
                                  <para>
                                    <caps:sentence sentenceid="65298cd1387373567c3ce80fc50563a7" id="tgt371" class="tgtSentence">https://&lt;connectorFQDN&gt;/_wmcs/licensing</caps:sentence>
                                  </para>
                                </listItem>
                              </list>
                            </TD>
                          </tr>
                        </tbody>
                      </table>
                      <para>
                        <embeddedLabel>
                          <caps:sentence sentenceid="72a43bf3a41b9e52faaec8adcc836ab2" id="tgt372" class="tgtSentence">Para Exchange Server 2010:</caps:sentence>
                        </embeddedLabel>
                      </para>
                      <table>
                        <thead>
                          <tr>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="b75ba2542571d3ceaab9c5d83c92075c" id="tgt373" class="tgtSentence">Ruta de acceso del registro</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="599dcce2998a6b40b1e38e8c6006cb0a" id="tgt374" class="tgtSentence">Tipo</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="2063c1608d6e0baf80249c42e2be5804" id="tgt375" class="tgtSentence">Valor</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="8d777f385d3dfec8815d20f7496026dc" id="tgt376" class="tgtSentence">Datos</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                        </thead>
                        <tbody>
                          <tr>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="79ca1b8c2bde5ffb54f84618991ea02c" id="tgt377" class="tgtSentence">HKLM\SOFTWARE\Microsoft\ExchangeServer\v14\IRM\LicenseServerRedirection</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="2b1bda4361069cdf7a4437824c22893c" id="tgt378" class="tgtSentence">Reg_SZ</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="c3d957a855225df0e45cb87b34facd88" id="tgt379" class="tgtSentence">https://&lt;AD RMS Intranet Licensing URL&gt;/_wmcs/licensing</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="5e9f115816f9a71685775cd8d7bf469f" id="tgt380" class="tgtSentence">Una de las siguientes, en función de si usas HTTP o HTTPS desde tu servidor Exchange al conector RMS:</caps:sentence>
                              </para>
                              <list class="bullet">
                                <listItem>
                                  <para>
                                    <caps:sentence sentenceid="6378b91b7748d08e6db05d742d0d9341" id="tgt381" class="tgtSentence">http://&lt;connectorName&gt;/_wmcs/licensing</caps:sentence>
                                  </para>
                                </listItem>
                                <listItem>
                                  <para>
                                    <caps:sentence sentenceid="fb67fe12165a832ef54d0fde1c564982" id="tgt382" class="tgtSentence">https://&lt;connectorName&gt;/_wmcs/licensing</caps:sentence>
                                  </para>
                                </listItem>
                              </list>
                            </TD>
                          </tr>
                          <tr>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="f74b707c98c3d36302cf00f38d047678" id="tgt383" class="tgtSentence">HKLM\SOFTWARE\Microsoft\ExchangeServer\v14\IRM\LicenseServerRedirection </caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="2b1bda4361069cdf7a4437824c22893c" id="tgt384" class="tgtSentence">Reg_SZ</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="c59e0643dded1f67b95dc4bd20e91159" id="tgt385" class="tgtSentence">https://&lt;AD RMS Extranet Licensing URL&gt;/_wmcs/licensing</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="5e9f115816f9a71685775cd8d7bf469f" id="tgt386" class="tgtSentence">Una de las siguientes, en función de si usas HTTP o HTTPS desde tu servidor Exchange al conector RMS:</caps:sentence>
                              </para>
                              <list class="bullet">
                                <listItem>
                                  <para>
                                    <caps:sentence sentenceid="6378b91b7748d08e6db05d742d0d9341" id="tgt387" class="tgtSentence">http://&lt;connectorName&gt;/_wmcs/licensing</caps:sentence>
                                  </para>
                                </listItem>
                                <listItem>
                                  <para>
                                    <caps:sentence sentenceid="fb67fe12165a832ef54d0fde1c564982" id="tgt388" class="tgtSentence">https://&lt;connectorName&gt;/_wmcs/licensing</caps:sentence>
                                  </para>
                                </listItem>
                              </list>
                            </TD>
                          </tr>
                        </tbody>
                      </table>
                    </content>
                  </step>
                </steps>
              </procedure>
              <para>
                <caps:sentence sentenceid="0c0abd7b51e76b51a287edcfa68680ef" id="tgt389" class="tgtSentence">Después de completar estos procedimientos, asegúrese de leer la sección <embeddedLabel>Pasos siguientes</embeddedLabel> del tema <link xlink:href="90e7e33f-9ecc-497b-89c5-09205ffc5066">Deploying the Azure Rights Management Connector</link>.</caps:sentence>
              </para>
            </content>
          </section>
          <section address="BKMK_Step8Migration">
            <title>
              <caps:sentence sentenceid="d8785da18caa06d14c0e8952f7dcd32b" id="tgt390" class="tgtSentence">Paso 8.</caps:sentence>
              <caps:sentence sentenceid="a46740565efff323a443abd3c32c5ec1" id="tgt391" class="tgtSentence"> Retire AD RMS</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="f24462cc508f5bf969819d53db8282eb" id="tgt392" class="tgtSentence">Opcional: Quite el punto de conexión de servicio (SCP) de Active Directory para evitar que los equipos detecten la infraestructura local de Rights Management.</caps:sentence>
                <caps:sentence sentenceid="fb1479a40c4c4ecf3411a4711e9fdae8" id="tgt393" class="tgtSentence"> Esta acción es opcional debido al redireccionamiento configurado en el registro (por ejemplo, al ejecutar el script de migración).</caps:sentence>
                <caps:sentence sentenceid="4edd9136b92d92ec99f88fd06bca3788" id="tgt394" class="tgtSentence"> Para quitar el punto de conexión de servicio, use la herramienta de registro de AD SCP desde el <externalLink><linkText>kit de herramientas de administración de Rights Management Services</linkText><linkUri>http://www.microsoft.com/download/details.aspx?id=1479</linkUri></externalLink>.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="6358aa903cadff21f0dd08ad1132af44" id="tgt395" class="tgtSentence">Supervise la actividad de los servidores de AD RMS. Para ello, por ejemplo, compruebe las <externalLink><linkText>solicitudes en el informe de mantenimiento del sistema</linkText><linkUri>https://technet.microsoft.com/library/ee221012(v=ws.10).aspx</linkUri></externalLink>, la <externalLink><linkText>tabla ServiceRequest</linkText><linkUri>http://technet.microsoft.com/library/dd772686(v=ws.10).aspx</linkUri></externalLink> o realice una <externalLink><linkText>auditoría del acceso de los usuarios a contenido protegido</linkText><linkUri>http://social.technet.microsoft.com/wiki/contents/articles/3440.ad-rms-frequently-asked-questions-faq.aspx</linkUri></externalLink>.</caps:sentence>
                <caps:sentence sentenceid="dc3fe8e83a556aee7fff9c3dc5de0824" id="tgt396" class="tgtSentence"> Cuando haya confirmado que los clientes de RMS ya no se comunican con estos servidores y que los clientes están utilizando Azure RMS correctamente, puede quitar el rol de servidor de AD RMS de estos servidores.</caps:sentence>
                <caps:sentence sentenceid="b73f62cbcca2f9dd62969242fc593aa0" id="tgt397" class="tgtSentence"> Si usa servidores dedicados, es preferible aplicar una medida de cautela basada en cerrar primero los servidores durante un período de tiempo para asegurarse de que no hay ningún problema notificado que requiera reiniciar estos servidores para garantizar la continuidad del servicio mientras investiga por qué los clientes no usan Azure RMS.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="b445dc536cdcaac5e52afab6f17ccc04" id="tgt398" class="tgtSentence">Después de retirar los servidores de AD RMS, seguramente le interese revisar las plantillas en el Portal de Azure clásico y consolidarlas para que los usuarios tengan menos opciones entre las que elegir, volver a configurarlas o incluso agregar plantillas nuevas.</caps:sentence>
                <caps:sentence sentenceid="1c24f8517834ee2908d00b738c4a1e08" id="tgt399" class="tgtSentence"> También sería una buena oportunidad para publicar las plantillas predeterminadas.</caps:sentence>
                <caps:sentence sentenceid="1070f425823a6e05a98eb2d747f0c53d" id="tgt400" class="tgtSentence"> Para obtener más información, vea <link xlink:href="1775d8d0-9a59-42c8-914f-ce285b71ac1c">Configuring Custom Templates for Azure Rights Management</link>.</caps:sentence>
              </para>
            </content>
          </section>
          <section address="BKMK_Step9Migration">
            <title>
              <caps:sentence sentenceid="9740009227fb6c485ee9234e2bb22aad" id="tgt401" class="tgtSentence">Step 9.</caps:sentence>
              <caps:sentence sentenceid="712c1499aa587e340e896f4ad5f549f6" id="tgt402" class="tgtSentence"> Vuelva a escribir su clave de inquilino de Azure RMS.</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="3590f7e71dbdd8af3a75878020ec66a2" id="tgt403" class="tgtSentence">Este paso es necesario cuando la migración está completa si la implementación de AD RMS usaba el modo criptográfico 1 de RMS, porque al volver a escribir la clave se crea una nueva clave de inquilino que usa el modo criptográfico 2 de RMS.</caps:sentence>
                <caps:sentence sentenceid="46fb3a8918cfddefa14d51b279e44b8c" id="tgt404" class="tgtSentence"> Se admite el uso de Azure RMS con el modo criptográfico 1 únicamente durante el proceso de migración.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="4d6b96ac0fd56ec3524bd8e8eb8209c2" id="tgt405" class="tgtSentence">Este paso es opcional pero se recomienda cuando la migración se ha completado incluso si estuviera ejecutando el modo criptográfico 2 de RMS, porque ayuda a proteger la clave de inquilino de Azure RMS de posibles infracciones de seguridad para su clave de AD RMS.</caps:sentence>
                <caps:sentence sentenceid="cf1ef74a2b503a8f29a4f96b475f3620" id="tgt406" class="tgtSentence"> Si vuelve a definir la clave de inquilino de Azure RMS (lo que también se conoce como "revertir su clave"), se crea una nueva clave y se archiva la clave original.</caps:sentence>
                <caps:sentence sentenceid="9c76dda946a62e989f0d2f106da2d0b8" id="tgt407" class="tgtSentence"> Sin embargo, dado que el paso de una clave a otra no es inmediato, sino que requiere unas cuantas semanas, no espere hasta sospechar de una infracción de la clave original y, en su lugar, vuelva a definir la clave del inquilino de RMS en cuanto se complete la migración.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="760ae5f1e9e540510c59d7672295d5a1" id="tgt408" class="tgtSentence">Vuelva a definir la clave del inquilino de Azure RMS:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="d75850d3af942b4c253ea62e47f8bd5d" id="tgt409" class="tgtSentence">Si Microsoft administra su clave de inquilino de RMS: llame a los servicios de soporte técnico de Microsoft (CSS) y demuestre que es el administrador del inquilino de RMS.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="556593379eb58e05fab79933f104f64d" id="tgt410" class="tgtSentence">Si la clave de inquilino de RMS está administrada por el usuario (BYOK): Repita el procedimiento BYOK para generar y crear una nueva clave a través de Internet o en persona.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="3bd4825c070d7882d0e732aaebeb0c48" id="tgt411" class="tgtSentence">Para obtener más información acerca de la administración de la clave de inquilino de RMS, consulte <link xlink:href="1284d0ee-0a72-45ba-a64c-3dcb25846c3d">Operations for Your Azure Rights Management Tenant Key</link>.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
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
          <caps:sentence id="src1" class="srcSentence">Use the following set of instructions to  migrate your Active Directory Rights Management Services (AD RMS) deployment to Azure Rights Management (Azure RMS).</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> After the migration, users will still have access to documents and email messages that your organization protected by using AD RMS, and newly protected content will use Azure RMS.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src3" class="srcSentence">Not sure whether this AD RMS migration is right for your organization?</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src4" class="srcSentence">For an introduction to Azure RMS,  the business problems that it can solve, what it looks like to administrators and users, and how it works, see <link xlink:href="aeeebcd7-6646-4405-addf-ee1cc74df5df">What is Azure Rights Management?</link></caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src5" class="srcSentence">For a comparison of Azure RMS with AD RMS, see <link xlink:href="8123bd62-1814-4d79-b306-e20c1a00e264">Comparing Azure Rights Management and AD RMS</link>.</caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src6" class="srcSentence">Prerequisites for migrating AD RMS to Azure RMS</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src7" class="srcSentence">Before you start the migration to Azure RMS, make sure that the following prerequisites are in place and that you understand any limitations.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src8" class="srcSentence">Requirement</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src9" class="srcSentence">More information</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src10" class="srcSentence">A supported RMS deployment</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src11" class="srcSentence">All releases of AD RMS from Windows Server 2008 through Windows Server 2012 R2 support a migration to Azure RMS:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src12" class="srcSentence">Windows Server 2008 (x86 or x64)</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src13" class="srcSentence">Windows Server 2008 R2 (x64)</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src14" class="srcSentence">Windows Server 2012 (x64)</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src15" class="srcSentence">Windows Server 2012 R2 (x64)</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <alert class="note">
                    <para>
                      <caps:sentence id="src16" class="srcSentence">If you are running Windows RMS on Windows Server 2003, this version of the operating system will be out of support during 2015.</caps:sentence>
                      <caps:sentence id="src17" class="srcSentence"> You can migrate this version of RMS to Azure RMS, but this process is supported only if the operating system is still supported.</caps:sentence>
                      <caps:sentence id="src18" class="srcSentence"> As a workaround, you could import your trusted publishing domain (TPD) to a version of AD RMS that is supported, and then re-import the TPD without the RMS 1.0 compatibility option.</caps:sentence>
                      <caps:sentence id="src19" class="srcSentence"> For more information about TPDs, see <externalLink><linkText>Trusted Publishing Domain</linkText><linkUri>http://technet.microsoft.com/library/dd996639(v=ws.10).aspx</linkUri></externalLink></caps:sentence>
                    </para>
                  </alert>
                  <para>
                    <caps:sentence id="src20" class="srcSentence">All valid AD RMS topologies are supported:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src21" class="srcSentence">Single forest, single RMS cluster</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src22" class="srcSentence">Single forest, multiple licensing-only RMS clusters</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src23" class="srcSentence">Multiple forests, multiple RMS clusters</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <alert class="note">
                    <para>
                      <caps:sentence id="src24" class="srcSentence">By default, multiple RMS clusters migrate to a single Azure RMS tenant.</caps:sentence>
                      <caps:sentence id="src25" class="srcSentence"> If you want different RMS tenants, you must treat them as different migrations.</caps:sentence>
                      <caps:sentence id="src26" class="srcSentence"> A key from one RMS cluster cannot be imported to more than one Azure RMS tenant.</caps:sentence>
                    </para>
                  </alert>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src27" class="srcSentence">All requirements to run Azure RMS, including an Azure RMS tenant (not activated)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src28" class="srcSentence">See <link xlink:href="dc78321d-d759-4653-8818-80da74b6cdeb">Requirements for Azure Rights Management</link>.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src29" class="srcSentence">Although you must have an Azure RMS tenant before you can migrate from AD RMS, we recommend that you do not activate the Rights Management service before the migration.</caps:sentence>
                    <caps:sentence id="src30" class="srcSentence"> The migration process includes this step after you have exported keys and templates from AD RMS and imported them to Azure RMS.</caps:sentence>
                    <caps:sentence id="src31" class="srcSentence"> However, if Azure RMS is already activated, you can still migrate from AD RMS.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src32" class="srcSentence">Preparation for Azure RMS:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src33" class="srcSentence">Directory synchronization between your on-premises directory and Azure Active Directory</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src34" class="srcSentence">Mail-enabled groups in Azure Active Directory</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src35" class="srcSentence">See <link xlink:href="afbca2d6-32a7-4bda-8aaf-9f93f5da5abc">Preparing for Azure Rights Management</link>.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src36" class="srcSentence">If you have used the Information Rights Management (IRM) functionality of Exchange Server (for example, transport rules and Outlook Web Access) or SharePoint Server with AD RMS:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src37" class="srcSentence">Plan for a short period of time when IRM will not be available on these servers</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src38" class="srcSentence">You can continue to use IRM on these servers with Azure RMS after the migration.</caps:sentence>
                    <caps:sentence id="src39" class="srcSentence"> However, one of the migration steps is to temporarily disable the IRM service, install and configure a connector, reconfigure the servers, and then re-enable IRM.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src40" class="srcSentence">This is the only interruption to service during the migration process.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <caps:sentence id="src41" class="srcSentence">Limitations:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src42" class="srcSentence">Although the migration process supports migrating your server licensing certificate (SLC) key to a hardware security module (HSM) for Azure RMS, Exchange Online does not currently support this configuration. If you want full IRM functionality with Exchange Online after you migrate to Azure RMS, your Azure RMS tenant key must be <externalLink><linkText>managed by Microsoft</linkText><linkUri>http://technet.microsoft.com/library/dn440580.aspx</linkUri></externalLink>. Alternatively, you can run IRM with reduced functionality in Exchange Online  when your Azure RMS tenant is managed by you (BYOK). For more information about using Exchange Online with Azure RMS, see <link xlink:href="#BKMK_Step6Migration">Step 6. Configure IRM integration for Exchange Online</link> in these instructions.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src43" class="srcSentence">If you have software and clients that are not supported with Azure RMS, they will not be able to protect or consume content that is protected by Azure RMS.</caps:sentence>
                <caps:sentence id="src44" class="srcSentence"> Be sure to check the supported applications and clients section in the <link xlink:href="dc78321d-d759-4653-8818-80da74b6cdeb">Requirements for Azure Rights Management</link> topic.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src45" class="srcSentence">If you import your on-premises key to Azure RMS as archived (you do not set the TPD to be the active during the import process) and you migrate users in batches for a phased migration, content that is newly protected by the migrated users will not be accessible to users who remain on AD RMS.</caps:sentence>
                <caps:sentence id="src46" class="srcSentence"> In this scenario, whenever  possible, keep the migration time short and migrate users in logical batches such that if they collaborate with one another, they are migrated together.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src47" class="srcSentence">This limitation does not apply when you set the TPD to active during the import process, because all users will protect content by using the same key.</caps:sentence>
                <caps:sentence id="src48" class="srcSentence"> We recommend this configuration because it lets you migrate all users independently and at your own pace.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src49" class="srcSentence">If you collaborate with external partners (for example, by using trusted user domains or federation), they must also migrate to Azure RMS either at the same time as your migration, or as soon as possible afterwards.</caps:sentence>
                <caps:sentence id="src50" class="srcSentence"> To continue to access content that your organization previously protected by using AD RMS, they must make client configuration changes that are similar to those that you make, and included in this document.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src51" class="srcSentence">Because of the possible configuration variations that your partners might have, exact instructions for this reconfiguration are out of scope for this document.</caps:sentence>
                <caps:sentence id="src52" class="srcSentence"> For help, contact Microsoft Customer Support Services (CSS).</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src53" class="srcSentence">Steps for migrating AD RMS to Azure RMS</caps:sentence>
        </title>
        <content>
          <para></para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src54" class="srcSentence">Migration step</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src55" class="srcSentence">More information</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <embeddedLabel>
                      <caps:sentence id="src56" class="srcSentence">1. Download the Azure RMS Management Administration Tools</caps:sentence>
                    </embeddedLabel>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src57" class="srcSentence">For instructions, see <link xlink:href="828cf1f7-d0e7-4edf-8525-91896dbe3172#BKMK_Step1Migration">Step 1: Download the Azure Rights Management Administration Tool</link>.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <embeddedLabel>
                      <caps:sentence id="src58" class="srcSentence">2. Export configuration data from AD RMS and import it to Azure RMS</caps:sentence>
                    </embeddedLabel>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src59" class="srcSentence">You export the configuration data (keys, templates, URLs) from AD RMS to an XML file, and then upload that file to Azure RMS by using the Import-AadrmTpd Windows PowerShell cmdlet.</caps:sentence>
                    <caps:sentence id="src60" class="srcSentence"> Additional steps might be needed, depending your on AD RMS key configuration:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src61" class="srcSentence">Software-protected key to software-protected key migration: Centrally managed, password-based keys in AD RMS to Microsoft-managed Azure RMS tenant key.</caps:sentence>
                        <caps:sentence id="src62" class="srcSentence"> This is the simplest migration path and no additional steps are required.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src63" class="srcSentence">HSM-protected  key to HSM-protected key migration: Keys that are stored by an HSM for AD RMS to customer-managed Azure RMS tenant key (the “bring your own key” or BYOK scenario).</caps:sentence>
                        <caps:sentence id="src64" class="srcSentence"> This requires additional steps to transfer the key from your on-premises Thales HSM to the Azure RMS HSM.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src65" class="srcSentence">Software-protected key to HSM-protected key migration: Centrally managed, password-based keys in AD RMS to customer-managed Azure RMS tenant key (the “bring your own key” or BYOK scenario).</caps:sentence>
                        <caps:sentence id="src66" class="srcSentence"> This requires the most configuration because you must first extract your software key and import it to an on-premises HSM, and then do the additional steps to transfer the key from your on-premises Thales HSM to the Azure RMS HSM.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence id="src67" class="srcSentence">For instructions, see <link xlink:href="828cf1f7-d0e7-4edf-8525-91896dbe3172#BKMK_Step2Migration">Step 2. Export configuration data from AD RMS and import it to Azure RMS</link>.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <embeddedLabel>
                      <caps:sentence id="src68" class="srcSentence">3. Activate your RMS tenant</caps:sentence>
                    </embeddedLabel>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src69" class="srcSentence">If possible, do this step after the import process and not before.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src70" class="srcSentence">For more information and instructions, see <link xlink:href="828cf1f7-d0e7-4edf-8525-91896dbe3172#BKMK_Step3Migration">Step 3. Activate your RMS tenant</link>.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <embeddedLabel>
                      <caps:sentence id="src71" class="srcSentence">4. Configure imported templates</caps:sentence>
                    </embeddedLabel>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src72" class="srcSentence">When you import your rights policy templates, their status is archived.</caps:sentence>
                    <caps:sentence id="src73" class="srcSentence"> If you want users to be able to see and use them, you must change the template status to published in the Azure classic portal.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src74" class="srcSentence">For instructions, see <link xlink:href="828cf1f7-d0e7-4edf-8525-91896dbe3172#BKMK_Step4Migration">Step 4. Configure imported templates</link>.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <embeddedLabel>
                      <caps:sentence id="src75" class="srcSentence">5. Reconfigure clients to use Azure RMS</caps:sentence>
                    </embeddedLabel>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src76" class="srcSentence">Existing Windows computers must be reconfigured to use the Azure RMS service instead of AD RMS.</caps:sentence>
                    <caps:sentence id="src77" class="srcSentence"> This step applies to computers in your organization, and to computers in partner organizations if you have collaborated with them while you were running AD RMS.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src78" class="srcSentence">In addition, if you have deployed the <externalLink><linkText>mobile device extensions</linkText><linkUri>http://technet.microsoft.com/library/dn673574.aspx</linkUri></externalLink> to support mobile devices such as iOS phones and iPads, Android phones and tablets, Windows phone, and Mac computers, you must remove the SRV records in DNS that redirected these clients to use AD RMS.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src79" class="srcSentence">For instructions, see <link xlink:href="828cf1f7-d0e7-4edf-8525-91896dbe3172#BKMK_Step5Migration">Step 5. Reconfigure clients to use Azure RMS</link>.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <embeddedLabel>
                      <caps:sentence id="src80" class="srcSentence">6. Configure IRM integration with Exchange Online</caps:sentence>
                    </embeddedLabel>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src81" class="srcSentence">This step is required if you want to use Exchange Online with Azure RMS.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src82" class="srcSentence">For instructions, see <link xlink:href="#BKMK_Step6Migration">Step 6. Configure IRM integration for Exchange Online</link>.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <embeddedLabel>
                      <caps:sentence id="src83" class="srcSentence">7. Deploy the RMS connector</caps:sentence>
                    </embeddedLabel>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src84" class="srcSentence">This step is required if you want to use any of the following on-premises services with Azure RMS:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src85" class="srcSentence">Exchange Server (for example, transport rules and Outlook Web Access)</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src86" class="srcSentence">SharePoint Server </caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src87" class="srcSentence">Windows Server that runs File Classification Infrastructure</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence id="src88" class="srcSentence">For instructions, see <link xlink:href="#BKMK_Step7Migration">Step 7. Deploy the RMS connector</link>.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src89" class="srcSentence">
                      <embeddedLabel>8. Decommission AD RMS</embeddedLabel> </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src90" class="srcSentence">When you have confirmed that all clients are using Azure RMS and no longer accessing the AD RMS servers, you can decommission your AD RMS deployment.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src91" class="srcSentence">For instructions, see <link xlink:href="#BKMK_Step8Migration">Step 8. Decommission AD RMS</link>.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <embeddedLabel>
                      <caps:sentence id="src92" class="srcSentence">9. Re-key your Azure RMS tenant key</caps:sentence>
                    </embeddedLabel>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src93" class="srcSentence">This step is required if you were not running in Cryptographic Mode 2 before the migration, and optional but recommended for all migrations to help safeguard the security of your Azure RMS tenant key.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src94" class="srcSentence">For instructions, see <link xlink:href="#BKMK_Step9Migration">Step 9. Re-key your Azure RMS tenant key</link>.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
        <sections>
          <section address="BKMK_Step1Migration">
            <title>
              <caps:sentence id="src95" class="srcSentence">Step 1: Download the Azure Rights Management Administration Tool</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src96" class="srcSentence">Go to the Microsoft Download Center and download the <externalLink><linkText>Azure Rights Management Administration Tool</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=257721</linkUri></externalLink>, which contains the Azure RMS administration module for Windows PowerShell.</caps:sentence>
              </para>
            </content>
          </section>
          <section address="BKMK_Step2Migration">
            <title>
              <caps:sentence id="src97" class="srcSentence">Step 2.</caps:sentence>
              <caps:sentence id="src98" class="srcSentence"> Export configuration data from AD RMS and import it to Azure RMS</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src99" class="srcSentence">This step is a two-part process:</caps:sentence>
              </para>
              <list class="ordered">
                <listItem>
                  <para>
                    <caps:sentence id="src100" class="srcSentence">Export the configuration data from AD RMS by exporting the trusted publishing domains (TPDs) to an .xml file.</caps:sentence>
                    <caps:sentence id="src101" class="srcSentence"> This process is the same for all migrations.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src102" class="srcSentence">Import the configuration data to Azure RMS.</caps:sentence>
                    <caps:sentence id="src103" class="srcSentence"> There are different processes for this step, depending on your current AD RMS deployment configuration and your preferred topology for your Azure RMS tenant key.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
            <sections>
              <section>
                <title>
                  <caps:sentence id="src104" class="srcSentence">Export the configuration data from AD RMS</caps:sentence>
                </title>
                <content>
                  <para>
                    <caps:sentence id="src105" class="srcSentence">Do the following procedure on all AD RMS clusters, for all trusted publishing domains that have protected content for your organization.</caps:sentence>
                    <caps:sentence id="src106" class="srcSentence"> You do not need to run this on licensing-only clusters.</caps:sentence>
                  </para>
                  <alert class="note">
                    <para>
                      <caps:sentence id="src107" class="srcSentence">If you are using Windows Server 2003 Rights Management, instead of these instructions, follow the procedure <externalLink><linkText>Export SLC, TUD, TPD and RMS private key</linkText><linkUri>http://technet.microsoft.com/library/jj835767(v=ws.10).aspx</linkUri></externalLink> from the <externalLink><linkText>Migrating from Windows RMS to AD RMS in a Different Infrastructure</linkText><linkUri>http://technet.microsoft.com/library/jj835767(v=ws.10).aspx</linkUri></externalLink> topic.</caps:sentence>
                    </para>
                  </alert>
                  <procedure>
                    <title>
                      <caps:sentence id="src108" class="srcSentence">To export the configuration data (trusted publishing domain information)</caps:sentence>
                    </title>
                    <steps class="ordered">
                      <step>
                        <content>
                          <para>
                            <caps:sentence id="src109" class="srcSentence">Log on the AD RMS cluster as a user with AD RMS administration permissions.</caps:sentence>
                          </para>
                        </content>
                      </step>
                      <step>
                        <content>
                          <para>
                            <caps:sentence id="src110" class="srcSentence">From the AD RMS management console (<ui>Active Directory Rights Management Services</ui>), expand the AD RMS cluster name, expand <ui>Trust Policies</ui>, and then click <ui>Trusted Publishing Domains</ui>.</caps:sentence>
                          </para>
                        </content>
                      </step>
                      <step>
                        <content>
                          <para>
                            <caps:sentence id="src111" class="srcSentence">In the results pane, select the trusted publishing domain, and then, from the Actions pane, click <ui>Export Trusted Publishing Domain</ui>.</caps:sentence>
                          </para>
                        </content>
                      </step>
                      <step>
                        <content>
                          <para>
                            <caps:sentence id="src112" class="srcSentence">In the <ui>Export Trusted Publishing Domain</ui> dialog box: </caps:sentence>
                          </para>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence id="src113" class="srcSentence">Click <ui>Save As</ui> and save to path and a file name of your choice.</caps:sentence>
                                <caps:sentence id="src114" class="srcSentence"> Make sure to specify <userInput>.xml</userInput> as the file name extension (this is not appended automatically).</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src115" class="srcSentence">Specify and confirm a strong password.</caps:sentence>
                                <caps:sentence id="src116" class="srcSentence"> Remember this password, because you will need it later, when you import the configuration data to Azure RMS.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src117" class="srcSentence">Do not select the checkbox to save the trusted domain file in RMS version 1.0.</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </content>
                      </step>
                    </steps>
                    <conclusion>
                      <content>
                        <para>
                          <caps:sentence id="src118" class="srcSentence">When you have exported all the trusted publishing domains, you’re ready to start the procedure to import this data to Azure RMS.</caps:sentence>
                        </para>
                      </content>
                    </conclusion>
                  </procedure>
                </content>
              </section>
              <section>
                <title>
                  <caps:sentence id="src119" class="srcSentence">Import the configuration data to Azure RMS</caps:sentence>
                </title>
                <content>
                  <para>
                    <caps:sentence id="src120" class="srcSentence">The exact procedures for this step depend on your current AD RMS deployment configuration, and your preferred topology for your Azure RMS tenant key.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src121" class="srcSentence">Your current AD RMS deployment will be using one of the following configurations for your server licensor certificate (SLC) key:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src122" class="srcSentence">Password protection in the AD RMS database.</caps:sentence>
                        <caps:sentence id="src123" class="srcSentence"> This is the default configuration.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src124" class="srcSentence">HSM protection by using a Thales hardware security module (HSM).</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src125" class="srcSentence">HSM protection by using a hardware security module (HSM) from a supplier other than Thales.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src126" class="srcSentence">Password protected by using an external cryptographic provider.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <alert class="note">
                    <para>
                      <caps:sentence id="src127" class="srcSentence">For more information about using hardware security modules with AD RMS, see <externalLink><linkText>Using AD RMS with Hardware Security Modules</linkText><linkUri>http://technet.microsoft.com/library/jj651024.aspx</linkUri></externalLink>.</caps:sentence>
                    </para>
                  </alert>
                  <para>
                    <caps:sentence id="src128" class="srcSentence">The two Azure RMS tenant key topology options are: Microsoft manages your tenant key (<embeddedLabel>Microsoft-managed</embeddedLabel>) or you manage your tenant key (<embeddedLabel>customer-managed</embeddedLabel>).</caps:sentence>
                    <caps:sentence id="src129" class="srcSentence"> When you manage your own Azure RMS tenant key, it’s sometimes referred to as “bring your own key” (BYOK) and requires a hardware security module (HSM) from Thales.</caps:sentence>
                    <caps:sentence id="src130" class="srcSentence"> For more information, see the <link xlink:href="f0d33c5f-a6a6-44a1-bdec-5be1bc8e1e14#BKMK_ChooseTenantKey">Choose your tenant key topology: Managed by Microsoft (the default) or managed by you (BYOK)</link> section in the <link xlink:href="f0d33c5f-a6a6-44a1-bdec-5be1bc8e1e14">Planning and Implementing Your Azure Rights Management Tenant Key</link> topic.</caps:sentence>
                  </para>
                  <alert class="important">
                    <para>
                      <caps:sentence id="src131" class="srcSentence"> Exchange Online is not currently  compatible with Azure RMS BYOK.</caps:sentence>
                      <caps:sentence id="src132" class="srcSentence">  If you want to use BYOK after your migration and plan to use Exchange Online, make sure that you understand how this configuration reduces IRM functionality for Exchange Online.</caps:sentence>
                      <caps:sentence id="src133" class="srcSentence"> Review  the information in the <link xlink:href="f0d33c5f-a6a6-44a1-bdec-5be1bc8e1e14#BKMK_Pricing">BYOK pricing and restrictions</link> section in the  <link xlink:href="f0d33c5f-a6a6-44a1-bdec-5be1bc8e1e14">Planning and Implementing Your Azure Rights Management Tenant Key</link> topic to help you choose the best Azure RMS tenant key topology for your migration.</caps:sentence>
                    </para>
                  </alert>
                  <para>
                    <caps:sentence id="src134" class="srcSentence">Use the following table to identify which procedure to use for your migration.</caps:sentence>
                    <caps:sentence id="src135" class="srcSentence"> Combinations that are not listed are not supported.</caps:sentence>
                  </para>
                  <table>
                    <thead>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src136" class="srcSentence">Current AD RMS deployment</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src137" class="srcSentence">Chosen Azure RMS tenant key topology</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src138" class="srcSentence">Migration instructions</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </thead>
                    <tbody>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src139" class="srcSentence">Password protection in the AD RMS database</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src140" class="srcSentence">Microsoft-managed</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src141" class="srcSentence">See the <embeddedLabel>Software-protected key to software-protected key migration</embeddedLabel> procedure after this table.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence id="src142" class="srcSentence">This is the simplest migration path and requires only that you transfer your configuration data to Azure RMS.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src143" class="srcSentence">HSM protection by using a Thales nShield hardware security module (HSM)</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src144" class="srcSentence">Customer-managed (BYOK)</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src145" class="srcSentence">See the <embeddedLabel>HSM-protected key to HSM-protected key migration</embeddedLabel> procedure after this table.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence id="src146" class="srcSentence">This requires the BYOK toolset and two set of steps to transfer the key from your on-premises HSM to the Azure RMS HSMs and then transfer your configuration data to Azure RMS.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src147" class="srcSentence">Password protection in the AD RMS database</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src148" class="srcSentence">Customer-managed (BYOK)</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src149" class="srcSentence">See the <embeddedLabel>Software-protected key to HSM-protected key migration</embeddedLabel> procedure after this table.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence id="src150" class="srcSentence">This requires the BYOK toolset and three sets of steps to first extract your software key and import it to an on-premises HSM, then transfer the key from your on-premises HSM to the Azure RMS HSMs, and finally transfer your configuration data to Azure RMS.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src151" class="srcSentence">HSM protection by using a hardware security module (HSM) from a supplier other than Thales</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src152" class="srcSentence">Customer-managed (BYOK)</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src153" class="srcSentence">Contact the supplier for you HSM for instructions how to transfer your key from this HSM to a Thales nShield Hardware Security Module (HSM).</caps:sentence>
                            <caps:sentence id="src154" class="srcSentence"> Then follow the instructions for the <embeddedLabel>HSM-protected key to HSM-protected key migration</embeddedLabel> procedure after this table.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src155" class="srcSentence">Password protected by using an external cryptographic provider</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src156" class="srcSentence">Customer-managed (BYOK)</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src157" class="srcSentence">Contact the supplier for you cryptographic provider for instructions how to transfer your key to a Thales nShield hardware security module (HSM).</caps:sentence>
                            <caps:sentence id="src158" class="srcSentence"> Then follow the instructions for the <embeddedLabel>HSM-protected key to HSM-protected key migration</embeddedLabel> procedure after this table.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </tbody>
                  </table>
                  <para>
                    <caps:sentence id="src159" class="srcSentence">Before you start these procedures, make sure that you can access the .xml files that you created earlier when you exported the trusted publishing domains.</caps:sentence>
                    <caps:sentence id="src160" class="srcSentence"> For example, these might be saved to a USB thumb drive that you move from the AD RMS server to the Internet-connected workstation.</caps:sentence>
                  </para>
                  <alert class="security note">
                    <para>
                      <caps:sentence id="src161" class="srcSentence">However you store these files, use security best practices to protect them because this data includes your private key.</caps:sentence>
                    </para>
                  </alert>
                </content>
                <sections>
                  <section expanded="false">
                    <title>
                      <caps:sentence id="src162" class="srcSentence">Software-protected key to software-protected key migration</caps:sentence>
                    </title>
                    <content>
                      <para>
                        <caps:sentence id="src163" class="srcSentence">Use this procedure to import the AD RMS configuration to Azure RMS, to result in your Azure RMS tenant key that is managed by Microsoft.</caps:sentence>
                      </para>
                      <procedure>
                        <title>
                          <caps:sentence id="src164" class="srcSentence">To import the configuration data to Azure RMS</caps:sentence>
                        </title>
                        <steps class="ordered">
                          <step>
                            <content>
                              <para>
                                <caps:sentence id="src165" class="srcSentence">On an Internet-connected workstation, download and install the Windows PowerShell module for Azure RMS (minimum version 2.1.0.0), which includes the <externalLink><linkText>Import-AadrmTpd</linkText><linkUri>http://msdn.microsoft.com/library/azure/dn857523.aspx</linkUri></externalLink> cmdlet.</caps:sentence>
                              </para>
                              <alert class="tip">
                                <para>
                                  <caps:sentence id="src166" class="srcSentence">If you have previously downloaded and installed the module, check the version number by running: <codeInline>(Get-Module aadrm -ListAvailable).Version</codeInline></caps:sentence>
                                </para>
                              </alert>
                              <para>
                                <caps:sentence id="src167" class="srcSentence">For installation instructions, see <link xlink:href="0d665ed6-b1de-4d63-854a-bc57c1c49844">Installing Windows PowerShell for Azure Rights Management</link>.</caps:sentence>
                              </para>
                            </content>
                          </step>
                          <step>
                            <content>
                              <para>
                                <caps:sentence id="src168" class="srcSentence">Start Windows PowerShell with the <ui>Run as administrator</ui> option and use the <externalLink><linkText>Connect-AadrmService</linkText><linkUri>http://msdn.microsoft.com/library/azure/dn629415.aspx</linkUri></externalLink> cmdlet to connect to the Azure RMS service:</caps:sentence>
                              </para>
                              <code>Connect-AadrmService</code>
                              <para>
                                <caps:sentence id="src169" class="srcSentence">When prompted, enter your <token>aad_rightsmanagement_1</token> tenant administrator credentials (typically, you will use an account that is a global administrator for Azure Active Directory or Office 365).</caps:sentence>
                              </para>
                            </content>
                          </step>
                          <step>
                            <content>
                              <para>
                                <caps:sentence id="src170" class="srcSentence">Use the <externalLink><linkText>Import-AadrmTpd</linkText><linkUri>http://msdn.microsoft.com/library/azure/dn857523.aspx</linkUri></externalLink> cmdlet to upload the first exported trusted publishing domain (.xml) file.</caps:sentence>
                                <caps:sentence id="src171" class="srcSentence"> If you have more than one .xml file because you had multiple trusted publishing domains, choose the file that contains the exported trusted publishing domain that you want to use in Azure RMS to protect content after the migration.</caps:sentence>
                                <caps:sentence id="src172" class="srcSentence"> Use the following command:</caps:sentence>
                              </para>
                              <code>Import-AadrmTpd -TpdFile &lt;PathToTpdPackageFile&gt; -ProtectionPassword -Active $True -Verbose 
</code>
                              <para>
                                <caps:sentence id="src173" class="srcSentence">For example: <userInput>Import-AadrmTpd -TpdFile E:\contosokey1.xml -ProtectionPassword -Active $true -Verbose</userInput></caps:sentence>
                              </para>
                              <para>
                                <caps:sentence id="src174" class="srcSentence">When prompted, enter the password that you specified earlier, and confirm that you want to perform this action.</caps:sentence>
                              </para>
                            </content>
                          </step>
                          <step>
                            <content>
                              <para>
                                <caps:sentence id="src175" class="srcSentence">When the command completes, repeat step 3 for each remaining  .xml file that you created by exporting your trusted publishing domains.</caps:sentence>
                                <caps:sentence id="src176" class="srcSentence"> But for these files, set <userInput>-Active</userInput> to <userInput>false</userInput> when you run the Import command.</caps:sentence>
                                <caps:sentence id="src177" class="srcSentence"> For example: <userInput>Import-AadrmTpd -TpdFile E:\contosokey2.xml -ProtectionPassword -Active $false -Verbose</userInput></caps:sentence>
                              </para>
                            </content>
                          </step>
                          <step>
                            <content>
                              <para>
                                <caps:sentence id="src178" class="srcSentence">Use the <externalLink><linkText>Disconnect-AadrmService</linkText><linkUri>http://msdn.microsoft.com/library/azure/dn629416.aspx</linkUri></externalLink> cmdlet to disconnect from the Azure RMS service:</caps:sentence>
                              </para>
                              <code>Disconnect-AadrmService</code>
                            </content>
                          </step>
                        </steps>
                        <conclusion>
                          <content>
                            <para>
                              <caps:sentence id="src179" class="srcSentence">You’re now ready to go to <link xlink:href="828cf1f7-d0e7-4edf-8525-91896dbe3172#BKMK_Step3Migration">Step 3. Activate your RMS tenant</link>.</caps:sentence>
                            </para>
                          </content>
                        </conclusion>
                      </procedure>
                    </content>
                  </section>
                  <section expanded="false">
                    <title>
                      <caps:sentence id="src180" class="srcSentence">HSM-protected key to HSM-protected key migration</caps:sentence>
                    </title>
                    <content>
                      <para>
                        <caps:sentence id="src181" class="srcSentence">It’s a two-part procedure to import your HSM key and AD RMS configuration to Azure RMS, to result in your Azure RMS tenant key that is managed by you (BYOK).</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src182" class="srcSentence">You must first package your HSM key so it's ready to transfer to Azure RMS, and then import it with the configuration data.</caps:sentence>
                      </para>
                      <procedure>
                        <title>
                          <caps:sentence id="src183" class="srcSentence">Part 1: Package your HSM key so it's ready to transfer to Azure RMS</caps:sentence>
                        </title>
                        <steps class="ordered">
                          <step>
                            <content>
                              <para>
                                <caps:sentence id="src184" class="srcSentence">Follow the steps in the <link xlink:href="f0d33c5f-a6a6-44a1-bdec-5be1bc8e1e14#BKMK_ImplementBYOK">Implementing bring your own key (BYOK)</link> section of the <link xlink:href="f0d33c5f-a6a6-44a1-bdec-5be1bc8e1e14">Planning and Implementing Your Azure Rights Management Tenant Key</link>, using the procedure <embeddedLabel>Generate and transfer your tenant key – over the Internet</embeddedLabel> with the following exceptions:</caps:sentence>
                              </para>
                              <list class="bullet">
                                <listItem>
                                  <para>
                                    <caps:sentence id="src185" class="srcSentence">Do not follow the steps for <embeddedLabel>Generate your tenant key</embeddedLabel>, because you already have the equivalent from your AD RMS deployment.</caps:sentence>
                                    <caps:sentence id="src186" class="srcSentence"> You must identify the key used by your AD RMS server from the Thales installation and use this key during the migration.</caps:sentence>
                                    <caps:sentence id="src187" class="srcSentence"> Thales encrypted key files are usually named <ui>key_(keyAppName)_(keyIdentifier)</ui> locally on the server.</caps:sentence>
                                  </para>
                                </listItem>
                                <listItem>
                                  <para>
                                    <caps:sentence id="src188" class="srcSentence">Do not follow the steps for <embeddedLabel>Transfer your tenant key to Azure RMS</embeddedLabel>, which uses the  Add-AadrmKey command.</caps:sentence>
                                    <caps:sentence id="src189" class="srcSentence">  Instead, you will transfer your prepared HSM key when you upload your exported trusted publishing domain, by using the Import-AadrmTpd command.</caps:sentence>
                                  </para>
                                </listItem>
                              </list>
                            </content>
                          </step>
                          <step>
                            <content>
                              <para>
                                <caps:sentence id="src190" class="srcSentence">On the Internet-connected workstation, in Windows PowerShell session, reconnect to the Azure RMS service.</caps:sentence>
                              </para>
                            </content>
                          </step>
                        </steps>
                        <conclusion>
                          <content>
                            <para>
                              <caps:sentence id="src191" class="srcSentence">Now that you’ve prepared your HSM key for Azure RMS, you’re ready to import your HSM key file and AD RMS configuration data.</caps:sentence>
                            </para>
                          </content>
                        </conclusion>
                      </procedure>
                      <procedure>
                        <title>
                          <caps:sentence id="src192" class="srcSentence">Part 2: Import the HSM key and configuration data to Azure RMS</caps:sentence>
                        </title>
                        <steps class="ordered">
                          <step>
                            <content>
                              <para>
                                <caps:sentence id="src193" class="srcSentence">Still on the Internet-connect workstation and in the Windows PowerShell session, upload the first exported trusted publishing domain (.xml) file.</caps:sentence>
                                <caps:sentence id="src194" class="srcSentence"> If you have more than one .xml file because you had multiple trusted publishing domains, choose the file that contains the exported trusted publishing domain that corresponds to the HSM key you want to use in Azure RMS to protect content after the migration.</caps:sentence>
                                <caps:sentence id="src195" class="srcSentence"> Use the following command:</caps:sentence>
                              </para>
                              <code>Import-AadrmTpd -TpdFile &lt;PathToTpdPackageFile&gt; -ProtectionPassword -HsmKeyFile &lt;PathToBYOKPackage&gt; -Active $True -Verbose</code>
                              <para>
                                <caps:sentence id="src196" class="srcSentence">For example: <userInput>Import -TpdFile E:\no_key_tpd_contosokey1.xml  -HsmKeyFile E:\KeyTransferPackage-contosokey.byok -ProtectionPassword -Active $true -Verbose</userInput></caps:sentence>
                              </para>
                              <para>
                                <caps:sentence id="src197" class="srcSentence">When prompted, enter the password that you specified earlier, and confirm that you want to perform this action.</caps:sentence>
                              </para>
                            </content>
                          </step>
                          <step>
                            <content>
                              <para>
                                <caps:sentence id="src198" class="srcSentence">When the command completes, repeat step 1 for each remaining  .xml file that you created by exporting your trusted publishing domains.</caps:sentence>
                                <caps:sentence id="src199" class="srcSentence"> But for these files, set <userInput>-Active</userInput> to <userInput>false</userInput> when you run the Import command.</caps:sentence>
                                <caps:sentence id="src200" class="srcSentence">  For example: <userInput>Import -TpdFile E:\contosokey2.xml -HsmKeyFile E:\KeyTransferPackage-contosokey.byok -ProtectionPassword -Active $false -Verbose</userInput></caps:sentence>
                              </para>
                            </content>
                          </step>
                          <step>
                            <content>
                              <para>
                                <caps:sentence id="src201" class="srcSentence">Use the <externalLink><linkText>Disconnect-AadrmService</linkText><linkUri>http://msdn.microsoft.com/library/windowsazure/dn629416.aspx</linkUri></externalLink> cmdlet to disconnect from the Azure RMS service:</caps:sentence>
                              </para>
                              <code>Disconnect-AadrmService</code>
                            </content>
                          </step>
                        </steps>
                        <conclusion>
                          <content>
                            <para>
                              <caps:sentence id="src202" class="srcSentence">You’re now ready to go to <link xlink:href="828cf1f7-d0e7-4edf-8525-91896dbe3172#BKMK_Step3Migration">Step 3. Activate your RMS tenant</link>.</caps:sentence>
                            </para>
                          </content>
                        </conclusion>
                      </procedure>
                    </content>
                  </section>
                  <section expanded="false">
                    <title>
                      <caps:sentence id="src203" class="srcSentence">Software-protected key to HSM-protected key migration</caps:sentence>
                    </title>
                    <content>
                      <para>
                        <caps:sentence id="src204" class="srcSentence">It’s a three-part procedure to import the AD RMS configuration to Azure RMS, to result in your Azure RMS tenant key that is managed by you (BYOK).</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src205" class="srcSentence">You must first extract your server licensor certificate (SLC) key from the configuration data and transfer the key to an on-premises Thales HSM, then package and transfer your HSM key to Azure RMS, and then import the configuration data.</caps:sentence>
                      </para>
                      <procedure>
                        <title>
                          <caps:sentence id="src206" class="srcSentence">Part 1: Extract your SLC from the configuration data and import the key to your on-premises HSM</caps:sentence>
                        </title>
                        <steps class="ordered">
                          <step>
                            <content>
                              <para>
                                <caps:sentence id="src207" class="srcSentence">Use the following steps in the <link xlink:href="f0d33c5f-a6a6-44a1-bdec-5be1bc8e1e14#BKMK_ImplementBYOK">Implementing bring your own key (BYOK)</link> section of the <link xlink:href="f0d33c5f-a6a6-44a1-bdec-5be1bc8e1e14">Planning and Implementing Your Azure Rights Management Tenant Key</link> topic:</caps:sentence>
                              </para>
                              <list class="bullet">
                                <listItem>
                                  <para>
                                    <caps:sentence id="src208" class="srcSentence">
                                      <embeddedLabel>Generate and transfer your tenant key – over the Internet</embeddedLabel>: <embeddedLabel>Prepare your Internet-connected workstation</embeddedLabel></caps:sentence>
                                  </para>
                                </listItem>
                                <listItem>
                                  <para>
                                    <caps:sentence id="src209" class="srcSentence">
                                      <embeddedLabel>Generate and transfer your tenant key – over the Internet</embeddedLabel>: <embeddedLabel>Prepare your disconnected workstation</embeddedLabel></caps:sentence>
                                  </para>
                                </listItem>
                              </list>
                              <para>
                                <caps:sentence id="src210" class="srcSentence">Do not follow the steps to generate your tenant key, because you already have the equivalent in the exported configuration data (.xml) file.</caps:sentence>
                                <caps:sentence id="src211" class="srcSentence"> Instead, you will run a command to extract this key from the file and import it to your on-premises HSM.</caps:sentence>
                              </para>
                            </content>
                          </step>
                          <step>
                            <content>
                              <para>
                                <caps:sentence id="src212" class="srcSentence">On the disconnected workstation, run the following command:</caps:sentence>
                              </para>
                              <code>KeyTransferRemote.exe -ImportRmsCentrallyManagedKey -TpdFilePath &lt;TPD&gt; -ProtectionPassword -KeyIdentifier &lt;KeyID&gt; -ExchangeKeyPackage &lt;BYOK-KEK-pka-Region&gt; -NewSecurityWorldPackage &lt;BYOK-SecurityWorld-pkg-Region&gt;</code>
                              <para>
                                <caps:sentence id="src213" class="srcSentence">For example, for North America: <userInput>KeyTransferRemote.exe -ImportRmsCentrallyManagedKey -TpdFilePath E:\contosokey1.xml -ProtectionPassword -KeyIdentifier contosorms1key –- -ExchangeKeyPackage &lt;BYOK-KEK-pka-NA-1&gt; -NewSecurityWorldPackage &lt;BYOK-SecurityWorld-pkg-NA-1&gt;</userInput></caps:sentence>
                              </para>
                              <para>
                                <caps:sentence id="src214" class="srcSentence">Additional information:</caps:sentence>
                              </para>
                              <list class="bullet">
                                <listItem>
                                  <para>
                                    <caps:sentence id="src215" class="srcSentence">The ImportRmsCentrallyManagedKey parameter indicates that the operation is to import the SLC key.</caps:sentence>
                                  </para>
                                </listItem>
                                <listItem>
                                  <para>
                                    <caps:sentence id="src216" class="srcSentence">If you don’t specify the password in the command, you will be prompted to specify it.</caps:sentence>
                                  </para>
                                </listItem>
                                <listItem>
                                  <para>
                                    <caps:sentence id="src217" class="srcSentence">The KeyIdentifier parameter is for a key friendly name that creates the key file name.</caps:sentence>
                                    <caps:sentence id="src218" class="srcSentence"> You must use only lower-case ASCII characters.</caps:sentence>
                                  </para>
                                </listItem>
                                <listItem>
                                  <para>
                                    <caps:sentence id="src219" class="srcSentence">The ExchangeKeyPackage parameter specifies a region-specific key exchange key (KEK) package that has a name beginning with BYOK-KEK-pkg-.</caps:sentence>
                                  </para>
                                </listItem>
                                <listItem>
                                  <para>
                                    <caps:sentence id="src220" class="srcSentence">The NewSecurityWorldPackage parameter specifies a region-specific security world package that has a name beginning with BYOK-SecurityWorld-pkg-.</caps:sentence>
                                  </para>
                                </listItem>
                              </list>
                              <para>
                                <caps:sentence id="src221" class="srcSentence">This command results in the following:</caps:sentence>
                              </para>
                              <list class="bullet">
                                <listItem>
                                  <para>
                                    <caps:sentence id="src222" class="srcSentence">An HSM key file: %NFAST_KMDATA%\local\key_mscapi_&lt;KeyID&gt;</caps:sentence>
                                  </para>
                                </listItem>
                                <listItem>
                                  <para>
                                    <caps:sentence id="src223" class="srcSentence">RMS configuration data file with the SLC removed: %NFAST_KMDATA%\local\no_key_tpd_&lt;KeyID&gt;.xml</caps:sentence>
                                  </para>
                                </listItem>
                              </list>
                            </content>
                          </step>
                          <step>
                            <content>
                              <para>
                                <caps:sentence id="src224" class="srcSentence">If you have more than one RMS configuration data files, repeat step 2 for the remainder of these files.</caps:sentence>
                              </para>
                            </content>
                          </step>
                        </steps>
                        <conclusion>
                          <content>
                            <para>
                              <caps:sentence id="src225" class="srcSentence">Now that your SLC has been extracted so that it’s an HSM-based key, you’re ready to package and transfer it to Azure RMS.</caps:sentence>
                            </para>
                          </content>
                        </conclusion>
                      </procedure>
                      <procedure>
                        <title>
                          <caps:sentence id="src226" class="srcSentence">Part 2: Package and transfer your HSM key to Azure RMS</caps:sentence>
                        </title>
                        <steps class="ordered">
                          <step>
                            <content>
                              <para>
                                <caps:sentence id="src227" class="srcSentence">Use the following steps from the <link xlink:href="f0d33c5f-a6a6-44a1-bdec-5be1bc8e1e14#BKMK_ImplementBYOK">Implementing bring your own key (BYOK)</link> section of the <link xlink:href="f0d33c5f-a6a6-44a1-bdec-5be1bc8e1e14">Planning and Implementing Your Azure Rights Management Tenant Key</link>:</caps:sentence>
                              </para>
                              <list class="bullet">
                                <listItem>
                                  <para>
                                    <caps:sentence id="src228" class="srcSentence">
                                      <embeddedLabel>Generate and transfer your tenant key – over the Internet</embeddedLabel>: <embeddedLabel>Prepare your tenant key for transfer</embeddedLabel></caps:sentence>
                                  </para>
                                </listItem>
                                <listItem>
                                  <para>
                                    <caps:sentence id="src229" class="srcSentence">
                                      <embeddedLabel>Generate and transfer your tenant key – over the Internet</embeddedLabel>: <embeddedLabel>Transfer your tenant key to Azure RMS</embeddedLabel></caps:sentence>
                                  </para>
                                </listItem>
                              </list>
                            </content>
                          </step>
                        </steps>
                        <conclusion>
                          <content>
                            <para>
                              <caps:sentence id="src230" class="srcSentence">Now that you’ve transferred your HSM key to Azure RMS, you’re ready to import your AD RMS configuration data, which contains only a pointer to the newly transferred tenant key.</caps:sentence>
                            </para>
                          </content>
                        </conclusion>
                      </procedure>
                      <procedure>
                        <title>
                          <caps:sentence id="src231" class="srcSentence">Part 3: Import the configuration data to Azure RMS</caps:sentence>
                        </title>
                        <steps class="ordered">
                          <step>
                            <content>
                              <para>
                                <caps:sentence id="src232" class="srcSentence">Still on the Internet-connected workstation and in the Windows PowerShell session, copy over the RMS configuration files with the SLC removed (from the disconnected workstation, %NFAST_KMDATA%\local\no_key_tpd_&lt;KeyID&gt;.xml)</caps:sentence>
                              </para>
                            </content>
                          </step>
                          <step>
                            <content>
                              <para>
                                <caps:sentence id="src233" class="srcSentence">Upload the first file.</caps:sentence>
                                <caps:sentence id="src234" class="srcSentence"> If you have more than one .xml file because you had multiple trusted publishing domains, choose the file that contains the exported trusted publishing domain that corresponds to the HSM key you want to use in Azure RMS to protect content after the migration.</caps:sentence>
                                <caps:sentence id="src235" class="srcSentence"> Use the following command:</caps:sentence>
                              </para>
                              <code>Import-AadrmTpd -TpdFile &lt;PathToNoKeyTpdPackageFile&gt; -ProtectionPassword -HsmKeyFile &lt;PathToKeyTransferPackage&gt; -Active $true -Verbose </code>
                              <para>
                                <caps:sentence id="src236" class="srcSentence">For example: <userInput>Import -TpdFile E:\no_key_tpd_contosorms1key.xml -ProtectionPassword -HsmKeyFile E:\KeyTransferPackage-contosorms1key.byok -Active $true -Verbose </userInput></caps:sentence>
                              </para>
                              <para>
                                <caps:sentence id="src237" class="srcSentence">When prompted, enter the password that you specified earlier, and confirm that you want to perform this action.</caps:sentence>
                              </para>
                            </content>
                          </step>
                          <step>
                            <content>
                              <para>
                                <caps:sentence id="src238" class="srcSentence">When the command completes, repeat step 2 for each remaining  .xml file that you created by exporting your trusted publishing domains.</caps:sentence>
                                <caps:sentence id="src239" class="srcSentence"> But for these files, set <userInput>-Active</userInput> to <userInput>false</userInput> when you run the Import command.</caps:sentence>
                                <caps:sentence id="src240" class="srcSentence"> For example: <userInput>Import -TpdFile E:\no_key_tpd_contosorms2key.xml -ProtectionPassword -HsmKeyFile E:\KeyTransferPackage-contosorms1key.byok -Active $false -Verbose </userInput></caps:sentence>
                              </para>
                            </content>
                          </step>
                          <step>
                            <content>
                              <para>
                                <caps:sentence id="src241" class="srcSentence">Use the <externalLink><linkText>Disconnect-AadrmService</linkText><linkUri>http://msdn.microsoft.com/library/windowsazure/dn629416.aspx</linkUri></externalLink> cmdlet to disconnect from the Azure RMS service:</caps:sentence>
                              </para>
                              <code>Disconnect-AadrmService</code>
                            </content>
                          </step>
                        </steps>
                        <conclusion>
                          <content>
                            <para>
                              <caps:sentence id="src242" class="srcSentence">You’re now ready to go to <link xlink:href="828cf1f7-d0e7-4edf-8525-91896dbe3172#BKMK_Step3Migration">Step 3. Activate your RMS tenant</link>.</caps:sentence>
                            </para>
                          </content>
                        </conclusion>
                      </procedure>
                    </content>
                  </section>
                </sections>
              </section>
            </sections>
          </section>
          <section address="BKMK_Step3Migration">
            <title>
              <caps:sentence id="src243" class="srcSentence">Step 3.</caps:sentence>
              <caps:sentence id="src244" class="srcSentence"> Activate your RMS tenant</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src245" class="srcSentence">Instructions  for this step are fully covered in the <link xlink:href="f8707e01-b239-4d1a-a1ea-0d1cf9a8d214">Activating Azure Rights Management</link> topic.</caps:sentence>
              </para>
              <alert class="tip">
                <para>
                  <caps:sentence id="src246" class="srcSentence">If you have an Office 365 subscription, you can activate Azure RMS from the Office 365 admin center or the Azure classic portal.</caps:sentence>
                  <caps:sentence id="src247" class="srcSentence"> We recommend that you use the Azure classic portal because you will use this management portal to complete the next step.</caps:sentence>
                </para>
              </alert>
              <para>
                <caps:sentence id="src248" class="srcSentence">
                  <embeddedLabel>What if your Azure RMS tenant is already activated?</embeddedLabel> If the Azure RMS service is already activated for your organization, users might have already used Azure RMS to protect content with an automatically generated tenant key (and the default templates) rather than your existing keys (and templates) from AD RMS.</caps:sentence>
                <caps:sentence id="src249" class="srcSentence"> This is unlikely to happen on computers that are well-managed on your intranet, because they will be automatically configured for your AD RMS infrastructure.</caps:sentence>
                <caps:sentence id="src250" class="srcSentence"> But it can happen on workgroup computers or computers that infrequently connect to your intranet.</caps:sentence>
                <caps:sentence id="src251" class="srcSentence"> Unfortunately, it’s also difficult to identify these computers, which is why we recommend you do not activate the service before you import the configuration data from AD RMS.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src252" class="srcSentence">If your Azure RMS tenant is already activated and you can identify these computers, make sure that you run the CleanUpRMS_RUN_Elevated.cmd script on these computers, as described in Step 5.</caps:sentence>
                <caps:sentence id="src253" class="srcSentence"> Running this script forces them to reinitialize the user environment, so that they download the updated tenant key and imported templates.</caps:sentence>
              </para>
            </content>
          </section>
          <section address="BKMK_Step4Migration">
            <title>
              <caps:sentence id="src254" class="srcSentence">Step 4.</caps:sentence>
              <caps:sentence id="src255" class="srcSentence"> Configure imported templates</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src256" class="srcSentence">Because the templates that you imported have a default state of <ui>Archived</ui>, you must change this state to be <ui>Published</ui> if you want users to be able to use these templates with Azure RMS.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src257" class="srcSentence">In addition, if your templates in AD RMS used the <ui>ANYONE</ui> group, this group is automatically removed  when you import the templates to Azure RMS; you must manually add the equivalent group or users and the same rights to the imported templates.</caps:sentence>
                <caps:sentence id="src258" class="srcSentence"> The equivalent group for Azure RMS is named <system>AllStaff-&lt;tenant_GUID&gt;@&lt;tenant_name&gt;.onmicrosoft.com</system>.</caps:sentence>
                <caps:sentence id="src259" class="srcSentence"> For example, this group might look like the following for Contoso: <system>AllStaff-9c11c87a-ac8b-46a3-8d5c-f4d0b72ee29a@contoso.onmicrosoft.com</system>.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src260" class="srcSentence">If  you're not sure whether your AD RMS templates include the ANYONE group, expand the  <link xlink:href="#BKMK_ScriptForANYONE">PowerShell script to identify AD RMS templates that include the ANYONE group</link> section in this step to copy and use the sample PowerShell script to identify these templates.</caps:sentence>
                <caps:sentence id="src261" class="srcSentence"> For more information about using Windows PowerShell with AD RMS, see  <externalLink><linkText>Using Windows PowerShell to Administer AD RMS</linkText><linkUri>https://technet.microsoft.com/library/ee221079(v=ws.10).aspx</linkUri></externalLink>.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src262" class="srcSentence">You can see your organization's automatically created group if you copy one of the default rights policy templates in the Azure classic portal, and then identify the <ui>USER NAME</ui> on the <ui>RIGHTS</ui> page.</caps:sentence>
                <caps:sentence id="src263" class="srcSentence"> However, you cannot use the classic portal to add this group to a template that was manually created or imported and instead must use one of the following Azure RMS PowerShell options:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src264" class="srcSentence">Use the <externalLink><linkText>New-AadrmRightsDefinition</linkText><linkUri>https://msdn.microsoft.com/library/azure/dn727080.aspx</linkUri></externalLink> PowerShell cmdlet to define the  "AllStaff" group and rights as a rights definition object, and run this command again for each of the other groups or users already granted rights in the original template in addition to the ANYONE group.</caps:sentence>
                    <caps:sentence id="src265" class="srcSentence"> Then add all these rights definition objects to the templates by using the  <externalLink><linkText>Set-AadrmTemplateProperty</linkText><linkUri>https://msdn.microsoft.com/en-us/library/azure/dn727076.aspx</linkUri></externalLink> cmdlet.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src266" class="srcSentence">Use the <externalLink><linkText>Export-AadrmTemplate</linkText><linkUri>https://msdn.microsoft.com/library/azure/dn727078.aspx</linkUri></externalLink> cmdlet to export the template to a .XML file that you can edit to add the "AllStaff" group and rights to the existing groups and rights, and then use the <externalLink><linkText>Import-AadrmTemplate</linkText><linkUri>https://msdn.microsoft.com/library/azure/dn727077.aspx</linkUri></externalLink> cmdlet to import this change back into Azure RMS.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <alert class="note">
                <para>
                  <caps:sentence id="src267" class="srcSentence">This "AllStaff" equivalent group isn't exactly the same as the ANYONE group in AD RMS:  The "AllStaff" group includes all users in your Azure tenant, whereas the ANYONE group includes all authenticated users, who could be outside your organization.</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src268" class="srcSentence">Because of this difference between the two groups, you might need to also add external users in addition to the "AllStaff" group.</caps:sentence>
                  <caps:sentence id="src269" class="srcSentence"> External email addresses for groups are not currently supported.</caps:sentence>
                </para>
              </alert>
              <para>
                <caps:sentence id="src270" class="srcSentence">Templates that you import from AD RMS look and behave just like custom templates that you can create in the Azure classic portal.</caps:sentence>
                <caps:sentence id="src271" class="srcSentence"> To change imported templates to be published so that users can see them and select them from applications, or to make other changes to the templates, see <link xlink:href="1775d8d0-9a59-42c8-914f-ce285b71ac1c">Configuring Custom Templates for Azure Rights Management</link>.</caps:sentence>
              </para>
              <alert class="tip">
                <para>
                  <caps:sentence id="src272" class="srcSentence">For a more consistent experience for users during the migration process, do not make changes to the imported templates other than these two changes; and do not publish the two default templates that come with Azure RMS, or create new templates at this time.</caps:sentence>
                  <caps:sentence id="src273" class="srcSentence"> Instead, wait until the migration process is complete and you have decommissioned the AD RMS servers.</caps:sentence>
                </para>
              </alert>
            </content>
            <sections>
              <section expanded="false" address="BKMK_ScriptForANYONE">
                <title>
                  <caps:sentence id="src274" class="srcSentence">Sample Windows PowerShell script to identify AD RMS templates that include the ANYONE group</caps:sentence>
                </title>
                <content>
                  <para>
                    <caps:sentence id="src275" class="srcSentence">This section contains the sample script to help you identify AD RMS templates that have the ANYONE group defined, as described in the preceding section.</caps:sentence>
                  </para>
                  <para>
                    <legacyItalic>
                      <caps:sentence id="src276" class="srcSentence">
                        <embeddedLabel>Disclaimer:</embeddedLabel> This sample script is not supported under any Microsoft standard support program or service.</caps:sentence>
                      <caps:sentence id="src277" class="srcSentence"> This sample script is provided AS IS without warranty of any kind.</caps:sentence>
                    </legacyItalic>
                  </para>
                  <code>import-module adrmsadmin New-PSDrive -Name MyRmsAdmin -PsProvider AdRmsAdmin -Root https://localhost -Force $ListofTemplates=dir MyRmsAdmin:\RightsPolicyTemplate foreach($Template in $ListofTemplates) { $templateID=$Template.id $rights = dir MyRmsAdmin:\RightsPolicyTemplate\$Templateid\userright $templateName=$Template.DefaultDisplayName if ($rights.usergroupname -eq "anyone") { $templateName = $Template.defaultdisplayname write-host "Template " -NoNewline write-host -NoNewline $templateName -ForegroundColor Red write-host " contains rights for " -NoNewline write-host ANYONE  -ForegroundColor Red } } Remove-PSDrive MyRmsAdmin -force
</code>
                </content>
              </section>
            </sections>
          </section>
          <section address="BKMK_Step5Migration">
            <title>
              <caps:sentence id="src278" class="srcSentence">Step 5.</caps:sentence>
              <caps:sentence id="src279" class="srcSentence"> Reconfigure clients to use Azure RMS</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src280" class="srcSentence">For Windows clients:</caps:sentence>
              </para>
              <list class="ordered">
                <listItem>
                  <para>
                    <caps:sentence id="src281" class="srcSentence">
                      <externalLink>
                        <linkText>Download the migration scripts</linkText>
                        <linkUri>http://go.microsoft.com/fwlink/?LinkId=524619</linkUri>
                      </externalLink>: </caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src282" class="srcSentence">CleanUpRMS_RUN_Elevated.cmd</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src283" class="srcSentence">Redirect_OnPrem.cmd</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence id="src284" class="srcSentence">These scripts reset the configuration on Windows computers so that they will use the Azure RMS service rather than AD RMS.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src285" class="srcSentence">Follow the instructions in the redirection script (Redirect_OnPrem.cmd) to modify the script to point to your new Azure RMS tenant.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src286" class="srcSentence">On the Windows computers, run these scripts with elevated privileges in the user’s context.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src287" class="srcSentence">For mobile device clients and Mac computers:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src288" class="srcSentence">Remove the DNS SRV records that you created when you deployed the <externalLink><linkText>AD RMS mobile device extension</linkText><linkUri>http://technet.microsoft.com/library/dn673574.aspx</linkUri></externalLink>.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
            <sections>
              <section expanded="false">
                <title>
                  <caps:sentence id="src289" class="srcSentence">Changes made by the migration scripts</caps:sentence>
                </title>
                <content>
                  <para>
                    <caps:sentence id="src290" class="srcSentence">This section documents the changes that the migration scripts make.</caps:sentence>
                    <caps:sentence id="src291" class="srcSentence"> You can use this information for reference purposes only, or for troubleshooting, or if you prefer to make these changes yourself.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src292" class="srcSentence">CleanUpRMS_RUN_Elevated.cmd:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src293" class="srcSentence">Delete the contents of the %userprofile%\AppData\Local\Microsoft\DRM and %userprofile%\AppData\Local\Microsoft\MSIPC folders, including any subfolders and any files with long file names.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src294" class="srcSentence">Delete the contents of the following registry keys:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence id="src295" class="srcSentence">HKEY_LOCAL_MACHINE\Software\Microsoft\Office\(11.0|12.0|14.0)\Common\DRM</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src296" class="srcSentence">HKEY_CURRENT_USER\Software\Microsoft\Office\(11.0|12.0|14.0)\Common\DRM</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src297" class="srcSentence">HKEY_LOCAL_MACHINE\Software\WoW6432Node\Microsoft\Office\(11.0|12.0|14.0)\Common\DRM</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src298" class="srcSentence">HKEY_CURRENT_USER\Software\WoW6432Node\Microsoft\Office\(11.0|12.0|14.0)\Common\DRM</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src299" class="srcSentence">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MSIPC\ServiceLocation</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src300" class="srcSentence">HKEY_LOCAL_MACHINE\SOFTWARE\WoW6432Node\Microsoft\MSIPC\ServiceLocation</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src301" class="srcSentence">HKEY_LOCAL_MACHINE\Software\Microsoft\MSDRM\ServiceLocation</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src302" class="srcSentence">Delete the following registry values:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence id="src303" class="srcSentence">HKEY_CURRENT_USER\Software\Microsoft\Office\15.0\Common\DRM\DefaultServerURL</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src304" class="srcSentence">HKEY_CURRENT_USER\Software\Microsoft\Office\15.0\Common\DRM\DefaultServer</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence id="src305" class="srcSentence">Redirect_OnPrem.cmd:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src306" class="srcSentence">Create the following registry values for each URL supplied as a parameter under each of the following locations:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence id="src307" class="srcSentence">HKEY_CURRENT_USER\Software\Microsoft\Office\(11.0|12.0|14.0)\Common\DRM\LicenseServerRedirection</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src308" class="srcSentence">HKEY_CURRENT_USER\Software\WoW6432Node\Microsoft\Office\(11.0|12.0|14.0)\Common\DRM\LicenseServerRedirection</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src309" class="srcSentence">HKEY_LOCAL_MACHINE\Software\Microsoft\Office\(11.0|12.0|14.0)\Common\DRM\LicenseServerRedirection</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src310" class="srcSentence">HKEY_LOCAL_MACHINE\Software\WoW6432Node\Microsoft\Office\(11.0|12.0|14.0)\Common\DRM\LicenseServerRedirection</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src311" class="srcSentence">HKEY_CURRENT_USER\Software\Classes\Local Settings\Software\Microsoft\MSIPC\LicensingRedirection</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                      <para>
                        <caps:sentence id="src312" class="srcSentence">Each entry has a REG_SZ value of <ui>https://OldRMSserverURL/_wmcs/licensing</ui> with the data in the following format: <ui>https://&lt;YourTenantURL&gt;/_wmcs/licensing</ui>.</caps:sentence>
                      </para>
                      <alert class="note">
                        <para>
                          <caps:sentence id="src313" class="srcSentence">
                            <placeholder>&lt;YourTenantURL&gt;</placeholder> has the following format: <ui>{GUID}.rms.[Region].aadrm.com</ui>.</caps:sentence>
                        </para>
                        <para>
                          <caps:sentence id="src314" class="srcSentence">For example:  5c6bb73b-1038-4eec-863d-49bded473437.rms.na.aadrm.com</caps:sentence>
                        </para>
                        <para>
                          <caps:sentence id="src315" class="srcSentence">You can find this value by identifying the <ui>RightsManagementServiceId</ui> value when you run the <externalLink><linkText>Get-AadrmConfiguration</linkText><linkUri>http://msdn.microsoft.com/library/windowsazure/dn629410.aspx</linkUri></externalLink> cmdlet for Azure RMS.</caps:sentence>
                        </para>
                      </alert>
                    </listItem>
                  </list>
                </content>
              </section>
            </sections>
          </section>
          <section address="BKMK_Step6Migration">
            <title>
              <caps:sentence id="src316" class="srcSentence">Step 6.</caps:sentence>
              <caps:sentence id="src317" class="srcSentence"> Configure IRM integration for Exchange Online</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src318" class="srcSentence">If you have previously imported your TDP from AD RMS to Exchange Online, you must remove this TDP to avoid conflicting templates and policies after you have migrated to Azure RMS.</caps:sentence>
                <caps:sentence id="src319" class="srcSentence"> To do this, use the <externalLink><linkText>Remove-RMSTrustedPublishingDomain</linkText><linkUri>https://technet.microsoft.com/en-us/library/jj200720(v=exchg.150).aspx</linkUri></externalLink> cmdlet from Exchange Online.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src320" class="srcSentence">If you chose an Azure RMS tenant key topology of <embeddedLabel>Microsoft managed</embeddedLabel>:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src321" class="srcSentence">See the <link xlink:href="ea09cbc5-b98b-444e-8b60-5bc3cb199c36#BKMK_ExchangeOnline">Exchange Online: IRM Configuration</link> section in the <link xlink:href="ea09cbc5-b98b-444e-8b60-5bc3cb199c36">Configuring Applications for Azure Rights Management</link> topic.</caps:sentence>
                    <caps:sentence id="src322" class="srcSentence"> This section includes typical commands to run that connects to the Exchange Online service, imports the tenant key from Azure RMS,  and enables IRM functionality for Exchange Online.</caps:sentence>
                    <caps:sentence id="src323" class="srcSentence"> After you complete these steps, you will have full RMS functionality with Exchange Online.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src324" class="srcSentence">If you chose an Azure RMS tenant key topology of <embeddedLabel>customer-managed (BYOK)</embeddedLabel>:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src325" class="srcSentence"> You will  have reduced RMS functionality with Exchange Online, as described in the <link xlink:href="f0d33c5f-a6a6-44a1-bdec-5be1bc8e1e14#BKMK_Pricing">BYOK pricing and restrictions</link> section in the <link xlink:href="f0d33c5f-a6a6-44a1-bdec-5be1bc8e1e14">Planning and Implementing Your Azure Rights Management Tenant Key</link> topic.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
          <section address="BKMK_Step7Migration">
            <title>
              <caps:sentence id="src326" class="srcSentence">Step 7.</caps:sentence>
              <caps:sentence id="src327" class="srcSentence"> Deploy the RMS connector</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src328" class="srcSentence">If you have used the Information Rights Management (IRM) functionality of Exchange Server or SharePoint Server with AD RMS, you must first disable IRM on these servers and remove AD RMS configuration.</caps:sentence>
                <caps:sentence id="src329" class="srcSentence"> Then, deploy the Rights Management (RMS) connector, which acts as a communications interface (a relay) between the on-premises servers and Azure RMS.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src330" class="srcSentence">Finally for this step, if you have imported multiple TPDs into Azure RMS that were used to protect email messages, you must manually edit the registry on the Exchange Server computers to redirect all TPDs URLs to the RMS connector.</caps:sentence>
              </para>
              <alert class="note">
                <para>
                  <caps:sentence id="src331" class="srcSentence">Before you start, check the supported versions of the on-premises servers that the RMS connector supports in “On-premises servers that support Azure RMS” in the <link xlink:href="dc78321d-d759-4653-8818-80da74b6cdeb#BKMK_SupportedApplications">Applications that support Azure RMS</link> section of the <link xlink:href="dc78321d-d759-4653-8818-80da74b6cdeb">Requirements for Azure Rights Management</link> topic.</caps:sentence>
                </para>
              </alert>
              <procedure>
                <title>
                  <caps:sentence id="src332" class="srcSentence">Disable IRM on Exchange Servers and remove AD RMS configuration</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src333" class="srcSentence">On each Exchange server, locate the following folder and delete all the entries in that folder: \ProgramData\Microsoft\DRM\Server\S-1-5-18</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src334" class="srcSentence">From one of the Exchange servers, use the Exchange <externalLink><linkText>Set_IRMConfiguration</linkText><linkUri>http://technet.microsoft.com/library/dd979792.aspx</linkUri></externalLink> cmdlet to first disable IRM features for messages that are sent to internal recipients: </caps:sentence>
                      </para>
                      <code>Set-IRMConfiguration -InternalLicensingEnabled $false</code>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src335" class="srcSentence">Then use the same cmdlet to disable IRM features for messages that are sent to external recipients:</caps:sentence>
                      </para>
                      <code>Set-IRMConfiguration -ExternalLicensingEnabled $false</code>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src336" class="srcSentence">Next, use the same cmdlet to disable IRM in Microsoft Office Outlook Web App and in Microsoft Exchange ActiveSync:</caps:sentence>
                      </para>
                      <code>Set-IRMConfiguration -ClientAccessServerEnabled $false</code>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src337" class="srcSentence">Finally, use the same cmdlet to clear any cached certificates:</caps:sentence>
                      </para>
                      <code>Set-IRMConfiguration -RefreshServerCertificates</code>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src338" class="srcSentence">On each Exchange Server, now reset IIS, for example, by running a command prompt as an administrator and typing <userInput>iisreset</userInput>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
              <procedure>
                <title>
                  <caps:sentence id="src339" class="srcSentence">Disable IRM on SharePoint Servers and remove AD RMS configuration</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src340" class="srcSentence">Make sure that there are no documents checked out from RMS-protected libraries.</caps:sentence>
                        <caps:sentence id="src341" class="srcSentence"> If there are, they will be become inaccessible at the end of this procedure.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src342" class="srcSentence">On the SharePoint Central Administration Web site, in the <ui>Quick Launch</ui> section, click <ui>Security</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src343" class="srcSentence">On the <ui>Security</ui> page, in the <ui>Information Policy</ui> section, click <ui>Configure information rights management</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src344" class="srcSentence">On the <ui>Information Rights Management</ui> page, in the <ui>Information Rights Management</ui> section, select <ui>Do not use IRM on this server</ui>, then click <ui>OK</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src345" class="srcSentence">On each of the SharePoint Server computers, delete the contents of the folder \ProgramData\Microsoft\MSIPC\Server\<placeholder>&lt;SID of the account running SharePoint Server&gt;</placeholder>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
              <procedure>
                <title>
                  <caps:sentence id="src346" class="srcSentence">Install and configure the RMS connector</caps:sentence>
                </title>
                <steps class="bullet">
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src347" class="srcSentence">Use the instructions in the <link xlink:href="90e7e33f-9ecc-497b-89c5-09205ffc5066">Deploying the Azure Rights Management Connector</link> topic.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
              <procedure>
                <title>
                  <caps:sentence id="src348" class="srcSentence">For Exchange only and multiple TPDs: Edit the registry</caps:sentence>
                </title>
                <steps class="bullet">
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src349" class="srcSentence">On each Exchange Server, manually add the following registry keys for each additional TPD that you imported, to redirect the TPD URLs to the RMS connector.</caps:sentence>
                        <caps:sentence id="src350" class="srcSentence"> These registry entries are specific to migration and are not added by the server configuration tool for Microsoft RMS connector.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src351" class="srcSentence">When you make these registry edits, use the following instructions:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence id="src352" class="srcSentence">Replace <placeholder>ConnectorFQDN</placeholder> with the name that you defined in DNS for the connector.</caps:sentence>
                            <caps:sentence id="src353" class="srcSentence"> For example, <ui>rmsconnector.contoso.com</ui>.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src354" class="srcSentence">Use the HTTP or HTTPS prefix for the connector URL, depending on whether you have configured the connector to use HTTP or HTTPS to communicate with your on-premises servers.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                      <para> </para>
                      <para>
                        <embeddedLabel>
                          <caps:sentence id="src355" class="srcSentence">For Exchange 2013:</caps:sentence>
                        </embeddedLabel>
                      </para>
                      <table>
                        <thead>
                          <tr>
                            <TD>
                              <para>
                                <caps:sentence id="src356" class="srcSentence">Registry path</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src357" class="srcSentence">Type</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src358" class="srcSentence">Value</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src359" class="srcSentence">Data</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                        </thead>
                        <tbody>
                          <tr>
                            <TD>
                              <para>
                                <caps:sentence id="src360" class="srcSentence">HKLM\SOFTWARE\Microsoft\ExchangeServer\v15\IRM\LicenseServerRedirection</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src361" class="srcSentence">Reg_SZ</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src362" class="srcSentence">https://&lt;AD RMS Intranet Licensing URL&gt;/_wmcs/licensing</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src363" class="srcSentence">One of the following, depending on whether you are using HTTP or HTTPS from your Exchange server to the RMS connector:</caps:sentence>
                              </para>
                              <list class="bullet">
                                <listItem>
                                  <para>
                                    <caps:sentence id="src364" class="srcSentence">http://&lt;connectorFQDN&gt;/_wmcs/licensing</caps:sentence>
                                  </para>
                                </listItem>
                                <listItem>
                                  <para>
                                    <caps:sentence id="src365" class="srcSentence">https://&lt;connectorName&gt;/_wmcs/licensing</caps:sentence>
                                  </para>
                                </listItem>
                              </list>
                            </TD>
                          </tr>
                          <tr>
                            <TD>
                              <para>
                                <caps:sentence id="src366" class="srcSentence">HKLM\SOFTWARE\Microsoft\ExchangeServer\v15\IRM\LicenseServerRedirection </caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src367" class="srcSentence">Reg_SZ</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src368" class="srcSentence">https://&lt;AD RMS Extranet Licensing URL&gt;/_wmcs/licensing</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src369" class="srcSentence">One of the following, depending on whether you are using HTTP or HTTPS from your Exchange server to the RMS connector:</caps:sentence>
                              </para>
                              <list class="bullet">
                                <listItem>
                                  <para>
                                    <caps:sentence id="src370" class="srcSentence">http://&lt;connectorFQDN&gt;/_wmcs/licensing</caps:sentence>
                                  </para>
                                </listItem>
                                <listItem>
                                  <para>
                                    <caps:sentence id="src371" class="srcSentence">https://&lt;connectorFQDN&gt;/_wmcs/licensing</caps:sentence>
                                  </para>
                                </listItem>
                              </list>
                            </TD>
                          </tr>
                        </tbody>
                      </table>
                      <para>
                        <embeddedLabel>
                          <caps:sentence id="src372" class="srcSentence">For Exchange Server 2010:</caps:sentence>
                        </embeddedLabel>
                      </para>
                      <table>
                        <thead>
                          <tr>
                            <TD>
                              <para>
                                <caps:sentence id="src373" class="srcSentence">Registry path</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src374" class="srcSentence">Type</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src375" class="srcSentence">Value</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src376" class="srcSentence">Data</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                        </thead>
                        <tbody>
                          <tr>
                            <TD>
                              <para>
                                <caps:sentence id="src377" class="srcSentence">HKLM\SOFTWARE\Microsoft\ExchangeServer\v14\IRM\LicenseServerRedirection</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src378" class="srcSentence">Reg_SZ</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src379" class="srcSentence">https://&lt;AD RMS Intranet Licensing URL&gt;/_wmcs/licensing</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src380" class="srcSentence">One of the following, depending on whether you are using HTTP or HTTPS from your Exchange server to the RMS connector:</caps:sentence>
                              </para>
                              <list class="bullet">
                                <listItem>
                                  <para>
                                    <caps:sentence id="src381" class="srcSentence">http://&lt;connectorName&gt;/_wmcs/licensing</caps:sentence>
                                  </para>
                                </listItem>
                                <listItem>
                                  <para>
                                    <caps:sentence id="src382" class="srcSentence">https://&lt;connectorName&gt;/_wmcs/licensing</caps:sentence>
                                  </para>
                                </listItem>
                              </list>
                            </TD>
                          </tr>
                          <tr>
                            <TD>
                              <para>
                                <caps:sentence id="src383" class="srcSentence">HKLM\SOFTWARE\Microsoft\ExchangeServer\v14\IRM\LicenseServerRedirection </caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src384" class="srcSentence">Reg_SZ</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src385" class="srcSentence">https://&lt;AD RMS Extranet Licensing URL&gt;/_wmcs/licensing</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src386" class="srcSentence">One of the following, depending on whether you are using HTTP or HTTPS from your Exchange server to the RMS connector:</caps:sentence>
                              </para>
                              <list class="bullet">
                                <listItem>
                                  <para>
                                    <caps:sentence id="src387" class="srcSentence">http://&lt;connectorName&gt;/_wmcs/licensing</caps:sentence>
                                  </para>
                                </listItem>
                                <listItem>
                                  <para>
                                    <caps:sentence id="src388" class="srcSentence">https://&lt;connectorName&gt;/_wmcs/licensing</caps:sentence>
                                  </para>
                                </listItem>
                              </list>
                            </TD>
                          </tr>
                        </tbody>
                      </table>
                    </content>
                  </step>
                </steps>
              </procedure>
              <para>
                <caps:sentence id="src389" class="srcSentence">After you have completed these procedures, be sure to read the <embeddedLabel>Next steps</embeddedLabel> section in the <link xlink:href="90e7e33f-9ecc-497b-89c5-09205ffc5066">Deploying the Azure Rights Management Connector</link> topic.</caps:sentence>
              </para>
            </content>
          </section>
          <section address="BKMK_Step8Migration">
            <title>
              <caps:sentence id="src390" class="srcSentence">Step 8.</caps:sentence>
              <caps:sentence id="src391" class="srcSentence"> Decommission AD RMS</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src392" class="srcSentence">Optional: Remove the Service Connection Point (SCP) from Active Directory to prevent computers from discovering your on-premises Rights Management infrastructure.</caps:sentence>
                <caps:sentence id="src393" class="srcSentence"> This is optional because of the redirection that you configured in the registry (for example, by running the migration script).</caps:sentence>
                <caps:sentence id="src394" class="srcSentence"> To remove the Service Connection Point, use the AD SCP Register tool from the <externalLink><linkText>Rights Management Services Administration Toolkit</linkText><linkUri>http://www.microsoft.com/download/details.aspx?id=1479</linkUri></externalLink>.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src395" class="srcSentence">Monitor your AD RMS servers for activity, for example, by checking the <externalLink><linkText>requests in the System Health report</linkText><linkUri>https://technet.microsoft.com/library/ee221012(v=ws.10).aspx</linkUri></externalLink>, the <externalLink><linkText>ServiceRequest table</linkText><linkUri>http://technet.microsoft.com/library/dd772686(v=ws.10).aspx</linkUri></externalLink> or <externalLink><linkText>auditing of user access to protected content</linkText><linkUri>http://social.technet.microsoft.com/wiki/contents/articles/3440.ad-rms-frequently-asked-questions-faq.aspx</linkUri></externalLink>.</caps:sentence>
                <caps:sentence id="src396" class="srcSentence"> When you have confirmed that RMS clients are no longer communicating with these servers and that clients are successfully using Azure RMS, you can remove the AD RMS server role from these server.</caps:sentence>
                <caps:sentence id="src397" class="srcSentence"> If you’re using dedicated servers, you might prefer the cautionary step of first shutting down the servers for a period of time to make sure that there are no reported problems that might require restarting these servers to ensure service continuity while you investigate why clients are not using Azure RMS.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src398" class="srcSentence">After decommissioning your AD RMS servers, you might want to take the opportunity to review your templates in the Azure classic portal and consolidate them so that users have fewer to choose between, or reconfigure them, or even add new templates.</caps:sentence>
                <caps:sentence id="src399" class="srcSentence"> This would be also a good time to publish the default templates.</caps:sentence>
                <caps:sentence id="src400" class="srcSentence"> For more information, see <link xlink:href="1775d8d0-9a59-42c8-914f-ce285b71ac1c">Configuring Custom Templates for Azure Rights Management</link>.</caps:sentence>
              </para>
            </content>
          </section>
          <section address="BKMK_Step9Migration">
            <title>
              <caps:sentence id="src401" class="srcSentence">Step 9.</caps:sentence>
              <caps:sentence id="src402" class="srcSentence"> Re-key your Azure RMS tenant key</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src403" class="srcSentence">This step is required when migration is complete if your AD RMS deployment was using RMS Cryptographic Mode 1, because re-keying creates a new tenant key that uses RMS Cryptographic Mode 2.</caps:sentence>
                <caps:sentence id="src404" class="srcSentence"> Using Azure RMS with Cryptographic Mode 1 is supported only during the migration process.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src405" class="srcSentence">This step is optional but recommended when migration is complete even if you were running in RMS Cryptographic Mode 2, because it helps to secure your Azure RMS tenant key from potential security breaches to your AD RMS key.</caps:sentence>
                <caps:sentence id="src406" class="srcSentence"> When you re-key your Azure RMS tenant key (also known as “rolling your key”), a new key is created and the original key is archived.</caps:sentence>
                <caps:sentence id="src407" class="srcSentence"> However, because moving from one key to another doesn’t happen immediately but over a few weeks, do not wait until you suspect a breach to your original key but re-key your RMS tenant key as soon as the migration is complete.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src408" class="srcSentence">To re-key your Azure RMS tenant key:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src409" class="srcSentence">If your RMS tenant key is managed by Microsoft: Call Microsoft Customer Support Services (CSS) and prove that you are the RMS tenant administrator.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src410" class="srcSentence">If your RMS tenant key is managed by you (BYOK): Repeat the BYOK procedure to generate and create a new key over the Internet or in person.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src411" class="srcSentence">For more information about managing your RMS tenant key, see <link xlink:href="1284d0ee-0a72-45ba-a64c-3dcb25846c3d">Operations for Your Azure Rights Management Tenant Key</link>.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </section>
      <relatedTopics>
        <link xlink:href="206a0bfe-0912-4e0e-aa15-484b000b264c">Configuring Azure Rights Management</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>