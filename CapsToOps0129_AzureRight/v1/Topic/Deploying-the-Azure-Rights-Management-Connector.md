---
title: Implementaci&#243;n del conector de Azure Rights Management
ms.custom: na
ms.reviewer: na
ms.service: rights-management
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 90e7e33f-9ecc-497b-89c5-09205ffc5066
---
# Implementaci&#243;n del conector de Azure Rights Management
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="es-ES">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="7a6162944876d30464058f0949503015" id="tgt1" class="tgtSentence">Use esta información para obtener más detalles acerca del conector Microsoft y sobre cómo puede usarlo para proporcionar protección de la información con implementaciones locales existentes que usan Microsoft Exchange Server, Microsoft SharePoint Server, o servidores de archivo que ejecutan Windows Server y usan la función de la Infraestructura de clasificación de archivos (FCI) del administrador de recursos del servidor de archivos.</caps:sentence>
        </para>
        <alert class="tip">
          <para>
            <caps:sentence sentenceid="7fc01b361b5631a192db69caffdcd7e8" id="tgt2" class="tgtSentence">Para ver un escenario de ejemplo de alto nivel con capturas de pantalla, consulte la sección <link xlink:href="aeeebcd7-6646-4405-addf-ee1cc74df5df#BKMK_Example_FCI">Automatically protecting files on file servers running Windows Server and File Classification Infrastructure</link> en el tema <link xlink:href="aeeebcd7-6646-4405-addf-ee1cc74df5df">What is Azure Rights Management?</link>.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <section address="OverviewConnector">
        <title>
          <caps:sentence sentenceid="b5d593e32f204c735a7cc2a1ee26773f" id="tgt3" class="tgtSentence">Visión general del conector Rights Management de Microsoft</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="055cd4a135730b9a2452b3f71e42bcae" id="tgt4" class="tgtSentence">El conector Rights Management (RMS) de Microsoft le permite habilitar rápidamente servidores locales existentes para usar su funcionalidad de Information Rights Management (IRM) con el servicio Rights Management de Microsoft basado en la nube (Azure RMS).</caps:sentence>
            <caps:sentence sentenceid="d37cd5e9cee3f98d1e1e8e14925cc908" id="tgt5" class="tgtSentence"> Con esta funcionalidad, los TI y los usuarios pueden proteger fácilmente documentos e imágenes tanto dentro como fuera de la organización, sin tener que instalar más infraestructuras o establecer relaciones de confianza con otras organizaciones.</caps:sentence>
            <caps:sentence sentenceid="8b4640e162d8b6f30ce69650ec8dec72" id="tgt6" class="tgtSentence"> Puede usar este conector incluso si algunos de los usuarios se conectan a servicios en línea, en un escenario híbrido.</caps:sentence>
            <caps:sentence sentenceid="92aa1d9cff38a744b73674c9684d348c" id="tgt7" class="tgtSentence"> Por ejemplo, los buzones de algunos usuarios usan Exchange Online y los buzones de otros usuarios usan Exchange Server.</caps:sentence>
            <caps:sentence sentenceid="f1340f9202cba685f30dcd8a9408f1d5" id="tgt8" class="tgtSentence"> Después de instalar el conector RMS, todos los usuarios pueden proteger y consumir mensajes de correo electrónico y archivos adjuntos con Azure RMS, y la protección de la información funciona sin problemas entre las dos configuraciones de implementación.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="e709d918112fb063e845785a8ddc51c8" id="tgt9" class="tgtSentence">El conector RMS es un servicio de una superficie pequeña que instala localmente en servidores que ejecutan Windows Server 2012 R2, Windows Server 2012 o Windows Server 2008 R2.</caps:sentence>
            <caps:sentence sentenceid="65102465684db5837c8273fc9062a53c" id="tgt10" class="tgtSentence"> Además de ejecutar el conector en equipos físicos, también puede ejecutarlo en máquinas virtuales, incluidas las máquinas virtuales de IaaS de Azure.</caps:sentence>
            <caps:sentence sentenceid="18dd3d1247d38f9a03fd4aeaf5b05844" id="tgt11" class="tgtSentence"> Después de que instalar y configurar el conector, actúa como una interfaz de comunicaciones (una retransmisión) entre servidores locales y el servicio en la nube.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="906859d1fbb2c7b383c26bbd802771a5" id="tgt12" class="tgtSentence">Si administra su propia clave de inquilino para Azure RMS (el escenario bring your own key o BYOK), el conector RMS y los servidores locales que lo usan no tienen acceso al módulo de seguridad de hardware (HSM) que contiene la clave de inquilino.</caps:sentence>
            <caps:sentence sentenceid="da886071099dcdb972fc5b81a3c7dbb2" id="tgt13" class="tgtSentence"> Esto se debe a que todas las operaciones criptográficas que utilizan la clave de inquilino se ejecutan en Azure RMS y no a nivel local.</caps:sentence>
          </para>
          <mediaLink>
            <image xlink:href="fca243be-b886-43ad-91e6-6900f7e2cd85"></image>
          </mediaLink>
          <para></para>
          <para></para>
          <para>
            <caps:sentence sentenceid="9791cbcb95885c74e73fb153b6a17c09" id="tgt14" class="tgtSentence">El conector RMS admite los siguientes servidores locales: Exchange Server, SharePoint Server y servidores de archivos que ejecutan Windows Server y usan las Infraestructuras de clasificación de archivos para clasificar y aplicar directivas a documentos de Office de una carpeta.</caps:sentence>
            <caps:sentence sentenceid="e1ff50040607e9a3434a57e3d86f49d3" id="tgt15" class="tgtSentence"> Si desea proteger todos los tipos de archivos mediante la clasificación de archivos, no use el conector RMS, sino los <externalLink><linkText>cmdlets de protección de RMS</linkText><linkUri>https://msdn.microsoft.com/library/azure/mt433195.aspx</linkUri></externalLink>.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="52ccad7301b8accfe3221729aca291fb" id="tgt16" class="tgtSentence">Para obtener más información acerca de versiones compatibles de estos servidores locales, consulte "Servidores locales que admite Azure RMS" en la sección <link xlink:href="dc78321d-d759-4653-8818-80da74b6cdeb#BKMK_SupportedApplications">Applications that support Azure RMS</link> del tema <link xlink:href="dc78321d-d759-4653-8818-80da74b6cdeb">Requirements for Azure Rights Management</link>.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence sentenceid="c1feb4df24b8f53572830176cc5d76ae" id="tgt17" class="tgtSentence">Use las secciones siguientes para tratar de planificar, instalar y configurar el conector RMS.</caps:sentence>
            <caps:sentence sentenceid="c02f0587eb0c5f44ea097651abb7371e" id="tgt18" class="tgtSentence"> A continuación, debe modificar la configuración después de la instalación para que sus servidores puedan usar el conector.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <link xlink:href="90e7e33f-9ecc-497b-89c5-09205ffc5066#BKMK_Prereqs">Prerequisites for the RMS connector</link>
              </para>
            </listItem>
            <listItem>
              <para>
                <embeddedLabel>
                  <caps:sentence sentenceid="6ca7c6f16311428a9540360a29c0a7da" id="tgt19" class="tgtSentence">Paso 1: </caps:sentence>
                </embeddedLabel>
                <link xlink:href="90e7e33f-9ecc-497b-89c5-09205ffc5066#BKMK_InstallingConnector">Installing the RMS connector</link>
              </para>
            </listItem>
            <listItem>
              <para>
                <embeddedLabel>
                  <caps:sentence sentenceid="029a39daeec69f6bae5275d8aabbe5c2" id="tgt20" class="tgtSentence">Paso 2: </caps:sentence>
                </embeddedLabel>
                <link xlink:href="90e7e33f-9ecc-497b-89c5-09205ffc5066#EnteringCredentials">Entering credentials</link>
              </para>
            </listItem>
            <listItem>
              <para>
                <embeddedLabel>
                  <caps:sentence sentenceid="6f60a71936fbce180817beb0074f20ce" id="tgt21" class="tgtSentence">Paso 3: </caps:sentence>
                </embeddedLabel>
                <link xlink:href="90e7e33f-9ecc-497b-89c5-09205ffc5066#AuthorizingServers">Authorizing servers to use the RMS connector</link>
              </para>
            </listItem>
            <listItem>
              <para>
                <embeddedLabel>
                  <caps:sentence sentenceid="58e2e9cd07b16bc37c239296a4cfe3e1" id="tgt22" class="tgtSentence">Paso 4: </caps:sentence>
                </embeddedLabel>
                <link xlink:href="90e7e33f-9ecc-497b-89c5-09205ffc5066#ConfiguringConnector">Configuring load balancing and high availability</link>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="16b3cffc06da141a8ba5bb6c27709e12" id="tgt23" class="tgtSentence">Opcional: <link xlink:href="90e7e33f-9ecc-497b-89c5-09205ffc5066#BKMK_ConfiguringHTTPS">Configuring the RMS connector to use HTTPS</link></caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="16b3cffc06da141a8ba5bb6c27709e12" id="tgt24" class="tgtSentence">Opcional: <link xlink:href="90e7e33f-9ecc-497b-89c5-09205ffc5066#BKMK_ConfiguringWebProxy">Configuring the RMS connector for a web proxy server</link></caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="16b3cffc06da141a8ba5bb6c27709e12" id="tgt25" class="tgtSentence">Opcional: <link xlink:href="90e7e33f-9ecc-497b-89c5-09205ffc5066#BKMK_InstallingStandaloneTool">Installing the RMS connector administration tool on administrative computers</link></caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <embeddedLabel>
                  <caps:sentence sentenceid="f30fc367a4cf35d144e04c4d95519c8a" id="tgt26" class="tgtSentence">Paso 5: </caps:sentence>
                </embeddedLabel>
                <link xlink:href="90e7e33f-9ecc-497b-89c5-09205ffc5066#ConfiguringServers">Configuring servers to use the RMS connector</link>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <link xlink:href="90e7e33f-9ecc-497b-89c5-09205ffc5066#BKMK_ExchangeServer">Configuring an Exchange server to use the connector</link>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <link xlink:href="90e7e33f-9ecc-497b-89c5-09205ffc5066#BKMK_ConfiguringSharePoint">Configuring a SharePoint server to use the connector</link>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <link xlink:href="90e7e33f-9ecc-497b-89c5-09205ffc5066#BKMK_FileServer">Configuring a file server for File Classification Infrastructure to use the connector</link>
                  </para>
                </listItem>
              </list>
            </listItem>
            <listItem>
              <para>
                <link xlink:href="90e7e33f-9ecc-497b-89c5-09205ffc5066#BKMK_NextSteps">Next steps</link>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <section address="BKMK_Prereqs">
        <title>
          <caps:sentence sentenceid="1ccfe81dd120310397a2c86bb13142f5" id="tgt27" class="tgtSentence">Requisitos previos para el conector RMS</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="2753d692d0129a3db955c26257fc24be" id="tgt28" class="tgtSentence">Antes de instalar el conector RMS, asegúrese de que se cumplen los requisitos siguientes.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ba12fb48e2d23bb2bd2819f64d02ec7e" id="tgt29" class="tgtSentence">Requisito</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5dc731e46ae38b87ff3e3e2eaf459db2" id="tgt30" class="tgtSentence">Más información</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4cc693aa561a743fe51fd95b50ec9ab4" id="tgt31" class="tgtSentence">El servicio Rights Management (RMS) está activado</caps:sentence>
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
                    <caps:sentence sentenceid="a39487505ec7117bf1492b761a6f6441" id="tgt32" class="tgtSentence">Sincronización de directorios entre sus bosques de Active Directory y Azure Active Directory</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8c4c3dd641424a103119c6e1f8b9940b" id="tgt33" class="tgtSentence">Tras activar RMS, se debe configurar Azure Active Directory para trabajar con los usuarios y grupos de tu base de datos de Active Directory.</caps:sentence>
                  </para>
                  <alert class="important">
                    <para>
                      <caps:sentence sentenceid="509b0b290dfd78fe591e65518a910d87" id="tgt34" class="tgtSentence">Debe realizar este paso de sincronización de directorios para que el conector RMS funcione, incluso en una red de prueba.</caps:sentence>
                      <caps:sentence sentenceid="3ee60f6a516d94750c9130d7f944a827" id="tgt35" class="tgtSentence"> Aunque puede usar Office 365 y Azure Active Directory mediante cuentas que crea manualmente en Azure Active Directory, este conector requiere que las cuentas de Azure Active Directory se sincronicen con Servicios de dominio de Active Directory; la sincronización de contraseñas manual no es suficiente.</caps:sentence>
                    </para>
                  </alert>
                  <para>
                    <caps:sentence sentenceid="8a4bbdf5f66ee36c5612a9237510a57f" id="tgt36" class="tgtSentence">Para obtener más información, vea los recursos siguientes:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <externalLink>
                          <linkText>
                            <caps:sentence sentenceid="3e65fcb329eccafe488ef11660214ac5" id="tgt37" class="tgtSentence">Instrucciones para la configuración de su inquilino Azure AD</caps:sentence>
                          </linkText>
                          <linkUri>http://technet.microsoft.com/library/hh967611.aspx</linkUri>
                        </externalLink>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <externalLink>
                          <linkText>
                            <caps:sentence sentenceid="366821e84306191c5ec1b4ff9e8ccb11" id="tgt38" class="tgtSentence">Instrucciones para habilitar la sincronización de directorios con AAD mediante DirSync</caps:sentence>
                          </linkText>
                          <linkUri>http://technet.microsoft.com/library/hh967642.aspx</linkUri>
                        </externalLink>
                        <br />
                      </para>
                    </listItem>
                  </list>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="818270815a83e7634bad4832d21d9d5d" id="tgt39" class="tgtSentence">Opcional pero recomendable: </caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="82d267c56f58dfbc3812cafed3444112" id="tgt40" class="tgtSentence">Habilitar la federación entre los Active Directory y Azure Active Directory locales  </caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8392c40c5baf1a26c9344283ee2d6a36" id="tgt41" class="tgtSentence">Puede habilitar la federación de identidades entre sus directorios locales y Azure Active Directory.</caps:sentence>
                    <caps:sentence sentenceid="4176578bb48c0aaaddbc4626333bad56" id="tgt42" class="tgtSentence"> Esta configuración habilita una experiencia de usuario más sencilla mediante un único inicio de sesión en el servicio RMS.</caps:sentence>
                    <caps:sentence sentenceid="1c6ed80577ce90979fbe4402e70c8195" id="tgt43" class="tgtSentence"> Sin un inicio de sesión único, a los usuarios se les piden sus credenciales para que puedan usar el contenido protegido por derechos.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="b2365eee5db710147350dcfd7fe810da" id="tgt44" class="tgtSentence">Para obtener información para configurar la federación mediante Active Directory Federation Services (AD FS) entre los Servicios de dominio Active Directory y Azure Active Directory, vea la <externalLink><linkText>Lista de comprobación: Usar AD FS para implementar y administrar inicios de sesión únicos</linkText><linkUri>http://technet.microsoft.com/library/jj205462.aspx</linkUri></externalLink> en la biblioteca de Windows Server.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="071b86d5dceed0e99b064aaa5b0cf0ad" id="tgt45" class="tgtSentence">Dos equipos miembro como mínimo en los que instalar el conector RMS:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="743ac00b3533aa77df2122ea451e0af2" id="tgt46" class="tgtSentence">Un ordenador virtual o físico de 64 bits que ejecute uno de los sistemas operativos siguientes: </caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="dcfe8446422dcac28d99767b484594f0" id="tgt47" class="tgtSentence">Windows Server 2012 R2</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="0e22230e53d6559d213afe9ce343ebf5" id="tgt48" class="tgtSentence">Windows Server 2012</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="e4dd9fe1b5efc59f4b6383a1e8e6ccd0" id="tgt49" class="tgtSentence">Windows Server 2008 R2</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="fb46a715b458a6439f4c1c8954c58a24" id="tgt50" class="tgtSentence">Como mínimo 1 GB de RAM</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="de435841b10527c4c6543b5389a57ef3" id="tgt51" class="tgtSentence">Un mínimo de 64 GB de espacio en disco</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="8a22600aef9db831ec10619c162d4aba" id="tgt52" class="tgtSentence">Como mínimo una interfaz de red</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="411b32416763480d0426f0201d575c0d" id="tgt53" class="tgtSentence">Acceso a Internet a través de un firewall (o proxy web) que no precise autenticación</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="482d832f7ce2667a49d4ec0bb76ff242" id="tgt54" class="tgtSentence">Debe encontrarse en un bosque o dominio que confíe en otros bosques de la organización que contengan instalaciones de servidores de Exchange o SharePoint que quiera usar con el conector RMS.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="be829763c3ab214a76cc04344f3e4aca" id="tgt55" class="tgtSentence">Para la tolerancia a errores y alta disponibilidad, debe instalar el conector RMS como mínimo en dos equipos.</caps:sentence>
                  </para>
                  <alert class="tip">
                    <para>
                      <caps:sentence sentenceid="e06f17edc1c0af9ca06d63df33e0254d" id="tgt56" class="tgtSentence">Si utiliza Outlook Web Access o dispositivos móviles que utilizan Exchange ActiveSync IRM y es fundamental mantener el acceso a los correos electrónicos y archivos adjuntos protegidos por RMS de Azure, se recomienda implementar un grupo de servidores de conector de carga equilibrada para garantizar una alta disponibilidad.</caps:sentence>
                    </para>
                  </alert>
                  <para>
                    <caps:sentence sentenceid="5afb51fb26e7c5af4abb8660840eccfc" id="tgt57" class="tgtSentence">No necesita servidores dedicados para ejecutar el conector pero debe instalarlo en un ordenador independiente respecto a los servidores que usarán el conector.</caps:sentence>
                  </para>
                  <alert class="important">
                    <para>
                      <caps:sentence sentenceid="ce6105ea435c7505486ad146f3d6eb5e" id="tgt58" class="tgtSentence">No instale el conector en un equipo que ejecute Exchange Server, SharePoint Server o un servidor de archivos que esté configurado para las infraestructuras de clasificación de archivos si quiere usar la funcionalidad desde estos servicios con Azure RMS.</caps:sentence>
                      <caps:sentence sentenceid="5952ef47c89b6eeb70c806f4e256b86b" id="tgt59" class="tgtSentence"> Además, no instale este conector en un controlador de dominio.</caps:sentence>
                    </para>
                  </alert>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section address="BKMK_InstallingConnector">
        <title>
          <caps:sentence sentenceid="a097531c7c73ba2168b7fd0023037981" id="tgt60" class="tgtSentence">Instalación del conector RMS</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="2683aff2913538589624d5341751493f" id="tgt61" class="tgtSentence">Tras haber confirmado los requisitos previos en la sección anterior, use las instrucciones siguientes para instalar el conector RMS:</caps:sentence>
          </para>
          <list class="ordered">
            <listItem>
              <para>
                <caps:sentence sentenceid="5dba1d0f718bd4797a48a73d554aa7e9" id="tgt62" class="tgtSentence">Identifique los equipos (dos como mínimo) que ejecutarán el conector RMS.</caps:sentence>
                <caps:sentence sentenceid="65a75631b3c8a144e8c2790e1fe01c8d" id="tgt63" class="tgtSentence"> Deben cumplir con las especificaciones mínimas enumeradas en la sección anterior.</caps:sentence>
              </para>
              <alert class="note">
                <para>
                  <caps:sentence sentenceid="29fbb72aff9e109ed56013148758d88f" id="tgt64" class="tgtSentence">Instalará un solo conector RMS (que consta de múltiples servidores para alta disponibilidad) por inquilino (inquilino de Office 365 o Azure AD).</caps:sentence>
                  <caps:sentence sentenceid="eb01f1c670f3277d52a2d3c7b03907a4" id="tgt65" class="tgtSentence"> Al contrario de lo que sucede con Active Directory RMS, no tendrá que instalar un conector RMS en cada bosque.</caps:sentence>
                </para>
              </alert>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="6ad617dfefeb1ce2bdd17602e58ee19c" id="tgt66" class="tgtSentence">Descargue los archivos de origen para el conector RMS desde el <externalLink><linkText>Centro de descarga de Microsoft</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=314106</linkUri></externalLink>.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="2baf601fe5549c9246d69973f36aa263" id="tgt67" class="tgtSentence">Para instalar el conector RMS, descargue RMSConnectorSetup.exe.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="cffdd0bc68b81b41855c6d1dfd403038" id="tgt68" class="tgtSentence">Además:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="db53535715f025a7acec80ecfa44282c" id="tgt69" class="tgtSentence">Si posteriormente quiere configurar el conector desde un equipo de 32 bits, descargue también RMSConnectorAdminToolSetup_x86.exe.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="c7e0e8551b1daf0b1878241811edcb12" id="tgt70" class="tgtSentence">Si quiere usar la herramienta de configuración del servidor para el conector RMS, para automatizar la configuración de los parámetros de registro en tus servidores locales, descargue también GenConnectorConfig.ps1.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="7df8401333044f571ba23d79452b23e2" id="tgt71" class="tgtSentence">En el equipo en que desea instalar el conector RMS, ejecute <legacyBold>RMSConnectorSetup.exe</legacyBold> con privilegios de administrador.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="fb1f144df529fb3686201af678647e9f" id="tgt72" class="tgtSentence">En la página de bienvenida de la página de Configuración del conector de Rights Management de Microsoft, seleccione <ui>Instalar el conector de Rights Management de Microsoft en el ordenador</ui> y después haga clic en <ui>Siguiente</ui>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="f6750556263fa6a90035e84aca8a3a88" id="tgt73" class="tgtSentence">Lea y acepte los términos de licencia del conector RMS y, a continuación, haga clic en <legacyBold>Siguiente</legacyBold>.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="b9be15fccc81a0be0495ca57869884b4" id="tgt74" class="tgtSentence">Para continuar, escriba una cuenta y una contraseña para configurar el conector RMS.</caps:sentence>
          </para>
        </content>
      </section>
      <section address="EnteringCredentials">
        <title>
          <caps:sentence sentenceid="f3ab65572ec1a60cccba387066475792" id="tgt75" class="tgtSentence">Introducción de credenciales</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="cb348a59fe77cb8a13563b6c2d096435" id="tgt76" class="tgtSentence">Para poder configurar el conector RMS, debe introducir las credenciales para una cuenta en que tenga suficientes privilegios para configurar el conector RMS.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="d3d920ac821595ad446b513e8e9a2cfa" id="tgt77" class="tgtSentence">Además, si implementó <externalLink><linkText>controles de incorporación</linkText><linkUri>https://technet.microsoft.com/library/jj658941.aspx#BKMK_OnboardingControls</linkUri></externalLink>, asegúrese de que la cuenta especificada es capaz de proteger el contenido. Por ejemplo, si restringió la capacidad de proteger el contenido al grupo “Departamento de TI”, la cuenta que especifique aquí debe pertenecer a ese grupo. En caso contrario, verá el mensaje de error: <ui>Error al intentar detectar la ubicación de la organización y el servicio de administración. Asegúrese de que el servicio Microsoft Rights Management está habilitado para su organización.</ui></caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="f1bb02f59ce23ab4c46f5cfdb0be3f02" id="tgt78" class="tgtSentence">Puede usar una cuenta que tenga solo uno de los privilegios siguientes:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="721928e95c3e4470484e63ec4a0a892e" id="tgt79" class="tgtSentence">
                  <legacyBold>Administrador de inquilinos de Office 365</legacyBold>: una cuenta que sea un administrador global para el inquilino de Office 365.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="aaa4c1c71dd5c17c11a14f0253bd01e5" id="tgt80" class="tgtSentence">
                  <legacyBold> Administrador global de Azure Rights Management</legacyBold>: Una cuenta con privilegios de administrador para su inquilino de Azure RMS.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="6d3697a2c3fc42aec1c10c7baafe0a34" id="tgt81" class="tgtSentence">
                  <legacyBold>Administrador de conector de Microsoft RMS</legacyBold>: Una cuenta de Azure Active Directory que tiene garantizados los permisos para instalar y administrar el conector RMS para la organización.</caps:sentence>
              </para>
              <para></para>
              <alert class="note">
                <para>
                  <caps:sentence sentenceid="a4cfb8c9b77637682a5f4eca5c437c52" id="tgt82" class="tgtSentence">Si quiere usar la cuenta de administrador del conector de Microsoft RMS, en primer lugar, debe seguir las siguientes indicaciones para asignar el rol de administrador del conector RMS:</caps:sentence>
                </para>
                <list class="ordered">
                  <listItem>
                    <para>
                      <caps:sentence sentenceid="fdf56343b661842aa0b6e37fdf12a7f3" id="tgt83" class="tgtSentence">En el mismo equipo, descargue e instale Windows PowerShell para Rights Management.</caps:sentence>
                      <caps:sentence sentenceid="1070f425823a6e05a98eb2d747f0c53d" id="tgt84" class="tgtSentence"> Para obtener más información, vea <link xlink:href="0d665ed6-b1de-4d63-854a-bc57c1c49844">Installing Windows PowerShell for Azure Rights Management</link>.</caps:sentence>
                    </para>
                    <para>
                      <caps:sentence sentenceid="a796808f0542040254624a40c5de067c" id="tgt85" class="tgtSentence">Inicie Windows PowerShell con el comando <ui>Ejecutar como administrador</ui> y conecte el servicio Azure RMS mediante el comando <externalLink><linkText>Connect-AadrmService</linkText><linkUri>https://msdn.microsoft.com/library/azure/dn629415.aspx</linkUri></externalLink>: </caps:sentence>
                    </para>
                    <code>Connect-AadrmService                   //provide Office 365 tenant administrator or Azure RMS global administrator credentials</code>
                  </listItem>
                  <listItem>
                    <para>
                      <caps:sentence sentenceid="8919365c5c68f46a9fe26ea91750f360" id="tgt86" class="tgtSentence">Luego ejecute el comando <externalLink><linkText>Add-AadrmRoleBasedAdministrator</linkText><linkUri>https://msdn.microsoft.com/library/azure/dn629417.aspx</linkUri></externalLink> mediante solo uno de los parámetros siguientes:   </caps:sentence>
                    </para>
                    <code>Add-AadrmRoleBasedAdministrator -EmailAddress &lt;email address&gt; -Role "ConnectorAdministrator"</code>
                    <code>Add-AadrmRoleBasedAdministrator -ObjectId &lt;object id&gt; -Role "ConnectorAdministrator"</code>
                    <code>Add-AadrmRoleBasedAdministrator -SecurityGroupDisplayName &lt;group Name&gt; -Role "ConnectorAdministrator"</code>
                    <para>
                      <caps:sentence sentenceid="62f09bdf0c668d96dae04afe4a65c6c0" id="tgt87" class="tgtSentence">Por ejemplo, escriba: <userInput>Add-AadrmRoleBasedAdministrator -EmailAddress melisa@contoso.com -Role " ConnectorAdministrator "</userInput></caps:sentence>
                    </para>
                    <para>
                      <caps:sentence sentenceid="216f4216e4c945f3c920e7500c84d937" id="tgt88" class="tgtSentence">Aunque estos comandos usan el rol ConnectorAdministrator, aquí también puede usar el rol GlobalAdministrator.</caps:sentence>
                    </para>
                  </listItem>
                </list>
              </alert>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="48c33e420a248058e2bbd625b7a34970" id="tgt89" class="tgtSentence">Durante el proceso de instalación del conector RMS, se valida e instala todo el software que sea un requisito previo, se instala Internet Information Services (IIS) si ya no lo está, y se instalará y configurará el software del conector.</caps:sentence>
            <caps:sentence sentenceid="beb35addbc938394bbd44ea88e344c6f" id="tgt90" class="tgtSentence"> Además, se prepara RMS para su configuración mediante la creación de los siguientes elementos:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="1e4cdaf9ab90508068e985fa431c9f26" id="tgt91" class="tgtSentence">Una tabla vacía de servidores autorizados para usar el conector para comunicarse con Azure RMS.</caps:sentence>
                <caps:sentence sentenceid="955f4d8c6905a4bbb95744d0c6f6cc1b" id="tgt92" class="tgtSentence"> Agregará servidores a esta tabla posteriormente.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="be814012ee77847e7183933f5f00bfdb" id="tgt93" class="tgtSentence">Un conjunto de tokens de seguridad para el conector que autorizan operaciones con Azure RMS.</caps:sentence>
                <caps:sentence sentenceid="ebc2ff50cd76fd12aa3c159e735dfc8b" id="tgt94" class="tgtSentence"> Estos tokens se descargan de Azure RMS y se instalan en el equipo local en el Registro.</caps:sentence>
                <caps:sentence sentenceid="ce6b2a1425f0bcda64af2c1fbf277f6e" id="tgt95" class="tgtSentence"> Están protegidos mediante la interfaz de programación de aplicaciones de protección de datos (DPAPI) y las credenciales de la cuenta del sistema local.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="585f16e4f6f2ac28947880d321fd082b" id="tgt96" class="tgtSentence">En la página final del asistente, haga lo que se indica y, a continuación, haga clic en <ui>Finalizar</ui>:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="e7a8aad1e2923e9f3a5eb5a441f023c2" id="tgt97" class="tgtSentence">Si este es el primer conector que ha instalado, no seleccione <ui>Iniciar la consola de administración del conector para autorizar servidores</ui>.</caps:sentence>
                <caps:sentence sentenceid="b3270ab9c3d0af9feb445dd94f6b6f5e" id="tgt98" class="tgtSentence"> Seleccionará esta opción después de que haya instalado su segundo (o último) conector RMS.</caps:sentence>
                <caps:sentence sentenceid="2b4e0a614cd77b42f7d76081228dbf62" id="tgt99" class="tgtSentence"> En su lugar, ejecute el asistente de nuevo como mínimo en otro equipo.</caps:sentence>
                <caps:sentence sentenceid="0902aa712955f05caec15a8b74d25ce9" id="tgt100" class="tgtSentence"> Debe instalar un mínimo de dos conectores.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="2a8dbb6ef8c095f46e806d796b75a30b" id="tgt101" class="tgtSentence">Si ha instalado su segundo (o último) conector, seleccione <ui>Iniciar la consola de administración del conector para autorizar servidores</ui>.</caps:sentence>
              </para>
            </listItem>
          </list>
          <alert class="tip">
            <para>
              <caps:sentence sentenceid="df6dcb3a83256911b88b67bb071ae445" id="tgt102" class="tgtSentence">Llegado a este punto, encontramos una prueba de comprobación que puede llevar a cabo para evaluar si los servicios web para el conector RMS son operativos: </caps:sentence>
            </para>
            <list class="bullet">
              <listItem>
                <para>
                  <caps:sentence sentenceid="e2caec12484fc91954de516e88a6e270" id="tgt103" class="tgtSentence">En un explorador web, conéctese a <userInput>http://&lt;connectoraddress&gt;/_wmcs/certification/servercertification.asmx</userInput>, reemplace <placeholder>&lt;connectoraddress&gt;</placeholder> por la dirección o el nombre del servidor que tenga instalado el conector RMS.</caps:sentence>
                  <caps:sentence sentenceid="96f9568af7dcb52bbe651774991fa54d" id="tgt104" class="tgtSentence"> Si la conexión es correcta aparecerá una página <ui>ServerCertificationWebService</ui>.</caps:sentence>
                </para>
              </listItem>
            </list>
          </alert>
          <para>
            <caps:sentence sentenceid="f2d538e4f0c1c2e742e383da8171c027" id="tgt105" class="tgtSentence">Si necesita desinstalar el conector RMS, ejecute el asistente de nuevo y seleccione la opción desinstalar.</caps:sentence>
          </para>
        </content>
      </section>
      <section address="AuthorizingServers">
        <title>
          <caps:sentence sentenceid="8214573b296103dbf1a5995811a1f621" id="tgt106" class="tgtSentence">Autorización para que los servidores usen el conector RMS</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="1d3d4797d2c7b0915d44aa19c772697b" id="tgt107" class="tgtSentence">Cuando haya instalado el conector RMS en dos equipo al menos, estará preparado para autorizar a los servidores y servicios en que quiera usar el conector RMS.</caps:sentence>
            <caps:sentence sentenceid="c2a56e3bbc38fd5b16f71436ba5d2ce6" id="tgt108" class="tgtSentence"> Por ejemplo, sus servidores que ejecutan Exchange Server 2013 o SharePoint Server 2013.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="b3b86015971adac6b8f3e444ecb4d5aa" id="tgt109" class="tgtSentence">Para definir estos servidores, ejecute la herramienta de administración del conector RMS y agregue entradas a la lista de servidores permitidos.</caps:sentence>
            <caps:sentence sentenceid="13168f22ff5466332095675df81a5d13" id="tgt110" class="tgtSentence"> Puede ejecutar esta herramienta cuando seleccione <ui>Iniciar la consola de administración del conector para autorizar servidores</ui> al final del asistente de configuración del conector Rights Management de Microsoft, o puede ejecutarla de forma independiente desde el asistente.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="ddfbe0c4ee033218eceaa53926be88a1" id="tgt111" class="tgtSentence">Cuando autorice estos servidores, tenga en cuenta las consideraciones siguientes:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="101ebdc12421108a1e09ccb784b5e510" id="tgt112" class="tgtSentence">Los servidores que agregue tendrán garantizados privilegios especiales.</caps:sentence>
                <caps:sentence sentenceid="4fd11713639079db66ddbd3b56934f67" id="tgt113" class="tgtSentence"> Se concederá el <externalLink><linkText>rol de superusuario</linkText><linkUri>https://technet.microsoft.com/library/mt147272.aspx</linkUri></externalLink> en Azure RMS a todas las cuentas que especifique para el rol de Exchange Server en la configuración del conector, lo que les permitirá acceder a todo el contenido de este inquilino de RMS.</caps:sentence>
                <caps:sentence sentenceid="c960a65524412d07fa83118cbee540c4" id="tgt114" class="tgtSentence"> La característica de superusuario se habilita automáticamente en este momento, si es necesario.</caps:sentence>
                <caps:sentence sentenceid="5e7a4edd8a45688746b57b47c13facfc" id="tgt115" class="tgtSentence"> Para evitar el riesgo de seguridad de elevación de privilegios, tenga la precaución de especificar únicamente las cuentas que van a ser usadas por los servidores de Exchange de la organización.</caps:sentence>
                <caps:sentence sentenceid="89b8846d51dac31d9c31bcf4d31a7173" id="tgt116" class="tgtSentence"> Todos los servidores configurados como servidores de SharePoint o servidores de archivos que usen FCI tendrán garantizados los privilegios de usuario regular.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="d05e949be91d74ff1fd012b56939f1db" id="tgt117" class="tgtSentence">Puede agregar servidores múltiples como una entrada única especificando un grupo de seguridad o distribución de Active Directory, o una cuenta de servicio usada por más de un servidor.</caps:sentence>
                <caps:sentence sentenceid="700a748799136643f241bb185af329f0" id="tgt118" class="tgtSentence"> Cuando use esta configuración, el grupo de servidores compartirá los mismos certificados RMS y todos serán considerados propietarios del contenido que cualquiera de ellos haya protegido.</caps:sentence>
                <caps:sentence sentenceid="37f27ab8e26a1787691255d375aa011c" id="tgt119" class="tgtSentence"> Para minimizar la sobrecarga administrativa, es recomendable que use esta configuración de un solo grupo, en lugar de servidores individuales para autorizar sus servidores de Exchange de la organización o una granja de servidores de SharePoint.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt120" class="tgtSentence">En la página <ui>Servidores a los que se permite utilizar el conector</ui>, haga clic en <ui>Agregar</ui>.</caps:sentence>
          </para>
        </content>
        <sections>
          <section address="BKMK_AddServer">
            <title>
              <caps:sentence sentenceid="14abea1c2bfc5791205ea144663cbd47" id="tgt121" class="tgtSentence">Agregar un servidor a la lista de servidores autorizados</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt122" class="tgtSentence">En la página <ui>Permitir a un servidor que utilice el conector</ui>, escriba el nombre del objeto, o explore para identificar el objeto que se autorizará.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="a850f1ef21d283acc5f7437d3d4b1c21" id="tgt123" class="tgtSentence">Es importante que autorice el objeto apropiado.</caps:sentence>
                <caps:sentence sentenceid="bcd7cac37b32b3645578df87a01522d3" id="tgt124" class="tgtSentence"> Para que un servidor use el conector, se debe seleccionar la cuenta que ejecuta el servicio local (por ejemplo, Exchange o SharePoint) para recibir la autorización.</caps:sentence>
                <caps:sentence sentenceid="6e42100cbfb4b7483b579a291cec06fc" id="tgt125" class="tgtSentence"> Por ejemplo, si el servicio se ejecuta como una cuenta de servicio configurada, agregue el nombre de esa cuenta de servicio a la lista.</caps:sentence>
                <caps:sentence sentenceid="1ffc6906ab4dd3e65d5edfb969f21a3b" id="tgt126" class="tgtSentence"> Si el servicio se ejecuta como sistema local, agregue el nombre del objeto de equipo (por ejemplo, SERVERNAME$).</caps:sentence>
                <caps:sentence sentenceid="e7aeabf9f8d208053898aa5944c47dbc" id="tgt127" class="tgtSentence"> Como consejo, cree un grupo que contenga estas cuentas y especifique el grupo en lugar de nombres de servidor individuales.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="4e65b04de4a199b2dc7cf8cf59088377" id="tgt128" class="tgtSentence">Más información acerca de los diferentes roles del servidor:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="c36ed3bd2f47ee5610078f81000f550f" id="tgt129" class="tgtSentence">Para servidores que ejecutan Exchange: Debe especificar un grupo de seguridad y puede usar el grupo predeterminado (<ui>Servidores de Exchange</ui>) que Exchange crea y mantiene automáticamente de todos los servidores Exchange del bosque.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="431c88da3303d82a5d63d601d48f851a" id="tgt130" class="tgtSentence">Para servidores que ejecutan SharePoint: </caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="9f7e007bd69bc299dda2a379909d1f42" id="tgt131" class="tgtSentence">Si un servidor de SharePoint 2010 se configura para ejecutarse como sistema local (no usa una cuenta de servicio), cree manualmente un grupo de seguridad en Servicios de dominio de Active Directory y agregue el objeto de nombre del equipo para el servidor de esta configuración a este grupo.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="ab82a845c2c646f4f8112b80483b6758" id="tgt132" class="tgtSentence">Si un servidor de SharePoint se configura para usar una cuenta de servicio (la práctica recomendada para SharePoint 2010 y la única opción para SharePoint 2013), haga lo siguiente:</caps:sentence>
                      </para>
                      <list class="ordered">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="95dc43df1668336ffdc23440d6ca41ac" id="tgt133" class="tgtSentence">Agregue la cuenta de servicio que ejecuta el servicio de administración central SharePoint para habilitar SharePoint a fin de que se configure desde la consola del administrador.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="f83b6e14857e379b24024800fa080459" id="tgt134" class="tgtSentence">Agregue la cuenta que se ha configurado para el grupo de aplicaciones SharePoint.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                      <alert class="tip">
                        <para>
                          <caps:sentence sentenceid="35b8c2b7036dc41f31c9eedd41af2618" id="tgt135" class="tgtSentence">Si estas dos cuentas son diferentes, tenga en cuenta la creación de un solo grupo que contenga ambas cuentas para minimizar las sobrecargas administrativas.</caps:sentence>
                        </para>
                      </alert>
                    </listItem>
                  </list>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="7022e31bdb2b82cfc831936790b529bb" id="tgt136" class="tgtSentence">Para servidores de archivos que usan Infraestructura de clasificación de archivos, los servicios asociados se ejecutan como la cuenta del sistema local, de modo que debe autorizar la cuenta del equipo para los servidores de archivo (por ejemplo, SERVERNAME$) o un grupo que contenga esas cuentas de equipo.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="ca12fcb347ae7a98476777536faa020a" id="tgt137" class="tgtSentence">Cuando haya acabado de agregar servidores a la lista, haga clic en <ui>Cerrar</ui>.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="8cd07aa9575e6ba1199e187d32afc8c0" id="tgt138" class="tgtSentence">Si todavía no lo ha hecho, debe configurar ahora el equilibrio de carga para los servidores que tengan instalado el conector RMS, y considerar si usar HTTPS para las conexiones entre estos servidores y los servidores que acaba de autorizar.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </section>
      <section address="ConfiguringConnector">
        <title>
          <caps:sentence sentenceid="b9d3f87e64bd72d1b8a3af29fb98d785" id="tgt139" class="tgtSentence">Configuración del equilibrio de carga y alta disponibilidad</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="2fbe27422cd3fbb3544d351a72ce2e53" id="tgt140" class="tgtSentence">Tras haber instalado la segunda o última instancia del conector RMS, defina un nombre de servidor URL conector y configure un sistema de equilibrio de carga.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="8b676bf7ae0610785175239af6993c22" id="tgt141" class="tgtSentence">El nombre de servidor URL conector puede ser cualquier nombre en un espacio de nombres que controle.</caps:sentence>
            <caps:sentence sentenceid="3234547ad470d131db6e55dc2edd63d0" id="tgt142" class="tgtSentence"> Por ejemplo, podría crear una entrada en su sistema DNS para <userInput>rmsconnector.contoso.com</userInput> y configurar dicha entrada para usar una dirección IP en su sistema de equilibrio de carga.</caps:sentence>
            <caps:sentence sentenceid="d252bcebaf1e0a99853146377279ee89" id="tgt143" class="tgtSentence"> No existen requisitos especiales para este nombre y no es necesario configurarlo en los servidores del conector propiamente dichos.</caps:sentence>
            <caps:sentence sentenceid="ef70e1e93629262689c3e3309a7b6413" id="tgt144" class="tgtSentence"> A menos que los servidores Exchange y SharePoint vayan a comunicarse con el conector a través de Internet, este nombre no tiene que resolverse en Internet.</caps:sentence>
          </para>
          <alert class="important">
            <para>
              <caps:sentence sentenceid="f187618170083b0b2b19066488f93670" id="tgt145" class="tgtSentence">Recomendamos que no cambie este nombre tras haber configurado servidores Exchange o SharePoint para usar el conector, ya que tendrá que limpiar posteriormente estos servidores de todas las configuraciones de IRM y, después, reconfigurarlos.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence sentenceid="d6d0f1e53afffec21069db10e0ecbfec" id="tgt146" class="tgtSentence">Tras crear el nombre en DNS y configurarlo para una dirección IP, configure el equilibrio de carga para esa dirección, que dirige el tráfico a los servidores del conector.</caps:sentence>
            <caps:sentence sentenceid="d7305ec48e40b34f0eaa42ac26b92064" id="tgt147" class="tgtSentence"> Puede usar cualquier equilibrador de carga basado en IP con este motivo, que incluye la característica Equilibrio de carga de red (NLB) en Windows Server.</caps:sentence>
            <caps:sentence sentenceid="1070f425823a6e05a98eb2d747f0c53d" id="tgt148" class="tgtSentence"> Para obtener más información, consulte <externalLink><linkText>Método de equilibrio de carga de conmutación por error</linkText><linkUri>http://technet.microsoft.com/library/cc754833(v=WS.10).aspx</linkUri></externalLink>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="cf4fb16767518f48195ba3f946728caa" id="tgt149" class="tgtSentence">Use la configuración siguiente para configurar el clúster NLB:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="feeb3797f0549991724a949eaa053b37" id="tgt150" class="tgtSentence">Puertos: 80 (para HTTP) o 443 (para HTTPS)</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="1653c99d41f41e3f9ea479e95ad21ac4" id="tgt151" class="tgtSentence">Para obtener más información acerca de si usar HTTP o HTTPS, vea la sección siguiente.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="2cbe97607860ac168d6763b6802b2681" id="tgt152" class="tgtSentence">Afinidad: Ninguno</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="fffbe5db38ffa671e782f9e55e4f980b" id="tgt153" class="tgtSentence">Método de distribución: Igual</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="70b9ef85fcd69000856a2bca8a849588" id="tgt154" class="tgtSentence">Este nombre que defina para el sistema de carga equilibrada (para los servidores que ejecutan el servicio de conector de RMS) es el nombre del conector RMS de su organización que utilizará más adelante, cuando configure los servidores locales para usar Azure RMS.</caps:sentence>
          </para>
        </content>
      </section>
      <section address="BKMK_ConfiguringHTTPS">
        <title>
          <caps:sentence sentenceid="77ec061e6df54b764ab96859bad97a9e" id="tgt155" class="tgtSentence">Configuración del conector RMS para usar HTTPS</caps:sentence>
        </title>
        <content>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="adef3a240ea0ba176a4a53bff8d02540" id="tgt156" class="tgtSentence">Este paso de configuración es opcional, pero es recomendable para conseguir más seguridad.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence sentenceid="805bf92503a1da709b7b4cc9706a3649" id="tgt157" class="tgtSentence">Aunque el uso de TLS o SSL es opcional para el conector RMS, lo recomendamos para cualquier servicio de seguridad basado en HTTP.</caps:sentence>
            <caps:sentence sentenceid="a2c93bde42fd8a2caea2f206df051119" id="tgt158" class="tgtSentence"> Esta configuración autentica los servidores que ejecutan el conector en sus servidores Exchange y SharePoint que usen el conector.</caps:sentence>
            <caps:sentence sentenceid="a40550bd88df79e22227e779d901419d" id="tgt159" class="tgtSentence"> Además, todos los datos que se envían desde estos servidores al conector son cifrados.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="182d8d028289f6f0f3cecc33d5a10dd0" id="tgt160" class="tgtSentence">Para habilitar el conector RMS para que use TLS, en cada servidor que se ejecuta el conector RMS, instale un certificado de autenticación del servidor que contenga el nombre que usará para el conector.</caps:sentence>
            <caps:sentence sentenceid="fc617969b1a217fd42479cceb563bd02" id="tgt161" class="tgtSentence"> Por ejemplo, si el nombre del conector RMS que ha definido en DNS es <system>rmsconnector.contoso.com</system>, implemente un certificado de autenticación del servidor que contenga <system>rmsconnector.contoso.com</system> en el asunto del certificado como el nombre común.</caps:sentence>
            <caps:sentence sentenceid="c6152d12661a75eaef3f4ec463aba688" id="tgt162" class="tgtSentence"> También puede especificar <system>rmsconnector.contoso.com</system> en el nombre de certificado alternativo como el valor DNS.</caps:sentence>
            <caps:sentence sentenceid="0820af866ffd98ce739ce6af617cdece" id="tgt163" class="tgtSentence"> El certificado no tiene que incluir el nombre del servidor.</caps:sentence>
            <caps:sentence sentenceid="d8a7921d1cc583ed1be4c2d4aea1c254" id="tgt164" class="tgtSentence"> A continuación, en IIS, enlace este certificado al sitio web predeterminado.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="7bfb369589d448d139ea2249a55ebc6f" id="tgt165" class="tgtSentence">Si usa la opción HTTPS, asegúrese de que todos los servidores que ejecutan el conector tienen un certificado de autenticación de servidor válido que se encadena a una CA raíz en que confían sus servidores Exchange y SharePoint.</caps:sentence>
            <caps:sentence sentenceid="12b94bf1b90a5f1dfc699edb772ff2f2" id="tgt166" class="tgtSentence"> Además, si la autoridad de certificación (CA) que han emitido los certificados para los servidores del conector publica una lista de revocaciones de certificados (CRL), los servidores Exchange y SharePoint deben ser aptos para descargar esta CRL.</caps:sentence>
          </para>
          <alert class="tip">
            <para>
              <caps:sentence sentenceid="5e19cd30bbf23d0e8432875f7737ae18" id="tgt167" class="tgtSentence">Puede usar la información y los recursos siguientes para tratar de solicitar e instalar un certificado de autenticación de servidor, y para enlazar este certificado al sitio web predeterminado en IIS:</caps:sentence>
            </para>
            <list class="bullet">
              <listItem>
                <para>
                  <caps:sentence sentenceid="b806d67763b33e943caf2576141ed412" id="tgt168" class="tgtSentence">Si usa Active Directory Certificate Services (AD CS) y una autoridad de certificación (CA) empresarial para implementar estos certificados de autenticación de servidor, puede duplicar y, a continuación, usar la plantilla de certificados del servidor web.</caps:sentence>
                  <caps:sentence sentenceid="013085b0b42d20c932aba492fa3aa956" id="tgt169" class="tgtSentence"> Esta plantilla de certificados usa <ui>Suministrado en la solicitud</ui> para el nombre del asunto del certificado, lo que significa que puede proporcionar el FQDN del nombre del conector RMS para el nombre del asunto del certificado o el nombre alternativo del asunto cuando solicite el certificado.</caps:sentence>
                </para>
              </listItem>
              <listItem>
                <para>
                  <caps:sentence sentenceid="6ff693df102d320dbcbaf74584cce73d" id="tgt170" class="tgtSentence">Si usa un CA independiente o compra este certificado desde otra compañía, consulte <externalLink><linkText>Configuración de certificados de servidores de Internet (IIS 7)</linkText><linkUri>http://technet.microsoft.com/library/cc731977(v=ws.10).aspx</linkUri></externalLink> de la biblioteca de documentación del <externalLink><linkText>Servidor web (IIS)</linkText><linkUri>http://technet.microsoft.com/library/cc753433(v=ws.10).aspx</linkUri></externalLink> en TechNet.</caps:sentence>
                </para>
              </listItem>
              <listItem>
                <para>
                  <caps:sentence sentenceid="ea3c18c6812e5c4578da6145289f355f" id="tgt171" class="tgtSentence">Para configurar IIS para usar el certificado, consulte <externalLink><linkText>Agregar un enlace a un sitio (IIS 7)</linkText><linkUri>http://technet.microsoft.com/library/cc731692.aspx</linkUri></externalLink> de la biblioteca de documentación del <externalLink><linkText>Servidor web (IIS)</linkText><linkUri>http://technet.microsoft.com/library/cc753433(v=ws.10).aspx</linkUri></externalLink> en TechNet.</caps:sentence>
                </para>
              </listItem>
            </list>
          </alert>
        </content>
      </section>
      <section address="BKMK_ConfiguringWebProxy">
        <title>
          <caps:sentence sentenceid="470350076c092a07e1efa445e9a8eaa0" id="tgt172" class="tgtSentence">Configuración del conector RMS para un servidor proxy web</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="d4ca6ed64a55ee164b5a661ebd25aa9a" id="tgt173" class="tgtSentence">Si los servidores del conector están instalados en una red que no tiene conexión directa con Internet y precisa configuración manual de un servidor proxy web para acceso de salida a Internet, debe configurar el registro en estos servidores para el conector RMS.</caps:sentence>
          </para>
          <procedure>
            <title>
              <caps:sentence sentenceid="3a69bed528711f3a4a9cf4e546098566" id="tgt174" class="tgtSentence">Para configurar el conector RMS para que use el servidor proxy web</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="c9a0088c5d7c5508f7af41b873246b66" id="tgt175" class="tgtSentence">En cada servidor que ejecute el conector RMS, abra un editor de registro, como Regedit.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="52a0a486115949d5009cfa2b41666228" id="tgt176" class="tgtSentence">Navegue hasta <ui>HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AADRM\Connector</ui></caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="cfe6c7e5de4ac45d09deeed107852ddf" id="tgt177" class="tgtSentence">Agregue el valor de la cadena de <ui>ProxyAddress</ui> y luego establezca que los datos para este valor sean <ui>http://&lt;MyProxyDomainOrIPaddress&gt;:&lt;MyProxyPort&gt;</ui></caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="d05370276e06291b048268558cc39bee" id="tgt178" class="tgtSentence">Por ejemplo: <userInput>http://proxyserver.contoso.com:8080</userInput></caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="a5444341c5554ac673a8d830e8e91b7c" id="tgt179" class="tgtSentence">Cierre el editor del registro y, a continuación, reinicie el servidor o realice un comando IISReset para reiniciar IIS.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
        </content>
      </section>
      <section address="BKMK_InstallingStandaloneTool">
        <title>
          <caps:sentence sentenceid="87b721e8df1d5b7207fd6e05c93a8c14" id="tgt180" class="tgtSentence">Instalación de la herramienta de administración del conector RMS en equipos administrativos</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="ea648935604210387d51ae1aca3e3567" id="tgt181" class="tgtSentence">Puede ejecutar la herramienta de administración del conector RMS desde un equipo que no tenga instalado el conector RMS si cumple los requisitos siguientes:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="965f4b130debf6c988269afef269e961" id="tgt182" class="tgtSentence">Un equipo físico o virtual que ejecute Windows Server 2012 o Windows Server 2012 R2 (todas las ediciones), Windows Server 2008 R2 o Windows Server 2008 R2 Service Pack 1 (todas las ediciones), Windows 8.1, Windows 8 o Windows 7.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="a184309d02204286057d805a56928206" id="tgt183" class="tgtSentence">Como mínimo 1 GB de RAM.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="0f6f15494b5fabde6354d833d11f8ad4" id="tgt184" class="tgtSentence">Un mínimo de 64 GB de espacio en disco.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="387bf14f59f185bf1b10187db81a5887" id="tgt185" class="tgtSentence">Como mínimo una interfaz de red.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="606f0f7a808fd0972b0f1ed4e359c1a2" id="tgt186" class="tgtSentence">Acceso a Internet a través de un firewall (o proxy web).</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="ea4085a910b5e1a30d93625a6ffb9f22" id="tgt187" class="tgtSentence">Para instalar la herramienta de administración del conector RMS, ejecute los archivos siguientes:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="5a29c4564da1c8b825649b46aa338ef4" id="tgt188" class="tgtSentence">Para un equipo de 32 bits: RMSConnectorAdminToolSetup_x86.exe</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="7debc5e80182b4f674dfcda627c792bb" id="tgt189" class="tgtSentence">Para un equipo de 64 bits: RMSConnectorSetup.exe</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="e5fc65457f5284596b2fcbbf8887b240" id="tgt190" class="tgtSentence">Si ya ha descargado estos archivos, puede hacerlo desde el <externalLink><linkText>Centro de descarga de Microsoft</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=314106</linkUri></externalLink>.</caps:sentence>
          </para>
        </content>
      </section>
      <section address="ConfiguringServers">
        <title>
          <caps:sentence sentenceid="74f4aac82aa84ad266b8253a7bd81f84" id="tgt191" class="tgtSentence">Configuración de servidores para que usen el conector RMS</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="4f5e120cbab68e245fac99819263bd21" id="tgt192" class="tgtSentence">Después de haber instalado y configurado el conector RMS, está listo para configurar los servidores locales que utilizarán Rights Management y se conectarán a Azure RMS mediante el conector.</caps:sentence>
            <caps:sentence sentenceid="b500f1273e74b5dc1851fb98b7953408" id="tgt193" class="tgtSentence"> Esto supone configurar los siguientes servidores:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="75ab9f7302e3c0fd43bfe63aae6ed893" id="tgt194" class="tgtSentence">Para Exchange 2013: Servidores de acceso de cliente y servidores de buzones</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="f9225d260844019a9000684099b2d221" id="tgt195" class="tgtSentence">Para Exchange 2010: Servidores de acceso de cliente y servidores de transporte de concentradores</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="d579234f8b0a3b253825bc5455efef5a" id="tgt196" class="tgtSentence">Para SharePoint: Servidores web front-end de SharePoint, incluidos los que hospedan el servidor de la administración central</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="950a68f86e387e8fcf5f43b7cfbaf476" id="tgt197" class="tgtSentence">Para la infraestructura de clasificación de archivos: Equipos con Windows Server que tienen instalado el administrador de recursos de archivos</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="adcdbbeb59fae881c7bad2ca86f9685b" id="tgt198" class="tgtSentence">Esta configuración precisa parámetros de registro.</caps:sentence>
            <caps:sentence sentenceid="ca7dd50b718b601f0cff4f1c16a1d4ac" id="tgt199" class="tgtSentence"> Para hacer esto, tiene dos opciones:</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c56624f03735109b674157dbec3ee2c4" id="tgt200" class="tgtSentence">Opción de configuración</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="faee742e2b3290f02a639a53e875a4a9" id="tgt201" class="tgtSentence">Ventajas</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="eee807afe84fa8929a981009cda95720" id="tgt202" class="tgtSentence">Desventajas</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a50e60770c165f10aec7ec16c6f2d17b" id="tgt203" class="tgtSentence">Automáticamente, al usar la herramienta de configuración del servidor para el conector RMS de Microsoft</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b2f440fca4b0f4e9d5f2ccfb0e9b9f6f" id="tgt204" class="tgtSentence">Sin edición directa del registro.</caps:sentence>
                    <caps:sentence sentenceid="15edfe5b858de477a2e6df54e812b906" id="tgt205" class="tgtSentence"> Este proceso se automatiza para usted mediante un script.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="50fffd7cff719fce9b20aa0d5c662d2a" id="tgt206" class="tgtSentence">Sin necesidad de ejecutar un cmdlet de Windows PowerShell para obtener su URL de Microsoft RMS.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="1cb8a9c9852b509605bbac7684272a67" id="tgt207" class="tgtSentence">Si la ejecuta de forma local, se comprueban automáticamente los requisitos previos (pero no se solucionan de forma automática).</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6eae477a74fb6dcc19138c1c1df14eae" id="tgt208" class="tgtSentence">Cuando ejecuta la herramienta, debe realizar una conexión a un servidor que ya ejecuta el conector RMS.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b88e392ac6de32731a1af908b2386862" id="tgt209" class="tgtSentence">De forma manual, mediante la edición del registro</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4dae4c54dd8523538b9b1088d924b5c1" id="tgt210" class="tgtSentence">No se requiere conexión a un servidor que ejecute el conector RMS.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ea5dee735dc6be3a6c6dadbd062a1b93" id="tgt211" class="tgtSentence">Más sobrecargas administrativas que son propensas a errores.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="4cf59648f7c34689179b98e2b78da6f9" id="tgt212" class="tgtSentence">Debe obtener tu URL de Microsoft RMS, lo que precisa que ejecute un comando Windows PowerShell.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="ce1962c627f471b08268ec28c6abf85e" id="tgt213" class="tgtSentence">Siempre debe hacer la comprobación de todos los requisitos previos.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para></para>
          <alert class="important">
            <para>
              <caps:sentence sentenceid="ed7c3e2f3b240bb253492a68010ea038" id="tgt214" class="tgtSentence">En ambos casos, debe instalar los requisitos previos manualmente y configurar Exchange, SharePoint y la infraestructura de clasificación de archivos para utilizar Rights Management.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence sentenceid="66c5ed030691ea50ef8dc9063dd00e68" id="tgt215" class="tgtSentence">Para la mayoría de organizaciones, la configuración automática mediante la herramienta de configuración del servidor para el conector RMS de Microsoft será la mejor opción, ya que proporciona mayor eficacia y fiabilidad que la configuración manual.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="6bb95e0fe54658143777b991e5c45b8f" id="tgt216" class="tgtSentence">Después de realizar los cambios de configuración en estos servidores, debe reiniciarlos si se está ejecutando Exchange o SharePoint y los ha configurado previamente para usar AD RMS.</caps:sentence>
            <caps:sentence sentenceid="9629643a0086c00faac4a3a8817026f5" id="tgt217" class="tgtSentence"> No es necesario reiniciar estos servidores si es la primera vez que los va a configurar para Rights Management.</caps:sentence>
            <caps:sentence sentenceid="088dc00b3bb91ee0b9aa7d5a5a8933e4" id="tgt218" class="tgtSentence"> Siempre debe reiniciar el servidor de archivos configurado para utilizar la infraestructura de clasificación de archivos después de realizar estos cambios de configuración.</caps:sentence>
          </para>
          <procedure address="BKMK_HowToRunTheTool">
            <title>
              <caps:sentence sentenceid="474b37d2c4ee0a9d48d3a2eace0a33c9" id="tgt219" class="tgtSentence">Cómo usar la herramienta de configuración del servidor para el conector de Microsoft RMS</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="4cd85d335ea3adb7465f130a6c329533" id="tgt220" class="tgtSentence">Si no ha descargado ya el script para la herramienta de configuración del servidor para el conector de Microsoft RMS (GenConnectorConfig.ps1), descárguela desde el <externalLink><linkText>Centro de descarga de Microsoft</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=314106</linkUri></externalLink>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="ee565b68fa3207a84aced68cf71478cb" id="tgt221" class="tgtSentence">Guarde el archivo GenConnectorConfig.ps1 en el equipo en que ejecutará la herramienta.</caps:sentence>
                    <caps:sentence sentenceid="8fff5a18866da527b640bffa8a45179f" id="tgt222" class="tgtSentence"> Si va a ejecutar la herramienta localmente, debe ser el servidor que desea configurar para comunicarse con el conector RMS.</caps:sentence>
                    <caps:sentence sentenceid="e982fc40fbc0d125d065b97b2040d601" id="tgt223" class="tgtSentence"> De otro modo, puede guardarla en cualquier equipo.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="fe3f6190c07c4210a6d38e17685afbb1" id="tgt224" class="tgtSentence">Decida cómo ejecutar la herramienta:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="541d9ea5c06c020da2e6f7412c2a5ca5" id="tgt225" class="tgtSentence">
                          <embeddedLabel>Localmente</embeddedLabel>: Puede ejecutar la herramienta de forma interactiva, desde el servidor que se va a configurar para comunicarse con el conector RMS.</caps:sentence>
                        <caps:sentence sentenceid="c4e32d98878c1032ff4fce8b6b74f656" id="tgt226" class="tgtSentence"> Esta ejecución es útil para una configuración de uso único, como un entorno de evaluación.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="3551e53bd26b5127721e1325eba85f79" id="tgt227" class="tgtSentence">
                          <embeddedLabel>Implementación de software</embeddedLabel> Puede ejecutar la herramienta para producir archivos de registro que, a continuación, implementará en un servidor pertinente (o más) mediante una aplicación de administración de sistemas que admite la implementación de software, como un administrador de la configuración del centro de sistemas.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="5bd26da783bcef74076c48270966baf7" id="tgt228" class="tgtSentence">
                          <embeddedLabel>Directiva de grupo</embeddedLabel>: Puede ejecutar la herramienta para producir un script que le proporcione a un administrador que pueda crear objetos de directivas de grupo para los servidores que se van a configurar.</caps:sentence>
                        <caps:sentence sentenceid="15225b0d22073ce07aebf0b983350300" id="tgt229" class="tgtSentence"> Este script crea un objeto de directiva de grupo para cada tipo de servidor que se va a configurar, que el administrador pueda asignar a servidores pertinentes posteriormente.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <alert class="note">
                    <para>
                      <caps:sentence sentenceid="1e18c8657b38c3e7f1d5d1d6aa500ad2" id="tgt230" class="tgtSentence">Esta herramienta configura los servidores que se comunicarán con el conector RMS y que se enumeran al principio de esta sección.</caps:sentence>
                      <caps:sentence sentenceid="5d9ad58123246feee655ea75b7a7082a" id="tgt231" class="tgtSentence"> No ejecute esta herramienta en los servidores que ejecutan el conector RMS.</caps:sentence>
                    </para>
                  </alert>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="986a1e9cf69d28fc407425532bc33082" id="tgt232" class="tgtSentence">Inicie Windows PowerShell con la opción <ui>Ejecutar como administrador</ui> y use el comando Get-help para leer instrucciones sobre cómo usar la herramienta para el método de configuración elegido:</caps:sentence>
                  </para>
                  <code>Get-help .\GenConnectorConfig.ps1 -detailed</code>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence sentenceid="9f5cb11e117fee46e846fc7fbf2b967e" id="tgt233" class="tgtSentence">Para ejecutar el script, debe escribir la dirección URL del conector RMS para la organización.</caps:sentence>
                  <caps:sentence sentenceid="ac313f03669a05284f565868408ee90f" id="tgt234" class="tgtSentence"> Escriba el prefijo del protocolo (HTTP:// o HTTPS://) y el nombre del conector que ha definido en DNS para la dirección equilibrada de carga de su conector.</caps:sentence>
                  <caps:sentence sentenceid="b51da18abcdaf8a72d8f62df4b62b8be" id="tgt235" class="tgtSentence"> Por ejemplo, https://connector.contoso.com.</caps:sentence>
                  <caps:sentence sentenceid="a44dd3bd6b0c624f84973ad942e7b081" id="tgt236" class="tgtSentence"> Entonces la herramienta usa esa URL para poner en contacto los servidores que ejecutan el conector RMS y obtener otros parámetros que se usan para crear las configuraciones requeridas.</caps:sentence>
                </para>
                <alert class="important">
                  <para>
                    <caps:sentence sentenceid="83796ae083ea77d8b72a0748d72a9f63" id="tgt237" class="tgtSentence">Al ejecutar esta herramienta, asegúrese de especificar el nombre del conector RMS de carga equilibrada para su organización y no el nombre de un único servidor que ejecuta el servicio del conector RMS.</caps:sentence>
                  </para>
                </alert>
              </content>
            </conclusion>
          </procedure>
          <para>
            <caps:sentence sentenceid="5c008d1edcebe6c72c32bd7111662b81" id="tgt238" class="tgtSentence">Use las secciones siguientes para obtener información específica para cada tipo de servicio:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <link xlink:href="90e7e33f-9ecc-497b-89c5-09205ffc5066#BKMK_ExchangeServer">Configuring an Exchange server to use the connector</link>
              </para>
            </listItem>
            <listItem>
              <para>
                <link xlink:href="90e7e33f-9ecc-497b-89c5-09205ffc5066#BKMK_ConfiguringSharePoint">Configuring a SharePoint server to use the connector</link>
              </para>
            </listItem>
            <listItem>
              <para>
                <link xlink:href="90e7e33f-9ecc-497b-89c5-09205ffc5066#BKMK_FileServer">Configuring a file server for File Classification Infrastructure to use the connector</link>
              </para>
            </listItem>
          </list>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="2ca1797944d1696b53594317cc20252d" id="tgt239" class="tgtSentence">Después de configurar estos servidores para usar el conector, es posible que las aplicaciones cliente que se han instalado localmente en esos servidores no funcionen con RMS.</caps:sentence>
              <caps:sentence sentenceid="bf8cef0d32a59188dd405114cda550a5" id="tgt240" class="tgtSentence"> Cuando esto ocurre, se debe a que las aplicaciones tratan de usar el conector en lugar de usar RMS directamente, que no es compatible.</caps:sentence>
            </para>
            <para>
              <caps:sentence sentenceid="bbcb4953c0bcb16f2ed76e21ea8ac465" id="tgt241" class="tgtSentence">Además, si Office 2010 se instala localmente en un servidor Exchange, es posible que las características IRM de la aplicación cliente funcionen desde ese equipo después de configurar el servidor para usar el conector, pero esto no es compatible.</caps:sentence>
            </para>
            <para>
              <caps:sentence sentenceid="8ac468a4b72bc2ffff2d8e7a8d691e5d" id="tgt242" class="tgtSentence">En ambos escenarios, debe instalar las aplicaciones cliente en equipos independientes que no estén configurados para usar el conector.</caps:sentence>
              <caps:sentence sentenceid="2479c18c80624e6ebe088f2df8250317" id="tgt243" class="tgtSentence"> Entonces usarán correctamente RMS de forma directa.</caps:sentence>
            </para>
          </alert>
        </content>
        <sections>
          <section address="BKMK_ExchangeServer">
            <title>
              <caps:sentence sentenceid="6f8902761cd662d41021c9b8ae5aeca2" id="tgt244" class="tgtSentence">Configuración de un servidor Exchange para usar el conector</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="5da369a2abff2b68d2601cd47f9c7e7c" id="tgt245" class="tgtSentence">Los siguientes roles de Exchange se comunican con el conector RMS:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="2ae2efbcf3ff4a434659305e19c73bb9" id="tgt246" class="tgtSentence">Para Exchange 2013: Servidor de acceso de cliente y servidor de buzones</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="627d3c1dbcce04e2da8e179f76b665e4" id="tgt247" class="tgtSentence">Para Exchange 2010: Servidor de acceso de cliente y servidor de transporte de concentradores</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="05314a8d540a6f8eae2186bef3d6251a" id="tgt248" class="tgtSentence">Para usar el conector RMS, estos servidores con Exchange deben ejecutar una de las versiones de software siguientes:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="9fa293b4ba1a0a055d1542dc03958970" id="tgt249" class="tgtSentence">Exchange Server 2013 con la actualización acumulativa 3 de Exchange 2013</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="bc07df932ed238061e8bde54b636d371" id="tgt250" class="tgtSentence">Exchange Server 2010 con la actualización acumulativa 6 de Exchange 2010 Service Pack 3</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="0a1b926c903022e1a9ee77402097cb83" id="tgt251" class="tgtSentence">También necesitará instalar en estos servidores una versión del cliente de RMS que incluye compatibilidad con el Modo criptográfico 2 de RMS.</caps:sentence>
                <caps:sentence sentenceid="d7354911a146d254dfc5a95b545aa942" id="tgt252" class="tgtSentence"> La versión mínima compatible en Windows Server 2008 está incluida en la revisión que puede descargarse desde <externalLink><linkText>Se aumentó la longitud de la clave RSA hasta 2048 bits para AD RMS en Windows Server 2008 R2 y Windows Server 2008</linkText><linkUri>http://support.microsoft.com/kb/2627272</linkUri></externalLink>.</caps:sentence>
                <caps:sentence sentenceid="f092a8c0c7ff427b36ec960c0d5cef84" id="tgt253" class="tgtSentence"> La versión mínima para Windows Server 2008 R2 se puede descargar desde <externalLink><linkText>Se ha aumentado la longitud de la clave RSA hasta 2048 bits para AD RMS en Windows 7 o Windows Server 2008 R2</linkText><linkUri>http://support.microsoft.com/kb/2627273</linkUri></externalLink>.</caps:sentence>
                <caps:sentence sentenceid="3f2d9f3e1d7e9f51e73e65c4f9a0d210" id="tgt254" class="tgtSentence"> Windows Server 2012 y Windows Server 2012 R2 son compatibles de forma nativa con el Modo 2 criptográfico.</caps:sentence>
              </para>
              <alert class="important">
                <para>
                  <caps:sentence sentenceid="65fd65b2af65ebacf47f03d8dda514a5" id="tgt255" class="tgtSentence">Si estas versiones (o posteriores) de Exchange y del cliente RMS no están instaladas, no podrá configurar Exchange para usar el conector.</caps:sentence>
                  <caps:sentence sentenceid="6a79deab0bab16e8b1e7ce2437da8b32" id="tgt256" class="tgtSentence"> Compruebe que estas versiones están instaladas antes de continuar.</caps:sentence>
                </para>
              </alert>
              <procedure>
                <title>
                  <caps:sentence sentenceid="8b571dab8bec8ac749efaa1bd3cddad8" id="tgt257" class="tgtSentence">Para configurar los servidores Exchange para que usen el conector</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="f4dcf06a3c6c76ed81983602e69a932e" id="tgt258" class="tgtSentence">En los roles de servidor de Exchange que se comunican con el conector RMS, realice una de las acciones siguientes:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="063549edfc9dd655691728ca4f9f28e9" id="tgt259" class="tgtSentence">Ejecute la herramienta de configuración del servidor para el conector de Microsoft RMS.</caps:sentence>
                            <caps:sentence sentenceid="1070f425823a6e05a98eb2d747f0c53d" id="tgt260" class="tgtSentence"> Para obtener más información, consulte <link xlink:href="90e7e33f-9ecc-497b-89c5-09205ffc5066#BKMK_HowToRunTheTool">How to use the server configuration tool for Microsoft RMS connector</link> en este tema.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence sentenceid="8a5ed0273d0042b026cc052fe80af2b1" id="tgt261" class="tgtSentence">Por ejemplo, para ejecutar la herramienta de forma local y configurar un servidor que ejecute Exchange 2013: </caps:sentence>
                          </para>
                          <code>.\GenConnectorConfig.ps1 -ConnectorUri https://rmsconnector.contoso.com -SetExchange2013</code>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="3eb38313fcab30a4abdb15491967954c" id="tgt262" class="tgtSentence">Efectúe modificaciones en el registro de forma manual usando las tablas de las secciones siguientes para agregar manualmente configuraciones de registro en los servidores.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="b9b1843ed74ab2eab43cda358047a376" id="tgt263" class="tgtSentence">Habilita la funcionalidad IRM en Exchange.</caps:sentence>
                        <caps:sentence sentenceid="1070f425823a6e05a98eb2d747f0c53d" id="tgt264" class="tgtSentence"> Para obtener más información, consulte <externalLink><linkText>Procedimientos de Information Rights Management</linkText><linkUri>https://technet.microsoft.com/library/dd351212(v=exchg.150).aspx</linkUri></externalLink> en la biblioteca de Exchange.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
              <para>
                <caps:sentence sentenceid="524e639c5fc8e9152b93f6e835c9acd9" id="tgt265" class="tgtSentence">Use las tablas de las secciones siguientes solamente si quiere agregar o comprobar las configuraciones de registro en los servidores de forma manual, lo que configura los servidores para usar el conector RMS.</caps:sentence>
                <caps:sentence sentenceid="516b17f9c3f5d0db4a96a4e8c632613c" id="tgt266" class="tgtSentence"> Instrucciones para cuando uses estas tablas:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="53fa3f5e0f111dc66718fdc1136c3e56" id="tgt267" class="tgtSentence">
                      <placeholder>MicrosoftRMSURL</placeholder> es la URL del servicio de Microsoft RMS de tu organización.</caps:sentence>
                    <caps:sentence sentenceid="347410f9de63594a5a8baf48a20f257c" id="tgt268" class="tgtSentence"> Para encontrar este valor:</caps:sentence>
                  </para>
                  <list class="ordered">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="3a3aa7b24413b30b9af6fcd3f9f9f652" id="tgt269" class="tgtSentence">Ejecute el cmdlet <externalLink><linkText>Get-AadrmConfiguration</linkText><linkUri>http://msdn.microsoft.com/library/windowsazure/dn629410.aspx</linkUri></externalLink> para Azure RMS.</caps:sentence>
                        <caps:sentence sentenceid="392df028cf931bb6a18776d3a688dda0" id="tgt270" class="tgtSentence"> Si no ha instalado todavía el módulo Windows PowerShell para Azure RMS, consulte <link xlink:href="0d665ed6-b1de-4d63-854a-bc57c1c49844">Installing Windows PowerShell for Azure Rights Management</link>.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="ae3e3733f4fd83ce1d71232828624cb0" id="tgt271" class="tgtSentence">En la salida, identifique el valor <ui>LicensingIntranetDistributionPointUrl</ui>.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="d05370276e06291b048268558cc39bee" id="tgt272" class="tgtSentence">Por ejemplo: <ui>LicensingIntranetDistributionPointUrl   : https://5c6bb73b-1038-4eec-863d-49bded473437.rms.na.aadrm.com/_wmcs/licensing</ui></caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="329dda22837a719a5a3008628608d0cc" id="tgt273" class="tgtSentence">En el valor, quite <ui>/_wmcs/licensing</ui> de esta cadena.</caps:sentence>
                        <caps:sentence sentenceid="ea79174a667e4ce268e4422bd74aff5a" id="tgt274" class="tgtSentence"> La cadena resultante es su URL de Microsoft RMS.</caps:sentence>
                        <caps:sentence sentenceid="4ec4e88e5c682c0bd6034bfc49168c70" id="tgt275" class="tgtSentence"> En nuestro ejemplo, la URL de Microsoft RMS sería el valor siguiente:</caps:sentence>
                      </para>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="3a510940ac5f0bf0d12f8307afb8c7aa" id="tgt276" class="tgtSentence">https://5c6bb73b-1038-4eec-863d-49bded473437.rms.na.aadrm.com</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                  </list>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="040c27cf3069e277567eec1f0b7c9ab4" id="tgt277" class="tgtSentence">
                      <placeholder>ConnectorFQDN</placeholder> es el nombre de equilibrio de carga que definió en DNS para el conector.</caps:sentence>
                    <caps:sentence sentenceid="4eee3758f1bf4073d94deae936dd0a13" id="tgt278" class="tgtSentence"> Por ejemplo, <system>rmsconnector.contoso.com</system>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="ed69df32fb51528c4623b7b5da5828fa" id="tgt279" class="tgtSentence">Use el prefijo HTTPS para la URL del conector si ha configurado el conector para usar HTTPS para comunicarte con tus servidores locales.</caps:sentence>
                    <caps:sentence sentenceid="be021ab36c2c99a549fc25f5fcee238c" id="tgt280" class="tgtSentence"> Para obtener más información, consulte la sección <link xlink:href="90e7e33f-9ecc-497b-89c5-09205ffc5066#BKMK_ConfiguringHTTPS">Configuring the RMS connector to use HTTPS</link> de este tema.</caps:sentence>
                    <caps:sentence sentenceid="378cbd311a843a7701e45a31ba958471" id="tgt281" class="tgtSentence"> Las URL de Microsoft RMS usan siempre HTTPS.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
            <sections>
              <section expanded="false">
                <title>
                  <caps:sentence sentenceid="7f14ce57459fb0db4b6eada5724c32dc" id="tgt282" class="tgtSentence">Tabla para configuraciones de registro de Exchange 2013</caps:sentence>
                </title>
                <content>
                  <table>
                    <thead>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="b75ba2542571d3ceaab9c5d83c92075c" id="tgt283" class="tgtSentence">Ruta de acceso del registro</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="599dcce2998a6b40b1e38e8c6006cb0a" id="tgt284" class="tgtSentence">Tipo</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="2063c1608d6e0baf80249c42e2be5804" id="tgt285" class="tgtSentence">Valor</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="8d777f385d3dfec8815d20f7496026dc" id="tgt286" class="tgtSentence">Datos</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </thead>
                    <tbody>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="40d2921628d72e2b9fe991a68c260ea7" id="tgt287" class="tgtSentence">HKEY_LOCAL_MACHINE\Software\Microsoft\MSDRM\ServiceLocation\Activation</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="2b1bda4361069cdf7a4437824c22893c" id="tgt288" class="tgtSentence">Reg_SZ</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="c21f969b5f03d33d43e04f8f136e7682" id="tgt289" class="tgtSentence">Default</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="f8eae6750519389e078e1eb1bcb3d708" id="tgt290" class="tgtSentence">https://<placeholder>MicrosoftRMSURL/_wmcs/certification</placeholder></caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="1968469740d260461985dbaee69c890d" id="tgt291" class="tgtSentence">HKEY_LOCAL_MACHINE\Software\Microsoft\MSDRM\ServiceLocation\EnterprisePublishing</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="2b1bda4361069cdf7a4437824c22893c" id="tgt292" class="tgtSentence">Reg_SZ</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="c21f969b5f03d33d43e04f8f136e7682" id="tgt293" class="tgtSentence">Default</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="a08eea8e5273aedda6feb796d49d643b" id="tgt294" class="tgtSentence">https://MicrosoftRMSURL/_wmcs/Licensing</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="b422ee7b9c081ec95e5c95d5a9e6f2dc" id="tgt295" class="tgtSentence">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\ExchangeServer\v15\IRM\CertificationServerRedirection</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="2b1bda4361069cdf7a4437824c22893c" id="tgt296" class="tgtSentence">Reg_SZ</caps:sentence>
                          </para>
                          <para></para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="f8eae6750519389e078e1eb1bcb3d708" id="tgt297" class="tgtSentence">https://<placeholder>MicrosoftRMSURL</placeholder></caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="5e9f115816f9a71685775cd8d7bf469f" id="tgt298" class="tgtSentence">Una de las siguientes, en función de si usas HTTP o HTTPS desde tu servidor Exchange al conector RMS:</caps:sentence>
                          </para>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="dbd7790bcd23fde7607101ef6a633779" id="tgt299" class="tgtSentence">http://<placeholder>ConnectorFQDN</placeholder></caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="f8eae6750519389e078e1eb1bcb3d708" id="tgt300" class="tgtSentence">https://<placeholder>ConnectorFQDN</placeholder></caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="8d386fa8e79b481db738381489bcf29b" id="tgt301" class="tgtSentence">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\ExchangeServer\v15\IRM\LicenseServerRedirection</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="2b1bda4361069cdf7a4437824c22893c" id="tgt302" class="tgtSentence">Reg_SZ</caps:sentence>
                          </para>
                          <para></para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="f8eae6750519389e078e1eb1bcb3d708" id="tgt303" class="tgtSentence">https://<placeholder>MicrosoftRMSURL</placeholder></caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="5e9f115816f9a71685775cd8d7bf469f" id="tgt304" class="tgtSentence">Una de las siguientes, en función de si usas HTTP o HTTPS desde tu servidor Exchange al conector RMS:</caps:sentence>
                          </para>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="dbd7790bcd23fde7607101ef6a633779" id="tgt305" class="tgtSentence">http://<placeholder>ConnectorFQDN</placeholder></caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="f8eae6750519389e078e1eb1bcb3d708" id="tgt306" class="tgtSentence">https://<placeholder>ConnectorFQDN</placeholder></caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                    </tbody>
                  </table>
                </content>
              </section>
              <section expanded="false">
                <title>
                  <caps:sentence sentenceid="a5476942e0ac240a59f25d5be535b72d" id="tgt307" class="tgtSentence">Tabla para configuraciones del Registro de Exchange 2010</caps:sentence>
                </title>
                <content>
                  <table>
                    <thead>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="b75ba2542571d3ceaab9c5d83c92075c" id="tgt308" class="tgtSentence">Ruta de acceso del registro</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="599dcce2998a6b40b1e38e8c6006cb0a" id="tgt309" class="tgtSentence">Tipo</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="2063c1608d6e0baf80249c42e2be5804" id="tgt310" class="tgtSentence">Valor</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="8d777f385d3dfec8815d20f7496026dc" id="tgt311" class="tgtSentence">Datos</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </thead>
                    <tbody>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="40d2921628d72e2b9fe991a68c260ea7" id="tgt312" class="tgtSentence">HKEY_LOCAL_MACHINE\Software\Microsoft\MSDRM\ServiceLocation\Activation</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="2b1bda4361069cdf7a4437824c22893c" id="tgt313" class="tgtSentence">Reg_SZ</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="c21f969b5f03d33d43e04f8f136e7682" id="tgt314" class="tgtSentence">Default</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="f8eae6750519389e078e1eb1bcb3d708" id="tgt315" class="tgtSentence">https://<placeholder>MicrosoftRMSURL</placeholder>/_wmcs/certification</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="1968469740d260461985dbaee69c890d" id="tgt316" class="tgtSentence">HKEY_LOCAL_MACHINE\Software\Microsoft\MSDRM\ServiceLocation\EnterprisePublishing</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="2b1bda4361069cdf7a4437824c22893c" id="tgt317" class="tgtSentence">Reg_SZ</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="c21f969b5f03d33d43e04f8f136e7682" id="tgt318" class="tgtSentence">Default</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="f8eae6750519389e078e1eb1bcb3d708" id="tgt319" class="tgtSentence">https://<placeholder>MicrosoftRMSURL</placeholder>/_wmcs/Licensing</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="f79261c614e5a42a2b495720d2e71d27" id="tgt320" class="tgtSentence">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\ExchangeServer\v14\IRM\CertificationServerRedirection</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="2b1bda4361069cdf7a4437824c22893c" id="tgt321" class="tgtSentence">Reg_SZ</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="f8eae6750519389e078e1eb1bcb3d708" id="tgt322" class="tgtSentence">https://<placeholder>MicrosoftRMSURL</placeholder></caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="5e9f115816f9a71685775cd8d7bf469f" id="tgt323" class="tgtSentence">Una de las siguientes, en función de si usas HTTP o HTTPS desde tu servidor Exchange al conector RMS:</caps:sentence>
                          </para>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="dbd7790bcd23fde7607101ef6a633779" id="tgt324" class="tgtSentence">http://<placeholder>ConnectorFQDN</placeholder></caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="f8eae6750519389e078e1eb1bcb3d708" id="tgt325" class="tgtSentence">https://<placeholder>ConnectorFQDN</placeholder></caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="9ef008b28f9abb5f0c22fcbe9cf20585" id="tgt326" class="tgtSentence">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\ExchangeServer\v14\IRM\LicenseServerRedirection</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="2b1bda4361069cdf7a4437824c22893c" id="tgt327" class="tgtSentence">Reg_SZ</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="f8eae6750519389e078e1eb1bcb3d708" id="tgt328" class="tgtSentence">https://<placeholder>MicrosoftRMSURL</placeholder></caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="5e9f115816f9a71685775cd8d7bf469f" id="tgt329" class="tgtSentence">Una de las siguientes, en función de si usas HTTP o HTTPS desde tu servidor Exchange al conector RMS:</caps:sentence>
                          </para>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="dbd7790bcd23fde7607101ef6a633779" id="tgt330" class="tgtSentence">http://<placeholder>ConnectorFQDN</placeholder></caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="f8eae6750519389e078e1eb1bcb3d708" id="tgt331" class="tgtSentence">https://<placeholder>ConnectorFQDN</placeholder></caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                    </tbody>
                  </table>
                </content>
              </section>
            </sections>
          </section>
          <section address="BKMK_ConfiguringSharePoint">
            <title>
              <caps:sentence sentenceid="cc0d9be880f5ebbe982fd3ac32404743" id="tgt332" class="tgtSentence">Configuración de un servidor SharePoint para usar el conector</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="cea9638235b316274203c972b038fab5" id="tgt333" class="tgtSentence">Los siguientes roles de SharePoint se comunican con el conector RMS:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="d6c3aca227e10a02fc3d1aa88a01e6a9" id="tgt334" class="tgtSentence">Servidores web front-end de SharePoint, incluidos los que hospedan el servidor de la administración central</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="cb8a5db9648789f4fb37fda863c033c5" id="tgt335" class="tgtSentence">Para usar el conector RMS, estos servidores con SharePoint deben ejecutar una de las versiones de software siguientes:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="b279dfbc63630c1d69db32965313e462" id="tgt336" class="tgtSentence">SharePoint Server 2013</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="963b0beeac78c2c2122cf389c55f7ec1" id="tgt337" class="tgtSentence">SharePoint Server 2010</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="a9e013ed7de6efef4e3d102904a5e4e0" id="tgt338" class="tgtSentence">Un servidor SharePoint 2013 también debe ejecutar una versión del cliente MSIPC 2.1, que abarca de 1.0.622.34 a 1.0.10907.0.</caps:sentence>
              </para>
              <alert class="warning">
                <para>
                  <caps:sentence sentenceid="25ae79362814d278ed6f5cbdcccbac69" id="tgt339" class="tgtSentence">Hay múltiples versiones del cliente MSIPC 2.1, de modo que asegúrese de instalar una versión que mencionamos en este artículo.</caps:sentence> </para>
                <para>
                  <caps:sentence sentenceid="f411832ad3a1f54800f1242c6e8dcb8e" id="tgt340" class="tgtSentence">Puede verificar la versión del cliente comprobando el número de la versión de MSIPC.dll, que está ubicada en <system>\Program Files\Active Directory Rights Management Services Client 2.1</system>.</caps:sentence>
                  <caps:sentence sentenceid="87e687dd6042ff2e467b47091a1a1d53" id="tgt341" class="tgtSentence"> El cuadro de diálogo Propiedades muestra el número de la versión del cliente MSIPC 2.1.</caps:sentence>
                </para>
              </alert>
              <para>
                <caps:sentence sentenceid="8b7e3605c6f2fb41922db9309700ff18" id="tgt342" class="tgtSentence">Estos servidores que ejecutan SharePoint 2010 deben tener instalada una versión del cliente MSDRM que sea compatible con el Modo criptográfico 2 de RMS.</caps:sentence>
                <caps:sentence sentenceid="d7354911a146d254dfc5a95b545aa942" id="tgt343" class="tgtSentence"> La versión mínima compatible para Windows Server 2008 está incluida en la revisión que puedes descargar desde <externalLink><linkText>Se aumentó la longitud de la clave RSA hasta 2048 bits para AD RMS en Windows Server 2008 R2 y en Windows Server 2008</linkText><linkUri>http://support.microsoft.com/kb/2627272</linkUri></externalLink>, y la versión mínima para Windows Server 2008 R2 se puede descargar desde <externalLink><linkText>Se aumentó la longitud de la clave RSA hasta 2048 bits para AD RMS en Windows 7 o en Windows Server 2008 R2</linkText><linkUri>http://support.microsoft.com/kb/2627273</linkUri></externalLink>.</caps:sentence>
                <caps:sentence sentenceid="ca0e04e3a450fd1994299cee720d7cfb" id="tgt344" class="tgtSentence"> Windows Server 2012 y Windows Server 2012 R2 son compatibles de forma nativa con el Modo criptográfico 2.</caps:sentence>
              </para>
              <procedure>
                <title>
                  <caps:sentence sentenceid="d6a6383b8a793c65494de2da699d3d6e" id="tgt345" class="tgtSentence">Para configurar servidores SharePoint para que usen el conector</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="a9fcd74e91355864b4f13b22ef032165" id="tgt346" class="tgtSentence">En los servidores de SharePoint que se comunican con el conector RMS, realice una de las acciones siguientes:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="063549edfc9dd655691728ca4f9f28e9" id="tgt347" class="tgtSentence">Ejecute la herramienta de configuración del servidor para el conector de Microsoft RMS.</caps:sentence>
                            <caps:sentence sentenceid="1070f425823a6e05a98eb2d747f0c53d" id="tgt348" class="tgtSentence"> Para obtener más información, consulte <link xlink:href="90e7e33f-9ecc-497b-89c5-09205ffc5066#BKMK_HowToRunTheTool">How to use the server configuration tool for Microsoft RMS connector</link> en este tema.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence sentenceid="024cff3c470c7498cb937bce12c87d1d" id="tgt349" class="tgtSentence">Por ejemplo, para ejecutar la herramienta de forma local y configurar un servidor que ejecute SharePoint 2013: </caps:sentence>
                          </para>
                          <code>.\GenConnectorConfig.ps1 -ConnectorUri https://rmsconnector.contoso.com -SetSharePoint2013</code>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="3704a9924c4759d4255e5f4dff866022" id="tgt350" class="tgtSentence">Si usa SharePoint 2013, efectúe modificaciones en el registro de forma manual usando la tabla de la sección siguiente para agregar manualmente configuraciones de registro en los servidores.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="0b0b9fde661d43480a1c57bc0412e139" id="tgt351" class="tgtSentence">Habilite IRM en SharePoint.</caps:sentence>
                        <caps:sentence sentenceid="1070f425823a6e05a98eb2d747f0c53d" id="tgt352" class="tgtSentence"> Para obtener más información, lea <externalLink><linkText>Configurar Information Rights Management (SharePoint Server 2010)</linkText><linkUri>https://technet.microsoft.com/library/hh545607(v=office.14).aspx</linkUri></externalLink> en la biblioteca de SharePoint.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="76fb7604be6ef8a21950f3c84fd52bb2" id="tgt353" class="tgtSentence">Cuando siga estas instrucciones, debe configurar SharePoint para usar el conector especificando <ui>Usar este servidor RMS</ui> y, a continuación, escriba la dirección URL del conector de equilibrio de carga que ha configurado.</caps:sentence>
                        <caps:sentence sentenceid="ac313f03669a05284f565868408ee90f" id="tgt354" class="tgtSentence"> Escriba el prefijo del protocolo (HTTP:// o HTTPS://) y el nombre del conector que ha definido en DNS para la dirección equilibrada de carga de su conector.</caps:sentence>
                        <caps:sentence sentenceid="a7d443ddbdbaf838a2631c13130b3d4a" id="tgt355" class="tgtSentence"> Por ejemplo, si el nombre del conector es https://connector.contoso.com, la configuración se parecerá a la imagen siguiente:</caps:sentence>
                      </para>
                      <para>
                        <mediaLinkInline>
                          <image xlink:href="82377fdd-0c4b-4c2a-8c52-4d19e19f2cda"></image>
                        </mediaLinkInline>
                      </para>
                      <para>
                        <caps:sentence sentenceid="938938a19c5a5a838bd3e6be2afc0180" id="tgt356" class="tgtSentence">Después de habilitar IRM en una granja de SharePoint, puede habilitar IRM en bibliotecas individuales mediante la opción <ui>Information Rights Management</ui> en la página <ui>Configuración de la biblioteca</ui> para cada una de ellas.</caps:sentence>
                      </para>
                      <alert class="important">
                        <para>
                          <caps:sentence sentenceid="6e0770cc88b0a99bf07a6f875450ae20" id="tgt357" class="tgtSentence">Para que SharePoint acceda a RMS mediante el conector, debe autorizar las cuentas correspondientes en la herramienta de administración del conector RMS.</caps:sentence>
                          <caps:sentence sentenceid="388659ba0d628f64135b93d94856d5e7" id="tgt358" class="tgtSentence"> Si no ha hecho esto todavía, consulte <link xlink:href="90e7e33f-9ecc-497b-89c5-09205ffc5066#AuthorizingServers">Authorizing servers to use the RMS connector</link> en este tema.</caps:sentence>
                        </para>
                      </alert>
                    </content>
                  </step>
                </steps>
              </procedure>
              <para>
                <caps:sentence sentenceid="915fd880a282872dd1e24a7f995bce88" id="tgt359" class="tgtSentence">Use la tabla de la sección siguiente solamente si quiere agregar o comprobar las configuraciones del registro de forma manual en un servidor que ejecute SharePoint 2013.</caps:sentence>
              </para>
            </content>
            <sections>
              <section expanded="false">
                <title>
                  <caps:sentence sentenceid="a1105de718ad7416b50ad14db063cc9d" id="tgt360" class="tgtSentence">Tabla para configuraciones de registro de SharePoint 2013</caps:sentence>
                </title>
                <content>
                  <para>
                    <caps:sentence sentenceid="914b52489db7031497ab4b2c5cf60a6e" id="tgt361" class="tgtSentence">Instrucciones para cuando use esta tabla:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="53fa3f5e0f111dc66718fdc1136c3e56" id="tgt362" class="tgtSentence">
                          <placeholder>MicrosoftRMSURL</placeholder> es la URL del servicio de Microsoft RMS de tu organización.</caps:sentence>
                        <caps:sentence sentenceid="347410f9de63594a5a8baf48a20f257c" id="tgt363" class="tgtSentence"> Para encontrar este valor:</caps:sentence>
                      </para>
                      <list class="ordered">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="3a3aa7b24413b30b9af6fcd3f9f9f652" id="tgt364" class="tgtSentence">Ejecute el cmdlet <externalLink><linkText>Get-AadrmConfiguration</linkText><linkUri>http://msdn.microsoft.com/library/windowsazure/dn629410.aspx</linkUri></externalLink> para Azure RMS.</caps:sentence>
                            <caps:sentence sentenceid="392df028cf931bb6a18776d3a688dda0" id="tgt365" class="tgtSentence"> Si no ha instalado todavía el módulo Windows PowerShell para Azure RMS, consulte <link xlink:href="0d665ed6-b1de-4d63-854a-bc57c1c49844">Installing Windows PowerShell for Azure Rights Management</link>.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="ae3e3733f4fd83ce1d71232828624cb0" id="tgt366" class="tgtSentence">En la salida, identifique el valor <ui>LicensingIntranetDistributionPointUrl</ui>.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence sentenceid="d05370276e06291b048268558cc39bee" id="tgt367" class="tgtSentence">Por ejemplo: <ui>LicensingIntranetDistributionPointUrl   : https://5c6bb73b-1038-4eec-863d-49bded473437.rms.na.aadrm.com/_wmcs/licensing</ui></caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="329dda22837a719a5a3008628608d0cc" id="tgt368" class="tgtSentence">En el valor, quite <ui>/_wmcs/licensing</ui> de esta cadena.</caps:sentence>
                            <caps:sentence sentenceid="ea79174a667e4ce268e4422bd74aff5a" id="tgt369" class="tgtSentence"> La cadena resultante es su URL de Microsoft RMS.</caps:sentence>
                            <caps:sentence sentenceid="4ec4e88e5c682c0bd6034bfc49168c70" id="tgt370" class="tgtSentence"> En nuestro ejemplo, la URL de Microsoft RMS sería el valor siguiente:</caps:sentence>
                          </para>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="3a510940ac5f0bf0d12f8307afb8c7aa" id="tgt371" class="tgtSentence">https://5c6bb73b-1038-4eec-863d-49bded473437.rms.na.aadrm.com</caps:sentence>
                            </ui>
                          </para>
                        </listItem>
                      </list>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="040c27cf3069e277567eec1f0b7c9ab4" id="tgt372" class="tgtSentence">
                          <placeholder>ConnectorFQDN</placeholder> es el nombre de equilibrio de carga que definió en DNS para el conector.</caps:sentence>
                        <caps:sentence sentenceid="4eee3758f1bf4073d94deae936dd0a13" id="tgt373" class="tgtSentence"> Por ejemplo, <system>rmsconnector.contoso.com</system>.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="ed69df32fb51528c4623b7b5da5828fa" id="tgt374" class="tgtSentence">Use el prefijo HTTPS para la URL del conector si ha configurado el conector para usar HTTPS para comunicarte con tus servidores locales.</caps:sentence>
                        <caps:sentence sentenceid="be021ab36c2c99a549fc25f5fcee238c" id="tgt375" class="tgtSentence"> Para obtener más información, consulte la sección <link xlink:href="90e7e33f-9ecc-497b-89c5-09205ffc5066#BKMK_ConfiguringHTTPS">Configuring the RMS connector to use HTTPS</link> de este tema.</caps:sentence>
                        <caps:sentence sentenceid="378cbd311a843a7701e45a31ba958471" id="tgt376" class="tgtSentence"> Las URL de Microsoft RMS usan siempre HTTPS.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <table>
                    <thead>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="32dc846aee8a4677c0e887c786acaa73" id="tgt377" class="tgtSentence">Ruta de acceso del registro </caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="599dcce2998a6b40b1e38e8c6006cb0a" id="tgt378" class="tgtSentence">Tipo</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="2063c1608d6e0baf80249c42e2be5804" id="tgt379" class="tgtSentence">Valor</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="8d777f385d3dfec8815d20f7496026dc" id="tgt380" class="tgtSentence">Datos</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </thead>
                    <tbody>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="a44f68e8dc7b33eda05152583ca8308f" id="tgt381" class="tgtSentence">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MSIPC\ServiceLocation\LicensingRedirection</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="2b1bda4361069cdf7a4437824c22893c" id="tgt382" class="tgtSentence">Reg_SZ</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="f8eae6750519389e078e1eb1bcb3d708" id="tgt383" class="tgtSentence">https://<placeholder>MicrosoftRMSURL</placeholder>/_wmcs/licensing</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="d96648669089faf8782c0fec974c48ad" id="tgt384" class="tgtSentence">Una de las siguientes, en función de si usa HTTP o HTTPS desde su servidor SharePoint al conector RMS:</caps:sentence>
                          </para>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="dbd7790bcd23fde7607101ef6a633779" id="tgt385" class="tgtSentence">http://<placeholder>ConnectorFQDN</placeholder>/_wmcs/licensing</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="f8eae6750519389e078e1eb1bcb3d708" id="tgt386" class="tgtSentence">https://<placeholder>ConnectorFQDN</placeholder>/_wmcs/licensing</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="cfdaee60a3037aee34d42b496f4e4488" id="tgt387" class="tgtSentence">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MSIPC\ServiceLocation\EnterpriseCertification</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="2b1bda4361069cdf7a4437824c22893c" id="tgt388" class="tgtSentence">Reg_SZ</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="c21f969b5f03d33d43e04f8f136e7682" id="tgt389" class="tgtSentence">Default</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="d96648669089faf8782c0fec974c48ad" id="tgt390" class="tgtSentence">Una de las siguientes, en función de si usa HTTP o HTTPS desde su servidor SharePoint al conector RMS:</caps:sentence>
                          </para>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="dbd7790bcd23fde7607101ef6a633779" id="tgt391" class="tgtSentence">http://<placeholder>ConnectorFQDN</placeholder>/_wmcs/certification</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="f8eae6750519389e078e1eb1bcb3d708" id="tgt392" class="tgtSentence">https://<placeholder>ConnectorFQDN</placeholder>/_wmcs/certification</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="06d797cfd9dc4c2730156b866a454d0f" id="tgt393" class="tgtSentence">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MSIPC\ServiceLocation\EnterprisePublishing</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="2b1bda4361069cdf7a4437824c22893c" id="tgt394" class="tgtSentence">Reg_SZ</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="c21f969b5f03d33d43e04f8f136e7682" id="tgt395" class="tgtSentence">Default</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="d96648669089faf8782c0fec974c48ad" id="tgt396" class="tgtSentence">Una de las siguientes, en función de si usa HTTP o HTTPS desde su servidor SharePoint al conector RMS:</caps:sentence>
                          </para>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="dbd7790bcd23fde7607101ef6a633779" id="tgt397" class="tgtSentence">http://<placeholder>ConnectorFQDN</placeholder>/_wmcs/licensing</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="f8eae6750519389e078e1eb1bcb3d708" id="tgt398" class="tgtSentence">https://<placeholder>ConnectorFQDN</placeholder>/_wmcs/licensing</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                    </tbody>
                  </table>
                </content>
              </section>
            </sections>
          </section>
          <section address="BKMK_FileServer">
            <title>
              <caps:sentence sentenceid="da15d1a07d45de43331d9a9b899aeba1" id="tgt399" class="tgtSentence">Configuración de un servidor de archivos para que la Infraestructura de clasificación de archivos use el conector</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="73f163f0548a4e4810890ff693d22a30" id="tgt400" class="tgtSentence">Para usar el conector RMS y la Infraestructura de la clasificación de archivos para proteger documentos de Office, el servidor de archivos debe ejecutar uno de los sistemas operativos siguientes:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="dcfe8446422dcac28d99767b484594f0" id="tgt401" class="tgtSentence">Windows Server 2012 R2</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="0e22230e53d6559d213afe9ce343ebf5" id="tgt402" class="tgtSentence">Windows Server 2012</caps:sentence>
                  </para>
                </listItem>
              </list>
              <procedure>
                <title>
                  <caps:sentence sentenceid="366dcca03e45a4f70f1def3ecb1aa0e0" id="tgt403" class="tgtSentence">Para configurar servidores de archivo para que usen el conector</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="3fe6334b98b13756f6ce7dcdb25927ff" id="tgt404" class="tgtSentence">En los servidores de archivos configurados para la infraestructura de clasificación de archivos y que se comunicarán con el conector RMS, realice una de las acciones siguientes:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="063549edfc9dd655691728ca4f9f28e9" id="tgt405" class="tgtSentence">Ejecute la herramienta de configuración del servidor para el conector de Microsoft RMS.</caps:sentence>
                            <caps:sentence sentenceid="1070f425823a6e05a98eb2d747f0c53d" id="tgt406" class="tgtSentence"> Para obtener más información, consulte <link xlink:href="90e7e33f-9ecc-497b-89c5-09205ffc5066#BKMK_HowToRunTheTool">How to use the server configuration tool for Microsoft RMS connector</link> en este tema.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence sentenceid="228fd625c9dc383aca7012be0be433de" id="tgt407" class="tgtSentence">Por ejemplo, para ejecutar la herramienta de forma local y configurar un servidor de archivos que ejecute FCI: </caps:sentence>
                          </para>
                          <code>.\GenConnectorConfig.ps1 -ConnectorUri https://rmsconnector.contoso.com -SetFCI2012</code>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="71bc7c940032c6a7815b73d7b8635478" id="tgt408" class="tgtSentence">Efectúe modificaciones en el registro de forma manual usando la tabla de la sección siguiente para agregar manualmente configuraciones de registro en los servidores.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="99100e6b2e2f49c27506c24706afc879" id="tgt409" class="tgtSentence">Cree reglas de clasificación y tareas de administración de archivos para proteger los documentos con el cifrado de RMS y, a continuación, especifique una plantilla de RMS para aplicar automáticamente las directivas de RMS.</caps:sentence>
                        <caps:sentence sentenceid="1070f425823a6e05a98eb2d747f0c53d" id="tgt410" class="tgtSentence"> Para obtener más información, consulte <externalLink><linkText>Información general sobre el Administrador de recursos del servidor de archivos</linkText><linkUri>http://technet.microsoft.com/library/hh831701.aspx</linkUri></externalLink> en la biblioteca de documentación de Windows Server.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
              <para>
                <caps:sentence sentenceid="2b424857701920ac87ca46c7eb00c755" id="tgt411" class="tgtSentence">Use la tabla de la sección siguiente solamente si quiere agregar o comprobar las configuraciones del registro de forma manual en un servidor de archivo que use la Infraestructura de la clasificación de archivos para proteger documentos.</caps:sentence>
              </para>
            </content>
            <sections>
              <section expanded="false">
                <title>
                  <caps:sentence sentenceid="d65f30f583b3a9fe88786da1197d0010" id="tgt412" class="tgtSentence">Tabla para configuración de registros del servidor de archivos y de la Infraestructura de la clasificación de archivos</caps:sentence>
                </title>
                <content>
                  <para>
                    <caps:sentence sentenceid="914b52489db7031497ab4b2c5cf60a6e" id="tgt413" class="tgtSentence">Instrucciones para cuando use esta tabla:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="040c27cf3069e277567eec1f0b7c9ab4" id="tgt414" class="tgtSentence">
                          <placeholder>ConnectorFQDN</placeholder> es el nombre de equilibrio de carga que definió en DNS para el conector.</caps:sentence>
                        <caps:sentence sentenceid="4eee3758f1bf4073d94deae936dd0a13" id="tgt415" class="tgtSentence"> Por ejemplo, <system>rmsconnector.contoso.com</system>.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="ed69df32fb51528c4623b7b5da5828fa" id="tgt416" class="tgtSentence">Use el prefijo HTTPS para la URL del conector si ha configurado el conector para usar HTTPS para comunicarte con tus servidores locales.</caps:sentence>
                        <caps:sentence sentenceid="be021ab36c2c99a549fc25f5fcee238c" id="tgt417" class="tgtSentence"> Para obtener más información, consulte la sección <link xlink:href="90e7e33f-9ecc-497b-89c5-09205ffc5066#BKMK_ConfiguringHTTPS">Configuring the RMS connector to use HTTPS</link> de este tema.</caps:sentence>
                        <caps:sentence sentenceid="378cbd311a843a7701e45a31ba958471" id="tgt418" class="tgtSentence"> Las URL de Microsoft RMS usan siempre HTTPS.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <table>
                    <thead>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="32dc846aee8a4677c0e887c786acaa73" id="tgt419" class="tgtSentence">Ruta de acceso del registro </caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="599dcce2998a6b40b1e38e8c6006cb0a" id="tgt420" class="tgtSentence">Tipo</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="2063c1608d6e0baf80249c42e2be5804" id="tgt421" class="tgtSentence">Valor</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="8d777f385d3dfec8815d20f7496026dc" id="tgt422" class="tgtSentence">Datos</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </thead>
                    <tbody>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="1968469740d260461985dbaee69c890d" id="tgt423" class="tgtSentence">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MSDRM\ServiceLocation\EnterprisePublishing</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="2b1bda4361069cdf7a4437824c22893c" id="tgt424" class="tgtSentence">Reg_SZ</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="c21f969b5f03d33d43e04f8f136e7682" id="tgt425" class="tgtSentence">Default</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="dbd7790bcd23fde7607101ef6a633779" id="tgt426" class="tgtSentence">http://<placeholder>ConnectorFQDN</placeholder>/_wmcs/licensing</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="40d2921628d72e2b9fe991a68c260ea7" id="tgt427" class="tgtSentence">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MSDRM\ServiceLocation\Activation</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="2b1bda4361069cdf7a4437824c22893c" id="tgt428" class="tgtSentence">Reg_SZ</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="c21f969b5f03d33d43e04f8f136e7682" id="tgt429" class="tgtSentence">Default</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="dbd7790bcd23fde7607101ef6a633779" id="tgt430" class="tgtSentence">http://<placeholder>ConnectorFQDN</placeholder>/_wmcs/certification</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </tbody>
                  </table>
                </content>
              </section>
            </sections>
          </section>
        </sections>
      </section>
      <section address="BKMK_NextSteps">
        <title>
          <caps:sentence sentenceid="0a4f90ce90fc062c4fc00532513d86da" id="tgt431" class="tgtSentence">Pasos siguientes</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="15fcfe7bdbf319a4b1f75c148e3600f6" id="tgt432" class="tgtSentence">Ahora que ya está instalado y configurado el conector RMS, y sus servidores están configurados para usarlo, los administradores informáticos y los usuarios pueden proteger y consumir mensajes de correo electrónico y documentos mediante Azure RMS.</caps:sentence>
            <caps:sentence sentenceid="a405b0dc575d6a6e91ea3726dd0f118a" id="tgt433" class="tgtSentence"> Para facilitar este proceso a los usuarios, implemente la aplicación de uso compartido RMS, que instala un complemento para Office y agrega nuevas opciones de menú contextual al Explorador de archivos.</caps:sentence>
            <caps:sentence sentenceid="be021ab36c2c99a549fc25f5fcee238c" id="tgt434" class="tgtSentence"> Para más información, consulte la <externalLink><linkText>Guía de administrador de la aplicación Rights Management sharing</linkText><linkUri>http://technet.microsoft.com/library/ dn339003(v=ws.10).aspx</linkUri></externalLink>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="77f07411e6aa714057e408622313919f" id="tgt435" class="tgtSentence">Además, debería considerar los siguientes aspectos para facilitar la supervisión del conector RMS y de cómo se usa Azure RMS en la organización:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="742217359badf83e7eccf3d924afcdc2" id="tgt436" class="tgtSentence">Los contadores de rendimiento integrados del <ui>conector Microsoft Rights Management</ui>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="e3eb16afdbabab150c5da0ade825a14d" id="tgt437" class="tgtSentence">La <externalLink><linkText>herramienta RMS Analyzer</linkText><linkUri>https://www.microsoft.com/en-us/download/details.aspx?id=46437</linkUri></externalLink>, con la opción del conector RMS para ayudarle a supervisar el estado del conector y a identificar cualquier problema de configuración.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <link xlink:href="a735f3f7-6eb2-4901-9084-8c3cd3a9087e">Log and analyze rights management usage</link>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="796a75db26fb2b5ed1340e1b901fe1fd" id="tgt438" class="tgtSentence">Puede consultar <link xlink:href="086600c2-c5d8-47ec-a4c0-c782e1797486">Azure Rights Management Deployment Roadmap</link> para comprobar si hay otros pasos de configuración que puedan ser necesarios antes de revertir <token>aad_rightsmanagement_1</token> a usuarios y administradores.</caps:sentence>
            <caps:sentence sentenceid="30abe7ab952a58bd862c49f0e10fca5b" id="tgt439" class="tgtSentence"> Si no es necesario ningún otro paso de configuración, consulte <link xlink:href="18564e4a-9364-4ed2-8f17-89d24fc0d878">Using Azure Rights Management</link> para obtener instrucciones operativas para apoyar una implementación correcta en su organización.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="206a0bfe-0912-4e0e-aa15-484b000b264c">Configuring rights management</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Use this information to learn about the Microsoft Rights Management (RMS) connector and how you can use it to provide information protection with existing on-premises deployments that use Microsoft Exchange Server, Microsoft SharePoint Server, or file servers that run Windows Server and use the File Classification Infrastructure (FCI) capability of File Server Resource Manager.</caps:sentence>
        </para>
        <alert class="tip">
          <para>
            <caps:sentence id="src2" class="srcSentence">For a high-level example scenario with screenshots, see the <link xlink:href="aeeebcd7-6646-4405-addf-ee1cc74df5df#BKMK_Example_FCI">Automatically protecting files on file servers running Windows Server and File Classification Infrastructure</link> section in the <link xlink:href="aeeebcd7-6646-4405-addf-ee1cc74df5df">What is Azure Rights Management?</link> topic.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <section address="OverviewConnector">
        <title>
          <caps:sentence id="src3" class="srcSentence">Overview of the Microsoft Rights Management connector</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src4" class="srcSentence">The Microsoft Rights Management (RMS) connector lets you quickly enable existing on-premises servers to use their Information Rights Management (IRM) functionality with the cloud-based Microsoft Rights Management service (Azure RMS).</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> With this functionality, IT and users can easily protect documents and pictures both inside your organization and outside, without having to install additional infrastructure or establish trust relationships with other organizations.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> You can use this connector even if some of your users are connecting to online services, in a hybrid scenario.</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> For example, some users' mailboxes use Exchange Online and some users' mailboxes use Exchange Server.</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> After you install the RMS connector, all users can protect and consume emails and attachments by using Azure RMS, and information protection works seamlessly between the two deployment configurations.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src9" class="srcSentence">The RMS connector is a small-footprint service that you install on-premises, on servers that run Windows Server 2012 R2, Windows Server 2012, or Windows Server 2008 R2.</caps:sentence>
            <caps:sentence id="src10" class="srcSentence"> In addition to running the connector on physical computers, you can also run it on virtual machines, including Azure IaaS VMs.</caps:sentence>
            <caps:sentence id="src11" class="srcSentence"> After you install and configure the connector, it acts as a communications interface (a relay) between the on-premises servers and the cloud service.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src12" class="srcSentence">If you manage your own tenant key for Azure RMS (the bring you own key, or BYOK scenario), the RMS connector and the on-premises servers that use it do not access the hardware security module (HSM) that contains your tenant key.</caps:sentence>
            <caps:sentence id="src13" class="srcSentence"> This is because all cryptographic operations that use the tenant key are performed in Azure RMS, and not on-premises.</caps:sentence>
          </para>
          <mediaLink>
            <image xlink:href="fca243be-b886-43ad-91e6-6900f7e2cd85"></image>
          </mediaLink>
          <para></para>
          <para></para>
          <para>
            <caps:sentence id="src14" class="srcSentence">The RMS connector supports the following on-premises servers: Exchange Server, SharePoint Server, and file servers that run Windows Server and use File Classification Infrastructure to classify and apply policies to Office documents in a folder.</caps:sentence>
            <caps:sentence id="src15" class="srcSentence"> If you want to protect all files types using File Classification, do not use the RMS connector, but instead, use the <externalLink><linkText>RMS Protection cmdlets</linkText><linkUri>https://msdn.microsoft.com/library/azure/mt433195.aspx</linkUri></externalLink>.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src16" class="srcSentence">For supported versions of these on-premises servers, see “On-premises servers that support Azure RMS” in the <link xlink:href="dc78321d-d759-4653-8818-80da74b6cdeb#BKMK_SupportedApplications">Applications that support Azure RMS</link> section of the <link xlink:href="dc78321d-d759-4653-8818-80da74b6cdeb">Requirements for Azure Rights Management</link> topic.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence id="src17" class="srcSentence">Use the following sections to help you plan for, install, and configure the RMS connector.</caps:sentence>
            <caps:sentence id="src18" class="srcSentence"> You must then do some post installation configuration so that your servers can use the connector.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <link xlink:href="90e7e33f-9ecc-497b-89c5-09205ffc5066#BKMK_Prereqs">Prerequisites for the RMS connector</link>
              </para>
            </listItem>
            <listItem>
              <para>
                <embeddedLabel>
                  <caps:sentence id="src19" class="srcSentence">Step 1: </caps:sentence>
                </embeddedLabel>
                <link xlink:href="90e7e33f-9ecc-497b-89c5-09205ffc5066#BKMK_InstallingConnector">Installing the RMS connector</link>
              </para>
            </listItem>
            <listItem>
              <para>
                <embeddedLabel>
                  <caps:sentence id="src20" class="srcSentence">Step 2: </caps:sentence>
                </embeddedLabel>
                <link xlink:href="90e7e33f-9ecc-497b-89c5-09205ffc5066#EnteringCredentials">Entering credentials</link>
              </para>
            </listItem>
            <listItem>
              <para>
                <embeddedLabel>
                  <caps:sentence id="src21" class="srcSentence">Step 3: </caps:sentence>
                </embeddedLabel>
                <link xlink:href="90e7e33f-9ecc-497b-89c5-09205ffc5066#AuthorizingServers">Authorizing servers to use the RMS connector</link>
              </para>
            </listItem>
            <listItem>
              <para>
                <embeddedLabel>
                  <caps:sentence id="src22" class="srcSentence">Step 4: </caps:sentence>
                </embeddedLabel>
                <link xlink:href="90e7e33f-9ecc-497b-89c5-09205ffc5066#ConfiguringConnector">Configuring load balancing and high availability</link>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src23" class="srcSentence">Optional: <link xlink:href="90e7e33f-9ecc-497b-89c5-09205ffc5066#BKMK_ConfiguringHTTPS">Configuring the RMS connector to use HTTPS</link></caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src24" class="srcSentence">Optional: <link xlink:href="90e7e33f-9ecc-497b-89c5-09205ffc5066#BKMK_ConfiguringWebProxy">Configuring the RMS connector for a web proxy server</link></caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src25" class="srcSentence">Optional: <link xlink:href="90e7e33f-9ecc-497b-89c5-09205ffc5066#BKMK_InstallingStandaloneTool">Installing the RMS connector administration tool on administrative computers</link></caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <embeddedLabel>
                  <caps:sentence id="src26" class="srcSentence">Step 5: </caps:sentence>
                </embeddedLabel>
                <link xlink:href="90e7e33f-9ecc-497b-89c5-09205ffc5066#ConfiguringServers">Configuring servers to use the RMS connector</link>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <link xlink:href="90e7e33f-9ecc-497b-89c5-09205ffc5066#BKMK_ExchangeServer">Configuring an Exchange server to use the connector</link>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <link xlink:href="90e7e33f-9ecc-497b-89c5-09205ffc5066#BKMK_ConfiguringSharePoint">Configuring a SharePoint server to use the connector</link>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <link xlink:href="90e7e33f-9ecc-497b-89c5-09205ffc5066#BKMK_FileServer">Configuring a file server for File Classification Infrastructure to use the connector</link>
                  </para>
                </listItem>
              </list>
            </listItem>
            <listItem>
              <para>
                <link xlink:href="90e7e33f-9ecc-497b-89c5-09205ffc5066#BKMK_NextSteps">Next steps</link>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <section address="BKMK_Prereqs">
        <title>
          <caps:sentence id="src27" class="srcSentence">Prerequisites for the RMS connector</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src28" class="srcSentence">Before you install the RMS connector, make sure that the following requirements are in place.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src29" class="srcSentence">Requirement</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src30" class="srcSentence">More information</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src31" class="srcSentence">The Rights Management (RMS) service is activated</caps:sentence>
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
                    <caps:sentence id="src32" class="srcSentence">Directory synchronization between your Active Directory forests and Azure Active Directory</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src33" class="srcSentence">After RMS is activated, Azure Active Directory must be configured to work with the users and groups in your Active Directory database.</caps:sentence>
                  </para>
                  <alert class="important">
                    <para>
                      <caps:sentence id="src34" class="srcSentence">You must do this directory synchronization step for the RMS connector to work, even for a test network.</caps:sentence>
                      <caps:sentence id="src35" class="srcSentence"> Although you can use Office 365 and Azure Active Directory by using accounts that you manually create in Azure Active Directory, this connector requires that the accounts in Azure Active Directory are synchronized with Active Directory Domain Services; manual password synchronization is not sufficient.</caps:sentence>
                    </para>
                  </alert>
                  <para>
                    <caps:sentence id="src36" class="srcSentence">For more information, see the following resources:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <externalLink>
                          <linkText>
                            <caps:sentence id="src37" class="srcSentence">Instructions for configuring your Azure AD tenant</caps:sentence>
                          </linkText>
                          <linkUri>http://technet.microsoft.com/library/hh967611.aspx</linkUri>
                        </externalLink>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <externalLink>
                          <linkText>
                            <caps:sentence id="src38" class="srcSentence">Instructions for enabling directory synchronization with AAD using DirSync</caps:sentence>
                          </linkText>
                          <linkUri>http://technet.microsoft.com/library/hh967642.aspx</linkUri>
                        </externalLink>
                        <br />
                      </para>
                    </listItem>
                  </list>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src39" class="srcSentence">Optional but recommended: </caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src40" class="srcSentence">Enable federation between your on-premises Active Directory and Azure Active Directory  </caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src41" class="srcSentence">You can enable identity federation between your on-premises directory and Azure Active Directory.</caps:sentence>
                    <caps:sentence id="src42" class="srcSentence"> This configuration enables a more seamless user experience by using single sign-on to the RMS service.</caps:sentence>
                    <caps:sentence id="src43" class="srcSentence"> Without single sign on, users are prompted for their credentials before they can use rights-protected content.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src44" class="srcSentence">For instructions to configure federation by using Active Directory Federation Services (AD FS) between Active Directory Domain Services and Azure Active Directory, see the <externalLink><linkText>Checklist: Use AD FS to implement and manage single sign-on</linkText><linkUri>http://technet.microsoft.com/library/jj205462.aspx</linkUri></externalLink> in the Windows Server library.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src45" class="srcSentence">A minimum of two member computers on which to install the RMS connector:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src46" class="srcSentence">A 64-bit physical or virtual computer running one of the following operating systems: </caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence id="src47" class="srcSentence">Windows Server 2012 R2</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src48" class="srcSentence">Windows Server 2012</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src49" class="srcSentence">Windows Server 2008 R2</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src50" class="srcSentence">At least 1 GB of RAM</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src51" class="srcSentence">A minimum of 64 GB of disk space</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src52" class="srcSentence">At least one network interface</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src53" class="srcSentence">Access to the Internet via a firewall (or web proxy) that does not require authentication</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src54" class="srcSentence">Must be in a forest or domain that trusts other forests in the organization that contain installations of Exchange or SharePoint servers that you want to use with the RMS connector</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src55" class="srcSentence">For fault tolerance and high availability, you must install the RMS connector on a minimum of two computers.</caps:sentence>
                  </para>
                  <alert class="tip">
                    <para>
                      <caps:sentence id="src56" class="srcSentence">If you are using Outlook Web Access or mobile devices that use Exchange ActiveSync IRM and it is critical that you maintain access to emails and attachments that are protected by Azure RMS, we recommend that you deploy a load-balanced group of connector servers to ensure high availability.</caps:sentence>
                    </para>
                  </alert>
                  <para>
                    <caps:sentence id="src57" class="srcSentence">You do not need dedicated servers to run the connector but you must install it on a separate computer from the servers that will use the connector.</caps:sentence>
                  </para>
                  <alert class="important">
                    <para>
                      <caps:sentence id="src58" class="srcSentence">Do not install the connector on a computer that runs Exchange Server, SharePoint Server, or a file server that is configured for file classification infrastructure if you want to use the functionality from these services with Azure RMS.</caps:sentence>
                      <caps:sentence id="src59" class="srcSentence"> Also, do not install this connector on a domain controller.</caps:sentence>
                    </para>
                  </alert>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section address="BKMK_InstallingConnector">
        <title>
          <caps:sentence id="src60" class="srcSentence">Installing the RMS connector</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src61" class="srcSentence">After you have confirmed the prerequisites in the preceding section, use the following instructions to install the RMS connector:</caps:sentence>
          </para>
          <list class="ordered">
            <listItem>
              <para>
                <caps:sentence id="src62" class="srcSentence">Identify the computers (minimum of two) that will run the RMS connector.</caps:sentence>
                <caps:sentence id="src63" class="srcSentence"> They must meet the minimum specification listed in the preceding section.</caps:sentence>
              </para>
              <alert class="note">
                <para>
                  <caps:sentence id="src64" class="srcSentence">You will install a single RMS connector (consisting of multiple servers for high availability) per tenant (Office 365 tenant or Azure AD tenant).</caps:sentence>
                  <caps:sentence id="src65" class="srcSentence"> Unlike Active Directory RMS, you do not have to install an RMS connector in each forest.</caps:sentence>
                </para>
              </alert>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src66" class="srcSentence">Download the source files for the RMS connector from the <externalLink><linkText>Microsoft Download Center</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=314106</linkUri></externalLink>.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src67" class="srcSentence">To install the RMS connector, download RMSConnectorSetup.exe.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src68" class="srcSentence">In addition:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src69" class="srcSentence">If you later want to configure the connector from a 32-bit computer, also download RMSConnectorAdminToolSetup_x86.exe.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src70" class="srcSentence">If you want to use the server configuration tool for the RMS connector, to automate the configuration of registry settings on you on-premises servers, also download GenConnectorConfig.ps1.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src71" class="srcSentence">On the computer on which you want to install the RMS connector, run <legacyBold>RMSConnectorSetup.exe</legacyBold> with Administrator privileges.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src72" class="srcSentence">On the Welcome page of the Microsoft Rights Management Connector Setup page, select <ui>Install Microsoft Rights Management connector on the computer</ui>, and then click <ui>Next</ui>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src73" class="srcSentence">Read and agree to the RMS connector license terms, and then click <legacyBold>Next</legacyBold>.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src74" class="srcSentence">To continue, enter an account and password to configure the RMS connector.</caps:sentence>
          </para>
        </content>
      </section>
      <section address="EnteringCredentials">
        <title>
          <caps:sentence id="src75" class="srcSentence">Entering credentials</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src76" class="srcSentence">Before you can configure the RMS connector, you must enter credentials for an account that has sufficient privileges to configure the RMS connector.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src77" class="srcSentence">In addition, if you have implemented <externalLink><linkText>onboarding controls</linkText><linkUri>https://technet.microsoft.com/library/jj658941.aspx#BKMK_OnboardingControls</linkUri></externalLink>, make sure that the account you specify is able to protect content. For example, if you restricted the ability to protect content to the “IT department” group, the account that you specify here must be a member of that group. If not, you will see the error message: <ui>The attempt to discover the location of the administration service and organization failed. Make sure Microsoft Rights Management service is enabled for your organization.</ui></caps:sentence>
          </para>
          <para>
            <caps:sentence id="src78" class="srcSentence">You can use an account that has one of the following privileges:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src79" class="srcSentence">
                  <legacyBold>Office 365 tenant administrator</legacyBold>: An account that is a global admin for your Office 365 tenant.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src80" class="srcSentence">
                  <legacyBold> Azure Rights Management global administrator</legacyBold>: An account with administrator privileges for the Azure RMS tenant.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src81" class="srcSentence">
                  <legacyBold>Microsoft RMS connector Administrator</legacyBold>: An account in Azure Active Directory that has been granted rights to install and administer the RMS connector for your organization.</caps:sentence>
              </para>
              <para></para>
              <alert class="note">
                <para>
                  <caps:sentence id="src82" class="srcSentence">If you want to use the Microsoft RMS connector Administrator account, you must first do the following to assign the RMS connector administrator role:</caps:sentence>
                </para>
                <list class="ordered">
                  <listItem>
                    <para>
                      <caps:sentence id="src83" class="srcSentence">On the same computer, download and install Windows PowerShell for Rights Management.</caps:sentence>
                      <caps:sentence id="src84" class="srcSentence"> For more information, see <link xlink:href="0d665ed6-b1de-4d63-854a-bc57c1c49844">Installing Windows PowerShell for Azure Rights Management</link>.</caps:sentence>
                    </para>
                    <para>
                      <caps:sentence id="src85" class="srcSentence">Start Windows PowerShell with the <ui>Run as administrator</ui> command, and connect to the Azure RMS service by using the <externalLink><linkText>Connect-AadrmService</linkText><linkUri>https://msdn.microsoft.com/library/azure/dn629415.aspx</linkUri></externalLink> command: </caps:sentence>
                    </para>
                    <code>Connect-AadrmService                   //provide Office 365 tenant administrator or Azure RMS global administrator credentials</code>
                  </listItem>
                  <listItem>
                    <para>
                      <caps:sentence id="src86" class="srcSentence">Then run the <externalLink><linkText>Add-AadrmRoleBasedAdministrator</linkText><linkUri>https://msdn.microsoft.com/library/azure/dn629417.aspx</linkUri></externalLink> command, using just one of the following parameters:   </caps:sentence>
                    </para>
                    <code>Add-AadrmRoleBasedAdministrator -EmailAddress &lt;email address&gt; -Role "ConnectorAdministrator"</code>
                    <code>Add-AadrmRoleBasedAdministrator -ObjectId &lt;object id&gt; -Role "ConnectorAdministrator"</code>
                    <code>Add-AadrmRoleBasedAdministrator -SecurityGroupDisplayName &lt;group Name&gt; -Role "ConnectorAdministrator"</code>
                    <para>
                      <caps:sentence id="src87" class="srcSentence">For example, type: <userInput>Add-AadrmRoleBasedAdministrator -EmailAddress melisa@contoso.com -Role " ConnectorAdministrator "</userInput></caps:sentence>
                    </para>
                    <para>
                      <caps:sentence id="src88" class="srcSentence">Although these commands use the ConnectorAdministrator role, you could also use the GlobalAdministrator role here, as well.</caps:sentence>
                    </para>
                  </listItem>
                </list>
              </alert>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src89" class="srcSentence">During the RMS connector installation process, all prerequisite software is validated and installed, Internet Information Services (IIS) is installed if not already present, and the connector software is installed and configured.</caps:sentence>
            <caps:sentence id="src90" class="srcSentence"> In addition, Azure RMS is prepared for configuration by creating the following:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src91" class="srcSentence">An empty table of servers that are authorized to use the connector to communicate with Azure RMS.</caps:sentence>
                <caps:sentence id="src92" class="srcSentence"> You will add servers to this table later.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src93" class="srcSentence">A set of security tokens for the connector, which authorize operations with Azure RMS.</caps:sentence>
                <caps:sentence id="src94" class="srcSentence"> These tokens are downloaded from Azure RMS and installed on the local computer in the registry.</caps:sentence>
                <caps:sentence id="src95" class="srcSentence"> They are protected by using the data protection application programming interface (DPAPI) and the Local System account credentials.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src96" class="srcSentence">On the final page of the wizard, do the following, and then click <ui>Finish</ui>:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src97" class="srcSentence">If this is the first connector that you have installed, do not select <ui>Launch connector administrator console to authorize servers</ui> at this time.</caps:sentence>
                <caps:sentence id="src98" class="srcSentence"> You will select this option after you have installed your second (or final) RMS connector.</caps:sentence>
                <caps:sentence id="src99" class="srcSentence"> Instead, run the wizard again on at least one other computer.</caps:sentence>
                <caps:sentence id="src100" class="srcSentence"> You must install a minimum of two connectors.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src101" class="srcSentence">If you have installed your second (or final) connector, select <ui>Launch connector administrator console to authorize servers</ui>.</caps:sentence>
              </para>
            </listItem>
          </list>
          <alert class="tip">
            <para>
              <caps:sentence id="src102" class="srcSentence">At this point, there is a verification test that you can perform to test whether the web services for the RMS connector are operational: </caps:sentence>
            </para>
            <list class="bullet">
              <listItem>
                <para>
                  <caps:sentence id="src103" class="srcSentence">From a web browser, connect to <userInput>http://&lt;connectoraddress&gt;/_wmcs/certification/servercertification.asmx</userInput>, replacing <placeholder>&lt;connectoraddress&gt;</placeholder> with the server address or name that has the RMS connector installed.</caps:sentence>
                  <caps:sentence id="src104" class="srcSentence"> A successful connection displays a <ui>ServerCertificationWebService</ui> page.</caps:sentence>
                </para>
              </listItem>
            </list>
          </alert>
          <para>
            <caps:sentence id="src105" class="srcSentence">If you need to uninstall the RMS connector, run the wizard again and select the uninstall option.</caps:sentence>
          </para>
        </content>
      </section>
      <section address="AuthorizingServers">
        <title>
          <caps:sentence id="src106" class="srcSentence">Authorizing servers to use the RMS connector</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src107" class="srcSentence">When you have installed the RMS connector on at least two computers, you are ready to authorize the servers and services that you want to use the RMS connector.</caps:sentence>
            <caps:sentence id="src108" class="srcSentence"> For example, servers running Exchange Server 2013 or SharePoint Server 2013.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src109" class="srcSentence">To define these servers, run the RMS connector administration tool and add entries to the list of allowed servers.</caps:sentence>
            <caps:sentence id="src110" class="srcSentence"> You can run this tool when you select <ui>Launch connector administration console to authorize servers</ui> at the end of the Microsoft Rights Management connector Setup wizard, or you can run it separately from the wizard.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src111" class="srcSentence">When you authorize these servers, be aware of the following considerations:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src112" class="srcSentence">Servers that you add will be granted special privileges.</caps:sentence>
                <caps:sentence id="src113" class="srcSentence"> All accounts that you specify for the Exchange Server role in the connector configuration will be granted the <externalLink><linkText>super user role</linkText><linkUri>https://technet.microsoft.com/library/mt147272.aspx</linkUri></externalLink> in Azure RMS, which gives them access to all content for this RMS tenant.</caps:sentence>
                <caps:sentence id="src114" class="srcSentence"> The super user feature is automatically enabled at this point, if necessary.</caps:sentence>
                <caps:sentence id="src115" class="srcSentence"> To avoid the security risk of elevation of privileges, be careful to specify only the accounts that are used by your organization’s Exchange servers.</caps:sentence>
                <caps:sentence id="src116" class="srcSentence"> All servers configured as SharePoint servers or file servers that use FCI will be granted regular user privileges.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src117" class="srcSentence">You can add multiple servers as a single entry by specifying an Active Directory security or distribution group, or a service account that is used by more than one server.</caps:sentence>
                <caps:sentence id="src118" class="srcSentence"> When you use this configuration, the group of servers will share the same RMS certificates and will all be considered owners for content that any of them have protected.</caps:sentence>
                <caps:sentence id="src119" class="srcSentence"> To minimize administrative overheads, we recommend that you use this configuration of a single group rather than individual servers to authorize your organization’s Exchange servers or a SharePoint server farm.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src120" class="srcSentence">On the <ui>Servers allowed to utilize the connector</ui> page, click <ui>Add</ui>.</caps:sentence>
          </para>
        </content>
        <sections>
          <section address="BKMK_AddServer">
            <title>
              <caps:sentence id="src121" class="srcSentence">Add a server to the list of allowed servers</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src122" class="srcSentence">On the <ui>Allow a server to utilize the connector</ui> page, enter the name of the object, or browse to identify the object to authorize.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src123" class="srcSentence">It is important that you authorize the correct object.</caps:sentence>
                <caps:sentence id="src124" class="srcSentence"> For a server to use the connector, the account that runs the on-premises service (for example, Exchange or SharePoint) must be selected for authorization.</caps:sentence>
                <caps:sentence id="src125" class="srcSentence"> For example, if the service is running as a configured service account, add the name of that service account to the list.</caps:sentence>
                <caps:sentence id="src126" class="srcSentence"> If the service is running as Local System, add the name of the computer object (for example, SERVERNAME$).</caps:sentence>
                <caps:sentence id="src127" class="srcSentence"> As a best practice, create a group that contains these accounts and specify the group instead of individual server names.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src128" class="srcSentence">More information about the different server roles:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src129" class="srcSentence">For servers that run Exchange: You must specify a security group and you can use the default group (<ui>Exchange Servers</ui>) that Exchange automatically creates and maintains of all Exchange servers in the forest.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src130" class="srcSentence">For servers that run SharePoint: </caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src131" class="srcSentence">If a SharePoint 2010 server is configured to run as Local System (it's not using a service account), manually create a security group in Active Directory Domain Services, and add the computer name object for the server in this configuration to this group.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src132" class="srcSentence">If a SharePoint server is configured to use a service account (the recommended practice for SharePoint 2010 and the only option for SharePoint 2013), do the following:</caps:sentence>
                      </para>
                      <list class="ordered">
                        <listItem>
                          <para>
                            <caps:sentence id="src133" class="srcSentence">Add the service account that runs the SharePoint Central Administration service to enable SharePoint to be configured from its administrator console.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src134" class="srcSentence">Add the account that is configured for the SharePoint App Pool.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                      <alert class="tip">
                        <para>
                          <caps:sentence id="src135" class="srcSentence">If these two accounts are different, consider creating a single group that contains both accounts to minimize the administrative overheads.</caps:sentence>
                        </para>
                      </alert>
                    </listItem>
                  </list>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src136" class="srcSentence">For file servers that use File Classification Infrastructure, the associated services run as the Local System account, so you must authorize the computer account for the file servers (for example, SERVERNAME$) or a group that contains those computer accounts.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src137" class="srcSentence">When you have finished adding servers to the list, click <ui>Close</ui>.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src138" class="srcSentence">If you haven’t already done so, you must now configure load balancing for the servers that have the RMS connector installed, and consider whether to use HTTPS for the connections between these servers and the servers that you have just authorized.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </section>
      <section address="ConfiguringConnector">
        <title>
          <caps:sentence id="src139" class="srcSentence">Configuring load balancing and high availability</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src140" class="srcSentence">After you have installed the second or final instance of the RMS connector, define a connector URL server name and configure a load balancing system.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src141" class="srcSentence">The connector URL server name can be any name under a namespace that you control.</caps:sentence>
            <caps:sentence id="src142" class="srcSentence"> For example, you could create an entry in your DNS system for <userInput>rmsconnector.contoso.com</userInput> and configure this entry to use an IP address in your load balancing system.</caps:sentence>
            <caps:sentence id="src143" class="srcSentence"> There are no special requirements for this name and it doesn’t need to be configured on the connector servers themselves.</caps:sentence>
            <caps:sentence id="src144" class="srcSentence"> Unless your Exchange and SharePoint servers are going to be communicating with the connector over the Internet, this name doesn’t have to resolve on the Internet.</caps:sentence>
          </para>
          <alert class="important">
            <para>
              <caps:sentence id="src145" class="srcSentence">We recommend that you don’t change this name after you have configured Exchange or SharePoint servers to use the connector, because you have to then clear these servers of all IRM configurations and then reconfigure them.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence id="src146" class="srcSentence">After the name is created in DNS and is configured for an IP address, configure load balancing for that address, which directs traffic to the connector servers.</caps:sentence>
            <caps:sentence id="src147" class="srcSentence"> You can use any IP-based load balancer for this purpose, which includes  the Network Load Balancing (NLB) feature in Windows Server.</caps:sentence>
            <caps:sentence id="src148" class="srcSentence"> For more information, see <externalLink><linkText>Load Balancing Deployment Guide</linkText><linkUri>http://technet.microsoft.com/library/cc754833(v=WS.10).aspx</linkUri></externalLink>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src149" class="srcSentence">Use the following settings to configure the NLB cluster:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src150" class="srcSentence">Ports: 80 (for HTTP) or 443 (for HTTPS)</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src151" class="srcSentence">For more information about whether to use HTTP or HTTPS, see the next section.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src152" class="srcSentence">Affinity: None</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src153" class="srcSentence">Distribution method: Equal</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src154" class="srcSentence">This name that you define for the load-balanced system (for the servers running the RMS connector service) is your organization’s RMS connector name that you will use later, when you configure the on-premises servers to use Azure RMS.</caps:sentence>
          </para>
        </content>
      </section>
      <section address="BKMK_ConfiguringHTTPS">
        <title>
          <caps:sentence id="src155" class="srcSentence">Configuring the RMS connector to use HTTPS</caps:sentence>
        </title>
        <content>
          <alert class="note">
            <para>
              <caps:sentence id="src156" class="srcSentence">This configuration step is optional, but recommended for additional security.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence id="src157" class="srcSentence">Although the use of TLS or SSL is optional for the RMS connector, we recommend it for any HTTP-based security-sensitive service.</caps:sentence>
            <caps:sentence id="src158" class="srcSentence"> This configuration authenticates the servers running the connector to your Exchange and SharePoint servers that use the connector.</caps:sentence>
            <caps:sentence id="src159" class="srcSentence"> In addition, all data that is sent from these servers to the connector is encrypted.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src160" class="srcSentence">To enable the RMS connector to use TLS, on each server that runs the RMS connector, install a server authentication certificate that contains the name that you will use for the connector.</caps:sentence>
            <caps:sentence id="src161" class="srcSentence"> For example, if your RMS connector name that you defined in DNS is <system>rmsconnector.contoso.com</system>, deploy a server authentication certificate that contains <system>rmsconnector.contoso.com</system> in the certificate subject as the common name.</caps:sentence>
            <caps:sentence id="src162" class="srcSentence"> Or, specify <system>rmsconnector.contoso.com</system> in the certificate alternative name as the DNS value.</caps:sentence>
            <caps:sentence id="src163" class="srcSentence"> The certificate does not have to include the name of the server.</caps:sentence>
            <caps:sentence id="src164" class="srcSentence"> Then in IIS, bind this certificate to the Default Web Site.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src165" class="srcSentence">If you use the HTTPS option, ensure that all servers that run the connector have a valid server authentication certificate that chains to a root CA that your Exchange and SharePoint servers trust.</caps:sentence>
            <caps:sentence id="src166" class="srcSentence"> In addition, if the certification authority (CA) that issued the certificates for the connector servers publishes a certificate revocation list (CRL), the Exchange and SharePoint servers must be able to download this CRL.</caps:sentence>
          </para>
          <alert class="tip">
            <para>
              <caps:sentence id="src167" class="srcSentence">You can use the following information and resources to help you request and install a server authentication certificate, and to bind this certificate to the Default Web Site in IIS:</caps:sentence>
            </para>
            <list class="bullet">
              <listItem>
                <para>
                  <caps:sentence id="src168" class="srcSentence">If you use Active Directory Certificate Services (AD CS) and an enterprise certification authority (CA) to deploy these server authentication certificates, you can duplicate and then use the Web Server certificate template.</caps:sentence>
                  <caps:sentence id="src169" class="srcSentence"> This certificate template uses <ui>Supplied in the request</ui> for the certificate subject name, which means that you can provide the FQDN of the RMS connector name for the certificate subject name or subject alternative name when you request the certificate.</caps:sentence>
                </para>
              </listItem>
              <listItem>
                <para>
                  <caps:sentence id="src170" class="srcSentence">If you use a stand-alone CA or purchase this certificate from another company, see <externalLink><linkText>Configuring Internet Server Certificates (IIS 7)</linkText><linkUri>http://technet.microsoft.com/library/cc731977(v=ws.10).aspx</linkUri></externalLink> in the <externalLink><linkText>Web Server (IIS)</linkText><linkUri>http://technet.microsoft.com/library/cc753433(v=ws.10).aspx</linkUri></externalLink> documentation library on TechNet.</caps:sentence>
                </para>
              </listItem>
              <listItem>
                <para>
                  <caps:sentence id="src171" class="srcSentence">To configure IIS to use the certificate, see <externalLink><linkText>Add a Binding to a Site (IIS 7)</linkText><linkUri>http://technet.microsoft.com/library/cc731692.aspx</linkUri></externalLink> in the in the <externalLink><linkText>Web Server (IIS)</linkText><linkUri>http://technet.microsoft.com/library/cc753433(v=ws.10).aspx</linkUri></externalLink> documentation library on TechNet.</caps:sentence>
                </para>
              </listItem>
            </list>
          </alert>
        </content>
      </section>
      <section address="BKMK_ConfiguringWebProxy">
        <title>
          <caps:sentence id="src172" class="srcSentence">Configuring the RMS connector for a web proxy server</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src173" class="srcSentence">If your connector servers are installed in a network that does not have direct Internet connectivity and requires manual configuration of a web proxy server for outbound Internet access, you must configure the registry on these servers for the RMS connector.</caps:sentence>
          </para>
          <procedure>
            <title>
              <caps:sentence id="src174" class="srcSentence">To configure the RMS connector to use a web proxy server</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src175" class="srcSentence">On each server running the RMS connector, open a registry editor, such as Regedit.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src176" class="srcSentence">Navigate to <ui>HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AADRM\Connector</ui></caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src177" class="srcSentence">Add the string value of <ui>ProxyAddress</ui> and then set the Data for this value to be <ui>http://&lt;MyProxyDomainOrIPaddress&gt;:&lt;MyProxyPort&gt;</ui></caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src178" class="srcSentence">For example: <userInput>http://proxyserver.contoso.com:8080</userInput></caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src179" class="srcSentence">Close the registry editor, and then restart the server or perform an IISReset command to restart IIS.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
        </content>
      </section>
      <section address="BKMK_InstallingStandaloneTool">
        <title>
          <caps:sentence id="src180" class="srcSentence">Installing the RMS connector administration tool on administrative computers</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src181" class="srcSentence">You can run the RMS connector administration tool from a computer that does not have the RMS connector installed, if that computer meets the following requirements:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src182" class="srcSentence">A physical or virtual computer running Windows Server 2012 or Windows Server 2012 R2 (all editions), Windows Server 2008 R2 or Windows Server 2008 R2 Service Pack 1 (all editions), Windows 8.1, Windows 8, or Windows 7.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src183" class="srcSentence">At least 1 GB of RAM.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src184" class="srcSentence">A minimum of 64 GB of disk space.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src185" class="srcSentence">At least one network interface.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src186" class="srcSentence">Access to the Internet via a firewall (or web proxy).</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src187" class="srcSentence">To install the RMS connector administration tool, run the following files:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src188" class="srcSentence">For a 32-bit computer: RMSConnectorAdminToolSetup_x86.exe</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src189" class="srcSentence">For a 64-bit computer: RMSConnectorSetup.exe</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src190" class="srcSentence">If you haven’t already downloaded these files, you can do so from the <externalLink><linkText>Microsoft Download Center</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=314106</linkUri></externalLink>.</caps:sentence>
          </para>
        </content>
      </section>
      <section address="ConfiguringServers">
        <title>
          <caps:sentence id="src191" class="srcSentence">Configuring servers to use the RMS connector</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src192" class="srcSentence">After you have installed and configured the RMS connector, you are ready to configure your on-premises servers that will use Rights Management and connect to Azure RMS by using the connector.</caps:sentence>
            <caps:sentence id="src193" class="srcSentence"> This means configuring the following servers:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src194" class="srcSentence">For Exchange 2013: Client access servers and mailbox servers</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src195" class="srcSentence">For Exchange 2010: Client access servers and hub transport servers</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src196" class="srcSentence">For SharePoint: Front-end SharePoint webservers, including those hosting the Central Administration server</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src197" class="srcSentence">For File Classification Infrastructure: Windows Server computers that have installed File Resource Manager</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src198" class="srcSentence">This configuration requires registry settings.</caps:sentence>
            <caps:sentence id="src199" class="srcSentence"> To do this, you have two options:</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src200" class="srcSentence">Configuration option</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src201" class="srcSentence">Advantages</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src202" class="srcSentence">Disadvantages</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src203" class="srcSentence">Automatically by using the server configuration tool for Microsoft RMS connector</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src204" class="srcSentence">No direct editing of the registry.</caps:sentence>
                    <caps:sentence id="src205" class="srcSentence"> This is automated for you by using a script.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src206" class="srcSentence">No need to run a Windows PowerShell cmdlet to obtain your Microsoft RMS URL.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src207" class="srcSentence">The prerequisites are automatically checked for you (but not automatically remediated) if you run it locally.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src208" class="srcSentence">When you run the tool, you must make a connection to a server that is already running the RMS connector.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src209" class="srcSentence">Manually by editing the registry</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src210" class="srcSentence">No connectivity to a server running the RMS connector is required.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src211" class="srcSentence">More administrative overheads that are error-prone.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src212" class="srcSentence">You must obtain your Microsoft RMS URL, which requires you to run a Windows PowerShell command.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src213" class="srcSentence">You must always make all the prerequisites checks yourself.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para></para>
          <alert class="important">
            <para>
              <caps:sentence id="src214" class="srcSentence">In both cases, you must manually install any prerequisites and configure Exchange, SharePoint, and File Classification Infrastructure to use Rights Management.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence id="src215" class="srcSentence">For most organizations, automatic configuration by using the server configuration tool for Microsoft RMS connector will be the better option, because it provides greater efficiency and reliability than manual configuration.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src216" class="srcSentence">After making the configuration changes on these servers, you must restart them if they are running Exchange or SharePoint and previously configured to use AD RMS.</caps:sentence>
            <caps:sentence id="src217" class="srcSentence"> There is no need to restart these servers if you are configuring them for Rights Management for the first time.</caps:sentence>
            <caps:sentence id="src218" class="srcSentence"> You must always restart the file server that is configured to use File Classification Infrastructure after you make these configuration changes.</caps:sentence>
          </para>
          <procedure address="BKMK_HowToRunTheTool">
            <title>
              <caps:sentence id="src219" class="srcSentence">How to use the server configuration tool for Microsoft RMS connector</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src220" class="srcSentence">If you haven’t already downloaded the script for the server configuration tool for Microsoft RMS connector (GenConnectorConfig.ps1), download it from the <externalLink><linkText>Microsoft Download Center</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=314106</linkUri></externalLink>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src221" class="srcSentence">Save the GenConnectorConfig.ps1 file on the computer where you will run the tool.</caps:sentence>
                    <caps:sentence id="src222" class="srcSentence"> If you will run the tool locally, this must be the server that you want to configure to communicate with the RMS connector.</caps:sentence>
                    <caps:sentence id="src223" class="srcSentence"> Otherwise, you can save it on any computer.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src224" class="srcSentence">Decide how to run the tool:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src225" class="srcSentence">
                          <embeddedLabel>Locally</embeddedLabel>: You can run the tool interactively, from the server to be configured to communicate with the RMS connector.</caps:sentence>
                        <caps:sentence id="src226" class="srcSentence"> This is useful for a one-off configuration, such as a testing environment.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src227" class="srcSentence">
                          <embeddedLabel>Software deployment</embeddedLabel>: You can run the tool to produce registry files that you then deploy to one or more relevant servers by using a systems management application that supports software deployment, such as System Center Configuration Manager.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src228" class="srcSentence">
                          <embeddedLabel>Group Policy</embeddedLabel>: You can run the tool to produce a script that you give to an administrator who can create Group Policy objects for the servers to be configured.</caps:sentence>
                        <caps:sentence id="src229" class="srcSentence"> This script creates one Group Policy object for each server type to be configured, which the administrator can then assign to the relevant servers.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <alert class="note">
                    <para>
                      <caps:sentence id="src230" class="srcSentence">This tool configures the servers that will communicate with the RMS connector and that are listed at the beginning of this section.</caps:sentence>
                      <caps:sentence id="src231" class="srcSentence"> Do not run this tool on the servers that run the RMS connector.</caps:sentence>
                    </para>
                  </alert>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src232" class="srcSentence">Start Windows PowerShell with the <ui>Run as an administrator</ui> option, and use the Get-help command to read instructions how to the use the tool for your chosen configuration method:</caps:sentence>
                  </para>
                  <code>Get-help .\GenConnectorConfig.ps1 -detailed</code>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence id="src233" class="srcSentence">To run the script, you must enter the URL of the RMS connector for your organization.</caps:sentence>
                  <caps:sentence id="src234" class="srcSentence"> Enter the protocol prefix (HTTP:// or HTTPS://) and the name of the connector that you defined in DNS for the load balanced address of your connector.</caps:sentence>
                  <caps:sentence id="src235" class="srcSentence"> For example, https://connector.contoso.com.</caps:sentence>
                  <caps:sentence id="src236" class="srcSentence"> The tool then uses that URL to contact the servers running the RMS connector and obtain other parameters that are used to create the required configurations.</caps:sentence>
                </para>
                <alert class="important">
                  <para>
                    <caps:sentence id="src237" class="srcSentence">When you run this tool, make sure that you specify the name of the load-balanced RMS connector for your organization and not the name of a single server that runs the RMS connector service.</caps:sentence>
                  </para>
                </alert>
              </content>
            </conclusion>
          </procedure>
          <para>
            <caps:sentence id="src238" class="srcSentence">Use the following sections for specific information for each service type:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <link xlink:href="90e7e33f-9ecc-497b-89c5-09205ffc5066#BKMK_ExchangeServer">Configuring an Exchange server to use the connector</link>
              </para>
            </listItem>
            <listItem>
              <para>
                <link xlink:href="90e7e33f-9ecc-497b-89c5-09205ffc5066#BKMK_ConfiguringSharePoint">Configuring a SharePoint server to use the connector</link>
              </para>
            </listItem>
            <listItem>
              <para>
                <link xlink:href="90e7e33f-9ecc-497b-89c5-09205ffc5066#BKMK_FileServer">Configuring a file server for File Classification Infrastructure to use the connector</link>
              </para>
            </listItem>
          </list>
          <alert class="note">
            <para>
              <caps:sentence id="src239" class="srcSentence">After these servers are configured to use the connector, client applications that are installed locally on these servers might not work with RMS.</caps:sentence>
              <caps:sentence id="src240" class="srcSentence"> When this happens, it is because the applications try to use the connector rather than use RMS directly, which is not supported.</caps:sentence>
            </para>
            <para>
              <caps:sentence id="src241" class="srcSentence">In addition, if Office 2010 is installed locally on an Exchange server, the client app’s IRM features might work from that computer after the server is configured to use the connector, but this is not supported.</caps:sentence>
            </para>
            <para>
              <caps:sentence id="src242" class="srcSentence">In both scenarios, you must install the client applications on separate computers that are not configured to use the connector.</caps:sentence>
              <caps:sentence id="src243" class="srcSentence"> They will then correctly use RMS directly.</caps:sentence>
            </para>
          </alert>
        </content>
        <sections>
          <section address="BKMK_ExchangeServer">
            <title>
              <caps:sentence id="src244" class="srcSentence">Configuring an Exchange server to use the connector</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src245" class="srcSentence">The following Exchange roles communicate with the RMS connector:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src246" class="srcSentence">For Exchange 2013: Client access server and mailbox server</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src247" class="srcSentence">For Exchange 2010: Client access server and hub transport server</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src248" class="srcSentence">To use the RMS connector, these servers running Exchange must be running one of the following software versions:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src249" class="srcSentence">Exchange Server 2013 with Exchange 2013 Cumulative Update 3</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src250" class="srcSentence">Exchange Server 2010 with Exchange 2010 Service Pack 3 Rollup Update 6</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src251" class="srcSentence">You will also need to install on these servers, a version of the RMS client that includes support for RMS Cryptographic Mode 2.</caps:sentence>
                <caps:sentence id="src252" class="srcSentence"> The minimum version that is supported in Windows Server 2008 is included in the hotfix that you can download from <externalLink><linkText>RSA key length is increased to 2048 bits for AD RMS in Windows Server 2008 R2 and in Windows Server 2008</linkText><linkUri>http://support.microsoft.com/kb/2627272</linkUri></externalLink>.</caps:sentence>
                <caps:sentence id="src253" class="srcSentence"> The minimum version for Windows Server 2008 R2 can be downloaded from <externalLink><linkText>RSA key length is increased to 2048 bits for AD RMS in Windows 7 or in Windows Server 2008 R2</linkText><linkUri>http://support.microsoft.com/kb/2627273</linkUri></externalLink>.</caps:sentence>
                <caps:sentence id="src254" class="srcSentence"> Windows Server 2012 and Windows Server 2012 R2 natively support Cryptographic Mode 2.</caps:sentence>
              </para>
              <alert class="important">
                <para>
                  <caps:sentence id="src255" class="srcSentence">If these versions or later versions of Exchange and the RMS client are not installed, you will not be able to configure Exchange to use the connector.</caps:sentence>
                  <caps:sentence id="src256" class="srcSentence"> Check that these versions are installed before you continue.</caps:sentence>
                </para>
              </alert>
              <procedure>
                <title>
                  <caps:sentence id="src257" class="srcSentence">To configure Exchange servers to use the connector</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src258" class="srcSentence">On the Exchange server roles that communicate with the RMS connector, do one of the following:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence id="src259" class="srcSentence">Run the server configuration tool for Microsoft RMS connector.</caps:sentence>
                            <caps:sentence id="src260" class="srcSentence"> For more information, see <link xlink:href="90e7e33f-9ecc-497b-89c5-09205ffc5066#BKMK_HowToRunTheTool">How to use the server configuration tool for Microsoft RMS connector</link> in this topic.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence id="src261" class="srcSentence">For example, to run the tool locally to configure a server running Exchange 2013: </caps:sentence>
                          </para>
                          <code>.\GenConnectorConfig.ps1 -ConnectorUri https://rmsconnector.contoso.com -SetExchange2013</code>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src262" class="srcSentence">Make manual registry edits by using the tables in the following sections to manually add registry settings on the servers.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src263" class="srcSentence">Enable IRM functionality in Exchange.</caps:sentence>
                        <caps:sentence id="src264" class="srcSentence"> For more information, see <externalLink><linkText>Information Rights Management Procedures</linkText><linkUri>https://technet.microsoft.com/library/dd351212(v=exchg.150).aspx</linkUri></externalLink> in the Exchange library.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
              <para>
                <caps:sentence id="src265" class="srcSentence">Use the tables in the following sections only if you want to manually add or check registry settings on these servers, which configures the servers to use the RMS connector.</caps:sentence>
                <caps:sentence id="src266" class="srcSentence"> Instructions for when you use these tables:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src267" class="srcSentence">
                      <placeholder>MicrosoftRMSURL</placeholder> is your organization’s Microsoft RMS service URL.</caps:sentence>
                    <caps:sentence id="src268" class="srcSentence"> To find this value:</caps:sentence>
                  </para>
                  <list class="ordered">
                    <listItem>
                      <para>
                        <caps:sentence id="src269" class="srcSentence">Run the <externalLink><linkText>Get-AadrmConfiguration</linkText><linkUri>http://msdn.microsoft.com/library/windowsazure/dn629410.aspx</linkUri></externalLink> cmdlet for Azure RMS.</caps:sentence>
                        <caps:sentence id="src270" class="srcSentence"> If you haven’t already installed the Windows PowerShell module for Azure RMS, see <link xlink:href="0d665ed6-b1de-4d63-854a-bc57c1c49844">Installing Windows PowerShell for Azure Rights Management</link>.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src271" class="srcSentence">From the output, identify the <ui>LicensingIntranetDistributionPointUrl</ui> value.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src272" class="srcSentence">For example: <ui>LicensingIntranetDistributionPointUrl   : https://5c6bb73b-1038-4eec-863d-49bded473437.rms.na.aadrm.com/_wmcs/licensing</ui></caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src273" class="srcSentence">From the value, remove <ui>/_wmcs/licensing</ui> from this string.</caps:sentence>
                        <caps:sentence id="src274" class="srcSentence"> The remaining string is your Microsoft RMS URL.</caps:sentence>
                        <caps:sentence id="src275" class="srcSentence"> In our example, the Microsoft RMS URL would be the following value:</caps:sentence>
                      </para>
                      <para>
                        <ui>
                          <caps:sentence id="src276" class="srcSentence">https://5c6bb73b-1038-4eec-863d-49bded473437.rms.na.aadrm.com</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                  </list>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src277" class="srcSentence">
                      <placeholder>ConnectorFQDN</placeholder> is the load-balancing name that you defined in DNS for the connector.</caps:sentence>
                    <caps:sentence id="src278" class="srcSentence"> For example, <system>rmsconnector.contoso.com</system>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src279" class="srcSentence">Use the HTTPS prefix for the connector URL if you have configured the connector to use HTTPS to communicate with your on-premises servers.</caps:sentence>
                    <caps:sentence id="src280" class="srcSentence"> For more information, see the <link xlink:href="90e7e33f-9ecc-497b-89c5-09205ffc5066#BKMK_ConfiguringHTTPS">Configuring the RMS connector to use HTTPS</link> section in this topic.</caps:sentence>
                    <caps:sentence id="src281" class="srcSentence"> The Microsoft RMS URLs always use HTTPS.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
            <sections>
              <section expanded="false">
                <title>
                  <caps:sentence id="src282" class="srcSentence">Table for Exchange 2013 registry settings</caps:sentence>
                </title>
                <content>
                  <table>
                    <thead>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src283" class="srcSentence">Registry path</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src284" class="srcSentence">Type</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src285" class="srcSentence">Value</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src286" class="srcSentence">Data</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </thead>
                    <tbody>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src287" class="srcSentence">HKEY_LOCAL_MACHINE\Software\Microsoft\MSDRM\ServiceLocation\Activation</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src288" class="srcSentence">Reg_SZ</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src289" class="srcSentence">Default</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src290" class="srcSentence">https://<placeholder>MicrosoftRMSURL/_wmcs/certification</placeholder></caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src291" class="srcSentence">HKEY_LOCAL_MACHINE\Software\Microsoft\MSDRM\ServiceLocation\EnterprisePublishing</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src292" class="srcSentence">Reg_SZ</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src293" class="srcSentence">Default</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src294" class="srcSentence">https://MicrosoftRMSURL/_wmcs/Licensing</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src295" class="srcSentence">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\ExchangeServer\v15\IRM\CertificationServerRedirection</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src296" class="srcSentence">Reg_SZ</caps:sentence>
                          </para>
                          <para></para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src297" class="srcSentence">https://<placeholder>MicrosoftRMSURL</placeholder></caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src298" class="srcSentence">One of the following, depending on whether you are using HTTP or HTTPS from your Exchange server to the RMS connector:</caps:sentence>
                          </para>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence id="src299" class="srcSentence">http://<placeholder>ConnectorFQDN</placeholder></caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src300" class="srcSentence">https://<placeholder>ConnectorFQDN</placeholder></caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src301" class="srcSentence">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\ExchangeServer\v15\IRM\LicenseServerRedirection</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src302" class="srcSentence">Reg_SZ</caps:sentence>
                          </para>
                          <para></para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src303" class="srcSentence">https://<placeholder>MicrosoftRMSURL</placeholder></caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src304" class="srcSentence">One of the following, depending on whether you are using HTTP or HTTPS from your Exchange server to the RMS connector:</caps:sentence>
                          </para>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence id="src305" class="srcSentence">http://<placeholder>ConnectorFQDN</placeholder></caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src306" class="srcSentence">https://<placeholder>ConnectorFQDN</placeholder></caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                    </tbody>
                  </table>
                </content>
              </section>
              <section expanded="false">
                <title>
                  <caps:sentence id="src307" class="srcSentence">Table for Exchange 2010 registry settings</caps:sentence>
                </title>
                <content>
                  <table>
                    <thead>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src308" class="srcSentence">Registry path</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src309" class="srcSentence">Type</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src310" class="srcSentence">Value</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src311" class="srcSentence">Data</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </thead>
                    <tbody>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src312" class="srcSentence">HKEY_LOCAL_MACHINE\Software\Microsoft\MSDRM\ServiceLocation\Activation</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src313" class="srcSentence">Reg_SZ</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src314" class="srcSentence">Default</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src315" class="srcSentence">https://<placeholder>MicrosoftRMSURL</placeholder>/_wmcs/certification</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src316" class="srcSentence">HKEY_LOCAL_MACHINE\Software\Microsoft\MSDRM\ServiceLocation\EnterprisePublishing</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src317" class="srcSentence">Reg_SZ</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src318" class="srcSentence">Default</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src319" class="srcSentence">https://<placeholder>MicrosoftRMSURL</placeholder>/_wmcs/Licensing</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src320" class="srcSentence">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\ExchangeServer\v14\IRM\CertificationServerRedirection</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src321" class="srcSentence">Reg_SZ</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src322" class="srcSentence">https://<placeholder>MicrosoftRMSURL</placeholder></caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src323" class="srcSentence">One of the following, depending on whether you are using HTTP or HTTPS from your Exchange server to the RMS connector:</caps:sentence>
                          </para>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence id="src324" class="srcSentence">http://<placeholder>ConnectorFQDN</placeholder></caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src325" class="srcSentence">https://<placeholder>ConnectorFQDN</placeholder></caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src326" class="srcSentence">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\ExchangeServer\v14\IRM\LicenseServerRedirection</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src327" class="srcSentence">Reg_SZ</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src328" class="srcSentence">https://<placeholder>MicrosoftRMSURL</placeholder></caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src329" class="srcSentence">One of the following, depending on whether you are using HTTP or HTTPS from your Exchange server to the RMS connector:</caps:sentence>
                          </para>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence id="src330" class="srcSentence">http://<placeholder>ConnectorFQDN</placeholder></caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src331" class="srcSentence">https://<placeholder>ConnectorFQDN</placeholder></caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                    </tbody>
                  </table>
                </content>
              </section>
            </sections>
          </section>
          <section address="BKMK_ConfiguringSharePoint">
            <title>
              <caps:sentence id="src332" class="srcSentence">Configuring a SharePoint server to use the connector</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src333" class="srcSentence">The following SharePoint roles communicate with the RMS connector:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src334" class="srcSentence">Front-end SharePoint webservers, including those hosting the Central Administration server</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src335" class="srcSentence">To use the RMS connector, these servers running SharePoint must be running one of the following software versions:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src336" class="srcSentence">SharePoint Server 2013</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src337" class="srcSentence">SharePoint Server 2010</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src338" class="srcSentence">A SharePoint 2013 server must also be running a version of the MSIPC client 2.1 that is from1.0.622.34 through 1.0.10907.0.</caps:sentence>
              </para>
              <alert class="warning">
                <para>
                  <caps:sentence id="src339" class="srcSentence">There are multiple versions of the MSIPC 2.1 client, so make sure to install a version referenced in this article.</caps:sentence> </para>
                <para>
                  <caps:sentence id="src340" class="srcSentence">You can verify the client version by checking the version number of MSIPC.dll, which is located in <system>\Program Files\Active Directory Rights Management Services Client 2.1</system>.</caps:sentence>
                  <caps:sentence id="src341" class="srcSentence"> The properties dialog box  shows the version number of the MSIPC 2.1 client.</caps:sentence>
                </para>
              </alert>
              <para>
                <caps:sentence id="src342" class="srcSentence">These servers running SharePoint 2010 must have installed a version of the MSDRM client that includes support for RMS Cryptographic Mode 2.</caps:sentence>
                <caps:sentence id="src343" class="srcSentence"> The minimum version that is supported in Windows Server 2008 is included in the hotfix that you can download from <externalLink><linkText>RSA key length is increased to 2048 bits for AD RMS in Windows Server 2008 R2 and in Windows Server 2008</linkText><linkUri>http://support.microsoft.com/kb/2627272</linkUri></externalLink>, and the minimum version for Windows Server 2008 R2 can be downloaded from <externalLink><linkText>RSA key length is increased to 2048 bits for AD RMS in Windows 7 or in Windows Server 2008 R2</linkText><linkUri>http://support.microsoft.com/kb/2627273</linkUri></externalLink>.</caps:sentence>
                <caps:sentence id="src344" class="srcSentence"> Windows Server 2012 and Windows Server 2012 R2 natively support Cryptographic Mode 2.</caps:sentence>
              </para>
              <procedure>
                <title>
                  <caps:sentence id="src345" class="srcSentence">To configure SharePoint servers to use the connector</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src346" class="srcSentence">On the SharePoint servers that communicate with the RMS connector, do one of the following:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence id="src347" class="srcSentence">Run the server configuration tool for Microsoft RMS connector.</caps:sentence>
                            <caps:sentence id="src348" class="srcSentence"> For more information, see <link xlink:href="90e7e33f-9ecc-497b-89c5-09205ffc5066#BKMK_HowToRunTheTool">How to use the server configuration tool for Microsoft RMS connector</link> in this topic.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence id="src349" class="srcSentence">For example, to run the tool locally to configure a server running SharePoint 2013: </caps:sentence>
                          </para>
                          <code>.\GenConnectorConfig.ps1 -ConnectorUri https://rmsconnector.contoso.com -SetSharePoint2013</code>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src350" class="srcSentence">If you are using SharePoint 2013, make manual registry edits by using the table in the following section to manually add registry settings on the servers.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src351" class="srcSentence">Enable IRM in SharePoint.</caps:sentence>
                        <caps:sentence id="src352" class="srcSentence"> For more information, see <externalLink><linkText>Configure Information Rights Management (SharePoint Server 2010)</linkText><linkUri>https://technet.microsoft.com/library/hh545607(v=office.14).aspx</linkUri></externalLink> in the SharePoint library.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src353" class="srcSentence">When you follow these instructions, you must configure SharePoint to use the connector by specifying <ui>Use this RMS server</ui>, and then enter the load-balancing connector URL that you configured.</caps:sentence>
                        <caps:sentence id="src354" class="srcSentence"> Enter the protocol prefix (HTTP:// or HTTPS://) and the name of the connector that you defined in DNS for the load balanced address of your connector.</caps:sentence>
                        <caps:sentence id="src355" class="srcSentence"> For example, if your connector name is  https://connector.contoso.com, your configuration will look like the following picture:</caps:sentence>
                      </para>
                      <para>
                        <mediaLinkInline>
                          <image xlink:href="82377fdd-0c4b-4c2a-8c52-4d19e19f2cda"></image>
                        </mediaLinkInline>
                      </para>
                      <para>
                        <caps:sentence id="src356" class="srcSentence">After IRM is enabled on a SharePoint farm, you can enable IRM on individual libraries by using the <ui>Information Rights Management</ui> option on the <ui>Library Settings</ui> page for each of the libraries.</caps:sentence>
                      </para>
                      <alert class="important">
                        <para>
                          <caps:sentence id="src357" class="srcSentence">For SharePoint to access RMS by using the connector, you must authorize the corresponding accounts in the RMS connector administration tool.</caps:sentence>
                          <caps:sentence id="src358" class="srcSentence"> If you haven’t already done this, see <link xlink:href="90e7e33f-9ecc-497b-89c5-09205ffc5066#AuthorizingServers">Authorizing servers to use the RMS connector</link> in this topic.</caps:sentence>
                        </para>
                      </alert>
                    </content>
                  </step>
                </steps>
              </procedure>
              <para>
                <caps:sentence id="src359" class="srcSentence">Use the table in the following section only if you want to manually add or check registry settings on a server that runs SharePoint 2013.</caps:sentence>
              </para>
            </content>
            <sections>
              <section expanded="false">
                <title>
                  <caps:sentence id="src360" class="srcSentence">Table for SharePoint 2013 registry settings</caps:sentence>
                </title>
                <content>
                  <para>
                    <caps:sentence id="src361" class="srcSentence">Instructions for when you use this table:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src362" class="srcSentence">
                          <placeholder>MicrosoftRMSURL</placeholder> is your organization’s Microsoft RMS service URL.</caps:sentence>
                        <caps:sentence id="src363" class="srcSentence"> To find this value:</caps:sentence>
                      </para>
                      <list class="ordered">
                        <listItem>
                          <para>
                            <caps:sentence id="src364" class="srcSentence">Run the <externalLink><linkText>Get-AadrmConfiguration</linkText><linkUri>http://msdn.microsoft.com/library/windowsazure/dn629410.aspx</linkUri></externalLink> cmdlet for Azure RMS.</caps:sentence>
                            <caps:sentence id="src365" class="srcSentence"> If you haven’t already installed the Windows PowerShell module for Azure RMS, see <link xlink:href="0d665ed6-b1de-4d63-854a-bc57c1c49844">Installing Windows PowerShell for Azure Rights Management</link>.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src366" class="srcSentence">From the output, identify the <ui>LicensingIntranetDistributionPointUrl</ui> value.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence id="src367" class="srcSentence">For example: <ui>LicensingIntranetDistributionPointUrl   : https://5c6bb73b-1038-4eec-863d-49bded473437.rms.na.aadrm.com/_wmcs/licensing</ui></caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src368" class="srcSentence">From the value, remove <ui>/_wmcs/licensing</ui> from this string.</caps:sentence>
                            <caps:sentence id="src369" class="srcSentence"> The remaining string is your Microsoft RMS URL.</caps:sentence>
                            <caps:sentence id="src370" class="srcSentence"> In our example, the Microsoft RMS URL would be the following value:</caps:sentence>
                          </para>
                          <para>
                            <ui>
                              <caps:sentence id="src371" class="srcSentence">https://5c6bb73b-1038-4eec-863d-49bded473437.rms.na.aadrm.com</caps:sentence>
                            </ui>
                          </para>
                        </listItem>
                      </list>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src372" class="srcSentence">
                          <placeholder>ConnectorFQDN</placeholder> is the load-balancing name that you defined in DNS for the connector.</caps:sentence>
                        <caps:sentence id="src373" class="srcSentence"> For example, <system>rmsconnector.contoso.com</system>.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src374" class="srcSentence">Use the HTTPS prefix for the connector URL if you have configured the connector to use HTTPS to communicate with your on-premises servers.</caps:sentence>
                        <caps:sentence id="src375" class="srcSentence"> For more information, see the <link xlink:href="90e7e33f-9ecc-497b-89c5-09205ffc5066#BKMK_ConfiguringHTTPS">Configuring the RMS connector to use HTTPS</link> section in this topic.</caps:sentence>
                        <caps:sentence id="src376" class="srcSentence"> The Microsoft RMS URLs always use HTTPS.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <table>
                    <thead>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src377" class="srcSentence">Registry path </caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src378" class="srcSentence">Type</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src379" class="srcSentence">Value</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src380" class="srcSentence">Data</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </thead>
                    <tbody>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src381" class="srcSentence">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MSIPC\ServiceLocation\LicensingRedirection</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src382" class="srcSentence">Reg_SZ</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src383" class="srcSentence">https://<placeholder>MicrosoftRMSURL</placeholder>/_wmcs/licensing</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src384" class="srcSentence">One of the following, depending on whether you are using HTTP or HTTPS from your SharePoint server to the RMS connector:</caps:sentence>
                          </para>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence id="src385" class="srcSentence">http://<placeholder>ConnectorFQDN</placeholder>/_wmcs/licensing</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src386" class="srcSentence">https://<placeholder>ConnectorFQDN</placeholder>/_wmcs/licensing</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src387" class="srcSentence">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MSIPC\ServiceLocation\EnterpriseCertification</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src388" class="srcSentence">Reg_SZ</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src389" class="srcSentence">Default</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src390" class="srcSentence">One of the following, depending on whether you are using HTTP or HTTPS from your SharePoint server to the RMS connector:</caps:sentence>
                          </para>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence id="src391" class="srcSentence">http://<placeholder>ConnectorFQDN</placeholder>/_wmcs/certification</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src392" class="srcSentence">https://<placeholder>ConnectorFQDN</placeholder>/_wmcs/certification</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src393" class="srcSentence">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MSIPC\ServiceLocation\EnterprisePublishing</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src394" class="srcSentence">Reg_SZ</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src395" class="srcSentence">Default</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src396" class="srcSentence">One of the following, depending on whether you are using HTTP or HTTPS from your SharePoint server to the RMS connector:</caps:sentence>
                          </para>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence id="src397" class="srcSentence">http://<placeholder>ConnectorFQDN</placeholder>/_wmcs/licensing</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src398" class="srcSentence">https://<placeholder>ConnectorFQDN</placeholder>/_wmcs/licensing</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                    </tbody>
                  </table>
                </content>
              </section>
            </sections>
          </section>
          <section address="BKMK_FileServer">
            <title>
              <caps:sentence id="src399" class="srcSentence">Configuring a file server for File Classification Infrastructure to use the connector</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src400" class="srcSentence">To use the RMS connector and File Classification Infrastructure to protect Office documents, the file server must be running one of the following operating systems:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src401" class="srcSentence">Windows Server 2012 R2</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src402" class="srcSentence">Windows Server 2012</caps:sentence>
                  </para>
                </listItem>
              </list>
              <procedure>
                <title>
                  <caps:sentence id="src403" class="srcSentence">To configure file servers to use the connector</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src404" class="srcSentence">On the file servers configured for File Classification Infrastructure and that will communicate with the RMS connector, do one of the following:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence id="src405" class="srcSentence">Run the server configuration tool for Microsoft RMS connector.</caps:sentence>
                            <caps:sentence id="src406" class="srcSentence"> For more information, see <link xlink:href="90e7e33f-9ecc-497b-89c5-09205ffc5066#BKMK_HowToRunTheTool">How to use the server configuration tool for Microsoft RMS connector</link> in this topic.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence id="src407" class="srcSentence">For example, to run the tool locally to configure a file server running FCI: </caps:sentence>
                          </para>
                          <code>.\GenConnectorConfig.ps1 -ConnectorUri https://rmsconnector.contoso.com -SetFCI2012</code>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src408" class="srcSentence">Make manual registry edits by using the table in the following section to manually add registry settings on the servers.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src409" class="srcSentence">Create classification rules and file management tasks to protect documents with RMS Encryption, and then specify an RMS template to automatically apply RMS policies.</caps:sentence>
                        <caps:sentence id="src410" class="srcSentence"> For more information, see <externalLink><linkText>File Server Resource Manager Overview</linkText><linkUri>http://technet.microsoft.com/library/hh831701.aspx</linkUri></externalLink> in the Windows Server documentation library.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
              <para>
                <caps:sentence id="src411" class="srcSentence">Use the table in the following section only if you want to manually add or check registry settings on a file server that uses the File Classification Infrastructure to protect documents.</caps:sentence>
              </para>
            </content>
            <sections>
              <section expanded="false">
                <title>
                  <caps:sentence id="src412" class="srcSentence">Table for file server and File Classification Infrastructure registry settings</caps:sentence>
                </title>
                <content>
                  <para>
                    <caps:sentence id="src413" class="srcSentence">Instructions for when you use this table:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src414" class="srcSentence">
                          <placeholder>ConnectorFQDN</placeholder> is the load-balancing name that you defined in DNS for the connector.</caps:sentence>
                        <caps:sentence id="src415" class="srcSentence"> For example, <system>rmsconnector.contoso.com</system>.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src416" class="srcSentence">Use the HTTPS prefix for the connector URL if you have configured the connector to use HTTPS to communicate with your on-premises servers.</caps:sentence>
                        <caps:sentence id="src417" class="srcSentence"> For more information, see the <link xlink:href="90e7e33f-9ecc-497b-89c5-09205ffc5066#BKMK_ConfiguringHTTPS">Configuring the RMS connector to use HTTPS</link> section in this topic.</caps:sentence>
                        <caps:sentence id="src418" class="srcSentence"> The Microsoft RMS URLs always use HTTPS.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <table>
                    <thead>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src419" class="srcSentence">Registry path </caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src420" class="srcSentence">Type</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src421" class="srcSentence">Value</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src422" class="srcSentence">Data</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </thead>
                    <tbody>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src423" class="srcSentence">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MSDRM\ServiceLocation\EnterprisePublishing</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src424" class="srcSentence">Reg_SZ</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src425" class="srcSentence">Default</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src426" class="srcSentence">http://<placeholder>ConnectorFQDN</placeholder>/_wmcs/licensing</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src427" class="srcSentence">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MSDRM\ServiceLocation\Activation</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src428" class="srcSentence">Reg_SZ</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src429" class="srcSentence">Default</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src430" class="srcSentence">http://<placeholder>ConnectorFQDN</placeholder>/_wmcs/certification</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </tbody>
                  </table>
                </content>
              </section>
            </sections>
          </section>
        </sections>
      </section>
      <section address="BKMK_NextSteps">
        <title>
          <caps:sentence id="src431" class="srcSentence">Next steps</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src432" class="srcSentence">Now that the RMS connector is installed and configured, and your servers are configured to use it, IT administrators and users can protect and consume email message and documents by using Azure RMS.</caps:sentence>
            <caps:sentence id="src433" class="srcSentence"> To make this easy for users, deploy the RMS sharing application, which installs an add-on for Office and adds new right-click options to File Explorer.</caps:sentence>
            <caps:sentence id="src434" class="srcSentence"> For more information, see the <externalLink><linkText>Rights Management sharing application administrator guide</linkText><linkUri>http://technet.microsoft.com/library/ dn339003(v=ws.10).aspx</linkUri></externalLink>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src435" class="srcSentence">In addition, you might consider the following to help you monitor the RMS connector and your organization’s usage of Azure RMS:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src436" class="srcSentence">The built-in <ui>Microsoft Rights Management connector</ui> performance counters.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src437" class="srcSentence">The <externalLink><linkText>RMS Analyzer tool</linkText><linkUri>https://www.microsoft.com/en-us/download/details.aspx?id=46437</linkUri></externalLink>, using the RMS connector option to help you monitor the health of the connector and identify any configuration issues.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <link xlink:href="a735f3f7-6eb2-4901-9084-8c3cd3a9087e">Log and analyze rights management usage</link>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src438" class="srcSentence">You can use the <link xlink:href="086600c2-c5d8-47ec-a4c0-c782e1797486">Azure Rights Management Deployment Roadmap</link> to check whether there are other configuration steps that you might want to do before you roll out <token>aad_rightsmanagement_1</token> to users and administrators.</caps:sentence>
            <caps:sentence id="src439" class="srcSentence"> If there are no other configuration steps that you need to do, see <link xlink:href="18564e4a-9364-4ed2-8f17-89d24fc0d878">Using Azure Rights Management</link> for operational guidance to support a successful deployment for your organization.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="206a0bfe-0912-4e0e-aa15-484b000b264c">Configuring rights management</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>