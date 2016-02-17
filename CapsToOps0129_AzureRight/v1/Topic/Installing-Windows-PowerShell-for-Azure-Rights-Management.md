---
title: Instalaci&#243;n de Windows PowerShell para Azure Rights Management
ms.custom: na
ms.reviewer: na
ms.service: rights-management
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0d665ed6-b1de-4d63-854a-bc57c1c49844
---
# Instalaci&#243;n de Windows PowerShell para Azure Rights Management
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="es-ES">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="cd3f5d276ce00c0604c913cd53306f1d" id="tgt1" class="tgtSentence">Use la información siguiente para instalar Windows PowerShell para Microsoft <token>aad_rightsmanagement_1</token> (Azure RMS).</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="95eb4c9647ead18e1d1ee6fbb51da57a" id="tgt2" class="tgtSentence">Puede utilizar este módulo de Windows PowerShell para administrar <token>aad_rightsmanagement_1</token> desde la línea de comandos mediante el uso de cualquier equipo que tenga una conexión a Internet y que cumpla los requisitos previos enumerados en la sección siguiente.</caps:sentence>
          <caps:sentence sentenceid="051b871b2f01859d3f3b2856a4426801" id="tgt3" class="tgtSentence"> Windows PowerShell para <token>aad_rightsmanagement_1</token> admite el uso de scripting para la automatización o puede que sea necesario para escenarios de configuración avanzada.</caps:sentence>
          <caps:sentence sentenceid="a5fdabf5af7a9f070c62bcc415503ef3" id="tgt4" class="tgtSentence"> Para obtener más información acerca de las tareas de administración y las configuraciones que admite el módulo, consulte <link xlink:href="a890e04a-4b70-41b5-8d5f-3c210a669faa">Administering Azure Rights Management by Using Windows PowerShell</link>.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="b5b8e67d6a37d24ad73c89e4c7ac8c9e" id="tgt5" class="tgtSentence">Requisitos previos</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="4af90e9d4bd32ceaed0a372eff422b94" id="tgt6" class="tgtSentence">Esta tabla enumera los requisitos previos para instalar Windows PowerShell para <token>aad_rightsmanagement_1</token>.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ba12fb48e2d23bb2bd2819f64d02ec7e" id="tgt7" class="tgtSentence">Requisito</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5dc731e46ae38b87ff3e3e2eaf459db2" id="tgt8" class="tgtSentence">Más información</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="663b5f67676b780a020968ed366ec499" id="tgt9" class="tgtSentence">Una versión de Windows que admita el módulo de administración <token>aad_rightsmanagement_2</token></caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="25323fb12ba6582f3434da55f594a860" id="tgt10" class="tgtSentence">Revise la lista de sistemas operativos compatibles en la sección <ui>Requisitos del sistema</ui> de la <externalLink><linkText>página de descargas de la herramienta de administración de Azure Rights Management</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=257721</linkUri></externalLink>.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e0d3592040eb5ae8a2899277541175b5" id="tgt11" class="tgtSentence">Versión mínima de Windows PowerShell: 2.0</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7d7bd932e8af8eb0f98b407871aa604f" id="tgt12" class="tgtSentence">El soporte para el módulo de administración <token>aad_rightsmanagement_2</token> se presenta en Windows PowerShell 2.0.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="0541480cf9e1c16de13df9646030dcb9" id="tgt13" class="tgtSentence">De forma predeterminada, la mayoría de sistemas operativos de Windows se instalan con una versión 2.0 de Windows PowerShell, como mínimo.</caps:sentence>
                    <caps:sentence sentenceid="55e4d7e3befb9c5133769ec0b148811d" id="tgt14" class="tgtSentence"> Si necesita instalar Windows PowerShell 2.0, consulte <externalLink><linkText>Instalación de Windows PowerShell 2.0</linkText><linkUri>http://msdn.microsoft.com/library/ff637750.aspx</linkUri></externalLink>.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="ca39d393387017832828d0c960a21992" id="tgt15" class="tgtSentence">Sugerencia: Puede confirmar la versión de Windows PowerShell que se está ejecutando. Para ello, escriba <userInput>$PSVersionTable</userInput> en una sesión de Windows PowerShell.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f40d92b61261314e0d4072c0e786fb22" id="tgt16" class="tgtSentence">Versión mínima de Microsoft .NET Framework: 4.5</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="642c100eb2611ca0301c80629a4aade7" id="tgt17" class="tgtSentence">Nota: Esta versión de Microsoft .NET Framework está incluida con los últimos sistemas operativos, por lo que solo tendrá que instalarla manualmente en el caso de que el sistema operativo del cliente sea anterior a Windows 8.0 o de que el sistema operativo del servidor sea anterior a Windows Server 2012.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cf05f7a02968aee70a9e3c693a0887dd" id="tgt18" class="tgtSentence">Si la versión mínima de Microsoft .NET Framework todavía no está instalada, puede descargar <externalLink><linkText>Microsoft .NET Framework 4.5</linkText><linkUri>http://www.microsoft.com/download/details.aspx?id=30653</linkUri></externalLink>.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="c8a7bac9811cf52c5eb87cb90faf1c24" id="tgt19" class="tgtSentence">Esta versión mínima de Microsoft .NET Framework es necesaria para algunas de las clases que usa el módulo de administración de <token>aad_rightsmanagement_2</token>.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e5b4cf428c2a06f927b82dd9443a013c" id="tgt20" class="tgtSentence">Ayudante para el inicio de sesión de Microsoft Online Services 7.0</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7d1b8775128b4cabf5de4d3088f6545e" id="tgt21" class="tgtSentence">Microsoft Online Services - Ayudante para el inicio de sesión es obligatorio para la autenticación de <token>aad_rightsmanagement_1</token>.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="3869d1e94bf61ebc084fb4052de0eb9f" id="tgt22" class="tgtSentence">Para obtener más información, vea <externalLink><linkText>Centro de descarga: Ayudante de Microsoft Online Services para profesionales de TI RTW</linkText><linkUri>http://www.microsoft.com/en-us/download/details.aspx?id=41950</linkUri></externalLink>.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="2c439576a88bbcf379b63af67e3e618e" id="tgt23" class="tgtSentence">Cómo instalar el módulo de administración Rights Management</caps:sentence>
        </title>
        <content>
          <procedure>
            <title></title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="fac5687afc458afa29dd1de0fb9979b3" id="tgt24" class="tgtSentence">Vaya al Centro de descarga de Microsoft y <externalLink><linkText>descargue la herramienta de administración de Azure Rights Management</linkText><linkUri>https://go.microsoft.com/fwlink/?LinkId=257721</linkUri></externalLink>, que contiene el módulo de administración de <token>aad_rightsmanagement_1</token> para Windows PowerShell.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="529c78bd5738bceb2e7afd5c29e7a19e" id="tgt25" class="tgtSentence">En la carpeta local en la que descargó y guardó el archivo de instalación de <token>aad_rightsmanagement_2</token>, haga doble clic en el archivo ejecutable que descargó para su plataforma (WindowsAzureADRightsManagementAdministration_x64 o WindowsAzureADRightsManagementAdministration_x86.exe) para iniciar el asistente para la configuración de administración Azure AD Rights Management.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="2267545103c9e1387bf304a0df2c06f5" id="tgt26" class="tgtSentence">Completa el asistente.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence sentenceid="29c22d6bb4e6088fc57059d5fa21a885" id="tgt27" class="tgtSentence">Ahora ya se ha instalado Windows PowerShell para <token>aad_rightsmanagement_1</token>.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="0a4f90ce90fc062c4fc00532513d86da" id="tgt28" class="tgtSentence">Pasos siguientes</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="2ba62d45f24d9a9c565993b59d794564" id="tgt29" class="tgtSentence">Para consultar los cmdlets disponibles, inicie Windows PowerShell con la opción <ui>Ejecutar como administrador</ui> y escriba lo que se indica a continuación: </caps:sentence>
          </para>
          <code>Get-Command -Module aadrm</code>
          <para>
            <caps:sentence sentenceid="1efafef9fcef64de5ee3d9dcd2663b0b" id="tgt30" class="tgtSentence">Use el comando <codeInline>the Get-Help &lt;cmdlet_name&gt;</codeInline> para consultar la Ayuda para un cmdlet específico.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="56641ceb67424355961097d449175b73" id="tgt31" class="tgtSentence">Para obtener más información:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="41f2cf542f95c5ddf245d0dd38023d8e" id="tgt32" class="tgtSentence">Lista completa de cmdlets disponibles: <externalLink><linkText>Cmdlets de Azure Rights Management</linkText><linkUri>https://msdn.microsoft.com/library/windowsazure/dn629398.aspx</linkUri></externalLink></caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="91848f5014f33ff8298a94d47c7bf8c4" id="tgt33" class="tgtSentence">Lista de los principales escenarios de configuración que admiten Windows PowerShell: <link xlink:href="a890e04a-4b70-41b5-8d5f-3c210a669faa">Administering Azure Rights Management by Using Windows PowerShell</link></caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="4d88b7ff6d60a3e437d6d61419072028" id="tgt34" class="tgtSentence">Antes de poder ejecutar cualquier comando que configure el servicio de <token>aad_rightsmanagement_1</token>, debe conectarse al servicio con el cmdlet <externalLink><linkText>Connect-AadrmService</linkText><linkUri>https://msdn.microsoft.com/library/windowsazure/dn629415.aspx</linkUri></externalLink>.</caps:sentence>
            <caps:sentence sentenceid="62a9e8e64df45f7461ee937bbe101f60" id="tgt35" class="tgtSentence"> Cuando termine de ejecutar los comandos de configuración que desea, desconéctese del servicio con el cmdlet <externalLink><linkText>Disconnect-AadrmService</linkText><linkUri>https://msdn.microsoft.com/library/windowsazure/dn629416.aspx</linkUri></externalLink>.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="d69ee7b160b369261cb36d6c2bbaa396" id="tgt36" class="tgtSentence">Si todavía no ha activado <token>aad_rightsmanagement_2</token>, puede hacerlo después de haberse conectado al servicio, mediante el cmdlet <externalLink><linkText>Enable-Aadrm</linkText><linkUri>https://msdn.microsoft.com/library/windowsazure/dn629412.aspx</linkUri></externalLink>.</caps:sentence>
            </para>
          </alert>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="a890e04a-4b70-41b5-8d5f-3c210a669faa">Administering Azure Rights Management by Using Windows PowerShell</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Use the following information to help you install Windows PowerShell for Microsoft <token>aad_rightsmanagement_1</token> (Azure RMS).</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src2" class="srcSentence">You can use this Windows PowerShell module to administer <token>aad_rightsmanagement_1</token> from the command line by using any computer that has an Internet connection and that meets the prerequisites listed in the next section.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> Windows PowerShell for <token>aad_rightsmanagement_1</token> supports scripting for automation or might be necessary for advanced configuration scenarios.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> For more information about the administration tasks and configurations that the module supports, see <link xlink:href="a890e04a-4b70-41b5-8d5f-3c210a669faa">Administering Azure Rights Management by Using Windows PowerShell</link>.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src5" class="srcSentence">Prerequisites</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src6" class="srcSentence">This table lists the prerequisites to install and use Windows PowerShell for <token>aad_rightsmanagement_1</token>.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src7" class="srcSentence">Requirement</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src8" class="srcSentence">More information</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src9" class="srcSentence">A version of Windows that supports the <token>aad_rightsmanagement_2</token> administration module</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src10" class="srcSentence">Check the list of supported operating systems in the <ui>System Requirements</ui> section of the <externalLink><linkText>download page for the Azure Rights Management Administration Tool</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=257721</linkUri></externalLink>.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src11" class="srcSentence">Minimum version of Windows PowerShell: 2.0</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src12" class="srcSentence">Support for the <token>aad_rightsmanagement_2</token> administration module is introduced in Windows PowerShell 2.0.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src13" class="srcSentence">By default, most Windows operating systems install with at least version 2.0 of Windows PowerShell.</caps:sentence>
                    <caps:sentence id="src14" class="srcSentence"> If you need to install Windows PowerShell 2.0, see <externalLink><linkText>Install Windows PowerShell 2.0</linkText><linkUri>http://msdn.microsoft.com/library/ff637750.aspx</linkUri></externalLink>.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src15" class="srcSentence">Tip: You can confirm the version of Windows PowerShell that you are running by typing <userInput>$PSVersionTable</userInput> in a Windows PowerShell session.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src16" class="srcSentence">Minimum version of the Microsoft .NET Framework: 4.5</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src17" class="srcSentence">Note: This version of the Microsoft .NET Framework is included with the later operating systems, so you should  need to manually install it only if your client operating system is less than Windows 8.0 or your server operating system is less than Windows Server 2012.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src18" class="srcSentence">If the minimum version of the  Microsoft .NET Framework is not already installed, you can download <externalLink><linkText>Microsoft .NET Framework 4.5</linkText><linkUri>http://www.microsoft.com/download/details.aspx?id=30653</linkUri></externalLink>.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src19" class="srcSentence">This minimum version of the Microsoft .NET Framework is required for some of the classes that the <token>aad_rightsmanagement_2</token> administration module uses.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src20" class="srcSentence">Microsoft Online Services Sign-In Assistant 7.0</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src21" class="srcSentence">The Microsoft Online Services Sign-In Assistant is required for <token>aad_rightsmanagement_1</token> authentication.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src22" class="srcSentence">For more information, see <externalLink><linkText>Download Center: Microsoft Online Services Assistant for IT Professionals RTW</linkText><linkUri>http://www.microsoft.com/en-us/download/details.aspx?id=41950</linkUri></externalLink>.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src23" class="srcSentence">How to install the Rights Management administration module</caps:sentence>
        </title>
        <content>
          <procedure>
            <title></title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src24" class="srcSentence">Go to the Microsoft Download Center and <externalLink><linkText>download the Azure Rights Management Administration Tool</linkText><linkUri>https://go.microsoft.com/fwlink/?LinkId=257721</linkUri></externalLink>, which contains the <token>aad_rightsmanagement_1</token> administration module for Windows PowerShell.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src25" class="srcSentence">From the local folder where you downloaded and saved the <token>aad_rightsmanagement_2</token> installer file, double-click the executable file that you downloaded for your platform (WindowsAzureADRightsManagementAdministration_x64 or WindowsAzureADRightsManagementAdministration_x86.exe) to start the Azure AD Rights Management Administration Setup Wizard.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src26" class="srcSentence">Complete the wizard.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence id="src27" class="srcSentence">Windows PowerShell for <token>aad_rightsmanagement_1</token> is now installed.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src28" class="srcSentence">Next steps</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src29" class="srcSentence">To see which cmdlets are available, start Windows PowerShell with the <ui>Run as administrator</ui> option and type the following: </caps:sentence>
          </para>
          <code>Get-Command -Module aadrm</code>
          <para>
            <caps:sentence id="src30" class="srcSentence">Use <codeInline>the Get-Help &lt;cmdlet_name&gt;</codeInline> command to see the Help for a specific cmdlet.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src31" class="srcSentence">For more information:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src32" class="srcSentence">Full list of cmdlets available: <externalLink><linkText>Azure Rights Management Cmdlets</linkText><linkUri>https://msdn.microsoft.com/library/windowsazure/dn629398.aspx</linkUri></externalLink></caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src33" class="srcSentence">List of main configuration scenarios that support Windows PowerShell: <link xlink:href="a890e04a-4b70-41b5-8d5f-3c210a669faa">Administering Azure Rights Management by Using Windows PowerShell</link></caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src34" class="srcSentence">Before you can run any commands that configure the <token>aad_rightsmanagement_1</token> service, you must connect to the  service by using the <externalLink><linkText>Connect-AadrmService</linkText><linkUri>https://msdn.microsoft.com/library/windowsazure/dn629415.aspx</linkUri></externalLink> cmdlet.</caps:sentence>
            <caps:sentence id="src35" class="srcSentence"> When you have finished running the configuration commands that you want, disconnect from the service by using the <externalLink><linkText>Disconnect-AadrmService</linkText><linkUri>https://msdn.microsoft.com/library/windowsazure/dn629416.aspx</linkUri></externalLink> cmdlet.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src36" class="srcSentence">If you have not yet activated <token>aad_rightsmanagement_2</token>, you can do this after you have connected to the service, by using the <externalLink><linkText>Enable-Aadrm</linkText><linkUri>https://msdn.microsoft.com/library/windowsazure/dn629412.aspx</linkUri></externalLink> cmdlet.</caps:sentence>
            </para>
          </alert>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="a890e04a-4b70-41b5-8d5f-3c210a669faa">Administering Azure Rights Management by Using Windows PowerShell</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>