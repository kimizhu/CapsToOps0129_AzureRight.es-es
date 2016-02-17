---
title: Gu&#237;a de administrador de la aplicaci&#243;n de uso compartido Rights Management
ms.custom: na
ms.reviewer: na
ms.service: rights-management
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d9992e30-f3d1-48d5-aedc-4e721f7d7c25
---
# Gu&#237;a de administrador de la aplicaci&#243;n de uso compartido Rights Management
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="es-ES">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="65ae4ea5c782cf701f78fb27dbe1de56" id="tgt1" class="tgtSentence">Use la siguiente información si es responsable de la aplicación Microsoft Rights Management sharing en una red de empresa, o si desea más información técnica que la que aparece en <link xlink:href="eaf6d02c-aa36-4915-856e-49bb71ab1484">Microsoft Rights Management sharing application User's Guide</link> o en <externalLink><linkText>Preguntas frecuentes sobre la aplicación Microsoft Rights Management sharing para Windows</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=303971</linkUri></externalLink>:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <link xlink:href="d9992e30-f3d1-48d5-aedc-4e721f7d7c25#BKMK_ScriptedInstall">Automatic deployment for the Microsoft Rights Management sharing application</link>
            </para>
            <list class="bullet">
              <listItem>
                <para>
                  <link xlink:href="d9992e30-f3d1-48d5-aedc-4e721f7d7c25#BKMK_verifyscripted">Verifying installation success</link>
                </para>
              </listItem>
              <listItem>
                <para>
                  <link xlink:href="d9992e30-f3d1-48d5-aedc-4e721f7d7c25#BKMK_uninstallscripted">Uninstall commands </link>
                </para>
              </listItem>
              <listItem>
                <para>
                  <link xlink:href="d9992e30-f3d1-48d5-aedc-4e721f7d7c25#BKMK_SuppressAutomaticUpdates">Suppressing automatic updates</link>
                </para>
              </listItem>
              <listItem>
                <para>
                  <link xlink:href="#BKMK_DocumentTracking">Azure RMS only: Configuring document tracking</link>
                </para>
              </listItem>
              <listItem>
                <para>
                  <link xlink:href="d9992e30-f3d1-48d5-aedc-4e721f7d7c25#BKMK_FederatedDomains">AD RMS only: Support for multiple email domains within your organization </link>
                </para>
              </listItem>
            </list>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="d9992e30-f3d1-48d5-aedc-4e721f7d7c25#BKMK_AdminOverview">Technical overview for the Microsoft Rights Management sharing application </link>
            </para>
            <list class="bullet">
              <listItem>
                <para>
                  <link xlink:href="d9992e30-f3d1-48d5-aedc-4e721f7d7c25#BKMK_LevelsofProtection">Levels of protection – native and generic</link>
                </para>
              </listItem>
              <listItem>
                <para>
                  <link xlink:href="d9992e30-f3d1-48d5-aedc-4e721f7d7c25#BKMK_SupportFileTypes">Supported file types and file name extensions</link>
                </para>
              </listItem>
              <listItem>
                <para>
                  <link xlink:href="d9992e30-f3d1-48d5-aedc-4e721f7d7c25#BKMK_ChangeDefaultProtection">Changing the default protection level of files</link>
                </para>
              </listItem>
            </list>
          </listItem>
        </list>
        <alert class="tip">
          <para>
            <caps:sentence sentenceid="27a149f3ee36536a5163bfc78a738f02" id="tgt2" class="tgtSentence">Si está familiarizado con la aplicación RMS sharing o desea obtener más información, consulte <externalLink><linkText>Cómo RMS protege todos los tipos de archivo mediante la aplicación RMS sharing</linkText><linkUri>https://curah.microsoft.com/191031/how-rms-protects-all-file-types-by-using-the-rms-sharing-app</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence sentenceid="d7a996ad80c8305c239d39e19d6190d7" id="tgt3" class="tgtSentence">La aplicación RMS resulta más adecuada para trabajar con Azure RMS, puesto que esta configuración de implementación admite el envío de datos adjuntos protegidos a los usuarios de otra organización, así como opciones tales como notificaciones por correo electrónico y seguimiento de documentos con revocación.</caps:sentence>
          <caps:sentence sentenceid="67d6660adbe37bc05c90a311f49004b4" id="tgt4" class="tgtSentence">  Sin embargo, también funciona con la versión local, AD RMS, pero con algunas limitaciones.</caps:sentence>
          <caps:sentence sentenceid="3599327c14976d3146c775bda4f815ae" id="tgt5" class="tgtSentence"> Para obtener una comparación exhaustiva de las características que son compatibles con Azure RMS y AD RMS, consulte <externalLink><linkText>Comparación de Azure Rights Management y AD RMS</linkText><linkUri>https://technet.microsoft.com/library/jj739831.aspx</linkUri></externalLink>.</caps:sentence>
          <caps:sentence sentenceid="f8ab519a3a349c3139ac89d62148dd32" id="tgt6" class="tgtSentence"> Si tiene AD RMS y quiere migrar a Azure RMS, consulte <externalLink><linkText>Migración de AD RMS a Azure Rights Management</linkText><linkUri>https://technet.microsoft.com/library/dn858447.aspx</linkUri></externalLink>.</caps:sentence>
        </para>
      </introduction>
      <section DoNotNumber="false" address="BKMK_ScriptedInstall">
        <title>
          <caps:sentence sentenceid="c62510e6143b57a4dd1bebee1ac6c492" id="tgt7" class="tgtSentence">Implementación automática de la aplicación Microsoft Rights Management sharing</caps:sentence>
        </title>
        <content>
          <para></para>
          <para>
            <caps:sentence sentenceid="229ccb8ea0b4cc16be94400f09fabc22" id="tgt8" class="tgtSentence">La versión de Windows de la aplicación RMS sharing admite una instalación con scripts, lo que la convierte en adecuada para las implementaciones empresariales.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="246c9488e228f4943e2b2b2fd2ef2eed" id="tgt9" class="tgtSentence">Los únicos requisitos previos para las instalaciones son que los equipos ejecuten una versión mínima de Windows 7 Service Pack 1 y que esté instalado Microsoft Framework, versión mínima 4.0.</caps:sentence>
            <caps:sentence sentenceid="c18f026fc314206a26e09c5d0f61080f" id="tgt10" class="tgtSentence"> Si necesita instalar Microsoft .NET Framework 4.0, puede <externalLink><linkText>descargarlo para la instalación desde el Centro de descarga de Microsoft</linkText><linkUri>http://www.microsoft.com/download/details.aspx?id=17718</linkUri></externalLink>.</caps:sentence>
          </para>
          <procedure>
            <title>
              <caps:sentence sentenceid="146cb87f494aa70f35d1f6a4d7b90b30" id="tgt11" class="tgtSentence">Para descargar la aplicación RMS sharing para la implementación automática</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="45568fffc1aefb85bb60ebc96a472dda" id="tgt12" class="tgtSentence">Vaya a la página <externalLink><linkText>Aplicación Microsoft Rights Management sharing para Windows</linkText><linkUri>http://www.microsoft.com/download/details.aspx?id=40857</linkUri></externalLink> en el Centro de descarga de Microsoft y haga clic en <ui>Descargar</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="132dd4844e649a6407513f807e98541c" id="tgt13" class="tgtSentence">Seleccione y descargue los archivos que necesita.</caps:sentence>
                    <caps:sentence sentenceid="0f4e5b7d8619509363ac0ec4d22a9f74" id="tgt14" class="tgtSentence"> Hay dos paquetes de instalación de cliente: uno para Windows de 64 bits (Microsoft Rights Management sharing application x64.zip) y otro para Windows de 32 bits (Microsoft Rights Management sharing application x86.zip).</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="8b35be3a6b81aea89539e2ffab22aabc" id="tgt15" class="tgtSentence">Extraiga los archivos de los paquetes de instalación comprimidos haciendo doble clic en ellos, por ejemplo.</caps:sentence>
                    <caps:sentence sentenceid="65f53aaa4a049595aece42b22488ae3b" id="tgt16" class="tgtSentence"> A continuación, copie los archivos extraídos en una ubicación de red a la que puedan tener acceso los equipos cliente.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
          <para>
            <caps:sentence sentenceid="e88953770092460e2631754541f01c06" id="tgt17" class="tgtSentence">Los paquetes de instalación de la aplicación RMS sharing admiten distintos escenarios de implementación e incluyen lo siguiente:</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt18" class="tgtSentence">Descripción</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="667d518c49e2a3f824b875943d31523d" id="tgt19" class="tgtSentence">Escenario de implementación</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="605f617c3289f94f057750d32c8bdf09" id="tgt20" class="tgtSentence">Ayudante para el inicio de sesión en línea de Microsoft</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="bf2b78fe6713d619bcb5f552409a74a8" id="tgt21" class="tgtSentence">Necesario para lo siguiente:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="724f2e5c097347476fa82c18a42c695a" id="tgt22" class="tgtSentence">Office 2010 y Azure RMS</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="7278735204b67214f718c46f24e423ba" id="tgt23" class="tgtSentence"> Office 2013 y Azure RMS si no ha instalado la <externalLink><linkText>actualización del 9 de junio de 2015 para Office 2013</linkText><linkUri>https://support.microsoft.com/kb/3054853</linkUri></externalLink> (KB3054853) </caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f537cb3218f92fbf32d2d2d6aee2b67c" id="tgt24" class="tgtSentence">Revisión para Office (KB 2596501)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="bf2b78fe6713d619bcb5f552409a74a8" id="tgt25" class="tgtSentence">Necesario para lo siguiente:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="724f2e5c097347476fa82c18a42c695a" id="tgt26" class="tgtSentence">Office 2010 y Azure RMS</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="25ecc218ba9ad01b8be8f6b6f8786d8a" id="tgt27" class="tgtSentence">Office 2010 y Active Directory RMS</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="dd59467738778e4ef427c9006b0042af" id="tgt28" class="tgtSentence">Revisión para permitir que el cliente de AD RMS 1.0 funcione con Azure RMS (KB 2843630 KB)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="bf2b78fe6713d619bcb5f552409a74a8" id="tgt29" class="tgtSentence">Necesario para lo siguiente:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="6d475172c2b404a3aa483c021606a009" id="tgt30" class="tgtSentence">Office 2010 y Azure RMS</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="25ecc218ba9ad01b8be8f6b6f8786d8a" id="tgt31" class="tgtSentence">Office 2010 y Active Directory RMS</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="504003788634c6ba2fec64d7735515bc" id="tgt32" class="tgtSentence">El cliente de AD RMS y la aplicación RMS sharing</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="bf2b78fe6713d619bcb5f552409a74a8" id="tgt33" class="tgtSentence">Necesario para lo siguiente:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="35d0e569d3f653c83d036e18e5e21030" id="tgt34" class="tgtSentence">Office 2016 u Office 2013 y Azure RMS o Active Directory RMS</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="218cf8ee0d59d320bb13e9328d725311" id="tgt35" class="tgtSentence">Office 2010 y Azure RMS </caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="534f1cf4c58abfa6d037835ba6f4b142" id="tgt36" class="tgtSentence">Office 2010 y Active Directory RMS</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="d503b72c023c12affc3d42796fcf1c3f" id="tgt37" class="tgtSentence">Aplicación RMS sharing y solo el complemento de Office</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d00bac8e70b86ad848948a3904aa2e53" id="tgt38" class="tgtSentence">Complemento de Office de la cinta de opciones</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="bf2b78fe6713d619bcb5f552409a74a8" id="tgt39" class="tgtSentence">Necesario para lo siguiente:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="35d0e569d3f653c83d036e18e5e21030" id="tgt40" class="tgtSentence">Office 2016 u Office 2013 y Azure RMS o Active Directory RMS</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="724f2e5c097347476fa82c18a42c695a" id="tgt41" class="tgtSentence">Office 2010 y Azure RMS</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="25ecc218ba9ad01b8be8f6b6f8786d8a" id="tgt42" class="tgtSentence">Office 2010 y Active Directory RMS</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="d503b72c023c12affc3d42796fcf1c3f" id="tgt43" class="tgtSentence">Aplicación RMS sharing y solo el complemento de Office</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5e58d27d45b0bf2d3cd9ff046562624b" id="tgt44" class="tgtSentence">Herramienta de preparación de Azure Active Directory Rights Management</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="bf2b78fe6713d619bcb5f552409a74a8" id="tgt45" class="tgtSentence">Necesario para lo siguiente:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="724f2e5c097347476fa82c18a42c695a" id="tgt46" class="tgtSentence">Office 2010 y Azure RMS</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
              </tr>
            </tbody>
          </table>
          <para></para>
          <para>
            <caps:sentence sentenceid="bd927c133bf90ef2b6eb22416b2619e1" id="tgt47" class="tgtSentence">Use los siguientes procedimientos para identificar los comandos necesarios para implementar la aplicación RMS sharing en estos escenarios de implementación:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <embeddedLabel>
                  <caps:sentence sentenceid="5aa6b021774610a051334b319f60e3d3" id="tgt48" class="tgtSentence">Office 2016 u Office 2013 y Azure RMS o Active Directory RMS</caps:sentence>
                </embeddedLabel>
              </para>
              <para>
                <caps:sentence sentenceid="b2a9267cec96ef47e81255e6254384ce" id="tgt49" class="tgtSentence">Los usuarios ejecutan Office 2016 u Office 2013, su organización usa Azure RMS o Active Directory RMS y los usuarios colaborar con otras organizaciones que usan Azure RMS o Active Directory RMS.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <embeddedLabel>
                  <caps:sentence sentenceid="c686cdb2f6a62f64e13eee3b6ea0ffef" id="tgt50" class="tgtSentence">Office 2010 y Azure RMS</caps:sentence>
                </embeddedLabel>
              </para>
              <para>
                <caps:sentence sentenceid="792776d56f7a6e8e7b1af430800407a3" id="tgt51" class="tgtSentence">Los usuarios ejecutan Office 2010, su organización usa Azure RMS o Active Directory RMS y los usuarios colaboran con otras organizaciones que usan Azure RMS o Active Directory RMS.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <embeddedLabel>
                  <caps:sentence sentenceid="534f1cf4c58abfa6d037835ba6f4b142" id="tgt52" class="tgtSentence">Office 2010 y Active Directory RMS</caps:sentence>
                </embeddedLabel>
              </para>
              <para>
                <caps:sentence sentenceid="dc404c40bdfaadc5fdd904c8b5054084" id="tgt53" class="tgtSentence">Los usuarios ejecutan Office 2010, su organización usa Azure RMS o Active Directory RMS y los usuarios colaboran con otras organizaciones que usan Azure RMS o Active Directory RMS.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <embeddedLabel>
                  <caps:sentence sentenceid="d503b72c023c12affc3d42796fcf1c3f" id="tgt54" class="tgtSentence">Aplicación RMS sharing y solo el complemento de Office</caps:sentence>
                </embeddedLabel>
              </para>
              <para>
                <caps:sentence sentenceid="61cac39bed8e940d0cd14cb8c194065b" id="tgt55" class="tgtSentence">Los usuarios ejecutan Office 2016, Office 2013 u Office 2010, su organización usa Azure RMS o Active Directory RMS y los usuarios no necesitan colaboran con otras organizaciones que usan Azure RMS.</caps:sentence>
                <caps:sentence sentenceid="f1432cb7ea09b872513dbcf89df965cd" id="tgt56" class="tgtSentence"> Esta instalación le permite instalar solamente la aplicación de uso compartido y el complemento de Office.</caps:sentence>
              </para>
            </listItem>
          </list>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="0ab5ef8e5eaa86501c3d5fd9f62741c8" id="tgt57" class="tgtSentence">En estos casos, si su organización ejecuta AD RMS, los usuarios pueden recibir contenido protegido de otras organizaciones que usan Azure RMS, pero los usuarios no pueden enviar contenido protegido a los usuarios de una organización que usa Azure RMS.</caps:sentence>
              <caps:sentence sentenceid="4073e51f967d7c10a71435eeba49188e" id="tgt58" class="tgtSentence"> Sin embargo, si su organización ejecuta Azure RMS, los usuarios pueden enviar y recibir contenido protegido de otras organizaciones.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence sentenceid="1ae6b34c66cbe690b72a743f2ec9dbad" id="tgt59" class="tgtSentence">Para completar la instalación de cada procedimiento, debe reiniciar el equipo.</caps:sentence>
            <caps:sentence sentenceid="603166023aa5bed1a484eca7e2985300" id="tgt60" class="tgtSentence"> Puede iniciar un reinicio automático mediante un comando como shutdown /i.</caps:sentence>
          </para>
          <procedure expanded="false">
            <title>
              <caps:sentence sentenceid="97f3b1b1cd92995f491ab1bdead9050b" id="tgt61" class="tgtSentence">Para implementar la aplicación RMS sharing para Office 2016 u Office 2013 y Azure RMS o Active Directory RMS</caps:sentence>
            </title>
            <steps class="bullet">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="3f170c70acc590a565e1546f8ee9d9d4" id="tgt62" class="tgtSentence">En cada equipo en el que quiera instalar la aplicación RMS sharing y los componentes relacionados, ejecute el siguiente comando con privilegios elevados:</caps:sentence>
                  </para>
                  <code>setup.exe /s</code>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence sentenceid="a67c01c6792b0af5eaec05a8236b246d" id="tgt63" class="tgtSentence">Para comprobar que se ejecuta correctamente, consulte la sección <link xlink:href="d9992e30-f3d1-48d5-aedc-4e721f7d7c25#BKMK_verifyscripted">Verifying installation success</link> de este tema.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
          <procedure expanded="false">
            <title>
              <caps:sentence sentenceid="814d83cf307b7655d1f87db736364e44" id="tgt64" class="tgtSentence">Para implementar la aplicación RMS sharing para Office 2010 y Azure RMS</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="966fe36f12eb39f47e9142fe82738c42" id="tgt65" class="tgtSentence">Debe ser el administrador global del inquilino de Office 365 o Azure Active Directory para poder obtener la dirección URL del servicio de certificación de su organización mediante la ejecución de la herramienta de preparación Azure Active Directory Rights Management.</caps:sentence>
                    <caps:sentence sentenceid="acdf634f357de6efda621106b967b0be" id="tgt66" class="tgtSentence"> Debe ejecutar esta herramienta solo una vez, en un único equipo.</caps:sentence>
                    <caps:sentence sentenceid="ec11d0fa6e8d674f9ff01a55124c9abc" id="tgt67" class="tgtSentence"> Usará la dirección URL del servicio de certificación al instalar la aplicación RMS sharing en cada equipo:</caps:sentence>
                  </para>
                  <list class="ordered">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="cb4c43da03ea50d5f290f4857c80a9af" id="tgt68" class="tgtSentence">Inicie sesión un equipo con una cuenta de administrador local.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="75952a005aaa8cc73cd3c0b8063434df" id="tgt69" class="tgtSentence">En ese equipo, <externalLink><linkText>descargue e instale el Ayudante para el inicio de sesión de Microsoft Online</linkText><linkUri>http://www.microsoft.com/download/details.aspx?id=28177</linkUri></externalLink>.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="a01fe45e132c26f887b79d47d998017a" id="tgt70" class="tgtSentence">Ejecute el siguiente comando para mostrar en la pantalla la dirección URL del servicio de certificación, que luego puede copiar y guardar para el siguiente paso:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="70facb5955dfc7cec756833724e442c2" id="tgt71" class="tgtSentence">Para Windows 8.1 y Windows 8, 64 bits:</caps:sentence>
                          </para>
                          <code>x64\aadrmprep.exe /findCertificationUrl /logfile "&lt;log file path and name&gt;"</code>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="c12524190d912f72a57af6f412f5b7e7" id="tgt72" class="tgtSentence">Para Windows 8.1 y Windows 8, 64 bits:</caps:sentence>
                          </para>
                          <code>X86\aadrmprep.exe /findCertificationUrl /logfile "&lt;log file path and name&gt;"</code>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="e07042d32d148b7e5ee13166c469769a" id="tgt73" class="tgtSentence">Para Windows 7, 64 bits:</caps:sentence>
                          </para>
                          <code>x64\win7\aadrmprep.exe /findCertificationUrl /logfile "&lt;log file path and name&gt;"</code>
                        </listItem>
                      </list>
                      <alert class="note">
                        <para>
                          <caps:sentence sentenceid="0d8738ba96bec3e5ea0b7c7864db38a5" id="tgt74" class="tgtSentence">Este comando podría solicitarle que especifique sus credenciales de Azure.</caps:sentence>
                          <caps:sentence sentenceid="266fb22722a87de0f8e77755d7e9a626" id="tgt75" class="tgtSentence"> Si el equipo no está unido a un dominio, se le pedirán.</caps:sentence>
                          <caps:sentence sentenceid="eb3faeec7623f85240e0f19cbcd0e9b3" id="tgt76" class="tgtSentence"> Si el equipo está unido a un dominio, es posible que la herramienta pueda usar las credenciales almacenadas en caché.</caps:sentence>
                        </para>
                      </alert>
                    </listItem>
                  </list>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="99bb1096710ebbc381357634c75473cf" id="tgt77" class="tgtSentence">En cada equipo en el que vaya a instalar la aplicación RMS sharing y los componentes relacionados, ejecute el siguiente comando con privilegios elevados:</caps:sentence>
                  </para>
                  <code>setup.exe /s /configureO2010Admin /certificationUrl &lt;certification_url&gt;</code>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="bfd845bd61de1085a1f080bd46722534" id="tgt78" class="tgtSentence">En cada equipo en el que vaya a instalar la aplicación RMS sharing y los componentes relacionados, ejecute el siguiente comando (no necesita privilegios elevados).</caps:sentence>
                    <caps:sentence sentenceid="65eeffbf28dba5f60a6fed184fdcb6f4" id="tgt79" class="tgtSentence"> Esto se puede hacer de diferentes maneras, como por ejemplo, pedir al usuario que ejecute el comando (desde un vínculo en un mensaje de correo electrónico o un vínculo en el portal del servicio de asistencia), o bien puede agregarlo a su script de inicio de sesión:</caps:sentence>
                  </para>
                  <code>bin\RMSSetup.exe /configureO2010Only</code>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence sentenceid="a67c01c6792b0af5eaec05a8236b246d" id="tgt80" class="tgtSentence">Para comprobar que se ejecuta correctamente, consulte la sección <link xlink:href="d9992e30-f3d1-48d5-aedc-4e721f7d7c25#BKMK_verifyscripted">Verifying installation success</link> de este tema.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
          <procedure expanded="false">
            <title>
              <caps:sentence sentenceid="d6975305c7272e72d4282e4cd3fb4ff8" id="tgt81" class="tgtSentence">Para implementar la aplicación RMS sharing para Office 2010 y Active Directory RMS</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="99bb1096710ebbc381357634c75473cf" id="tgt82" class="tgtSentence">En cada equipo en el que vaya a instalar la aplicación RMS sharing y los componentes relacionados, ejecute el siguiente comando con privilegios elevados:</caps:sentence>
                  </para>
                  <code>setup.exe /s /configureO2010Admin</code>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="bfd845bd61de1085a1f080bd46722534" id="tgt83" class="tgtSentence">En cada equipo en el que vaya a instalar la aplicación RMS sharing y los componentes relacionados, ejecute el siguiente comando (no necesita privilegios elevados).</caps:sentence>
                    <caps:sentence sentenceid="65eeffbf28dba5f60a6fed184fdcb6f4" id="tgt84" class="tgtSentence"> Esto se puede hacer de diferentes maneras, como por ejemplo, pedir al usuario que ejecute el comando (desde un vínculo en un mensaje de correo electrónico o un vínculo en el portal del servicio de asistencia), o bien puede agregarlo a su script de inicio de sesión:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="959f8c9d27eeaebe8bfe036a9b7e92a8" id="tgt85" class="tgtSentence">Para Windows 10, Windows 8.1 y Windows 8, 64 bits:</caps:sentence>
                      </para>
                      <code>x64\aadrmprep.exe /configureO2010</code>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="82d63ea53d45e6910b9e8f9ac7f1d67e" id="tgt86" class="tgtSentence">Para Windows 10, Windows 8.1 y Windows 8, 32 bits:</caps:sentence>
                      </para>
                      <code>X86\aadrmprep.exe /configureO2010</code>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="e07042d32d148b7e5ee13166c469769a" id="tgt87" class="tgtSentence">Para Windows 7, 64 bits:</caps:sentence>
                      </para>
                      <code>x64\win7\aadrmpep.exe /configureO2010</code>
                    </listItem>
                  </list>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence sentenceid="a67c01c6792b0af5eaec05a8236b246d" id="tgt88" class="tgtSentence">Para comprobar que se ejecuta correctamente, consulte la sección <link xlink:href="d9992e30-f3d1-48d5-aedc-4e721f7d7c25#BKMK_verifyscripted">Verifying installation success</link> de este tema.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
          <procedure expanded="false">
            <title>
              <caps:sentence sentenceid="2e536673835d7b4e70838e0445dfc367" id="tgt89" class="tgtSentence">Para instalar la aplicación RMS sharing y solo el complemento de Office</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="e972d5d1b7e997906f9a69d96b96335c" id="tgt90" class="tgtSentence">Instale el cliente de AD RMS y la aplicación RMS sharing mediante el siguiente comando:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="723ca82e68af8625a428fa8a369d2381" id="tgt91" class="tgtSentence">Para Windows de 64 bits: </caps:sentence>
                      </para>
                      <code>x64\setup_ipviewer.exe /norestart /quiet /msicl "MSIRESTARTMANAGERCONTROL=Disable" /log "&lt;log file path and name&gt;"</code>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="b47eb9efbe042a4b3fa81ed86c8a201e" id="tgt92" class="tgtSentence">Para Windows de 32 bits: </caps:sentence>
                      </para>
                      <code>X86\setup_ipviewer.exe /norestart /quiet /msicl "MSIRESTARTMANAGERCONTROL=Disable" /log "&lt;log file path and name&gt;"</code>
                    </listItem>
                  </list>
                  <para></para>
                  <para>
                    <caps:sentence sentenceid="d05370276e06291b048268558cc39bee" id="tgt93" class="tgtSentence">Por ejemplo: <codeInline>\\server5\apps\rms\x64\setup_ipviewer.exe /norestart /quiet /msicl "MSIRESTARTMANAGERCONTROL=Disable" /log "C:\Log files\ipviewerinstall.log"</codeInline></caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="3eadbcb1fd72019040b54e1e41a95a16" id="tgt94" class="tgtSentence">Instale el complemento de Office mediante los siguientes comandos:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="d665073860569ff6e68df42ae6adced0" id="tgt95" class="tgtSentence">Para la versión de Office de 64 bits: </caps:sentence>
                      </para>
                      <code>msiexec.exe /norestart /quiet MSIRESTARTMANAGERCONTROL=Disable /i "x64\Setup64.msi" /L*v "&lt;log file path and name&gt;"</code>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="10eabac6b35fdcf2dc3f66013f04a01e" id="tgt96" class="tgtSentence">Para la versión de Office de 32 bits: </caps:sentence>
                      </para>
                      <code>msiexec.exe /norestart /quiet MSIRESTARTMANAGERCONTROL=Disable /i "x86\Setup.msi" /L*v "&lt;log file path and name&gt;"</code>
                    </listItem>
                  </list>
                  <para></para>
                  <para>
                    <caps:sentence sentenceid="d05370276e06291b048268558cc39bee" id="tgt97" class="tgtSentence">Por ejemplo: <codeInline>\\server5\apps\rms\msiexec.exe /norestart /quiet MSIRESTARTMANAGERCONTROL=Disable /i "x64\Setup64.msi" /L*v "C:\Log files\rmsofficeinstall.log"</codeInline></caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence sentenceid="a67c01c6792b0af5eaec05a8236b246d" id="tgt98" class="tgtSentence">Para comprobar que se ejecuta correctamente, consulte la sección <link xlink:href="d9992e30-f3d1-48d5-aedc-4e721f7d7c25#BKMK_verifyscripted">Verifying installation success</link> de este tema.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
        </content>
        <sections>
          <section address="BKMK_verifyscripted">
            <title>
              <caps:sentence sentenceid="5df0a5b45c76efa48355fdf9c7caf2be" id="tgt99" class="tgtSentence">Comprobación de que la instalación se ha realizado correctamente</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="96f0b5360c425363694d422f9317b242" id="tgt100" class="tgtSentence">Puede usar los archivos de registro de instalación para comprobar si la instalación se realizó correctamente.</caps:sentence>
              </para>
              <procedure expanded="false">
                <title>
                  <caps:sentence sentenceid="a8594443bb6f32e77039d302c018ed2a" id="tgt101" class="tgtSentence">Para comprobar que la instalación de la aplicación RMS sharing para Office 2016 u Office 2013 y Azure RMS o Active Directory RMS se ha realizado correctamente</caps:sentence>
                </title>
                <steps class="bullet">
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="855d9215572be78fb096d75890f8bd63" id="tgt102" class="tgtSentence">Para comprobar que el comando Setup.exe se ha ejecutado correctamente, busque en cada equipo el archivo de registro de instalación <ui>RMInstaller.log</ui> en la carpeta <placeholder>%temp%\RMS_installer_&lt;guid&gt;</placeholder> y, luego, identifique el código de salida.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="3fdb8e45e7b59265e4e53cf42c898678" id="tgt103" class="tgtSentence">Una instalación correcta tiene un código de salida de 0 y cualquier otro número indica un error en la instalación.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="6bd85dcec8f2f3aad9819f95c0e954ab" id="tgt104" class="tgtSentence">Nombre de archivo de registro de ejemplo: <ui>C:\temp\RMS_Installer_9352fc91-1982-43bf-958a-2ef1fe9c2ed0\RMInstaller.log</ui> </caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
              <procedure expanded="false">
                <title>
                  <caps:sentence sentenceid="f03a80f811dea563a6fea7e96e08ddab" id="tgt105" class="tgtSentence">Para comprobar que la instalación de la aplicación RMS sharing para Office 2010 y Azure RMS se ha realizado correctamente</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="855d9215572be78fb096d75890f8bd63" id="tgt106" class="tgtSentence">Para comprobar que el comando Setup.exe se ha ejecutado correctamente, busque en cada equipo el archivo de registro de instalación <ui>RMInstaller.log</ui> en la carpeta <placeholder>%temp%\RMS_installer_&lt;guid&gt;</placeholder> y, luego, identifique el código de salida.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="3fdb8e45e7b59265e4e53cf42c898678" id="tgt107" class="tgtSentence">Una instalación correcta tiene un código de salida de 0 y cualquier otro número indica un error en la instalación.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="6bd85dcec8f2f3aad9819f95c0e954ab" id="tgt108" class="tgtSentence">Nombre de archivo de registro de ejemplo: <ui>C:\temp\RMS_Installer_9352fc91-1982-43bf-958a-2ef1fe9c2ed0</ui> </caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="e1661f875a214f1f846d40f873ce88b3" id="tgt109" class="tgtSentence">Para comprobar que el comando RMSSetup.exe se ha ejecutado correctamente, el usuario debe tener los siguientes archivos creados en su carpeta <placeholder>%localappdata%\microsoft\drm</placeholder>:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="b2b1fd8e1186b6def08a273b2bb5a83a" id="tgt110" class="tgtSentence">CERT-Machine-2048.drm</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="17a52ac8e99f53a78a3b3003e239c209" id="tgt111" class="tgtSentence">CERT-Machine.drm</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="750ac51215b7789a106d5290fc2550cb" id="tgt112" class="tgtSentence">CLC-*.drm</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="be436bf316ced4cf2ae5e6c9b829c240" id="tgt113" class="tgtSentence">GIC-*.drm</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                      <para></para>
                      <para>
                        <caps:sentence sentenceid="d6a8f3213d4a7ca74816024d0841a081" id="tgt114" class="tgtSentence">Ejemplo de un archivo CLC-*.drm: </caps:sentence>
                      </para>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="ddbe4093e6c323910bdd69b2655280cc" id="tgt115" class="tgtSentence">CLC-alice@isvtenant999.onmicrosoft.com-{1b9cfccf;k5b11;k4a10;kac15;k29b2b6980f4c}.drm</caps:sentence>
                        </ui>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
              <procedure expanded="false">
                <title>
                  <caps:sentence sentenceid="c4fc3f5ac159c6c570ca54487450f1d3" id="tgt116" class="tgtSentence">Para comprobar que la instalación de la aplicación RMS sharing para Office 2010 y Active Directory RMS se ha realizado correctamente</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="9cc57d876892faad65f99990ca739914" id="tgt117" class="tgtSentence">Para comprobar que el comando Setup.exe se ha ejecutado correctamente, busque en cada equipo el archivo de registro de instalación en la carpeta <placeholder>%temp%\RMS_installer_&lt;guid&gt;</placeholder> e identifique el código de salida.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="3fdb8e45e7b59265e4e53cf42c898678" id="tgt118" class="tgtSentence">Una instalación correcta tiene un código de salida de 0 y cualquier otro número indica un error en la instalación.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="6bd85dcec8f2f3aad9819f95c0e954ab" id="tgt119" class="tgtSentence">Nombre de archivo de registro de ejemplo: <ui>C:\temp\RMS_Installer_9352fc91-1982-43bf-958a-2ef1fe9c2ed0</ui> </caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="f6a94f456d59e953383a2aba4c4970d6" id="tgt120" class="tgtSentence">Para comprobar que el comando aadrmprep.exe se ha ejecutado correctamente, busque en cada equipo el siguiente texto en el archivo de registro de instalación: <ui>aadrmprep.exe exited with status SUCCESS</ui></caps:sentence>
                      </para>
                      <alert class="note">
                        <para>
                          <caps:sentence sentenceid="8ce06f66a46075b3072c3c9563823a0a" id="tgt121" class="tgtSentence">En ocasiones, la instalación puede ejecutarse dos veces; la primera vez resulta incorrecta y la segunda correcta.</caps:sentence>
                        </para>
                      </alert>
                      <para>
                        <caps:sentence sentenceid="e0f895ebf550ebc6bd1a1ed647ddeec6" id="tgt122" class="tgtSentence">Si quiere comprobar manualmente los cambios que realiza esta herramienta en el Registro, son estos:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="b047176b0add832167cefeda3e316604" id="tgt123" class="tgtSentence">[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MSDRM\Federation]</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence sentenceid="194808ad2d9704b27b717ac2f2b08904" id="tgt124" class="tgtSentence">"FederationHomeRealm"="urn:HostedRmsOnlineService:Certification"</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="928e5c5212709c528f5f5b7a50caed02" id="tgt125" class="tgtSentence">[HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\MSDRM\Federation]</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence sentenceid="194808ad2d9704b27b717ac2f2b08904" id="tgt126" class="tgtSentence">"FederationHomeRealm"="urn:HostedRmsOnlineService:Certification"</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="2bd4851276ecae1a0ff067ac1a0c6fed" id="tgt127" class="tgtSentence">[HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\MSDRM\ServiceLocation\Activation]</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence sentenceid="947746487ce45027f0955980184fd02e" id="tgt128" class="tgtSentence">@="&lt;certification url&gt;"
