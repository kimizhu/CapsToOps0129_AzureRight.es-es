---
title: Descargar e instalar la aplicaci&#243;n para uso compartido de Rights Management
ms.custom: na
ms.reviewer: na
ms.service: rights-management
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2bf09690-9dba-43b7-9e0a-0110915d4081
---
# Descargar e instalar la aplicaci&#243;n para uso compartido de Rights Management
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="es-ES">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="8c9bb888f4c9603bc98e0becd3cf1347" id="tgt1" class="tgtSentence">No hace falta que sea un administrador local para instalar la aplicación RMS sharing.</caps:sentence>
          <caps:sentence sentenceid="82df6faacee2862a7bdf283e00278857" id="tgt2" class="tgtSentence"> Sin embargo, si no lo es y usa Office 2010, hay algunas limitaciones.</caps:sentence>
          <caps:sentence sentenceid="b45356185bcd5869fce4036503e25313" id="tgt3" class="tgtSentence"> Para obtener más información, consulte la sección <link xlink:href="#BKMK_SetupOffice2010">If you are not a local administrator and use Office 2010</link> de este tema.</caps:sentence>
        </para>
        <procedure>
          <title>
            <caps:sentence sentenceid="3cf4cc52a998b14c5c7984a40033c719" id="tgt4" class="tgtSentence">Para descargar e instalar la aplicación Rights Management sharing</caps:sentence>
          </title>
          <steps class="ordered">
            <step>
              <content>
                <para>
                  <caps:sentence sentenceid="899369be6455fb30645fecfd0a8e727f" id="tgt5" class="tgtSentence">Vaya a la página de <externalLink><linkText>Microsoft Rights Management</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=303970</linkUri></externalLink> en el sitio web de Microsoft.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence sentenceid="85765d861a92249118dcdf8801724005" id="tgt6" class="tgtSentence">En la sección <ui>Equipos</ui>, haga clic en el icono de la <ui>aplicación RMS para Windows</ui> y guarde el archivo <ui>Setup.exe</ui> para instalar la aplicación Microsoft Rights Management sharing.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence sentenceid="399032730a8ace24e93c849cce10f050" id="tgt7" class="tgtSentence">Haga doble clic en el archivo Setup.exe que se descargó.</caps:sentence>
                  <caps:sentence sentenceid="0167027de0dbe004ace43d2ed2a2f550" id="tgt8" class="tgtSentence"> Si el sistema le pregunta si desea continuar, haga clic en <ui>Sí</ui>.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence sentenceid="abacc694f0d29dee144cf040dbc3e3ed" id="tgt9" class="tgtSentence">En la página <ui>Instalar Microsoft RMS</ui>, haga clic en <ui>siguiente</ui> y espere a que finalice la instalación.</caps:sentence>
                </para>
                <alert class="note">
                  <para>
                    <caps:sentence sentenceid="432ae073e8c370ce6dc8247b5faab66b" id="tgt10" class="tgtSentence">La aplicación RMS sharing requiere Microsoft .NET Framework, versión mínima 4.0.</caps:sentence>
                    <caps:sentence sentenceid="0ee787c49fc3c85d5422da017f84334c" id="tgt11" class="tgtSentence"> El programa de instalación comprueba si está instalado y, si no es así, verá un mensaje con un vínculo para instalarlo.</caps:sentence>
                  </para>
                </alert>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence sentenceid="bbf86a627e9d90a333b8e64aefbb6574" id="tgt12" class="tgtSentence">Cuando finalice la instalación, haga clic en <ui>Reiniciar</ui> para reiniciar el equipo y completar la instalación.</caps:sentence>
                  <caps:sentence sentenceid="cb5f70d5b72083957285c3af1cd1eb27" id="tgt13" class="tgtSentence"> O bien, haga clic en <ui>Cerrar</ui> y reinicie el equipo más tarde para completar la instalación.</caps:sentence>
                </para>
              </content>
            </step>
          </steps>
          <conclusion>
            <content>
              <para>
                <caps:sentence sentenceid="3308416b354d904c4536265b6ac18515" id="tgt14" class="tgtSentence">Ahora ya puede empezar a proteger sus archivos o a leer los archivos protegidos por otros usuarios.</caps:sentence>
              </para>
            </content>
          </conclusion>
        </procedure>
      </introduction>
      <section address="BKMK_SetupOffice2010" expanded="true">
        <title>
          <caps:sentence sentenceid="0fc6f91874dc4eb52e51cd6e3c1e2004" id="tgt15" class="tgtSentence">Si no es un administrador local y usa Office 2010</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="c3adf0413d07a2358adda230d9855950" id="tgt16" class="tgtSentence">Si inicia sesión en el equipo y no tiene derechos administrativos locales y el programa de instalación detecta que tiene instalado Office 2010, verá un mensaje de advertencia en el que se le indicará que algunos escenarios no funcionarán con tal configuración.</caps:sentence>
            <caps:sentence sentenceid="c01a6b6b104f552395841adf32799258" id="tgt17" class="tgtSentence"> Los escenarios son los siguientes:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="8eaf8df9889ba0d3a74c2496705bab7a" id="tgt18" class="tgtSentence">Si su organización usa Azure RMS en lugar de una versión local de RMS: </caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="639d6d19111395cb640d2c820b06af50" id="tgt19" class="tgtSentence">Las características de Information Rights Management (IRM) de Office no estarán disponibles.</caps:sentence>
                    <caps:sentence sentenceid="8a8f170afce37495958f1859bebbf3ee" id="tgt20" class="tgtSentence"> Por ejemplo, la opción <ui>No reenviar</ui> de los mensajes de correo electrónico y los permisos <ui>Restringir acceso</ui> que puede establecer desde el menú <ui>Archivo</ui> de Word y Excel.</caps:sentence>
                    <caps:sentence sentenceid="457acf0c7461bd65f27aa715dcd2c7b5" id="tgt21" class="tgtSentence"> Puede usar la opción Uso compartido protegido de la cinta y las opciones del botón derecho del Explorador de archivos.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="76ac3d004b398c5f094b959fd26e61ad" id="tgt22" class="tgtSentence">Si su organización usa una versión local de RMS en lugar de Azure RMS: </caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="aae52dba9eb865c568665d09f474b5fc" id="tgt23" class="tgtSentence">No podrá leer un documento protegido que le envíe alguien de otra organización que use Azure RMS.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="ff5a90ed45c2e54bfafa315b654fc25f" id="tgt24" class="tgtSentence">Si no es un administrador local y usa Office 365 u Office 2013, no verá este mensaje y se admitirán estos escenarios.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="bcaab1fe2b8b721d93823a7cac0035f4" id="tgt25" class="tgtSentence">Puede continuar la instalación con estas limitaciones conocidas.</caps:sentence>
            <caps:sentence sentenceid="916525d3e670455d000ab69fe6190b1b" id="tgt26" class="tgtSentence"> Asimismo, puede detener la instalación y volver a ejecutarla con la opción <ui>Ejecutar como administrador</ui> al ejecutar Setup.exe en el paso 3, o bien pedirle a un administrador que se lo instale.</caps:sentence>
            <caps:sentence sentenceid="d72d846483d203439358130c678876d0" id="tgt27" class="tgtSentence"> Los administradores pueden <externalLink><linkText>crear un script para esta instalación</linkText><linkUri>https://technet.microsoft.com/library/dn339003.aspx#BKMK_ScriptedInstall</linkUri></externalLink> para que se instale automáticamente.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="9b264ffec0213e0096618f896965a728" id="tgt28" class="tgtSentence">Ejemplos y otras instrucciones</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="7e679cf432376a1391e421a3d1ae6dc0" id="tgt29" class="tgtSentence">Para obtener ejemplos de cómo puede usar la aplicación para uso compartido de Rights Management e instrucciones de procedimientos, consulte las siguientes secciones de la guía de usuario de la aplicación para uso compartido de Rights Management:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <link xlink:href="eaf6d02c-aa36-4915-856e-49bb71ab1484#BKMK_SharingExamples">Examples for using the RMS sharing application</link>
              </para>
            </listItem>
            <listItem>
              <para>
                <link xlink:href="eaf6d02c-aa36-4915-856e-49bb71ab1484#BKMK_SharingInstructions">What do you want to do?</link>
              </para>
            </listItem>
          </list>
        </content>
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
          <caps:sentence id="src1" class="srcSentence">You do not have to be a local administrator to install the RMS sharing application.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> However, if you are not and you use Office 2010, there are some limitations.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> For more information, see the <link xlink:href="#BKMK_SetupOffice2010">If you are not a local administrator and use Office 2010</link> section in this topic.</caps:sentence>
        </para>
        <procedure>
          <title>
            <caps:sentence id="src4" class="srcSentence">To download and install the Rights Management sharing application</caps:sentence>
          </title>
          <steps class="ordered">
            <step>
              <content>
                <para>
                  <caps:sentence id="src5" class="srcSentence">Go to the <externalLink><linkText>Microsoft Rights Management</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=303970</linkUri></externalLink> page on the Microsoft website.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence id="src6" class="srcSentence">In the <ui>Computers</ui> section, click the icon for the <ui>RMS app for Windows</ui> and save the <ui>Setup.exe</ui> file to install Microsoft Rights Management sharing application.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence id="src7" class="srcSentence">Double-click the Setup.exe file that was downloaded.</caps:sentence>
                  <caps:sentence id="src8" class="srcSentence"> If you are prompted to continue, click <ui>Yes</ui>.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence id="src9" class="srcSentence">On the <ui>Setup Microsoft RMS</ui> page, click <ui>Next</ui>, and wait for the installation to finish.</caps:sentence>
                </para>
                <alert class="note">
                  <para>
                    <caps:sentence id="src10" class="srcSentence">The RMS sharing application requires the Microsoft .NET Framework, minimum version 4.0.</caps:sentence>
                    <caps:sentence id="src11" class="srcSentence"> Setup checks to see whether this is installed and if it is not, you will see a message with a link to install it.</caps:sentence>
                  </para>
                </alert>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence id="src12" class="srcSentence">When the installation finishes, click <ui>Restart</ui> to restart your computer and complete the installation.</caps:sentence>
                  <caps:sentence id="src13" class="srcSentence"> Or, click <ui>Close</ui> and restart your computer later to complete the installation.</caps:sentence>
                </para>
              </content>
            </step>
          </steps>
          <conclusion>
            <content>
              <para>
                <caps:sentence id="src14" class="srcSentence">You’re now ready to start protecting your files or read files that others have protected.</caps:sentence>
              </para>
            </content>
          </conclusion>
        </procedure>
      </introduction>
      <section address="BKMK_SetupOffice2010" expanded="true">
        <title>
          <caps:sentence id="src15" class="srcSentence">If you are not a local administrator and use Office 2010</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src16" class="srcSentence">If you sign in to your computer and do not have local administrative rights, and Setup detects that you have Office 2010 installed, you will see a warning message that some scenarios will not work with this configuration.</caps:sentence>
            <caps:sentence id="src17" class="srcSentence"> The scenarios are:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src18" class="srcSentence">If your organization uses Azure RMS rather than an on-premises version of RMS: </caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src19" class="srcSentence">The Information Rights Management (IRM) features of Office will not be available.</caps:sentence>
                    <caps:sentence id="src20" class="srcSentence"> For example, the <ui>Do Not Forward</ui> option for emails, and the <ui>Restrict Access</ui> permissions that you can set from the <ui>File</ui> menu in Word and Excel.</caps:sentence>
                    <caps:sentence id="src21" class="srcSentence"> You can use the Share Protected option on the ribbon, and the right-click options from File Explorer.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src22" class="srcSentence">If your organization uses an on-premises version of RMS rather than Azure RMS: </caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src23" class="srcSentence">You won’t be able to read a protected document sent to you by somebody from another organization that’s using Azure RMS.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src24" class="srcSentence">If you are not a local administrator and use Office 365 or Office 2013, you do not see this message and these scenarios are supported.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src25" class="srcSentence">You can continue the installation with these known limitations.</caps:sentence>
            <caps:sentence id="src26" class="srcSentence"> Or you can stop the installation and either rerun it with the <ui>Run as administrator</ui> option when you run Setup.exe in step 3, or ask an administrator to install it for you.</caps:sentence>
            <caps:sentence id="src27" class="srcSentence"> Administrators can <externalLink><linkText>script this installation</linkText><linkUri>https://technet.microsoft.com/library/dn339003.aspx#BKMK_ScriptedInstall</linkUri></externalLink> for you so that it installs automatically.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src28" class="srcSentence">Examples and other instructions</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src29" class="srcSentence">For examples for how you might use the Rights Management sharing application, and how-to instructions, see the following sections from the Rights Management sharing application user guide:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <link xlink:href="eaf6d02c-aa36-4915-856e-49bb71ab1484#BKMK_SharingExamples">Examples for using the RMS sharing application</link>
              </para>
            </listItem>
            <listItem>
              <para>
                <link xlink:href="eaf6d02c-aa36-4915-856e-49bb71ab1484#BKMK_SharingInstructions">What do you want to do?</link>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="eaf6d02c-aa36-4915-856e-49bb71ab1484">Rights Management sharing application user guide</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>