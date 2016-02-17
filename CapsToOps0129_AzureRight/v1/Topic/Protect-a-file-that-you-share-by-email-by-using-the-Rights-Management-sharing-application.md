---
title: Protecci&#243;n de un archivo que comparte por correo electr&#243;nico con la aplicaci&#243;n Rights Management sharing
ms.custom: na
ms.reviewer: na
ms.service: rights-management
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4c1cd1d3-78dd-4f90-8b37-dcc9205a6736
---
# Protecci&#243;n de un archivo que comparte por correo electr&#243;nico con la aplicaci&#243;n Rights Management sharing
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="es-ES">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://clixdevr3.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="7238a96e0c59bb6402060f9df9dfbf5b" id="tgt1" class="tgtSentence">Cuando protege un archivo que comparte por correo electrónico, se crea una nueva versión del archivo original.</caps:sentence>
          <caps:sentence sentenceid="fd4bec34ac16305d3a04ae6e9a0e5595" id="tgt2" class="tgtSentence"> El archivo original permanece desprotegido y la nueva versión se protege y se adjunta automáticamente a un correo electrónico que luego envía.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="5a7624b541982842bf700196500bb2cc" id="tgt3" class="tgtSentence">En algunos casos (como los archivos creados por Microsoft Word, Excel y PowerPoint), la aplicación RMS sharing crea dos versiones del archivo que se adjunta al mensaje de correo electrónico.</caps:sentence>
          <caps:sentence sentenceid="92c628512d2d68c346e286ff9ab4739f" id="tgt4" class="tgtSentence"> La segunda versión del archivo tiene una extensión de nombre de archivo llamada <ui>.ppdf</ui> y es una instantánea PDF del archivo.</caps:sentence>
          <caps:sentence sentenceid="3524774f9c15dc897f40f1c9d7125561" id="tgt5" class="tgtSentence"> Esta versión del archivo garantiza que los destinatarios siempre pueden leerlo, incluso si no tienen instalada la misma aplicación que usó para crearlo.</caps:sentence>
          <caps:sentence sentenceid="782003ebc13db80b4aedb9d030ce8738" id="tgt6" class="tgtSentence"> Este suele ser el caso cuando las personas leen su correo electrónico en dispositivos móviles y quieren ver los datos adjuntos.</caps:sentence>
          <caps:sentence sentenceid="1ad89c4714201bf686c129aad86ea483" id="tgt7" class="tgtSentence"> Todo lo que necesitan para abrir el archivo es la aplicación RMS sharing.</caps:sentence>
          <caps:sentence sentenceid="e7f7e214d78cf4f49fed6f423f314577" id="tgt8" class="tgtSentence"> Podrán leer entonces el archivo adjunto, pero no podrán modificarlo hasta que abran la otra versión del archivo con una aplicación que sea compatible con RMS.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="e9d93e2a96e4ee0c3b8864c9cfd3b38c" id="tgt9" class="tgtSentence">Si su organización usa Azure RMS, puede realizar un seguimiento de los archivos que se protegen mediante uso compartido:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="3bdf833a8a101476829e80a2b1008009" id="tgt10" class="tgtSentence">Seleccione una opción para recibir mensajes de correo electrónico cuando alguien intente abrir estos datos adjuntos protegidos.</caps:sentence>
              <caps:sentence sentenceid="0f1131a34884c9e69faae45d8ebbb0b4" id="tgt11" class="tgtSentence"> Cada vez que se tenga acceso al archivo, se le notificará quién intentó abrirlo y cuándo, y si lo lograron (se autenticaron correctamente) o no.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="92872eeb8d4006cc3076182ed7fe7876" id="tgt12" class="tgtSentence">Use el sitio de seguimiento de documentación.</caps:sentence>
              <caps:sentence sentenceid="40768e71470536ed5246114d35dd76a5" id="tgt13" class="tgtSentence"> Puede incluso dejar de compartir el archivo si revoca el acceso a él en el sitio de seguimiento de documentos.</caps:sentence>
              <caps:sentence sentenceid="1070f425823a6e05a98eb2d747f0c53d" id="tgt14" class="tgtSentence"> Para obtener más información, vea <link xlink:href="61f349ce-bdd2-45c1-acc5-bc83937fb187">Track and revoke your documents when you use the RMS sharing application</link>.</caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <section DoNotNumber="false" expanded="true">
        <title>
          <caps:sentence sentenceid="5dd8bd35b0254645f41c7d855eba3ff5" id="tgt15" class="tgtSentence">Uso de Outlook: Para proteger un archivo que se comparte por correo electrónico</caps:sentence>
        </title>
        <content>
          <procedure>
            <title></title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="6abaf6187b023cca7acdd4c315cbccd5" id="tgt16" class="tgtSentence">Cree su mensaje de correo electrónico y adjunte el archivo.</caps:sentence>
                    <caps:sentence sentenceid="56411d654ac26a142430f7d1b4320974" id="tgt17" class="tgtSentence"> A continuación, en la pestaña <ui>Mensaje</ui>, en el grupo <ui>RMS</ui>, haga clic en <ui>Compartir protegido</ui> y después otra vez en <ui>Compartir protegido</ui>:</caps:sentence>
                  </para>
                  <para>
                    <mediaLinkInline>
                      <image xlink:href="b2fcc3b2-4416-401b-b465-1c1962e1e69d"></image>
                    </mediaLinkInline>
                  </para>
                  <para>
                    <caps:sentence sentenceid="cee21ea29ee1ef9e16f2b8054df0ca00" id="tgt18" class="tgtSentence">Si no ve este botón, es probable que la aplicación RMS sharing no esté instalada en el equipo, que no esté instalada la última versión o que el equipo deba reiniciarse para completar la instalación.</caps:sentence>
                    <caps:sentence sentenceid="f11f058c6f406e49471bf5d434e7288f" id="tgt19" class="tgtSentence"> Para obtener más información sobre cómo instalar la aplicación de uso compartido, consulte <link xlink:href="2bf09690-9dba-43b7-9e0a-0110915d4081">Download and install the Rights Management sharing application</link>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="807ebf9aace52c2db05ab595997de564" id="tgt20" class="tgtSentence">Especifique las opciones que prefiera para este archivo en el <externalLink><linkText>cuadro de diálogo de uso compartido protegido</linkText><linkUri>http://technet.microsoft.com/library/dn574738.aspx</linkUri></externalLink> y, luego, haga clic en <ui>Enviar ahora</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
        </content>
        <sections>
          <section expanded="false">
            <title>
              <caps:sentence sentenceid="8999a50b2c07b4e9b62b49de1847f20f" id="tgt21" class="tgtSentence">Otras maneras de proteger un archivo que comparte por correo electrónico</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="d34dd6b1a8b58f22b39e6a2ea0d836b6" id="tgt22" class="tgtSentence">Además de compartir un archivo protegido mediante Outlook, también puede usar estas alternativas:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="04aa316462942520591dfa50fe42cbed" id="tgt23" class="tgtSentence">Desde el Explorador de archivos: Este método funciona para todos los archivos.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="9352819106318f91e66d9c16523c0444" id="tgt24" class="tgtSentence">Desde una aplicación de Office: Este método funciona para las aplicaciones compatibles con la aplicación de RMS sharing mediante el complemento de Office, de modo que verá el grupo <ui>RMS</ui> en la cinta de opciones.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <procedure>
                <title>
                  <caps:sentence sentenceid="785ebb09fd0200cdaa0c5e1f8952e7e7" id="tgt25" class="tgtSentence">Uso del Explorador de archivos o una aplicación de Office: Para proteger un archivo que se comparte por correo electrónico</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="1991731fd821fa894948e6549815b5b3" id="tgt26" class="tgtSentence">Use una de las siguientes opciones: </caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="5b9e916aee68aa16c2ced9b460d41cab" id="tgt27" class="tgtSentence">En el Explorador de archivos: Haga clic con el botón derecho, seleccione <ui>Proteger con RMS</ui> y, luego, seleccione <ui>Uso compartido seguro</ui>.</caps:sentence>
                          </para>
                          <mediaLink>
                            <image xlink:href="c046fc51-6b93-4cb9-a76e-ca4daccc37ee"></image>
                          </mediaLink>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="e032a81f27eaa5ae3037e4aac3f60e15" id="tgt28" class="tgtSentence">En las aplicaciones de Office, Word, Excel y PowerPoint: En primer lugar, asegúrese de que ha guardado el archivo.</caps:sentence>
                            <caps:sentence sentenceid="56411d654ac26a142430f7d1b4320974" id="tgt29" class="tgtSentence"> Luego, en la pestaña <ui>Inicio</ui> del grupo <ui>RMS</ui>, haga clic en <ui>Uso compartido seguro</ui> y luego haga clic en <ui>Uso compartido seguro</ui> nuevamente:</caps:sentence>
                          </para>
                          <mediaLink>
                            <image xlink:href="78b66704-90d6-4612-8264-b8b3a86db5ce"></image>
                          </mediaLink>
                        </listItem>
                      </list>
                      <para></para>
                      <para>
                        <caps:sentence sentenceid="ee2766fa989e7d0a3c4b7c0eebb22dca" id="tgt30" class="tgtSentence">Si no ve estas opciones de protección, es probable que la aplicación RMS sharing no esté instalada en el equipo, que no esté instalada la última versión o que el equipo deba reiniciarse para completar la instalación.</caps:sentence>
                        <caps:sentence sentenceid="f11f058c6f406e49471bf5d434e7288f" id="tgt31" class="tgtSentence"> Para obtener más información sobre cómo instalar la aplicación de uso compartido, consulte <link xlink:href="2bf09690-9dba-43b7-9e0a-0110915d4081">Download and install the Rights Management sharing application</link>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="807ebf9aace52c2db05ab595997de564" id="tgt32" class="tgtSentence">Especifique las opciones que prefiera para este archivo en el <externalLink><linkText>cuadro de diálogo de uso compartido protegido</linkText><linkUri>http://technet.microsoft.com/library/dn574738.aspx</linkUri></externalLink> y, luego, haga clic en <ui>Enviar</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="4a2d1cff9fe8a47ced536cf2d43df801" id="tgt33" class="tgtSentence">Puede que vea rápidamente un cuadro de diálogo que le dice que el archivo se está protegiendo, y que luego vea un mensaje de correo electrónico creado para usted que dice a los destinatarios que los datos adjuntos están protegidos con Microsoft RMS y que deben iniciar la sesión.</caps:sentence>
                        <caps:sentence sentenceid="3e9bf353ffda894f0569b2f6e2d6cd69" id="tgt34" class="tgtSentence"> Al hacer clic en el vínculo para iniciar sesión, verán instrucciones y vínculos para asegurarse de que pueden abrir los datos adjuntos protegidos.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="ca15073256d06d36bc03993f0f30893c" id="tgt35" class="tgtSentence">Ejemplo:</caps:sentence>
                      </para>
                      <mediaLink>
                        <image xlink:href="4740129b-622e-4323-bb71-5364ac08d041"></image>
                      </mediaLink>
                      <para></para>
                      <para>
                        <caps:sentence sentenceid="27344ef6106d610e8874c6309b21bd5f" id="tgt36" class="tgtSentence">Probablemente se esté preguntando: <link xlink:href="7b91ab30-6363-4929-bcbd-4dfbd05f644a#BKMK_PPDF">What’s the .ppdf file that’s automatically created?</link></caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="bdc82e725f8a87f61da9e9288ec18d2f" id="tgt37" class="tgtSentence">Opcional: Puede cambiar todo lo que quiera de este mensaje de correo electrónico.</caps:sentence>
                        <caps:sentence sentenceid="cf259d539602c529972e6d25f4c8f542" id="tgt38" class="tgtSentence"> Por ejemplo, puede agregar o cambiar el asunto o el texto del mensaje.</caps:sentence>
                      </para>
                      <alert class="warning">
                        <para>
                          <caps:sentence sentenceid="7f03177b3bde1d3bc6560b67eac27c82" id="tgt39" class="tgtSentence">Aunque puede agregar o quitar usuarios de este mensaje de correo electrónico, esto no cambiará los permisos de los datos adjuntos que especificó en el cuadro de diálogo <ui>Uso compartido seguro</ui>.</caps:sentence>
                          <caps:sentence sentenceid="c45f1722d64196a99322ba9b60b9d1f1" id="tgt40" class="tgtSentence"> Si quiere cambiar esos permisos para, por ejemplo, dar a una nueva persona permisos para abrir el archivo, cierre el mensaje de correo electrónico sin guardarlo ni enviarlo y regrese al paso 1.</caps:sentence>
                        </para>
                      </alert>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="852002bb154106985058f59559ffe06d" id="tgt41" class="tgtSentence">Envíe el mensaje de correo electrónico.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
            </content>
          </section>
        </sections>
      </section>
      <section DoNotNumber="false">
        <title>
          <caps:sentence sentenceid="9b264ffec0213e0096618f896965a728" id="tgt42" class="tgtSentence">Ejemplos y otras instrucciones</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="7e679cf432376a1391e421a3d1ae6dc0" id="tgt43" class="tgtSentence">Para obtener ejemplos de cómo puede usar la aplicación para uso compartido de Rights Management e instrucciones de procedimientos, consulte las siguientes secciones de la guía de usuario de la aplicación para uso compartido de Rights Management:</caps:sentence>
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
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://clixdevr3.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">When you protect a file that you share by email, it creates a new version of the original file.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> The original file remains unprotected and the new version is protected and automatically attached to an email that you then send.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src3" class="srcSentence">In some cases (for files that are created by Microsoft Word, Excel, and PowerPoint), the RMS sharing application creates two versions of the file that it attaches to the email message.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> The second version of the file has a <ui>.ppdf</ui> file name extension and it is a PDF shadow copy of the file.</caps:sentence>
          <caps:sentence id="src5" class="srcSentence"> This version of the file ensures that recipients can always read the file, even if they don’t have the same application installed that you used to create it.</caps:sentence>
          <caps:sentence id="src6" class="srcSentence"> This is often the case when people read their email on mobile devices, and want to view their email attachments.</caps:sentence>
          <caps:sentence id="src7" class="srcSentence"> All they need to open the file, is the RMS sharing application.</caps:sentence>
          <caps:sentence id="src8" class="srcSentence"> Then, they can read the attached file, but they won’t be able to change it until they open the other version of the file by using an application that supports RMS.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src9" class="srcSentence">If your organization uses Azure RMS, you can keep track of the files that you protect by sharing:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src10" class="srcSentence">Select an option to receive emails when somebody tries to open these protected attachments.</caps:sentence>
              <caps:sentence id="src11" class="srcSentence"> Each time the file is accessed, you will be notified who tried to open the file and when, and whether they were successful (they were successfully authenticated) or not.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src12" class="srcSentence">Use the documentation tracking site.</caps:sentence>
              <caps:sentence id="src13" class="srcSentence"> You can even stop sharing the file, by revoking access to it in the document tracking site.</caps:sentence>
              <caps:sentence id="src14" class="srcSentence"> For more information, see <link xlink:href="61f349ce-bdd2-45c1-acc5-bc83937fb187">Track and revoke your documents when you use the RMS sharing application</link>.</caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <section DoNotNumber="false" expanded="true">
        <title>
          <caps:sentence id="src15" class="srcSentence">Using Outlook: To protect a file that you share by email</caps:sentence>
        </title>
        <content>
          <procedure>
            <title></title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src16" class="srcSentence">Create your email message and attach the file.</caps:sentence>
                    <caps:sentence id="src17" class="srcSentence"> Then, on the <ui>Message</ui> tab, in the <ui>RMS</ui> group, click <ui>Share Protected</ui> and then click <ui>Share Protected</ui> again:</caps:sentence>
                  </para>
                  <para>
                    <mediaLinkInline>
                      <image xlink:href="b2fcc3b2-4416-401b-b465-1c1962e1e69d"></image>
                    </mediaLinkInline>
                  </para>
                  <para>
                    <caps:sentence id="src18" class="srcSentence">If you do not see this button, it’s likely that either the RMS sharing application is not installed on your computer, the latest version isn’t installed, or your computer must be restarted to complete the installation.</caps:sentence>
                    <caps:sentence id="src19" class="srcSentence"> For more information about how to install the sharing application, see <link xlink:href="2bf09690-9dba-43b7-9e0a-0110915d4081">Download and install the Rights Management sharing application</link>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src20" class="srcSentence">Specify the options that you want for this file in the <externalLink><linkText>share protected dialog box</linkText><linkUri>http://technet.microsoft.com/library/dn574738.aspx</linkUri></externalLink>, and then click <ui>Send Now</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
        </content>
        <sections>
          <section expanded="false">
            <title>
              <caps:sentence id="src21" class="srcSentence">Other ways to protect a file that you share by email</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src22" class="srcSentence">In addition to sharing a protected file by using Outlook, you can also use these alternatives:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src23" class="srcSentence">From File Explorer: This method works for all files.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src24" class="srcSentence">From an Office application: This method works for applications that the RMS sharing application supports by using the Office add-in so that you see the <ui>RMS</ui> group on the ribbon.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <procedure>
                <title>
                  <caps:sentence id="src25" class="srcSentence">Using File Explorer or an Office application: To protect a file that you share by email</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src26" class="srcSentence">Use one of the following options: </caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence id="src27" class="srcSentence">For File Explorer: Right-click the file, select <ui>Protect with RMS</ui>, and then select <ui>Share Protected</ui>:</caps:sentence>
                          </para>
                          <mediaLink>
                            <image xlink:href="c046fc51-6b93-4cb9-a76e-ca4daccc37ee"></image>
                          </mediaLink>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src28" class="srcSentence">For the Office applications, Word, Excel, and PowerPoint: Make sure that you have saved the file first.</caps:sentence>
                            <caps:sentence id="src29" class="srcSentence"> Then, on the <ui>Home</ui> tab, in the <ui>RMS</ui> group, click <ui>Share Protected</ui> and then click <ui>Share Protected</ui> again:</caps:sentence>
                          </para>
                          <mediaLink>
                            <image xlink:href="78b66704-90d6-4612-8264-b8b3a86db5ce"></image>
                          </mediaLink>
                        </listItem>
                      </list>
                      <para></para>
                      <para>
                        <caps:sentence id="src30" class="srcSentence">If you do not see these options for protection, it’s likely that either the RMS sharing application is not installed on your computer, the latest version isn’t installed, or your computer must be restarted to complete the installation.</caps:sentence>
                        <caps:sentence id="src31" class="srcSentence"> For more information about how to install the sharing application, see <link xlink:href="2bf09690-9dba-43b7-9e0a-0110915d4081">Download and install the Rights Management sharing application</link>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src32" class="srcSentence">Specify the options that you want for this file in the <externalLink><linkText>share protected dialog box</linkText><linkUri>http://technet.microsoft.com/library/dn574738.aspx</linkUri></externalLink>, and then click <ui>Send</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src33" class="srcSentence">You might quickly see a dialog box to tell you that the file is being protected, and then you see an email message created for you that tells the recipients that the attachments are protected with Microsoft RMS, and that they must sign in.</caps:sentence>
                        <caps:sentence id="src34" class="srcSentence"> When they click the link to sign in, they see instructions and links to ensure that they can open your protected attachment.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src35" class="srcSentence">Example:</caps:sentence>
                      </para>
                      <mediaLink>
                        <image xlink:href="4740129b-622e-4323-bb71-5364ac08d041"></image>
                      </mediaLink>
                      <para></para>
                      <para>
                        <caps:sentence id="src36" class="srcSentence">Are you wondering: <link xlink:href="7b91ab30-6363-4929-bcbd-4dfbd05f644a#BKMK_PPDF">What’s the .ppdf file that’s automatically created?</link></caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src37" class="srcSentence">Optional: You can change anything that you want in this email message.</caps:sentence>
                        <caps:sentence id="src38" class="srcSentence"> For example, you can add to or change the subject or text in the message.</caps:sentence>
                      </para>
                      <alert class="warning">
                        <para>
                          <caps:sentence id="src39" class="srcSentence">Although you can add or remove people from this email message, this does not change the permissions for the attachment that you specified in the <ui>share protected</ui> dialog box.</caps:sentence>
                          <caps:sentence id="src40" class="srcSentence"> If you want to change those permissions, for example, give a new person permissions to open the file, close the email message without saving or sending it, and return to step 1.</caps:sentence>
                        </para>
                      </alert>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src41" class="srcSentence">Send the email message.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
            </content>
          </section>
        </sections>
      </section>
      <section DoNotNumber="false">
        <title>
          <caps:sentence id="src42" class="srcSentence">Examples and other instructions</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src43" class="srcSentence">For examples for how you might use the Rights Management sharing application, and how-to instructions, see the following sections from the Rights Management sharing application user guide:</caps:sentence>
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