</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="4eb147456e1dd112daf29f9fd52708a8" id="tgt129" class="tgtSentence">[HKEY_CURRENT_USER\SOFTWARE\Microsoft\Office\14.0\Common\DRM] 
</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence sentenceid="2672ffcd3b5bc21a01fba0fa8eb4db61" id="tgt130" class="tgtSentence">DefaultUser="&lt;default_user&gt;"</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </content>
                  </step>
                </steps>
              </procedure>
              <procedure expanded="false">
                <title>
                  <caps:sentence sentenceid="e1220f81eb7888b3ed627171808351ff" id="tgt131" class="tgtSentence">Para comprobar que la instalación de la aplicación RMS sharing y solo el complemento de Office se ha realizado correctamente</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="f6101a200d9e8ba8e40cbdaf70290654" id="tgt132" class="tgtSentence">Para comprobar que el comando Setup_ipviewer.exe se ha ejecutado correctamente, busque el siguiente texto en el archivo de registro de instalación: <ui>Installation success or error status: 0</ui></caps:sentence>
                      </para>
                      <para></para>
                      <para>
                        <caps:sentence sentenceid="a1eb6bbf55b94d4940b42e6dcdf89aba" id="tgt133" class="tgtSentence">Líneas de ejemplo de una instalación correcta:  </caps:sentence>
                      </para>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="7e9e685718462bbbf972db02e803ecb9" id="tgt134" class="tgtSentence">MSI (s) (F0:B8) [14:19:57:854]: Product: Active Directory Rights Management Services Client 2.1 -- Installation completed successfully.</caps:sentence>
                        </ui>
                      </para>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="422be4c7e6bfd298c859fa8c9be4e1d6" id="tgt135" class="tgtSentence">MSI (s) (F0:B8) [14:19:57:854]: Windows Installer installed the product.</caps:sentence>
                          <caps:sentence sentenceid="b675cd8f6f876f02a4afb9ce541a6fac" id="tgt136" class="tgtSentence"> Product Name: Active Directory Rights Management Services Client 2.1.</caps:sentence>
                          <caps:sentence sentenceid="d2a443c81d0519141e2ce9b7bbba13f8" id="tgt137" class="tgtSentence"> Product Version: 1.0.1179.1.</caps:sentence>
                          <caps:sentence sentenceid="fc77f42cb990a18a7025bfc178b78fa9" id="tgt138" class="tgtSentence"> Product Language: 1033.</caps:sentence>
                          <caps:sentence sentenceid="97eec2f11eba207e830bd73a6400d463" id="tgt139" class="tgtSentence"> Fabricante: Microsoft Corporation</caps:sentence>
                          <caps:sentence sentenceid="c0b7c290e93c604bd0aa4f7d6f087d11" id="tgt140" class="tgtSentence"> Resultado de la instalación: 0.</caps:sentence>
                        </ui>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="4064de39b2f00b6feb81f5be4c44994b" id="tgt141" class="tgtSentence">Para comprobar que el complemento de Office se ha instalado correctamente, busque el siguiente texto en el archivo de registro de instalación: <ui>Installation success or error status: 0</ui></caps:sentence>
                      </para>
                      <para></para>
                      <para>
                        <caps:sentence sentenceid="a1eb6bbf55b94d4940b42e6dcdf89aba" id="tgt142" class="tgtSentence">Líneas de ejemplo de una instalación correcta:  </caps:sentence>
                      </para>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="f823afd362b1d6633ef6b7f01912cded" id="tgt143" class="tgtSentence">MSI (s) (9C:88) [18:49:04:007]: Product: Microsoft RMS Office Addins -- Installation completed successfully.</caps:sentence>
                        </ui>
                      </para>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="d4fdc0a0123c78517b326a546595b02e" id="tgt144" class="tgtSentence">MSI (s) (9C:88) [18:49:04:007]: Windows Installer installed the product.</caps:sentence>
                          <caps:sentence sentenceid="592958547205d14b4d56737eaa56afb0" id="tgt145" class="tgtSentence"> Product Name: Microsoft RMS Office Addins.</caps:sentence>
                          <caps:sentence sentenceid="9727e342d39caac79b9cbf3562b5f80d" id="tgt146" class="tgtSentence"> Product Version: 1.0.7.</caps:sentence>
                          <caps:sentence sentenceid="fc77f42cb990a18a7025bfc178b78fa9" id="tgt147" class="tgtSentence"> Product Language: 1033.</caps:sentence>
                          <caps:sentence sentenceid="3c017c5d5908433e7e878948a194c3bd" id="tgt148" class="tgtSentence"> Fabricante: Microsoft.</caps:sentence>
                          <caps:sentence sentenceid="c0b7c290e93c604bd0aa4f7d6f087d11" id="tgt149" class="tgtSentence"> Installation success or error status: 0.</caps:sentence>
                        </ui>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
            </content>
          </section>
          <section address="BKMK_uninstallscripted">
            <title>
              <caps:sentence sentenceid="da364dab94b5bf34bc33feb74582d474" id="tgt150" class="tgtSentence">Comandos de desinstalación </caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="a9d5e76ef7af34024cc8b5edbe3b1c7d" id="tgt151" class="tgtSentence">No todos los comandos de instalación necesarios para estas implementaciones admiten un comando de desinstalación.</caps:sentence>
                <caps:sentence sentenceid="49c0002ff6c1b4efa35b608fb4ac2b08" id="tgt152" class="tgtSentence"> Puede desinstalar el cliente de AD RMS y la aplicación de uso compartido, y puede desinstalar el complemento de Office.</caps:sentence>
                <caps:sentence sentenceid="738fa90ee000697f31e6f050b30209e5" id="tgt153" class="tgtSentence"> Use los siguientes comandos para desinstalar estos elementos.</caps:sentence>
              </para>
              <procedure expanded="false">
                <title>
                  <caps:sentence sentenceid="4bafca31da44187413d354ab55d808e1" id="tgt154" class="tgtSentence">Para desinstalar el cliente de AD RMS y la aplicación RMS sharing</caps:sentence>
                </title>
                <steps class="bullet">
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="0aa2fd4c78c1b13433dc0de8214ee360" id="tgt155" class="tgtSentence">Use los siguientes comandos:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="723ca82e68af8625a428fa8a369d2381" id="tgt156" class="tgtSentence">Para Windows de 64 bits: </caps:sentence>
                          </para>
                          <code>x64\setup_ipviewer.exe /uninstall /quiet</code>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="b47eb9efbe042a4b3fa81ed86c8a201e" id="tgt157" class="tgtSentence">Para Windows de 32 bits: </caps:sentence>
                          </para>
                          <code>x86\setup_ipviewer.exe /uninstall /quiet</code>
                        </listItem>
                      </list>
                    </content>
                  </step>
                </steps>
              </procedure>
              <procedure expanded="false">
                <title>
                  <caps:sentence sentenceid="fd6cc016384fc173caa078e6780da55b" id="tgt158" class="tgtSentence">Para desinstalar el complemento de Office</caps:sentence>
                </title>
                <steps class="bullet">
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="0aa2fd4c78c1b13433dc0de8214ee360" id="tgt159" class="tgtSentence">Use los siguientes comandos:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="d665073860569ff6e68df42ae6adced0" id="tgt160" class="tgtSentence">Para la versión de Office de 64 bits: </caps:sentence>
                          </para>
                          <code>msiexec /x \x64\Setup[64].msi /quiet</code>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="10eabac6b35fdcf2dc3f66013f04a01e" id="tgt161" class="tgtSentence">Para la versión de Office de 32 bits: </caps:sentence>
                          </para>
                          <code>msiexec /x \x86\Setup.msi /quiet</code>
                        </listItem>
                      </list>
                    </content>
                  </step>
                </steps>
              </procedure>
            </content>
          </section>
          <section address="BKMK_SuppressAutomaticUpdates">
            <title>
              <caps:sentence sentenceid="32a43b7be365a5cafe5ad8c990bb5d25" id="tgt162" class="tgtSentence">Supresión de actualizaciones automáticas</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="d26a90e81189a4e2f1554b3e1f0ec5ab" id="tgt163" class="tgtSentence">De forma predeterminada, los usuarios reciben una notificación si hay una versión posterior de la aplicación RMS sharing y se les pide que la descarguen.</caps:sentence>
                <caps:sentence sentenceid="dc9500be350df119882a6232fd053022" id="tgt164" class="tgtSentence"> Puede suprimir esta notificación realizando el siguiente cambio en el Registro:</caps:sentence>
              </para>
              <list class="ordered">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="52a0a486115949d5009cfa2b41666228" id="tgt165" class="tgtSentence">Vaya a <ui>HKEY_LOCAL_MACHINE\Software\Microsoft\MSIPC</ui> y, si no aparece ya ahí, cree una nueva clave denominada <ui>RmsSharingApp</ui>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="3d28822ef6b543a688f36f914f7304b4" id="tgt166" class="tgtSentence">Seleccione <ui>RmsSharingApp</ui>, cree un nuevo valor DWORD de <ui>AllowUpdatePrompt</ui> y establezca el valor en <ui>0</ui>.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="5e22ebadae8277bc3bb834323f59352a" id="tgt167" class="tgtSentence">Dado que la aplicación RMS sharing no es compatible con WSUS, puede usar la siguiente técnica para probar las nuevas versiones de dicha aplicación antes de implementarla para todos los usuarios:</caps:sentence>
              </para>
              <list class="ordered">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="8039075a23caa6cc755b59509e90b2b7" id="tgt168" class="tgtSentence">En los equipos de todos los usuarios, ejecute un script para suprimir las actualizaciones automáticas.</caps:sentence>
                    <caps:sentence sentenceid="5e77491b96eaad52ecff3373aa200181" id="tgt169" class="tgtSentence"> En los equipos que usan los administradores para probar nuevas versiones, no ejecute este script.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="d75a646df3e1a3148f6eb220e93a59f4" id="tgt170" class="tgtSentence">Cuando hay disponible una nueva versión, los administradores la descargan y la prueban.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="64a9682a340f8a8c9415e903fb1394c9" id="tgt171" class="tgtSentence">Cuando la prueba está completa y los posibles problemas se han resuelto, implemente la versión más reciente para todos los usuarios mediante las instrucciones de implementación automática de esta guía.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
          <section address="BKMK_DocumentTracking">
            <title>
              <caps:sentence sentenceid="d475e9452c9173e5d5904c78e002c35f" id="tgt172" class="tgtSentence">Solo Azure RMS: configuración del seguimiento de documentos</caps:sentence>
            </title>
            <content>
              <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt173" class="tgtSentence">
                <para>Si tiene una <externalLink><linkText>suscripción que admite el seguimiento de documentos</linkText><linkUri>https://technet.microsoft.com/en-us/dn858608</linkUri></externalLink>, el sitio de seguimiento de documentos está habilitado de forma predeterminada para todos los usuarios de su organización.  El seguimiento de documentos mostrará información, como las direcciones de correo electrónico de las personas que intentaron acceder a documentos protegidos que los usuarios compartieron, cuándo estas personas intentaron obtener acceso a ellos y su ubicación. Si mostrar esta información en su organización está prohibido debido a los requisitos de privacidad, puede deshabilitar el acceso al sitio de seguimiento de documentos mediante el cmdlet <externalLink><linkText>Disable-AadrmDocumentTrackingFeature</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=623032</linkUri></externalLink>. Puede volver a habilitar el acceso al sitio en cualquier momento, mediante el uso de <externalLink><linkText>Enable-AadrmDocumentTrackingFeature</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=623037</linkUri></externalLink>, y puede comprobar si acceso está actualmente habilitado o deshabilitado mediante <externalLink><linkText>Get AadrmDocumentTrackingFeature</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=623037</linkUri></externalLink>.</para> <para>Para ejecutar estos cmdlets, debe tener como mínimo la versión <embeddedLabel>2.3.0.0</embeddedLabel> del módulo Azure RMS para Windows PowerShell.  Para obtener instrucciones de instalación, consulte <externalLink><linkText>Instalación de Windows PowerShell para Azure Rights Management</linkText><linkUri>https://technet.microsoft.com/library/jj585012.aspx</linkUri></externalLink>.</para><alert class="tip"><para>Si anteriormente descargó e instaló el módulo, compruebe el número de versión ejecutando: <codeInline>(Get-Module aadrm –ListAvailable).Version</codeInline></para></alert><para>Las direcciones URL siguientes se usan para el seguimiento de documentos y se deben permitir (por ejemplo, agregarlas a sus sitios de confianza si está usando Internet Explorer con seguridad mejorada): </para><list class="bullet"><listItem><para>https://*.azurerms.com</para></listItem><listItem><para>https://ecn.dev.virtualearth.net</para><alert class="note"><para>Esta dirección URL es para mapas de Bing.</para></alert></listItem><listItem><para>https://*.microsoftonline.com</para></listItem><listItem><para>https://*.microsoftonline-p.com</para></listItem></list></caps:sentence>
            </content>
          </section>
          <section address="BKMK_FederatedDomains">
            <title>
              <caps:sentence sentenceid="9b5adb757a06e8b26d055f4cc9d21812" id="tgt174" class="tgtSentence">Solo AD RMS: Compatibilidad con varios dominios de correo electrónico dentro de su organización </caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="741ff32e03e58220c20e757767df5cae" id="tgt175" class="tgtSentence">Si usa AD RMS y los usuarios de su organización tienen varios dominios de correo electrónico, quizás como resultado de una fusión o adquisición, debe realizar la siguiente modificación en el Registro:</caps:sentence>
              </para>
              <list class="ordered">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="52a0a486115949d5009cfa2b41666228" id="tgt176" class="tgtSentence">Vaya a <ui>HKEY_LOCAL_MACHINE\Software\Microsoft\MSIPC</ui> y, si no aparece ya ahí, cree una nueva clave denominada <ui>RmsSharingApp</ui>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="3d28822ef6b543a688f36f914f7304b4" id="tgt177" class="tgtSentence">Seleccione <ui>RmsSharingApp</ui>, cree un nuevo valor de cadena múltiple denominado <ui>FederatedDomains</ui> y, luego, agregue los dominios y todos los subdominios que usa la organización.</caps:sentence>
                    <caps:sentence sentenceid="526e0285738e937b0d3a7d9d73949fde" id="tgt178" class="tgtSentence"> No se admiten caracteres comodín.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="0aa3aaabb43c1ebe9c7807670aceb459" id="tgt179" class="tgtSentence">Por ejemplo: La compañía Coho Vineyard &amp; Winery tiene un dominio de correo electrónico estándar de <embeddedLabel>cohovineyardandwinery.com</embeddedLabel>, pero como resultado de fusiones, también usan los dominios de correo electrónico <embeddedLabel>cohowinery.com</embeddedLabel>, <embeddedLabel>eastcoast.cohowinery.com</embeddedLabel> y <embeddedLabel>cohovineyard</embeddedLabel>.</caps:sentence>
                    <caps:sentence sentenceid="b74b069a828a9bdc4b4ba655dfd782ca" id="tgt180" class="tgtSentence"> Para los datos de valor <ui>FederatedDomains</ui>, el administrador escribe: <userInput>cohowinery.com; eastcoast.cohowinery.com; cohovineyard</userInput></caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="5bb76a35274f6ef8198ac60f37118899" id="tgt181" class="tgtSentence">Si no realiza este cambio en el Registro, los usuarios no podrán consumir contenido que han protegido otros usuarios de su organización.</caps:sentence>
                <caps:sentence sentenceid="686b7859ce268dd2879d35621d2fe79f" id="tgt182" class="tgtSentence"> Esta modificación del Registro no es necesaria si usa Azure RMS.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </section>
      <section DoNotNumber="false" address="BKMK_AdminOverview">
        <title>
          <caps:sentence sentenceid="70f4ac9cb556b2fb16d5bb98d0e83621" id="tgt183" class="tgtSentence">Información general técnica de la aplicación Microsoft Rights Management sharing </caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="1b4b63dcac3e6fd5e9215da3e9b3710c" id="tgt184" class="tgtSentence">La aplicación Microsoft Rights Management sharing es una aplicación opcional descargable para Microsoft Windows y otras plataformas, que ofrece lo siguiente:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="f342aefb04a5480888dd84fd56054514" id="tgt185" class="tgtSentence">Protección de un solo archivo o protección masiva de varios archivos, así como de todos los archivos dentro de una carpeta seleccionada.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="30d725a087c82921885231f43bea1005" id="tgt186" class="tgtSentence">Compatibilidad completa con la protección de cualquier tipo de archivo y un visor integrado para los tipos de archivo de texto e imagen usados más comúnmente.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="5489333c4bcb0b8b80177d9a2a2d4015" id="tgt187" class="tgtSentence">Protección genérica para los archivos que no admiten la protección de RMS.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="32fa844c2536cfecf8b50feeb7d677bf" id="tgt188" class="tgtSentence">Interoperabilidad completa con los archivos protegidos mediante Office Information Rights Management (IRM).</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="f91e4d1e144ec4af48e5f4d41690296d" id="tgt189" class="tgtSentence">Interoperabilidad completa con archivos PDF protegidos con SharePoint, FCI y herramientas de creación de PDF admitidas.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="78ba5c7d7c065e3ba898710464a52bdf" id="tgt190" class="tgtSentence">La aplicación Microsoft Rights Management sharing usa el nuevo <externalLink><linkText>tiempo de ejecución del cliente de AD RMS 2.1</linkText><linkUri>http://www.microsoft.com/download/details.aspx?id=38396</linkUri></externalLink>.</caps:sentence>
            <caps:sentence sentenceid="6946e206fcc7a60e96813efebcd6dc06" id="tgt191" class="tgtSentence"> Mediante el uso de la funcionalidad de AD RMS 2.1, la aplicación Microsoft Rights Management sharing proporciona a los usuarios finales una experiencia sencilla de protección y el consumo.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="4f85bbbcffe4f1394358d794c7eecd3b" id="tgt192" class="tgtSentence">Con la versión de RMS del 13 de octubre de 2013, puede proteger documentos de forma nativa mediante Office 2010 y enviarlos a personas de otra compañía, quienes pueden consumirlos entonces con Azure RMS.</caps:sentence>
            <caps:sentence sentenceid="0b2dc2526a391dce548a9193e6e1187f" id="tgt193" class="tgtSentence"> Además, con esta versión, si usa AD RMS en modo criptográfico 2, puede usar RMS para individuos y consumir contenido de personas de otra compañía que use Azure RMS.</caps:sentence>
            <caps:sentence sentenceid="2bdf853b958e7baffce8a3225693a06e" id="tgt194" class="tgtSentence"> Para obtener más información sobre el modo criptográfico 2, consulte <externalLink><linkText>Modos criptográficos de AD RMS</linkText><linkUri>http://technet.microsoft.com/library/hh867439(v=ws.10).aspx</linkUri></externalLink>.</caps:sentence>
          </para>
        </content>
        <sections>
          <section DoNotNumber="false" address="BKMK_LevelsofProtection">
            <title>
              <caps:sentence sentenceid="a505e96c3346a500786f95166bc546bf" id="tgt195" class="tgtSentence">Niveles de protección: nativo y genérico</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="5662ba04b21e97d436355f0f74a71fa6" id="tgt196" class="tgtSentence">La aplicación Microsoft Rights Management sharing admite la protección en dos niveles distintos, como se describe en la tabla siguiente.</caps:sentence>
              </para>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="9447854474935c37d58716ccfa52294b" id="tgt197" class="tgtSentence">Tipo de protección</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="8e5f3adee38c8fccc13c1f3be0143796" id="tgt198" class="tgtSentence">Nativa</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="3d517f8924ac7fd03699a29d97dc52d9" id="tgt199" class="tgtSentence">Genérico</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt200" class="tgtSentence">Descripción</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="faab6f6c8e06a7528150bc94000af033" id="tgt201" class="tgtSentence">Para archivos de texto, imagen, Microsoft Office (Word, Excel, PowerPoint), archivos .pdf y otros tipos de archivo de aplicaciones compatibles con AD RMS, la protección nativa ofrece un fuerte nivel de protección que incluye tanto cifrado como aplicación de derechos (permisos).</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="76b88e8d37a79cc71deb614ac7dce14a" id="tgt202" class="tgtSentence">Para todas las demás aplicaciones y tipos de archivo, la protección genérica proporciona un nivel de protección que incluye encapsulación de archivos mediante el tipo de archivo .pfile, y autenticación para comprobar si un usuario está autorizado para abrir el archivo.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="152f5dc0f7ac734f8e8ee17d4a482462" id="tgt203" class="tgtSentence">Protección</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="d24d2a585931356cf32230d4ddc150b1" id="tgt204" class="tgtSentence">Los archivos están completamente cifrados y la protección se aplica de las siguientes maneras:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="d85c8ec6f32ba4fb9580ba6c26221e18" id="tgt205" class="tgtSentence">Antes de presentar el contenido protegido, se debe autenticar correctamente a aquellas personas que reciben el archivo por correo electrónico o que se les concede acceso a él mediante permisos de archivo o recurso compartido.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="7d39e6b367e9d1c39d12e2525f64c457" id="tgt206" class="tgtSentence">Además, cuando el contenido se presenta en el Visor de IP (en el caso de archivos de texto e imagen protegidos) o en la aplicación asociada (en el caso de todos los demás tipos de archivo admitidos), se aplican completamente los derechos de uso y le directiva definida por el propietario del contenido cuando se protegen los archivos.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7e8bedc403ea37dbd6f6eed90e44df0c" id="tgt207" class="tgtSentence">La protección de los archivos se aplica de las siguientes formas:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="028345237801e3c250ebf4b3056b4c87" id="tgt208" class="tgtSentence">Antes de presentar el contenido protegido, se debe autenticar correctamente a aquellas personas que están autorizadas para abrir el archivo o que se les proporciona acceso a él.</caps:sentence>
                            <caps:sentence sentenceid="74f6f93b77e42269f6051c135fd96547" id="tgt209" class="tgtSentence"> Si la autorización da error, el archivo no se abre.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="72a35b10cd77c0b6de84ab7b4bd18319" id="tgt210" class="tgtSentence">Se muestran los derechos de uso y la directiva establecida por el propietario del contenido para informar a los usuarios autorizados de la directiva de uso previsto.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="13c03aa2c5630241516cc574608508ea" id="tgt211" class="tgtSentence">Tiene lugar el registro de auditoría de los usuarios autorizados a abrir y obtener acceso a los archivos; sin embargo, no se aplican derechos de uso por parte de las aplicaciones no admitidas.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="c254e6343e0364bcc7881d210bc1cecc" id="tgt212" class="tgtSentence">Valor predeterminado para tipos de archivo</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="f9d1d087802ab1d57c4529778d5b7663" id="tgt213" class="tgtSentence">Es el nivel predeterminado de protección para los siguientes tipos de archivo:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="66351e4307f0dc68cd7f411ba80f05c9" id="tgt214" class="tgtSentence">Archivos de texto e imagen </caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="30c3853d4758d3ff092e99b1bd8f7da0" id="tgt215" class="tgtSentence">Archivos de Microsoft Office (Word, Excel, PowerPoint) </caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="9f263d43cf23a4bde3bed2e15ec5edd1" id="tgt216" class="tgtSentence">Formato de documento portátil (.pdf)</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                      <para>
                        <caps:sentence sentenceid="7428fa04e5ee710d1f6189b699b1dded" id="tgt217" class="tgtSentence">Para obtener más información, consulte la sección siguiente, <link xlink:href="d9992e30-f3d1-48d5-aedc-4e721f7d7c25#BKMK_SupportFileTypes">Supported file types and file name extensions</link>.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="14f92f9b5d6a10966de4e5fa709608bc" id="tgt218" class="tgtSentence">Se trata de la protección predeterminada para todos los demás tipos de archivo (por ejemplo, .vsdx, .rtf etc.) que no son compatibles con la protección completa.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
              <para></para>
              <para>
                <caps:sentence sentenceid="d4b76be1bba1ef44a7e404d1059944b6" id="tgt219" class="tgtSentence">Puede cambiar el nivel de protección predeterminado que aplica la aplicación RMS sharing.</caps:sentence>
                <caps:sentence sentenceid="22a96fc7142a40fd53f76f19c072c019" id="tgt220" class="tgtSentence"> Puede cambiar el nivel predeterminado de nativo a genérico, de genérico a nativo, e incluso impedir que la aplicación RMS sharing aplique protección.</caps:sentence>
                <caps:sentence sentenceid="be021ab36c2c99a549fc25f5fcee238c" id="tgt221" class="tgtSentence"> Para obtener más información, consulte la sección <link xlink:href="d9992e30-f3d1-48d5-aedc-4e721f7d7c25#BKMK_ChangeDefaultProtection">Changing the default protection level of files</link> de este tema.</caps:sentence>
              </para>
            </content>
          </section>
          <section address="BKMK_SupportFileTypes" DoNotNumber="false">
            <title>
              <caps:sentence sentenceid="d41f438743b61540057d1f5b671aa8a2" id="tgt222" class="tgtSentence">Tipos de archivo y extensiones de nombre de archivo admitidos</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="5e43d02f3f5012b25bb3962d88dccb03" id="tgt223" class="tgtSentence">En la tabla siguiente se enumeran los tipos de archivo que admite de forma nativa la aplicación Microsoft Rights Management sharing.</caps:sentence>
                <caps:sentence sentenceid="274bc46203156c3f0abb898ca28edf23" id="tgt224" class="tgtSentence"> En estos tipos de archivo, la extensión de nombre de archivo original se cambia cuando se aplica el archivo nativo protegido, y estos archivos se vuelven de solo lectura.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="3b30a2db360cbfe7f2133419299956c7" id="tgt225" class="tgtSentence">Además, cuando la aplicación RMS sharing protege de forma nativa un archivo de Word, Excel o PowerPoint que protegen los usuarios mediante uso compartido, esta acción crea automáticamente un segundo archivo que es una copia del original con el mismo nombre pero con una extensión <ui>.ppdf</ui>¹.</caps:sentence>
                <caps:sentence sentenceid="cb8407d4cedd360a74079a162e680075" id="tgt226" class="tgtSentence"> Esta versión del archivo garantiza que los destinatarios que instalan la aplicación RMS sharing siempre pueden abrir el archivo al que se le ha aplicado protección nativa.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="16ae49a28bdfed9e21cae9c3e917df22" id="tgt227" class="tgtSentence">En el caso de los archivos que están protegidos de manera genérica, la extensión del nombre de archivo original siempre se cambia a .pfile.</caps:sentence>
              </para>
              <alert class="warning">
                <para>
                  <caps:sentence sentenceid="dc912a4f8e4dbc00344c962a3c785c6a" id="tgt228" class="tgtSentence">Si dispone de firewalls, servidores proxy web o software de seguridad que inspeccionan o realizan acciones en función de las extensiones de nombre de archivo, puede que tenga que volver a configurar estos para admitir las nuevas extensiones de nombre de archivo.</caps:sentence>
                </para>
              </alert>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="c3d3cff5d2f88161337e329063010f26" id="tgt229" class="tgtSentence">Extensión de nombre de archivo original</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="1e879312340251d933d44979a7266b51" id="tgt230" class="tgtSentence">Extensión de nombre de archivo con protección de RMS</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="be4117b0c842c4be8f9960294bdc2cd1" id="tgt231" class="tgtSentence">.txt</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="6ad30254869c6fe9b2af3d03dc6dd217" id="tgt232" class="tgtSentence">.ptxt</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="4e9f6c7fdef327a6b0e08505dc57a694" id="tgt233" class="tgtSentence">.xml</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="524dad41b7fd56187d3d561c7ece4efe" id="tgt234" class="tgtSentence">.pxml</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="25b2916b5c49db617f52fa5ea48efee7" id="tgt235" class="tgtSentence">.jpg</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="239700fc41b2d8bc3806de462a2b2927" id="tgt236" class="tgtSentence">.pjpg</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="46c4f3f7360db850647354c431662c8e" id="tgt237" class="tgtSentence">.jpeg</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="2193061638a8bcb619cc35c40df503df" id="tgt238" class="tgtSentence">.ppng</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="abdf095626d4a4ab2bcd4167b128c1f1" id="tgt239" class="tgtSentence">.pdf</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="f176a26e5c980419fdeca1373119364d" id="tgt240" class="tgtSentence">.ppdf</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="6446d860dbbfe540e9e2cbab5f98f1e3" id="tgt241" class="tgtSentence">.png</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="2193061638a8bcb619cc35c40df503df" id="tgt242" class="tgtSentence">.ppng</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="6907af83b3fff53966bfa1a4b8707a29" id="tgt243" class="tgtSentence">.tiff</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="3c93dc40dd5f4a40295c99cbb1882ae9" id="tgt244" class="tgtSentence">.ptiff</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="06adcbfe4f995d72e50498d910d95719" id="tgt245" class="tgtSentence">.bmp</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="022c945bb12b3c9ffcfe979d75ecd667" id="tgt246" class="tgtSentence">.pbmp</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="03a46779cf1ed515b29e1c471efd4c0f" id="tgt247" class="tgtSentence">.gif</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="c3aae478df4e395450322ed14f11b3ae" id="tgt248" class="tgtSentence">.pgif</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="cd57b82e0f56096af2999a3bb56317aa" id="tgt249" class="tgtSentence">.giff</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="8a467f919f821f5d85d861428c2ccbac" id="tgt250" class="tgtSentence">.pgiff</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="f31b703e40b6bb332d4e2badb60b346e" id="tgt251" class="tgtSentence">.jpe</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="6c1a0405d69c3576b1afc2d44195c1cd" id="tgt252" class="tgtSentence">.pjpe</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ee33d82cad600913585d5dfa584e4e24" id="tgt253" class="tgtSentence">.jfif</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="e39c8d8283449237129731b364d30c53" id="tgt254" class="tgtSentence">.pjfif</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="4faffa61d3f804d241a13fb8b5b818a8" id="tgt255" class="tgtSentence">.jif</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="bc06e75635a59e0f7305712a65289733" id="tgt256" class="tgtSentence">.pjif</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="023e5e089f8981a4d1890bfd9a956d81" id="tgt257" class="tgtSentence">.jt</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a434222f49897f2631828811a2a518b2" id="tgt258" class="tgtSentence">.pjt</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
              <para>
                <caps:sentence sentenceid="233a996b9c678752793612f1d2e186da" id="tgt259" class="tgtSentence">¹ Representación de PDF con tecnología Foxit.</caps:sentence>
                <caps:sentence sentenceid="8deb6d1b8a0f1baf8f0507a9da45a6b5" id="tgt260" class="tgtSentence"> Copyright © 2003–2014 by Foxit Corporation.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="7ed5b77a9f17186856b687764eb03940" id="tgt261" class="tgtSentence">En la tabla siguiente se enumeran los tipos de archivo que admite de forma nativa la aplicación Microsoft Rights Management sharing en Microsoft Office 2016, Office 2013 y Office 2010.</caps:sentence>
                <caps:sentence sentenceid="8307abea7a7502b3d3a6a626bd440ff9" id="tgt262" class="tgtSentence"> En estos archivos, la extensión de nombre de archivo permanece igual después de que el archivo se ha protegido con RMS.</caps:sentence>
              </para>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ba77e48974fe7f87a4f66c27d422293f" id="tgt263" class="tgtSentence">Tipos de archivo admitidos por Office</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ba77e48974fe7f87a4f66c27d422293f" id="tgt264" class="tgtSentence">Tipos de archivo admitidos por Office</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="228df97f93cdf894525c817df5b20306" id="tgt265" class="tgtSentence">.doc </caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="2e531d2c5ea5af32f7c11ef7d42a9fc3" id="tgt266" class="tgtSentence">.docm</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="8c7a7a618a6d4acfe85b4b4b1048846d" id="tgt267" class="tgtSentence">.docx</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="4a0232ed909f3574ffdb1f0d3bdb5660" id="tgt268" class="tgtSentence">.dot</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="24e383fa4e3fd90878c05c0a475842eb" id="tgt269" class="tgtSentence">.dotm</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="c99bd1fd200e9f0eed3360741e40fea6" id="tgt270" class="tgtSentence">.dotx</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="5a4b119ca13634088719bc2570c3a830" id="tgt271" class="tgtSentence">.potm</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="035065cf0a0c0bde907e582e233f0ef0" id="tgt272" class="tgtSentence">.potx</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="73b733af44cd574d15ace8f95402ac5f" id="tgt273" class="tgtSentence">.pps</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="b869587ef7083a314155e67e3427ff83" id="tgt274" class="tgtSentence">.ppsm</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="7930369cae67a4c6d47b4f008a19e788" id="tgt275" class="tgtSentence">.ppsx</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="d45e18c81b2330875c3f1079be347171" id="tgt276" class="tgtSentence">.ppt</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="2d87039f87f3530fa055c9e1aed18941" id="tgt277" class="tgtSentence">.pptm</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a9bec49e3e6504112d702f6449b79631" id="tgt278" class="tgtSentence">.pptx</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="c3706a99c4227b798d0d560555a9b248" id="tgt279" class="tgtSentence">.thmx</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="9044eca8b991d1bbf02693c6edd96d2c" id="tgt280" class="tgtSentence">.xla</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="8134c64d997f2241ddea945eafd26ef0" id="tgt281" class="tgtSentence">.xlam</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="303e9d780912940ea6ade0981c37e23e" id="tgt282" class="tgtSentence">.xls</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="a9b57817bc0f0ae1902fc98ff64cc386" id="tgt283" class="tgtSentence">.xlsb</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="3e816805c4a9a8aa4006d0b81b5128b9" id="tgt284" class="tgtSentence">.xlt</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="5008c13603a24e34e69dd21cae3fcf96" id="tgt285" class="tgtSentence">.xlsm</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="552c070e14cf0a9151d1b49064e4cde0" id="tgt286" class="tgtSentence">.xlsx</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="2d31fb440bb00b290aba57559a52f06b" id="tgt287" class="tgtSentence">.xltm</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="a4850add4848429f2ef4a409804cf1e3" id="tgt288" class="tgtSentence">.xltx</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="8b80d66c4b7ff30f2191b3ee3e947286" id="tgt289" class="tgtSentence">.xps</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section address="BKMK_ChangeDefaultProtection">
            <title>
              <caps:sentence sentenceid="2a5427a57d53b06c26bdec536f199acd" id="tgt290" class="tgtSentence">Cambio del nivel de protección predeterminado de los archivos</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="3fb74a6d12486361c420df0870e0b40b" id="tgt291" class="tgtSentence">Puede cambiar la manera en que la aplicación RMS sharing protege los archivos mediante la modificación del Registro.</caps:sentence>
                <caps:sentence sentenceid="ba0d21df4457ded8f71f70bf0184b68c" id="tgt292" class="tgtSentence"> Por ejemplo, puede forzar que los archivos que admiten la protección nativa estén protegidos de forma genérica por la aplicación RMS sharing.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="b3a90196fcc65748c8ac6403ab899f89" id="tgt293" class="tgtSentence">Puede que quiera hacer esto por los siguientes motivos:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="76b6d4ed45171f6e359e756e4d1127f6" id="tgt294" class="tgtSentence">Para asegurarse de que todos los usuarios pueden abrir el archivo desde sus dispositivos móviles.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="5ee6d43bc5a3e4e96eab51e384104568" id="tgt295" class="tgtSentence">Para asegurarse de que todos los usuarios pueden abrir el archivo si no tienen una aplicación que admite la protección nativa.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="0e9ee33613770aba39af37460ea716de" id="tgt296" class="tgtSentence">Para tener en cuenta sistemas de seguridad que realizan acciones sobre los archivos por su extensión de nombre de archivo y que se pueden reconfigurar para que tengan en cuenta la extensión de nombre de archivo .pfile pero no para admitir varias extensiones de nombre de archivo para la protección nativa.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="8309f72920ead216a12878cf0bb55e5b" id="tgt297" class="tgtSentence">De igual forma, puede forzar que la aplicación RMS sharing aplique protección nativa a archivos a los que, de forma predeterminada, se les aplicaría protección genérica.</caps:sentence>
                <caps:sentence sentenceid="6e92ab1b7ac942ccfc97dccb19f68906" id="tgt298" class="tgtSentence"> Esto podría resultar adecuados si tiene una aplicación que admite las API de RMS, por ejemplo, una aplicación de línea de negocio que han escrito sus desarrolladores internos o una aplicación adquirida a un fabricante de software independiente (ISV).</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="1119d11e83bd4366ed6022e7adf9d347" id="tgt299" class="tgtSentence">También puede forzar que la aplicación RMS sharing boquee la protección de los archivos, es decir, que no aplique protección nativa ni protección genérica.</caps:sentence>
                <caps:sentence sentenceid="a927eb9b8bcdde4007d9c03e84f7f7d2" id="tgt300" class="tgtSentence"> Por ejemplo, esto podría ser necesario si tiene una aplicación o un servicio automatizados que deben poder abrir un archivo específico para procesar su contenido.</caps:sentence>
                <caps:sentence sentenceid="43008894f5e3647744fef0117f083ad9" id="tgt301" class="tgtSentence"> Cuando se bloquea la protección para un tipo de archivo, los usuarios no pueden usar la aplicación RMS sharing para proteger un archivo con ese tipo de archivo.</caps:sentence>
                <caps:sentence sentenceid="251efad2a94842b2d7ea8204ec5ad3e3" id="tgt302" class="tgtSentence"> Cuando lo intentan, verán un mensaje que dice que el administrador ha impedido la protección y deben cancelar su acción para proteger el archivo.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="50dd0bcecdb71877bbd6a74aafc8d502" id="tgt303" class="tgtSentence">Para configurar la aplicación RMS sharing para aplicar protección genérica a todos los archivos a los que, de forma predeterminada, se les aplicaría protección nativa, realice las siguientes modificaciones en el Registro:</caps:sentence>
              </para>
              <list class="ordered">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="9973987ce852585fb954f16fcb8c509e" id="tgt304" class="tgtSentence">
                      <ui>HKEY_LOCAL_MACHINE\Software\Microsoft\MSIPC\RMSSharingApp\FileProtection</ui>: Cree una nueva clave llamada <ui>*</ui>.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="cce38d5443a2bf3ccdfc0a809ae878d5" id="tgt305" class="tgtSentence">Este valor indica archivos con cualquier extensión de nombre de archivo.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="00d9bf2851d42e4e0b4e89e6371c248d" id="tgt306" class="tgtSentence">En la clave recién agregada de <ui>HKEY_LOCAL_MACHINE\Software\Microsoft\MSIPC\RMSSharingApp\FileProtection\*</ui>, cree un nuevo valor de cadena (REG_SZ) llamado <ui>Encryption</ui> que tenga el valor de datos de <ui>Pfile</ui>.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="bbe821c508ddfc106912161505ec1e25" id="tgt307" class="tgtSentence">Este valor da como resultado la aplicación de protección genérica por parte de la aplicación RMS sharing.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="d1725aeb570203d1b029c1edff9a1497" id="tgt308" class="tgtSentence">Estos dos valores provocarán que la aplicación RMS sharing aplique protección genérica a todos los archivos que tiene una extensión de nombre de archivo.</caps:sentence>
                <caps:sentence sentenceid="449b49472c2a33158c5e5fc5cc5161c9" id="tgt309" class="tgtSentence"> Si éste es su objetivo, no es necesario configurar nada más.</caps:sentence>
                <caps:sentence sentenceid="77f950d7f7a3aefe5af98f0781573c95" id="tgt310" class="tgtSentence"> Sin embargo, puede definir excepciones para tipos de archivo específicos para que sigan estando protegidos de forma nativa.</caps:sentence>
                <caps:sentence sentenceid="c256f842511ca47b6356f6b051c90d08" id="tgt311" class="tgtSentence"> Para ello, debe realizar tres modificaciones adicionales en el Registro para cada tipo de archivo:</caps:sentence>
              </para>
              <list class="ordered">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="017698f1268de4a84172c7c4aa43f24b" id="tgt312" class="tgtSentence">
                      <ui>HKEY_LOCAL_MACHINE\Software\Microsoft\MSIPC\RMSSharingApp\FileProtection</ui>: Agregue una nueva clave que tenga el nombre de la extensión de nombre de archivo (sin el punto delante).</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="e4d6e39d8a59a00280e698e9b87ddc19" id="tgt313" class="tgtSentence">Por ejemplo, para los archivos que tienen una extensión .docx, cree una clave denominada <ui>DOCX</ui>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="b44d6be340b394236e098db2fda65042" id="tgt314" class="tgtSentence">En la clave de tipo de archivo recién agregada (por ejemplo, <ui>HKEY_LOCAL_MACHINE\Software\Microsoft\MSIPC\RMSSharingApp\FileProtection\DOCX</ui>), cree un nuevo valor DWORD llamado <ui>AllowPFILEEncryption</ui> que tenga un valor de <ui>0</ui>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="b44d6be340b394236e098db2fda65042" id="tgt315" class="tgtSentence">En la clave de tipo de archivo recién agregada (por ejemplo, <ui>HKEY_LOCAL_MACHINE\Software\Microsoft\MSIPC\RMSSharingApp\FileProtection\DOCX</ui>), cree un nuevo valor DWORD llamado <ui>Encryption</ui> que tenga un valor de <ui>Native</ui>.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="388d6689739a88ed277dd7a7aa40e804" id="tgt316" class="tgtSentence">Como resultado de esta configuración, todos los archivos están protegidos genéricamente, excepto los archivos que tienen una extensión de nombre de archivo .docx, que están protegidos de forma nativa por la aplicación RMS sharing.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="1e5504c8190a8b63bc8808c392562cb6" id="tgt317" class="tgtSentence">Repita estos tres pasos con otros tipos de archivo que quiera definir como excepciones porque admiten la protección nativa y no quiere que la aplicación RMS sharing los proteja de forma genérica.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="5b1534ae13200dff8217f480abb6fca2" id="tgt318" class="tgtSentence">Puede realizar modificaciones parecidas en el Registro para otras situaciones cambiando el valor de la cadena <ui>Encryption</ui> que admite los siguientes valores: </caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="9cb650f8f25d7640d8bc9d14606478c9" id="tgt319" class="tgtSentence">
                      <ui>Pfile</ui>: Protección genérica</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="586cc534cbd93f5aaba302c450459373" id="tgt320" class="tgtSentence">
                      <ui>Native</ui>: Protección nativa</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="536fe06ed7df72ca01f03049945fc27d" id="tgt321" class="tgtSentence">
                      <ui>Off</ui>: Bloquear protección</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
        </sections>
      </section>
      <relatedTopics>
        <link xlink:href="eaf6d02c-aa36-4915-856e-49bb71ab1484">Rights Management sharing application user guide</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Use the following information if you are responsible for the Microsoft Rights Management sharing application on an enterprise network, or if you want more technical information than is in the <link xlink:href="eaf6d02c-aa36-4915-856e-49bb71ab1484">Microsoft Rights Management sharing application User's Guide</link> or <externalLink><linkText>FAQ for Microsoft Rights Management Sharing Application for Windows</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=303971</linkUri></externalLink>:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <link xlink:href="d9992e30-f3d1-48d5-aedc-4e721f7d7c25#BKMK_ScriptedInstall">Automatic deployment for the Microsoft Rights Management sharing application</link>
            </para>
            <list class="bullet">
              <listItem>
                <para>
                  <link xlink:href="d9992e30-f3d1-48d5-aedc-4e721f7d7c25#BKMK_verifyscripted">Verifying installation success</link>
                </para>
              </listItem>
              <listItem>
                <para>
                  <link xlink:href="d9992e30-f3d1-48d5-aedc-4e721f7d7c25#BKMK_uninstallscripted">Uninstall commands </link>
                </para>
              </listItem>
              <listItem>
                <para>
                  <link xlink:href="d9992e30-f3d1-48d5-aedc-4e721f7d7c25#BKMK_SuppressAutomaticUpdates">Suppressing automatic updates</link>
                </para>
              </listItem>
              <listItem>
                <para>
                  <link xlink:href="#BKMK_DocumentTracking">Azure RMS only: Configuring document tracking</link>
                </para>
              </listItem>
              <listItem>
                <para>
                  <link xlink:href="d9992e30-f3d1-48d5-aedc-4e721f7d7c25#BKMK_FederatedDomains">AD RMS only: Support for multiple email domains within your organization </link>
                </para>
              </listItem>
            </list>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="d9992e30-f3d1-48d5-aedc-4e721f7d7c25#BKMK_AdminOverview">Technical overview for the Microsoft Rights Management sharing application </link>
            </para>
            <list class="bullet">
              <listItem>
                <para>
                  <link xlink:href="d9992e30-f3d1-48d5-aedc-4e721f7d7c25#BKMK_LevelsofProtection">Levels of protection – native and generic</link>
                </para>
              </listItem>
              <listItem>
                <para>
                  <link xlink:href="d9992e30-f3d1-48d5-aedc-4e721f7d7c25#BKMK_SupportFileTypes">Supported file types and file name extensions</link>
                </para>
              </listItem>
              <listItem>
                <para>
                  <link xlink:href="d9992e30-f3d1-48d5-aedc-4e721f7d7c25#BKMK_ChangeDefaultProtection">Changing the default protection level of files</link>
                </para>
              </listItem>
            </list>
          </listItem>
        </list>
        <alert class="tip">
          <para>
            <caps:sentence id="src2" class="srcSentence">If you are new to the RMS sharing app, or looking for more information, see <externalLink><linkText>How RMS protects all file types – by using the RMS sharing app</linkText><linkUri>https://curah.microsoft.com/191031/how-rms-protects-all-file-types-by-using-the-rms-sharing-app</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence id="src3" class="srcSentence">The RMS sharing application is best suited to work with Azure RMS, because this deployment configuration supports sending protected attachments to users in another organization, and options such as email notifications and document tracking with revocation.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence">  However, with some limitations, it also works with the on-premises version, AD RMS.</caps:sentence>
          <caps:sentence id="src5" class="srcSentence"> For a comprehensive comparison of features that are supported by Azure RMS and AD RMS, see <externalLink><linkText>Comparing Azure Rights Management and AD RMS</linkText><linkUri>https://technet.microsoft.com/library/jj739831.aspx</linkUri></externalLink>.</caps:sentence>
          <caps:sentence id="src6" class="srcSentence"> If you have AD RMS and want to migrate to Azure RMS, see <externalLink><linkText>Migrating from AD RMS to Azure Rights Management</linkText><linkUri>https://technet.microsoft.com/library/dn858447.aspx</linkUri></externalLink>.</caps:sentence>
        </para>
      </introduction>
      <section DoNotNumber="false" address="BKMK_ScriptedInstall">
        <title>
          <caps:sentence id="src7" class="srcSentence">Automatic deployment for the Microsoft Rights Management sharing application</caps:sentence>
        </title>
        <content>
          <para></para>
          <para>
            <caps:sentence id="src8" class="srcSentence">The Windows version of the RMS sharing application supports a scripted installation, which makes it suitable for enterprise deployments.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src9" class="srcSentence">The only prerequisites for installations are that the computers run a minimum version of Windows 7 Service Pack 1, and that the Microsoft Framework, minimum version 4.0 is installed.</caps:sentence>
            <caps:sentence id="src10" class="srcSentence"> If you need to install the Microsoft .NET Framework 4.0, you can <externalLink><linkText>download it for installation from the Microsoft Download Center</linkText><linkUri>http://www.microsoft.com/download/details.aspx?id=17718</linkUri></externalLink>.</caps:sentence>
          </para>
          <procedure>
            <title>
              <caps:sentence id="src11" class="srcSentence">To download the RMS sharing application for automatic deployment</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src12" class="srcSentence">Go to the <externalLink><linkText>Microsoft Rights Management sharing application for Windows</linkText><linkUri>http://www.microsoft.com/download/details.aspx?id=40857</linkUri></externalLink> page in the Microsoft Download Center, and click <ui>Download</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src13" class="srcSentence">Select and download the files that you need.</caps:sentence>
                    <caps:sentence id="src14" class="srcSentence"> There are two client installation packages: one for Windows 64-bit (Microsoft Rights Management sharing application x64.zip), and another for Windows 32-bit (Microsoft Rights Management sharing application x86.zip).</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src15" class="srcSentence">Extract the files from the compressed installation packages, for example, by double-clicking them.</caps:sentence>
                    <caps:sentence id="src16" class="srcSentence"> Then copy the extracted files to a network location that client computers can access.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
          <para>
            <caps:sentence id="src17" class="srcSentence">The setup packages for the RMS sharing application supports different deployment scenarios and includes the following:</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src18" class="srcSentence">Description</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src19" class="srcSentence">Deployment scenario</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src20" class="srcSentence">Microsoft Online Sign-In Assistant</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src21" class="srcSentence">Required for the following:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src22" class="srcSentence">Office 2010 and Azure RMS</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src23" class="srcSentence"> Office 2013 and Azure RMS if you have not installed the <externalLink><linkText>June 9, 2015, update for Office 2013</linkText><linkUri>https://support.microsoft.com/kb/3054853</linkUri></externalLink> (KB3054853) </caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src24" class="srcSentence">Hotfix for Office (KB 2596501)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src25" class="srcSentence">Required for the following:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src26" class="srcSentence">Office 2010 and Azure RMS</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src27" class="srcSentence">Office 2010 and Active Directory RMS</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src28" class="srcSentence">Hotfix to enable the AD RMS Client 1.0 to work with Azure RMS (KB 2843630)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src29" class="srcSentence">Required for the following:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src30" class="srcSentence">Office 2010 and Azure RMS</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src31" class="srcSentence">Office 2010 and Active Directory RMS</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src32" class="srcSentence">AD RMS Client and the RMS sharing application</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src33" class="srcSentence">Required for the following:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src34" class="srcSentence">Office 2016 or Office 2013 and Azure RMS or Active Directory RMS</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src35" class="srcSentence">Office 2010 and Azure RMS </caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src36" class="srcSentence">Office 2010 and Active Directory RMS</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src37" class="srcSentence">RMS sharing application and Office add-in only</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src38" class="srcSentence">Office add-in for the ribbon</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src39" class="srcSentence">Required for the following:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src40" class="srcSentence">Office 2016 or Office 2013 and Azure RMS or Active Directory RMS</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src41" class="srcSentence">Office 2010 and Azure RMS</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src42" class="srcSentence">Office 2010 and Active Directory RMS</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src43" class="srcSentence">RMS sharing application and Office add-in only</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src44" class="srcSentence">Azure Active Directory Rights Management preparation tool</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src45" class="srcSentence">Required for the following:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src46" class="srcSentence">Office 2010 and Azure RMS</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
              </tr>
            </tbody>
          </table>
          <para></para>
          <para>
            <caps:sentence id="src47" class="srcSentence">Use the following procedures to identify the commands required to deploy the RMS sharing application for these deployment scenarios:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <embeddedLabel>
                  <caps:sentence id="src48" class="srcSentence">Office 2016 or Office 2013 and Azure RMS or Active Directory RMS</caps:sentence>
                </embeddedLabel>
              </para>
              <para>
                <caps:sentence id="src49" class="srcSentence">Your users are running Office 2016 or Office 2013, your organization uses Azure RMS or Active Directory RMS, and users collaborate with other organizations who use Azure RMS or Active Directory RMS.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <embeddedLabel>
                  <caps:sentence id="src50" class="srcSentence">Office 2010 and Azure RMS</caps:sentence>
                </embeddedLabel>
              </para>
              <para>
                <caps:sentence id="src51" class="srcSentence">Your users are running Office 2010, your organization uses Azure RMS, and users collaborate with other organizations who use Azure RMS or Active Directory RMS.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <embeddedLabel>
                  <caps:sentence id="src52" class="srcSentence">Office 2010 and Active Directory RMS</caps:sentence>
                </embeddedLabel>
              </para>
              <para>
                <caps:sentence id="src53" class="srcSentence">Your users are running Office 2010, your organization uses AD RMS, and users collaborate with other organizations who use Azure RMS.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <embeddedLabel>
                  <caps:sentence id="src54" class="srcSentence">RMS sharing application and Office add-in only</caps:sentence>
                </embeddedLabel>
              </para>
              <para>
                <caps:sentence id="src55" class="srcSentence">Your users are running Office 2016, Office 2013, or Office 2010, your organization uses AD RMS, and users do not need to collaborate with other organizations who use Azure RMS.</caps:sentence>
                <caps:sentence id="src56" class="srcSentence"> This installation lets you install just the sharing application and Office add-in.</caps:sentence>
              </para>
            </listItem>
          </list>
          <alert class="note">
            <para>
              <caps:sentence id="src57" class="srcSentence">In these scenarios, if your organization is running AD RMS, your users can receive protected content from other organizations who use Azure RMS, but your users cannot send protected content to users in an organization that uses Azure RMS.</caps:sentence>
              <caps:sentence id="src58" class="srcSentence"> However, if your organization is running Azure RMS, your users can send and receive protected content from other organizations.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence id="src59" class="srcSentence">To complete the installation for each procedure, the computer must restart.</caps:sentence>
            <caps:sentence id="src60" class="srcSentence"> You can initiate an automatic restart by using a command such as shutdown /i.</caps:sentence>
          </para>
          <procedure expanded="false">
            <title>
              <caps:sentence id="src61" class="srcSentence">To deploy the RMS sharing application for Office 2016 or Office 2013 and Azure RMS or Active Directory RMS</caps:sentence>
            </title>
            <steps class="bullet">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src62" class="srcSentence">On each computer on which you want to install the RMS sharing application and related components, run the following command with elevated privileges:</caps:sentence>
                  </para>
                  <code>setup.exe /s</code>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence id="src63" class="srcSentence">To verify success, see the <link xlink:href="d9992e30-f3d1-48d5-aedc-4e721f7d7c25#BKMK_verifyscripted">Verifying installation success</link> section in this topic.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
          <procedure expanded="false">
            <title>
              <caps:sentence id="src64" class="srcSentence">To deploy the RMS sharing application for Office 2010 and Azure RMS</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src65" class="srcSentence">You must be the global administrator for your Office 365 or Azure Active Directory tenant so that you can get your organization’s certification service URL by running the Azure Active Directory Rights Management preparation tool.</caps:sentence>
                    <caps:sentence id="src66" class="srcSentence"> You need run this tool only once, on a single computer.</caps:sentence>
                    <caps:sentence id="src67" class="srcSentence"> You will use the certification service URL when you install the RMS sharing application on each computer:</caps:sentence>
                  </para>
                  <list class="ordered">
                    <listItem>
                      <para>
                        <caps:sentence id="src68" class="srcSentence">Log in to a computer by using a local administrator account.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src69" class="srcSentence">On that computer, <externalLink><linkText>download and install the Microsoft Online Sign In Assistant</linkText><linkUri>http://www.microsoft.com/download/details.aspx?id=28177</linkUri></externalLink>.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src70" class="srcSentence">Run the following command to see displayed on the screen the certification service URL, which you can then copy and save for the next step:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence id="src71" class="srcSentence">For Windows 8.1 and Windows 8, 64-bit:</caps:sentence>
                          </para>
                          <code>x64\aadrmprep.exe /findCertificationUrl /logfile "&lt;log file path and name&gt;"</code>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src72" class="srcSentence">For Windows 8.1 and  Windows 8, 32-bit:</caps:sentence>
                          </para>
                          <code>X86\aadrmprep.exe /findCertificationUrl /logfile "&lt;log file path and name&gt;"</code>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src73" class="srcSentence">For Windows 7, 64-bit:</caps:sentence>
                          </para>
                          <code>x64\win7\aadrmprep.exe /findCertificationUrl /logfile "&lt;log file path and name&gt;"</code>
                        </listItem>
                      </list>
                      <alert class="note">
                        <para>
                          <caps:sentence id="src74" class="srcSentence">This command might prompt you to enter your credentials for Azure.</caps:sentence>
                          <caps:sentence id="src75" class="srcSentence"> If the computer is not joined to a domain, you will be prompted.</caps:sentence>
                          <caps:sentence id="src76" class="srcSentence"> If the computer is joined to a domain, the tool might be able to use cached credentials.</caps:sentence>
                        </para>
                      </alert>
                    </listItem>
                  </list>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src77" class="srcSentence">On each computer on which you will install the RMS sharing application, run the following command with elevated privileges:</caps:sentence>
                  </para>
                  <code>setup.exe /s /configureO2010Admin /certificationUrl &lt;certification_url&gt;</code>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src78" class="srcSentence">On each computer on which you will install the RMS sharing application, users must run the following command (does not need elevated privileges).</caps:sentence>
                    <caps:sentence id="src79" class="srcSentence"> There are different ways to achieve this, including asking users to run the command (for example, a link in an email message or a link on the help desk portal) or you can add it to their logon script:</caps:sentence>
                  </para>
                  <code>bin\RMSSetup.exe /configureO2010Only</code>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence id="src80" class="srcSentence">To verify success, see the <link xlink:href="d9992e30-f3d1-48d5-aedc-4e721f7d7c25#BKMK_verifyscripted">Verifying installation success</link> section in this topic.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
          <procedure expanded="false">
            <title>
              <caps:sentence id="src81" class="srcSentence">To deploy the RMS sharing application for Office 2010 and Active Directory RMS</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src82" class="srcSentence">On each computer on which you will install the RMS sharing application, run the following command with elevated privileges:</caps:sentence>
                  </para>
                  <code>setup.exe /s /configureO2010Admin</code>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src83" class="srcSentence">On each computer on which you will install the RMS sharing application, users must run the following command (does not need elevated privileges).</caps:sentence>
                    <caps:sentence id="src84" class="srcSentence"> There are different ways to achieve this, including asking users to run the command (for example, a link in an email message or a link on the help desk portal) or you can add it to their logon script:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src85" class="srcSentence">For Windows 10, Windows 8.1  and Windows 8, 64-bit:</caps:sentence>
                      </para>
                      <code>x64\aadrmprep.exe /configureO2010</code>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src86" class="srcSentence">For Windows 10, Windows 8.1 and Windows 8, 32-bit:</caps:sentence>
                      </para>
                      <code>X86\aadrmprep.exe /configureO2010</code>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src87" class="srcSentence">For Windows 7, 64-bit:</caps:sentence>
                      </para>
                      <code>x64\win7\aadrmpep.exe /configureO2010</code>
                    </listItem>
                  </list>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence id="src88" class="srcSentence">To verify success, see the <link xlink:href="d9992e30-f3d1-48d5-aedc-4e721f7d7c25#BKMK_verifyscripted">Verifying installation success</link> section in this topic.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
          <procedure expanded="false">
            <title>
              <caps:sentence id="src89" class="srcSentence">To install the RMS sharing application and Office add-in only</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src90" class="srcSentence">Install the AD RMS Client and the RMS sharing application by using the following command:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src91" class="srcSentence">For 64-bit Windows: </caps:sentence>
                      </para>
                      <code>x64\setup_ipviewer.exe /norestart /quiet /msicl "MSIRESTARTMANAGERCONTROL=Disable" /log "&lt;log file path and name&gt;"</code>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src92" class="srcSentence">For 32-bit Windows: </caps:sentence>
                      </para>
                      <code>X86\setup_ipviewer.exe /norestart /quiet /msicl "MSIRESTARTMANAGERCONTROL=Disable" /log "&lt;log file path and name&gt;"</code>
                    </listItem>
                  </list>
                  <para></para>
                  <para>
                    <caps:sentence id="src93" class="srcSentence">For example: <codeInline>\\server5\apps\rms\x64\setup_ipviewer.exe /norestart /quiet /msicl "MSIRESTARTMANAGERCONTROL=Disable" /log "C:\Log files\ipviewerinstall.log"</codeInline></caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src94" class="srcSentence">Install the Office add-in by using the following commands:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src95" class="srcSentence">For 64-bit version of Office: </caps:sentence>
                      </para>
                      <code>msiexec.exe /norestart /quiet MSIRESTARTMANAGERCONTROL=Disable /i "x64\Setup64.msi" /L*v "&lt;log file path and name&gt;"</code>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src96" class="srcSentence">For 32-bit version of Office: </caps:sentence>
                      </para>
                      <code>msiexec.exe /norestart /quiet MSIRESTARTMANAGERCONTROL=Disable /i "x86\Setup.msi" /L*v "&lt;log file path and name&gt;"</code>
                    </listItem>
                  </list>
                  <para></para>
                  <para>
                    <caps:sentence id="src97" class="srcSentence">For example: <codeInline>\\server5\apps\rms\msiexec.exe /norestart /quiet MSIRESTARTMANAGERCONTROL=Disable /i "x64\Setup64.msi" /L*v "C:\Log files\rmsofficeinstall.log"</codeInline></caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence id="src98" class="srcSentence">To verify success, see the <link xlink:href="d9992e30-f3d1-48d5-aedc-4e721f7d7c25#BKMK_verifyscripted">Verifying installation success</link> section in this topic.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
        </content>
        <sections>
          <section address="BKMK_verifyscripted">
            <title>
              <caps:sentence id="src99" class="srcSentence">Verifying installation success</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src100" class="srcSentence">You can use the installation log files to verify a successful installation.</caps:sentence>
              </para>
              <procedure expanded="false">
                <title>
                  <caps:sentence id="src101" class="srcSentence">To verify installation success for the RMS sharing application for Office 2016 or Office 2013 and Azure RMS or Active Directory RMS</caps:sentence>
                </title>
                <steps class="bullet">
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src102" class="srcSentence">To verify success of the Setup.exe command, on each computer, search for the installation log file <ui>RMInstaller.log</ui> in the <placeholder>%temp%\RMS_installer_&lt;guid&gt;</placeholder> folder, and then identify the exit code.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src103" class="srcSentence">A successful installation has an exit code of 0 and any other number indicates a failed installation.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src104" class="srcSentence">Example log file name: <ui>C:\temp\RMS_Installer_9352fc91-1982-43bf-958a-2ef1fe9c2ed0\RMInstaller.log</ui> </caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
              <procedure expanded="false">
                <title>
                  <caps:sentence id="src105" class="srcSentence">To verify installation success for the RMS sharing application for Office 2010 and Azure RMS</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src106" class="srcSentence">To verify success of the Setup.exe command, on each computer, search for the installation log file <ui>RMInstaller.log</ui> in the <placeholder>%temp%\RMS_installer_&lt;guid&gt;</placeholder> folder, and then identify the exit code.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src107" class="srcSentence">A successful installation has an exit code of 0 and any other number indicates a failed installation.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src108" class="srcSentence">Example log file name: <ui>C:\temp\RMS_Installer_9352fc91-1982-43bf-958a-2ef1fe9c2ed0</ui> </caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src109" class="srcSentence">To verify success for the RMSSetup.exe command, the user should have the following files created in their <placeholder>%localappdata%\microsoft\drm</placeholder> folder:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence id="src110" class="srcSentence">CERT-Machine-2048.drm</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src111" class="srcSentence">CERT-Machine.drm</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src112" class="srcSentence">CLC-*.drm</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src113" class="srcSentence">GIC-*.drm</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                      <para></para>
                      <para>
                        <caps:sentence id="src114" class="srcSentence">Example of a CLC-*.drm file: </caps:sentence>
                      </para>
                      <para>
                        <ui>
                          <caps:sentence id="src115" class="srcSentence">CLC-alice@isvtenant999.onmicrosoft.com-{1b9cfccf;k5b11;k4a10;kac15;k29b2b6980f4c}.drm</caps:sentence>
                        </ui>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
              <procedure expanded="false">
                <title>
                  <caps:sentence id="src116" class="srcSentence">To verify installation success for the RMS sharing application for Office 2010 and Active Directory RMS</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src117" class="srcSentence">To verify success of the Setup.exe command, on each computer, search for the installation log file in the <placeholder>%temp%\RMS_installer_&lt;guid&gt;</placeholder> folder, and identify the exit code.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src118" class="srcSentence">A successful installation has an exit code of 0 and any other number indicates a failed installation.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src119" class="srcSentence">Example log file name: <ui>C:\temp\RMS_Installer_9352fc91-1982-43bf-958a-2ef1fe9c2ed0</ui> </caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src120" class="srcSentence">To verify success of the aadrmprep.exe command, on each computer, search for the following text in the installation log file: <ui>aadrmprep.exe exited with status SUCCESS</ui></caps:sentence>
                      </para>
                      <alert class="note">
                        <para>
                          <caps:sentence id="src121" class="srcSentence">Sometimes, this installation can run twice; the first occurrence fails and the second is successful.</caps:sentence>
                        </para>
                      </alert>
                      <para>
                        <caps:sentence id="src122" class="srcSentence">If you want to manually check the registry changes that this tool makes, they are as follows:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence id="src123" class="srcSentence">[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MSDRM\Federation]</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence id="src124" class="srcSentence">"FederationHomeRealm"="urn:HostedRmsOnlineService:Certification"</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src125" class="srcSentence">[HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\MSDRM\Federation]</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence id="src126" class="srcSentence">"FederationHomeRealm"="urn:HostedRmsOnlineService:Certification"</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src127" class="srcSentence">[HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\MSDRM\ServiceLocation\Activation]</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence id="src128" class="srcSentence">@="&lt;certification url&gt;"
</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src129" class="srcSentence">[HKEY_CURRENT_USER\SOFTWARE\Microsoft\Office\14.0\Common\DRM] 
</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence id="src130" class="srcSentence">DefaultUser="&lt;default_user&gt;"</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </content>
                  </step>
                </steps>
              </procedure>
              <procedure expanded="false">
                <title>
                  <caps:sentence id="src131" class="srcSentence">To verify installation success for the RMS sharing application and Office add-in only</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src132" class="srcSentence">To verify success of the Setup_ipviewer.exe command, search for the following text in the installation log file: <ui>Installation success or error status: 0</ui></caps:sentence>
                      </para>
                      <para></para>
                      <para>
                        <caps:sentence id="src133" class="srcSentence">Example lines from a successful installation:  </caps:sentence>
                      </para>
                      <para>
                        <ui>
                          <caps:sentence id="src134" class="srcSentence">MSI (s) (F0:B8) [14:19:57:854]: Product: Active Directory Rights Management Services Client 2.1 -- Installation completed successfully.</caps:sentence>
                        </ui>
                      </para>
                      <para>
                        <ui>
                          <caps:sentence id="src135" class="srcSentence">MSI (s) (F0:B8) [14:19:57:854]: Windows Installer installed the product.</caps:sentence>
                          <caps:sentence id="src136" class="srcSentence"> Product Name: Active Directory Rights Management Services Client 2.1.</caps:sentence>
                          <caps:sentence id="src137" class="srcSentence"> Product Version: 1.0.1179.1.</caps:sentence>
                          <caps:sentence id="src138" class="srcSentence"> Product Language: 1033.</caps:sentence>
                          <caps:sentence id="src139" class="srcSentence"> Manufacturer: Microsoft Corporation.</caps:sentence>
                          <caps:sentence id="src140" class="srcSentence"> Installation success or error status: 0.</caps:sentence>
                        </ui>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src141" class="srcSentence">To verify success of the Office add-in, on each computer, search for the following text in the installation log file: <ui>Installation success or error status: 0</ui></caps:sentence>
                      </para>
                      <para></para>
                      <para>
                        <caps:sentence id="src142" class="srcSentence">Example lines from a successful installation:  </caps:sentence>
                      </para>
                      <para>
                        <ui>
                          <caps:sentence id="src143" class="srcSentence">MSI (s) (9C:88) [18:49:04:007]: Product: Microsoft RMS Office Addins -- Installation completed successfully.</caps:sentence>
                        </ui>
                      </para>
                      <para>
                        <ui>
                          <caps:sentence id="src144" class="srcSentence">MSI (s) (9C:88) [18:49:04:007]: Windows Installer installed the product.</caps:sentence>
                          <caps:sentence id="src145" class="srcSentence"> Product Name: Microsoft RMS Office Addins.</caps:sentence>
                          <caps:sentence id="src146" class="srcSentence"> Product Version: 1.0.7.</caps:sentence>
                          <caps:sentence id="src147" class="srcSentence"> Product Language: 1033.</caps:sentence>
                          <caps:sentence id="src148" class="srcSentence"> Manufacturer: Microsoft.</caps:sentence>
                          <caps:sentence id="src149" class="srcSentence"> Installation success or error status: 0.</caps:sentence>
                        </ui>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
            </content>
          </section>
          <section address="BKMK_uninstallscripted">
            <title>
              <caps:sentence id="src150" class="srcSentence">Uninstall commands </caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src151" class="srcSentence">Not all of the installation commands that are required for these deployments support an uninstallation command.</caps:sentence>
                <caps:sentence id="src152" class="srcSentence"> You can uninstall the AD RMS client and the sharing application, and you can uninstall the Office add-in.</caps:sentence>
                <caps:sentence id="src153" class="srcSentence"> Use the following commands to uninstall these elements.</caps:sentence>
              </para>
              <procedure expanded="false">
                <title>
                  <caps:sentence id="src154" class="srcSentence">To uninstall the AD RMS Client and the RMS sharing application</caps:sentence>
                </title>
                <steps class="bullet">
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src155" class="srcSentence">Use the following commands:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence id="src156" class="srcSentence">For 64-bit Windows: </caps:sentence>
                          </para>
                          <code>x64\setup_ipviewer.exe /uninstall /quiet</code>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src157" class="srcSentence">For 32-bit Windows: </caps:sentence>
                          </para>
                          <code>x86\setup_ipviewer.exe /uninstall /quiet</code>
                        </listItem>
                      </list>
                    </content>
                  </step>
                </steps>
              </procedure>
              <procedure expanded="false">
                <title>
                  <caps:sentence id="src158" class="srcSentence">To uninstall the Office add-in</caps:sentence>
                </title>
                <steps class="bullet">
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src159" class="srcSentence">Use the following commands:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence id="src160" class="srcSentence">For 64-bit version of Office: </caps:sentence>
                          </para>
                          <code>msiexec /x \x64\Setup[64].msi /quiet</code>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src161" class="srcSentence">For 32-bit version of Office: </caps:sentence>
                          </para>
                          <code>msiexec /x \x86\Setup.msi /quiet</code>
                        </listItem>
                      </list>
                    </content>
                  </step>
                </steps>
              </procedure>
            </content>
          </section>
          <section address="BKMK_SuppressAutomaticUpdates">
            <title>
              <caps:sentence id="src162" class="srcSentence">Suppressing automatic updates</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src163" class="srcSentence">By default, users are notified if there is a later version of the RMS sharing application, and prompted to download it.</caps:sentence>
                <caps:sentence id="src164" class="srcSentence"> You can suppress this notification by making the following registry edit:</caps:sentence>
              </para>
              <list class="ordered">
                <listItem>
                  <para>
                    <caps:sentence id="src165" class="srcSentence">Navigate to <ui>HKEY_LOCAL_MACHINE\Software\Microsoft\MSIPC</ui> and if not already present, create a new key named <ui>RmsSharingApp</ui>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src166" class="srcSentence">Select <ui>RmsSharingApp</ui>, create a new DWORD Value of <ui>AllowUpdatePrompt</ui>, and set the value to <ui>0</ui>.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src167" class="srcSentence">Because the RMS sharing application is not supported by WSUS, you can use the following technique to test any new versions of the RMS sharing application before deploying it to all users:</caps:sentence>
              </para>
              <list class="ordered">
                <listItem>
                  <para>
                    <caps:sentence id="src168" class="srcSentence">On all users’ computers, run a script to suppress automatic updates.</caps:sentence>
                    <caps:sentence id="src169" class="srcSentence"> On the computers that administrators use to test new versions, do not run this script.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src170" class="srcSentence">When a new version is available, administrators download it and test it.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src171" class="srcSentence">When testing is complete and any issues resolved, deploy the latest version to all users by using the automatic deployment instructions in this guide.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
          <section address="BKMK_DocumentTracking">
            <title>
              <caps:sentence id="src172" class="srcSentence">Azure RMS only: Configuring document tracking</caps:sentence>
            </title>
            <content>
              <caps:sentence id="src173" class="srcSentence">
                <para>If you have a <externalLink><linkText>subscription that supports document tracking</linkText><linkUri>https://technet.microsoft.com/en-us/dn858608</linkUri></externalLink>, the document tracking site is enabled by default for all users in your organization.  Document tracking shows information such as email addresses of the people who attempted to access protected documents that users shared, when these people tried to access them, and their location. If displaying this information is prohibited in your organization because of privacy requirements, you can disable access to the document tracking site by using the  <externalLink><linkText>Disable-AadrmDocumentTrackingFeature</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=623032</linkUri></externalLink> cmdlet. You can re-enable access to the site at any time, by using the <externalLink><linkText>Enable-AadrmDocumentTrackingFeature</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=623037</linkUri></externalLink>, and you can check whether access is currently enabled or disabled by using <externalLink><linkText>Get-AadrmDocumentTrackingFeature</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=623037</linkUri></externalLink>.</para> <para>To run these cmdlets, you must have at least version <embeddedLabel>2.3.0.0</embeddedLabel> of the Azure RMS module for Windows PowerShell.  For installation instructions, see <externalLink><linkText>Installing Windows PowerShell for Azure Rights Management</linkText><linkUri>https://technet.microsoft.com/library/jj585012.aspx</linkUri></externalLink>.</para><alert class="tip"><para>If you have previously downloaded and installed the module, check the version number by running: <codeInline>(Get-Module aadrm –ListAvailable).Version</codeInline></para></alert><para>The following URLs are used for document tracking and must be allowed (for example, add them to your Trusted Sites if you're using Internet Explorer with Enhanced Security): </para><list class="bullet"><listItem><para>https://*.azurerms.com</para></listItem><listItem><para>https://ecn.dev.virtualearth.net</para><alert class="note"><para>This URL is for Bing maps.</para></alert></listItem><listItem><para>https://*.microsoftonline.com</para></listItem><listItem><para>https://*.microsoftonline-p.com</para></listItem></list></caps:sentence>
            </content>
          </section>
          <section address="BKMK_FederatedDomains">
            <title>
              <caps:sentence id="src174" class="srcSentence">AD RMS only: Support for multiple email domains within your organization </caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src175" class="srcSentence">If you use AD RMS and users in your organization have multiple email domains, perhaps as a result of a merger or acquisition, you must make the following registry edit:</caps:sentence>
              </para>
              <list class="ordered">
                <listItem>
                  <para>
                    <caps:sentence id="src176" class="srcSentence">Navigate to <ui>HKEY_LOCAL_MACHINE\Software\Microsoft\MSIPC</ui> and if not already present, create a new key named <ui>RmsSharingApp</ui>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src177" class="srcSentence">Select <ui>RmsSharingApp</ui>, create a new Multi-String Value named <ui>FederatedDomains</ui>, and then add the domains and all the subdomains that your organization uses.</caps:sentence>
                    <caps:sentence id="src178" class="srcSentence"> Wildcards are not supported.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src179" class="srcSentence">For example: The company Coho Vineyard &amp; Winery has a standard email domain of <embeddedLabel>cohovineyardandwinery.com</embeddedLabel>, but as a result of mergers, they also use the email domains <embeddedLabel>cohowinery.com</embeddedLabel>, <embeddedLabel>eastcoast.cohowinery.com</embeddedLabel>, and <embeddedLabel>cohovineyard</embeddedLabel>.</caps:sentence>
                    <caps:sentence id="src180" class="srcSentence"> For the <ui>FederatedDomains</ui> value data, the administrator enters: <userInput>cohowinery.com; eastcoast.cohowinery.com; cohovineyard</userInput></caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src181" class="srcSentence">If you do not make this registry change, users might not be able to consume content that has been protected by other users in their organization.</caps:sentence>
                <caps:sentence id="src182" class="srcSentence"> This registry edit is not needed if you use Azure RMS.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </section>
      <section DoNotNumber="false" address="BKMK_AdminOverview">
        <title>
          <caps:sentence id="src183" class="srcSentence">Technical overview for the Microsoft Rights Management sharing application </caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src184" class="srcSentence">The Microsoft Rights Management sharing application is an optional downloadable application for Microsoft Windows and other platforms that provides the following:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src185" class="srcSentence">Protection of a single file or bulk protection of multiple files as well as all files within a selected folder.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src186" class="srcSentence">Full support for protection of any type of file and a built-in viewer for commonly used text and image file types.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src187" class="srcSentence">Generic protection for files that do not support RMS protection.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src188" class="srcSentence">Full interoperability with files protected using Office Information Rights Management (IRM).</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src189" class="srcSentence">Full interoperability with PDF files protected using SharePoint, FCI, and supported PDF authoring tools.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src190" class="srcSentence">The Microsoft Rights Management sharing application uses the new <externalLink><linkText>AD RMS Client 2.1 runtime</linkText><linkUri>http://www.microsoft.com/download/details.aspx?id=38396</linkUri></externalLink>.</caps:sentence>
            <caps:sentence id="src191" class="srcSentence"> By using the functionality of AD RMS 2.1, the Microsoft Rights Management sharing application provides end users a simple protection and consumption experience.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src192" class="srcSentence">With the October 2013 release of RMS, you can natively protect documents by using Office 2010 and send them to people in another company, who can then consume them by using Azure RMS.</caps:sentence>
            <caps:sentence id="src193" class="srcSentence"> In addition, with this release, if you use AD RMS in Cryptographic Mode 2, you can use RMS for individuals and consume content from people in another company that uses Azure RMS.</caps:sentence>
            <caps:sentence id="src194" class="srcSentence"> For more information about Cryptographic Mode 2, see <externalLink><linkText>AD RMS Cryptographic Modes</linkText><linkUri>http://technet.microsoft.com/library/hh867439(v=ws.10).aspx</linkUri></externalLink>.</caps:sentence>
          </para>
        </content>
        <sections>
          <section DoNotNumber="false" address="BKMK_LevelsofProtection">
            <title>
              <caps:sentence id="src195" class="srcSentence">Levels of protection – native and generic</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src196" class="srcSentence">Microsoft Rights Management sharing application supports protection at two different levels, as described in the following table.</caps:sentence>
              </para>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src197" class="srcSentence">Type of protection</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src198" class="srcSentence">Native</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src199" class="srcSentence">Generic</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src200" class="srcSentence">Description</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src201" class="srcSentence">For text, image, Microsoft Office (Word, Excel, PowerPoint) files, .pdf files, and other application file types that support AD RMS, native protection provides a strong level of protection that includes both encryption and enforcement of rights (permissions).</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src202" class="srcSentence">For all other applications and file types, generic protection provides a level of protection that includes both file encapsulation using the .pfile file type and authentication to verify if a user is authorized to open the file.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src203" class="srcSentence">Protection</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src204" class="srcSentence">Files are fully encrypted and protection is enforced in the following ways:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence id="src205" class="srcSentence">Before protected content is rendered, successful authentication must occur for those who receive the file through email or are given access to it through file or share permissions.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src206" class="srcSentence">Additionally, usage rights and policy set by the content owner when files are protected are fully enforced when the content is rendered in either IP Viewer (for protected text and image files) or the associated application (for all other supported file types).</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src207" class="srcSentence">File protection is enforced in the following ways:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence id="src208" class="srcSentence">Before protected content is rendered, successful authentication must occur for those who are authorized to open the file and given access to it.</caps:sentence>
                            <caps:sentence id="src209" class="srcSentence"> If authorization fails, the file does not open.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src210" class="srcSentence">Usage rights and policy set by the content owner are displayed to inform authorized users of the intended usage policy.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src211" class="srcSentence">Audit logging of authorized users opening and accessing files occurs, however, no usage rights are enforced by non-supporting applications.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src212" class="srcSentence">Default for file types</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src213" class="srcSentence">This is the default level of protection for the following file types:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence id="src214" class="srcSentence">Text and image files </caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src215" class="srcSentence">Microsoft Office (Word, Excel, PowerPoint) files </caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src216" class="srcSentence">Portable document format (.pdf)</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                      <para>
                        <caps:sentence id="src217" class="srcSentence">For more information, see the following section, <link xlink:href="d9992e30-f3d1-48d5-aedc-4e721f7d7c25#BKMK_SupportFileTypes">Supported file types and file name extensions</link>.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src218" class="srcSentence">This is the default protection for all other file types (such as .vsdx, .rtf, and so on) not supported through full protection.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
              <para></para>
              <para>
                <caps:sentence id="src219" class="srcSentence">You can change the default protection level that the RMS sharing application applies.</caps:sentence>
                <caps:sentence id="src220" class="srcSentence"> You can change the default level of native to generic, from generic to native, and even prevent the RMS sharing application from applying protection.</caps:sentence>
                <caps:sentence id="src221" class="srcSentence"> For more information, see the <link xlink:href="d9992e30-f3d1-48d5-aedc-4e721f7d7c25#BKMK_ChangeDefaultProtection">Changing the default protection level of files</link> section in this topic.</caps:sentence>
              </para>
            </content>
          </section>
          <section address="BKMK_SupportFileTypes" DoNotNumber="false">
            <title>
              <caps:sentence id="src222" class="srcSentence">Supported file types and file name extensions</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src223" class="srcSentence">The following table lists file types that are natively supported by Microsoft Rights Management sharing application.</caps:sentence>
                <caps:sentence id="src224" class="srcSentence"> For these file types, the original file name extension is changed when native protected is applied, and these files become read-only.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src225" class="srcSentence">In addition, when the RMS sharing application natively protects a Word, Excel, or PowerPoint file that users protect by sharing, this action automatically creates a second file that is a copy of the original with the same file name but with a <ui>.ppdf</ui> file name extension ¹.</caps:sentence>
                <caps:sentence id="src226" class="srcSentence"> This version of the file ensures that recipients who install the RMS sharing application can always open the file that has native protection applied.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src227" class="srcSentence">For files that are generically protected, the original file name extension is always changed to .pfile.</caps:sentence>
              </para>
              <alert class="warning">
                <para>
                  <caps:sentence id="src228" class="srcSentence">If you have firewalls, web proxies, or security software that inspect and take action according to file name extensions, you might need to reconfigure these to support these new file name extensions.</caps:sentence>
                </para>
              </alert>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src229" class="srcSentence">Original file name extension</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src230" class="srcSentence">RMS-protected file name extension</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src231" class="srcSentence">.txt</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src232" class="srcSentence">.ptxt</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src233" class="srcSentence">.xml</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src234" class="srcSentence">.pxml</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src235" class="srcSentence">.jpg</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src236" class="srcSentence">.pjpg</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src237" class="srcSentence">.jpeg</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src238" class="srcSentence">.ppng</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src239" class="srcSentence">.pdf</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src240" class="srcSentence">.ppdf</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src241" class="srcSentence">.png</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src242" class="srcSentence">.ppng</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src243" class="srcSentence">.tiff</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src244" class="srcSentence">.ptiff</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src245" class="srcSentence">.bmp</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src246" class="srcSentence">.pbmp</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src247" class="srcSentence">.gif</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src248" class="srcSentence">.pgif</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src249" class="srcSentence">.giff</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src250" class="srcSentence">.pgiff</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src251" class="srcSentence">.jpe</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src252" class="srcSentence">.pjpe</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src253" class="srcSentence">.jfif</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src254" class="srcSentence">.pjfif</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src255" class="srcSentence">.jif</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src256" class="srcSentence">.pjif</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src257" class="srcSentence">.jt</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src258" class="srcSentence">.pjt</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
              <para>
                <caps:sentence id="src259" class="srcSentence">¹ PDF Rendering Powered by Foxit.</caps:sentence>
                <caps:sentence id="src260" class="srcSentence"> Copyright © 2003–2014 by Foxit Corporation.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src261" class="srcSentence">The following table lists the file types that the Microsoft Rights Management sharing application natively supports in Microsoft Office 2016,  Office 2013, and Office 2010.</caps:sentence>
                <caps:sentence id="src262" class="srcSentence"> For these files, the file name extension remains the same after the file is protected by RMS.</caps:sentence>
              </para>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src263" class="srcSentence">File types supported by Office</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src264" class="srcSentence">File types supported by Office</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src265" class="srcSentence">.doc </caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src266" class="srcSentence">.docm</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src267" class="srcSentence">.docx</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src268" class="srcSentence">.dot</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src269" class="srcSentence">.dotm</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src270" class="srcSentence">.dotx</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src271" class="srcSentence">.potm</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src272" class="srcSentence">.potx</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src273" class="srcSentence">.pps</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src274" class="srcSentence">.ppsm</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src275" class="srcSentence">.ppsx</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src276" class="srcSentence">.ppt</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src277" class="srcSentence">.pptm</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src278" class="srcSentence">.pptx</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src279" class="srcSentence">.thmx</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src280" class="srcSentence">.xla</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src281" class="srcSentence">.xlam</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src282" class="srcSentence">.xls</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src283" class="srcSentence">.xlsb</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src284" class="srcSentence">.xlt</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src285" class="srcSentence">.xlsm</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src286" class="srcSentence">.xlsx</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src287" class="srcSentence">.xltm</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src288" class="srcSentence">.xltx</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src289" class="srcSentence">.xps</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section address="BKMK_ChangeDefaultProtection">
            <title>
              <caps:sentence id="src290" class="srcSentence">Changing the default protection level of files</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src291" class="srcSentence">You can change how the RMS sharing application protects files by editing the registry.</caps:sentence>
                <caps:sentence id="src292" class="srcSentence"> For example, you can force files that support native protection to be generically protected by the RMS sharing application.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src293" class="srcSentence">Reasons for why you might want to do this:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src294" class="srcSentence">To ensure that all users can open the file from their mobile devices.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src295" class="srcSentence">To ensure that all users can open the file if they don’t have an application that supports native protection.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src296" class="srcSentence">To accommodate security systems that take action on files by their file name extension and can be reconfigured to accommodate the .pfile file name extension but cannot be reconfigured to accommodate multiple file name extensions for native protection.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src297" class="srcSentence">Similarly, you can force the RMS sharing application to apply native protection to files that by default, would have generic protection applied.</caps:sentence>
                <caps:sentence id="src298" class="srcSentence"> This might be appropriate if you have an application that supports the RMS APIs – for example, a line-of-business application written by your internal developers or an application purchased from an independent software vendor (ISV).</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src299" class="srcSentence">You can also force the RMS sharing application to block the protection of files (not apply native protection or generic protection).</caps:sentence>
                <caps:sentence id="src300" class="srcSentence"> For example, this might be required if you have an automated application or service that must be able to open a specific file to process its contents.</caps:sentence>
                <caps:sentence id="src301" class="srcSentence"> When you block protection for a file type, users cannot use the RMS sharing application to protect a file that has that file type.</caps:sentence>
                <caps:sentence id="src302" class="srcSentence"> When they try, they see a message that the administrator has prevented protection and they must cancel their action to protect the file.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src303" class="srcSentence">To configure the RMS sharing application to apply generic protection to all files that by default, would have native protection applied, make the following registry edits:</caps:sentence>
              </para>
              <list class="ordered">
                <listItem>
                  <para>
                    <caps:sentence id="src304" class="srcSentence">
                      <ui>HKEY_LOCAL_MACHINE\Software\Microsoft\MSIPC\RMSSharingApp\FileProtection</ui>: Create a new key named <ui>*</ui>.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src305" class="srcSentence">This setting denotes files with any file name extension.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src306" class="srcSentence">In the newly added key of <ui>HKEY_LOCAL_MACHINE\Software\Microsoft\MSIPC\RMSSharingApp\FileProtection\*</ui>, create a new string value (REG_SZ) named <ui>Encryption</ui> that has the data value of <ui>Pfile</ui>.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src307" class="srcSentence">This setting results in the RMS sharing application applying generic protection.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src308" class="srcSentence">These two settings result in the RMS sharing application applying generic protection to all files that have a file name extension.</caps:sentence>
                <caps:sentence id="src309" class="srcSentence"> If this is your goal, no further configuration is required.</caps:sentence>
                <caps:sentence id="src310" class="srcSentence"> However, you can define exceptions for specific file types, so that they are still natively protected.</caps:sentence>
                <caps:sentence id="src311" class="srcSentence"> To do this, you must make three additional registry edits for each file type:</caps:sentence>
              </para>
              <list class="ordered">
                <listItem>
                  <para>
                    <caps:sentence id="src312" class="srcSentence">
                      <ui>HKEY_LOCAL_MACHINE\Software\Microsoft\MSIPC\RMSSharingApp\FileProtection</ui>: Add a new key that has the name of the file name extension (without the preceding period).</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src313" class="srcSentence">For example, for files that have a .docx file name extension, create a key named <ui>DOCX</ui>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src314" class="srcSentence">In the newly added file type key (for example, <ui>HKEY_LOCAL_MACHINE\Software\Microsoft\MSIPC\RMSSharingApp\FileProtection\DOCX</ui>), create a new DWORD Value named <ui>AllowPFILEEncryption</ui> that has a value of <ui>0</ui>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src315" class="srcSentence">In the newly added file type key (for example, <ui>HKEY_LOCAL_MACHINE\Software\Microsoft\MSIPC\RMSSharingApp\FileProtection\DOCX</ui>), create a new String Value named <ui>Encryption</ui> that has a value of <ui>Native</ui>.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src316" class="srcSentence">As a result of these settings, all files are generically protected except files that have a .docx file name extension, which are natively protected by the RMS sharing application.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src317" class="srcSentence">Repeat these three steps for other file types that you want to define as exceptions because they support native protection and you do not want them to be generically protected by the RMS sharing application.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src318" class="srcSentence">You can make similar registry edits for other scenarios by changing the value of the <ui>Encryption</ui> string that supports the following values: </caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src319" class="srcSentence">
                      <ui>Pfile</ui>: Generic protection</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src320" class="srcSentence">
                      <ui>Native</ui>: Native protection</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src321" class="srcSentence">
                      <ui>Off</ui>: Block protection</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
        </sections>
      </section>
      <relatedTopics>
        <link xlink:href="eaf6d02c-aa36-4915-856e-49bb71ab1484">Rights Management sharing application user guide</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>