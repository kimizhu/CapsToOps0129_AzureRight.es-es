---
title: Configuraci&#243;n de aplicaciones para Azure Rights Management
ms.custom: na
ms.reviewer: na
ms.service: rights-management
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ea09cbc5-b98b-444e-8b60-5bc3cb199c36
---
# Configuraci&#243;n de aplicaciones para Azure Rights Management
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="es-ES">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <alert class="note">
          <para>
            <caps:sentence sentenceid="b8f1f0fe7b908e4d42fcbfceca6c3f54" id="tgt1" class="tgtSentence">Esta información está destinada a los asesores y administradores de TI que han implementado Azure Rights Management.</caps:sentence>
            <caps:sentence sentenceid="a8bffe1e3c4030decc5ba65c96311221" id="tgt2" class="tgtSentence"> Si busca ayuda e información sobre cómo usar Rights Management con una aplicación específica o cómo abrir un archivo protegido por derechos, use la ayuda y las instrucciones que se incluyen con la aplicación.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="a164322f8382077840014fb67bbdc38a" id="tgt3" class="tgtSentence">Por ejemplo, para las aplicaciones de Office, haga clic en el icono de Ayuda y escriba términos de búsqueda como <userInput>Rights Management</userInput> o <userInput>IRM</userInput>.</caps:sentence>
            <caps:sentence sentenceid="240aafc925215e53294d00d0b40cdbe9" id="tgt4" class="tgtSentence"> Para la aplicación de uso compartido de RMS para Windows, consulte la <externalLink><linkText>Guía del usuario de la aplicación de uso compartido de Rights Management</linkText><linkUri>http://technet.microsoft.com/library/dn339006.aspx</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence sentenceid="cdd0cc54e586d0675416084777f675d4" id="tgt5" class="tgtSentence">Después de haber implementado Azure Rights Management (Azure RMS) en su organización, use la siguiente información para configurar aplicaciones y servicios compatibles con Azure RMS.</caps:sentence>
          <caps:sentence sentenceid="ad4088be33b532ccd246ffbc60e186a5" id="tgt6" class="tgtSentence"> Aquí se incluyen aplicaciones de Office, como Word 2013 y Word 2010, y servicios, como Exchange Online (reglas de transporte, prevención de pérdida de datos, no reenviar y cifrado de mensajes) y SharePoint Online (bibliotecas protegidas).</caps:sentence>
          <caps:sentence sentenceid="7eddfd7dba28ad8a7405279b459eba7d" id="tgt7" class="tgtSentence"> Para obtener información sobre cómo estas aplicaciones y servicios son compatibles con Rights Management, vea <link xlink:href="2cdc7bde-4044-4021-b887-11476f99afd9">How Applications Support Azure Rights Management</link>.</caps:sentence>
        </para>
        <alert class="important">
          <para>
            <caps:sentence sentenceid="674eacb00dc0614d471f554b63f3caf9" id="tgt8" class="tgtSentence">Para obtener más información acerca de versiones compatibles y otros requisitos, consulte <link xlink:href="dc78321d-d759-4653-8818-80da74b6cdeb">Requirements for Azure Rights Management</link>.</caps:sentence>
          </para>
        </alert>
        <list class="bullet">
          <listItem>
            <para>
              <link xlink:href="ea09cbc5-b98b-444e-8b60-5bc3cb199c36#BKMK_O365">Office 365: Configuration for clients and online services</link>
            </para>
            <list class="bullet">
              <listItem>
                <para>
                  <link xlink:href="ea09cbc5-b98b-444e-8b60-5bc3cb199c36#BKMK_ExchangeOnline">Exchange Online: IRM Configuration</link>
                </para>
              </listItem>
              <listItem>
                <para>
                  <link xlink:href="#BKMK_SharePointOnline">SharePoint Online and OneDrive for Business: IRM Configuration</link>
                </para>
              </listItem>
            </list>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="#BKMK_Office2013Configuration">Office 2016 and Office 2013: Configuration for clients</link>
            </para>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="ea09cbc5-b98b-444e-8b60-5bc3cb199c36#BKMK_Office2010Configuration">Office 2010: Configuration for clients</link>
            </para>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="ea09cbc5-b98b-444e-8b60-5bc3cb199c36#BKMK_SharingApp">Rights Management sharing application: Installation and configuration for clients</link>
            </para>
            <list class="bullet">
              <listItem>
                <para>
                  <link xlink:href="ea09cbc5-b98b-444e-8b60-5bc3cb199c36#BKMK_SharingAppforWindows">The RMS sharing application for Windows: Installation and configuration</link>
                </para>
              </listItem>
              <listItem>
                <para>
                  <link xlink:href="ea09cbc5-b98b-444e-8b60-5bc3cb199c36#BKMK_SharingAppMovileDevices">The RMS sharing application for mobile platforms: Installation</link>
                </para>
              </listItem>
            </list>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="ea09cbc5-b98b-444e-8b60-5bc3cb199c36#BKMK_RMSAPIs">Other applications that support the RMS APIs: Installation and configuration</link>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence sentenceid="6d5fac5fa17b1a62550e7d202ac6178a" id="tgt9" class="tgtSentence">Para configurar servidores locales como Exchange Server y SharePoint Server, consulte <link xlink:href="90e7e33f-9ecc-497b-89c5-09205ffc5066">Deploying the Azure Rights Management Connector</link>.</caps:sentence>
        </para>
        <alert class="tip">
          <para>
            <caps:sentence sentenceid="d3660f69f174b44fccac1e5806290574" id="tgt10" class="tgtSentence">Para obtener ejemplos de alto nivel y capturas de pantalla de aplicaciones configuradas para usar Azure RMS, vea la sección <link xlink:href="aeeebcd7-6646-4405-addf-ee1cc74df5df#BKMK_RMSpictures">Azure RMS in action: What administrators and users see</link> del tema <link xlink:href="aeeebcd7-6646-4405-addf-ee1cc74df5df">What is Azure Rights Management?</link>.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <section address="BKMK_O365">
        <title>
          <caps:sentence sentenceid="f70ebde5965b3b5822f1901ecc3f2e9d" id="tgt11" class="tgtSentence">Office 365: Configuración para clientes y servicios en línea</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="a337b5aff3154676020b515a77e9fece" id="tgt12" class="tgtSentence">Como Office 365 es compatible de forma nativa con Azure RMS, no se requiere ninguna configuración para equipo cliente para conseguir la compatibilidad con las funciones de Information Rights Management (IRM) para aplicaciones como Word, Excel, PowerPoint, Outlook y la aplicación web de Outlook.</caps:sentence>
            <caps:sentence sentenceid="7b0cbc296279057ff1cbc36c965674f9" id="tgt13" class="tgtSentence"> Todo lo que tienen que hacer los usuarios es iniciar sesión en sus aplicaciones de Office con sus credenciales de <token>o365_1</token> y pueden proteger archivos y correos electrónicos, así como usar los que hayan sido protegidos por otros usuarios.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="bbbb6b8e8569e4f708b6559ae443d771" id="tgt14" class="tgtSentence">Sin embargo, se recomienda que complemente estas aplicaciones con la aplicación de uso compartido Rights Management, para que los usuarios obtengan los beneficios del complemento de Office.</caps:sentence>
            <caps:sentence sentenceid="be021ab36c2c99a549fc25f5fcee238c" id="tgt15" class="tgtSentence"> Para obtener más información, consulte la sección <link xlink:href="ea09cbc5-b98b-444e-8b60-5bc3cb199c36#BKMK_SharingApp">Rights Management sharing application: Installation and configuration for clients</link> de este tema.</caps:sentence>
          </para>
        </content>
        <sections>
          <section address="BKMK_ExchangeOnline" expanded="false">
            <title>
              <caps:sentence sentenceid="be672915c46503052a91bce8287e0212" id="tgt16" class="tgtSentence">Exchange Online: Configuración de IRM</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="a794aecc128061d02776cf6b42acfdf4" id="tgt17" class="tgtSentence">Para configurar Exchange Online para que sea compatible con Azure RMS, debe configurar el servicio Information Rights Management (IRM) para Exchange Online.</caps:sentence>
                <caps:sentence sentenceid="56de49160bb440dc9fdb27ddce535f11" id="tgt18" class="tgtSentence"> Para ello, use Windows PowerShell (no es preciso instalar un módulo independiente) y ejecute los <externalLink><linkText>comandos de PowerShell para Exchange Online</linkText><linkUri>https://technet.microsoft.com/library/jj200677.aspx</linkUri></externalLink>.</caps:sentence>
              </para>
              <alert class="note">
                <para>
                  <caps:sentence sentenceid="d8d7d07cb86ef58971d56ae3166e5b1f" id="tgt19" class="tgtSentence">Actualmente, no se puede configurar Exchange Online para admitir Azure RMS si usa una clave de inquilino administrada por el cliente (BYOK) con Azure RMS, en lugar de la configuración predeterminada de una clave de inquilino administrada por Microsoft.</caps:sentence>
                  <caps:sentence sentenceid="be021ab36c2c99a549fc25f5fcee238c" id="tgt20" class="tgtSentence"> Para obtener más información, consulte la sección <link xlink:href="f0d33c5f-a6a6-44a1-bdec-5be1bc8e1e14#BKMK_Pricing">BYOK pricing and restrictions</link> en el tema <link xlink:href="f0d33c5f-a6a6-44a1-bdec-5be1bc8e1e14">Planning and Implementing Your Azure Rights Management Tenant Key</link>.</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="c1d769bcbf3e557f3ad46a71cb6a2363" id="tgt21" class="tgtSentence">Si intenta configurar Exchange Online cuando Azure RMS usa BYOK, el comando para importar la clave (paso 5, en el siguiente procedimiento) generará un error con el mensaje  <ui>[FailureCategory=Cmdlet-FailedToGetTrustedPublishingDomainFromRmsOnlineException]</ui>.</caps:sentence>
                </para>
              </alert>
              <para>
                <caps:sentence sentenceid="1feda85779c40fe58449648d8fba43d6" id="tgt22" class="tgtSentence">Los pasos siguientes proporcionan un conjunto típico de comandos que se ejecutarían para permitir que Exchange Online usara Azure RMS:</caps:sentence>
              </para>
              <list class="ordered">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="d258bdf0935f2a63da37c72f1af96b46" id="tgt23" class="tgtSentence">Si es la primera vez que ha usado Windows PowerShell para Exchange Online en el equipo, debe configurar Windows PowerShell para ejecutar scripts firmados.</caps:sentence>
                    <caps:sentence sentenceid="e1fd602018937f4f66e73e1cf6ce4e3a" id="tgt24" class="tgtSentence"> Inicie una sesión de Windows PowerShell mediante la opción <ui>Ejecutar como administrador</ui> y, luego, escriba:</caps:sentence>
                  </para>
                  <code>
Set-ExecutionPolicy RemoteSigned </code>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="a8e7cb2af12e011a1ec2c627cc2ce4f1" id="tgt25" class="tgtSentence">En la sesión de Windows PowerShell, inicie sesión en Exchange Online con una cuenta que está habilitada para el acceso al shell remoto.</caps:sentence>
                    <caps:sentence sentenceid="2fa9b6fc9db793ee69a7bc5dbec47e33" id="tgt26" class="tgtSentence"> De forma predeterminada, todas las cuentas que se crean en Exchange Online están habilitadas para el acceso remoto al shell, pero esto se puede deshabilitar (y habilitar) con el comando <externalLink><linkText>Set-User &lt;UserIdentity&gt; -RemotePowerShellEnabled</linkText><linkUri>https://technet.microsoft.com/library/jj984292(v=exchg.160).aspx</linkUri></externalLink>.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="faf399755b76a6e984fcfa9f490eb02d" id="tgt27" class="tgtSentence">Para iniciar sesión, escriba:</caps:sentence>
                  </para>
                  <code>$Cred = Get-Credential</code>
                  <para>
                    <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt28" class="tgtSentence">En el cuadro de diálogo <ui>Solicitud de credenciales para Windows PowerShell</ui>, proporcione el nombre de usuario y la contraseña de Office 365.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="9c51e8012468065678cc4e94f8ea8129" id="tgt29" class="tgtSentence">Conecte con el servicio Exchange Online mediante la ejecución de los dos comandos siguientes:</caps:sentence>
                  </para>
                  <code>$Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.outlook.com/powershell/ -Credential $Cred -Authentication Basic –AllowRedirection</code>
                  <code>Import-PSSession $Session</code>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="5a661b10fc45980ce666d3f45555ce65" id="tgt30" class="tgtSentence">Especifique la ubicación de la clave de inquilino de Azure RMS, según su región:</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="8224573c3549cd3511b611e6d2d6f50b" id="tgt31" class="tgtSentence">Para Norteamérica (y las suscripciones de gobierno):</caps:sentence>
                  </para>
                  <code>Set-IRMConfiguration -RMSOnlineKeySharingLocation "https://sp-rms.na.aadrm.com/TenantManagement/ServicePartner.svc"</code>
                  <para>
                    <caps:sentence sentenceid="efb82bea4793d01165057d389b0c3c27" id="tgt32" class="tgtSentence">Para Europa:</caps:sentence>
                  </para>
                  <code>Set-IRMConfiguration -RMSOnlineKeySharingLocation "https://sp-rms.eu.aadrm.com/TenantManagement/ServicePartner.svc"</code>
                  <para>
                    <caps:sentence sentenceid="53ef12914c50d3fbf7a1aba6af951e90" id="tgt33" class="tgtSentence">Para Asia:</caps:sentence>
                  </para>
                  <code>Set-IRMConfiguration -RMSOnlineKeySharingLocation "https://sp-rms.ap.aadrm.com/TenantManagement/ServicePartner.svc"</code>
                  <para>
                    <caps:sentence sentenceid="efda5461a3a324f4be3af8e8efc9eba9" id="tgt34" class="tgtSentence">Para Sudamérica:</caps:sentence>
                  </para>
                  <code>Set-IRMConfiguration -RMSOnlineKeySharingLocation "https://sp-rms.sa.aadrm.com/TenantManagement/ServicePartner.svc"</code>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="20f3b38a188b66af12a28f9554aca22f" id="tgt35" class="tgtSentence">Importe datos de configuración de Azure RMS en Exchange Online, en forma del dominio de publicación de confianza (TPD).</caps:sentence>
                    <caps:sentence sentenceid="ce7383ce39866516e47a21370f31379f" id="tgt36" class="tgtSentence"> Esto incluye la clave de inquilino y las plantillas de Azure RMS:</caps:sentence>
                  </para>
                  <code>Import-RMSTrustedPublishingDomain -RMSOnline -name "RMS Online"</code>
                  <para>
                    <caps:sentence sentenceid="048fe4080204855bb520b7065663879e" id="tgt37" class="tgtSentence">En este comando hemos usado el nombre de <ui>RMS Online</ui> como nombre base de TDP para Azure RMS en Exchange Online.</caps:sentence>
                    <caps:sentence sentenceid="b6ac4dc7926a2d3fe406a95b90e5b107" id="tgt38" class="tgtSentence"> Una vez importado el TPD, se denomina <system>RMS Online - 1</system> en Exchange Online.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="fddf6ec8b8c92e80d9b98d5c302f37fd" id="tgt39" class="tgtSentence">Habilite la funcionalidad de Azure RMS para que las características de IRM estén disponibles para Exchange Online:</caps:sentence>
                  </para>
                  <code>Set-IRMConfiguration -InternalLicensingEnabled $true</code>
                  <para>
                    <caps:sentence sentenceid="52139e996766edc6ee5bd1e4d1f642f3" id="tgt40" class="tgtSentence">Después de ejecutar este comando, Rights Management se habilita automáticamente para el cliente de Outlook, la aplicación web de Outlook y Exchange Active Sync.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="8b3e11a6724e9b4ef85ad0865ff930db" id="tgt41" class="tgtSentence">Opcionalmente, pruebe que esta configuración es correcta mediante el siguiente comando:</caps:sentence>
                  </para>
                  <code>Test-IRMConfiguration -Sender &lt;user email address&gt;</code>
                  <para>
                    <caps:sentence sentenceid="d05370276e06291b048268558cc39bee" id="tgt42" class="tgtSentence">Por ejemplo: <userInput>Test-IRMConfiguration -Sender  adams@contoso.com</userInput></caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="a950d1cd15dfadfe3c1604528ecb33d1" id="tgt43" class="tgtSentence">Este comando ejecuta una serie de comprobaciones que incluyen la comprobación de la conectividad con el servicio y la recuperación de la configuración, los URI, las licencias y las plantillas.</caps:sentence>
                    <caps:sentence sentenceid="97ec442182e73bbcfb537dd318df8ce5" id="tgt44" class="tgtSentence"> En la sesión de Windows PowerShell verá los resultados de cada uno y, al final, si todo pasa estas comprobaciones: <ui>RESULTADO GLOBAL: CORRECTO</ui></caps:sentence> </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="1c898dc126acf685d04b1e4cca186f9d" id="tgt45" class="tgtSentence">Desconecte la sesión remota de PowerShell:</caps:sentence>
                  </para>
                  <code>Remove-PSSession $Session</code>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="e5117af35a99439c32a70792149f30bc" id="tgt46" class="tgtSentence">Los usuarios pueden proteger ahora sus mensajes de correo electrónico mediante el uso de Azure RMS.</caps:sentence>
                <caps:sentence sentenceid="70c2fbdc7a401ce88450f543f0cb76f9" id="tgt47" class="tgtSentence"> Por ejemplo, en la aplicación web de Outlook, seleccione <ui>Establecer permisos</ui> en el menú extendido (<ui>...</ui>) y, luego, elija <ui>No reenviar</ui> o una de las plantillas disponibles para aplicar la protección de la información al mensaje de correo electrónico y los datos adjuntos.</caps:sentence>
                <caps:sentence sentenceid="46a93875d3615012774a0b33c2e47c99" id="tgt48" class="tgtSentence"> Sin embargo, dado que la aplicación web de Outlook almacena en caché de interfaz de usuario durante un día, espere a que transcurra ese período de tiempo antes de intentar aplicar la protección de la información a los mensajes de correo electrónico y después de ejecutar estos comandos de configuración.</caps:sentence>
                <caps:sentence sentenceid="b5983fc69c89ff662233e2e2833a0cde" id="tgt49" class="tgtSentence"> Antes de que las actualizaciones de la interfaz de usuario reflejen la nueva configuración, no verá ninguna de las opciones del menú <ui>Establecer permisos</ui>.</caps:sentence>
              </para>
              <alert class="important">
                <para>
                  <caps:sentence sentenceid="dd2a28403591609fe5a3d6c382d3a8a4" id="tgt50" class="tgtSentence">Si crea nuevas <externalLink><linkText>plantillas personalizadas</linkText><linkUri>https://technet.microsoft.com/library/dn642472.aspx</linkUri></externalLink> para Azure RMS o actualiza las plantillas cada vez, debe ejecutar el siguiente comando de PowerShell para Exchange Online (si es necesario, ejecute primero los pasos 2 y 3) para sincronizar dichos cambios con Exchange Online: <codeInline>Import-RMSTrustedPublishingDomain -Name "RMS Online - 1" -RefreshTemplates –RMSOnline</codeInline></caps:sentence>
                </para>
              </alert>
              <para>
                <caps:sentence sentenceid="63c7bdb43fcc445beab1f11b7ee0ccdb" id="tgt51" class="tgtSentence">Como administrador de Exchange, ahora puede configurar las características que aplican automáticamente protección de la información, como <externalLink><linkText>reglas de transporte</linkText><linkUri>https://technet.microsoft.com/library/dd302432.aspx</linkUri></externalLink>, <externalLink><linkText>directivas de prevención de pérdida de datos (DLP)</linkText><linkUri>https://technet.microsoft.com/library/jj150527(v=exchg.150).aspx</linkUri></externalLink> y <externalLink><linkText>correo de voz protegido</linkText><linkUri>https://technet.microsoft.com/library/dn198211(v=exchg.150).aspx</linkUri></externalLink> (mensajería unificada).</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="3f0afb1f90f48c09bbcd5a137568303a" id="tgt52" class="tgtSentence"> Para obtener instrucciones detalladas para configurar Exchange Online para permitir la funcionalidad de IRM, vea la documentación de la biblioteca de Exchange.</caps:sentence>
                <caps:sentence sentenceid="4be0bb25039056347740ae85bcda324d" id="tgt53" class="tgtSentence"> Por ejemplo:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <externalLink>
                      <linkText>
                        <caps:sentence sentenceid="96d10c4ebd93c1c4b8eac31193055fc9" id="tgt54" class="tgtSentence">Conexión a Exchange Online mediante PowerShell remoto</caps:sentence>
                      </linkText>
                      <linkUri>https://technet.microsoft.com/library/jj984289(v=exchg.160).aspx</linkUri>
                    </externalLink>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <externalLink>
                      <linkText>
                        <caps:sentence sentenceid="5366949737749f15ee49cabc5ad39fc9" id="tgt55" class="tgtSentence">Configuración de IRM para usar Azure Rights Management</caps:sentence>
                      </linkText>
                      <linkUri>https://technet.microsoft.com/library/dn151475(v=exchg.150).aspx</linkUri>
                    </externalLink>
                  </para>
                </listItem>
              </list>
            </content>
            <sections>
              <section>
                <title>
                  <caps:sentence sentenceid="e920bd3dd42236768ac2a05a20b13ce8" id="tgt56" class="tgtSentence">Cifrado de mensajes de Office 365</caps:sentence>
                </title>
                <content>
                  <para>
                    <caps:sentence sentenceid="924c22aeed055bbeace8b5716713192f" id="tgt57" class="tgtSentence">Ejecute los mismos pasos que se documentan en la sección anterior, pero si no desea que se muestren las plantillas, antes del paso 6, ejecute el comando siguiente para evitar que las plantillas de IRM estén disponible la aplicación web de Outlook y el cliente de Outlook: <codeInline>Set-IRMConfiguration -ClientAccessServerEnabled $false</codeInline></caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="d8d2bd3cd4c6b9cef3a5ea84254ca31d" id="tgt58" class="tgtSentence">Ya está listo para configurar <externalLink><linkText>reglas de transporte</linkText><linkUri>https://technet.microsoft.com/library/dd302432.aspx</linkUri></externalLink> con el objeto de modificar automáticamente la seguridad de los mensajes cuando los destinatarios se encuentran fuera de la organización y seleccionar la opción <ui>Aplicar el cifrado de mensajes de Office 365</ui>.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="31044bec5ea816281c2cdd3bcfd032ac" id="tgt59" class="tgtSentence">Para obtener más información sobre el cifrado de mensajes, vea <externalLink><linkText>Cifrado en Office 365</linkText><linkUri>https://technet.microsoft.com/library/dn569286.aspx</linkUri></externalLink> en la biblioteca de Exchange.</caps:sentence>
                  </para>
                </content>
              </section>
            </sections>
          </section>
          <section address="BKMK_SharePointOnline" expanded="false">
            <title>
              <caps:sentence sentenceid="fc514fc0b77578c38592e8cb84a1609d" id="tgt60" class="tgtSentence">SharePoint Online y OneDrive para la Empresa: Configuración de IRM</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="05fa4868cfb9ceeed76fa2c85527cf1a" id="tgt61" class="tgtSentence">Para configurar SharePoint Online y OneDrive para la Empresa de forma que sean compatibles con Azure RMS, primero debe habilitar el servicio Information Rights Management (IRM) para SharePoint Online mediante el centro de administración de SharePoint.</caps:sentence>
                <caps:sentence sentenceid="844adcecbefa79e9203f6ffed335eb9d" id="tgt62" class="tgtSentence"> Luego, los propietarios de sitios pueden proteger con IRM sus listas y bibliotecas de documentos de SharePoint, y los usuarios pueden proteger con IRM su biblioteca de OneDrive para la Empresa, de modo que los documentos que están guardados ahí, y que se comparten con otros, estén protegidos automáticamente con Azure RMS.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="a5e38a89f2b3b2f11c0d0342713646b2" id="tgt63" class="tgtSentence">Para habilitar el servicio Information Rights Management (IRM) para SharePoint Online, vea las siguientes instrucciones en el sitio web de Office:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <externalLink>
                      <linkText>
                        <caps:sentence sentenceid="caf16d5da61f6a4e3b6a7b8282d710f6" id="tgt64" class="tgtSentence">Configuración de Information Rights Management (IRM) en el centro de administración de SharePoint</caps:sentence>
                      </linkText>
                      <linkUri>http://office.microsoft.com/office365-sharepoint-online-enterprise-help/set-up-information-rights-management-irm-insharepoint-online-HA102895193.aspx</linkUri>
                    </externalLink>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="acd37421fbaace25990aac6de9e1b4a8" id="tgt65" class="tgtSentence">Esta configuración se realiza mediante el administrador de Office 365.</caps:sentence>
              </para>
            </content>
            <sections>
              <section>
                <title>
                  <caps:sentence sentenceid="ccc024e7db3bb9c7a5b63ae73f328006" id="tgt66" class="tgtSentence">Configuración de IRM para listas y bibliotecas</caps:sentence>
                </title>
                <content>
                  <para>
                    <caps:sentence sentenceid="a3aa0b3d612c81bd9684a66f77c4afce" id="tgt67" class="tgtSentence">Después de haber habilitado el servicio IRM para SharePoint, los propietarios de sitios pueden proteger con IRM sus listas y bibliotecas de documentos de SharePoint.</caps:sentence>
                    <caps:sentence sentenceid="c38ea0ca68c4847ae4ea391c24d92a0b" id="tgt68" class="tgtSentence"> Para obtener instrucciones, vea los recursos siguientes en el sitio web de Office:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt69" class="tgtSentence"> <externalLink><linkText>Aplicación de Information Rights Management a una lista o biblioteca</linkText><linkUri>http://office.microsoft.com/sharepoint-help/apply-information-rights-management-to-a-list-or-library-HA102891460.aspx</linkUri></externalLink></caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence sentenceid="0681ee99bbd9c613cc01ea5cc4d511ef" id="tgt70" class="tgtSentence">Esta configuración se realiza mediante el administrador de sitios de SharePoint.</caps:sentence>
                  </para>
                </content>
              </section>
              <section address="BKMK_OneDrive" expanded="true">
                <title>
                  <caps:sentence sentenceid="102f7ca408c361e25f92b6f0cbc2883a" id="tgt71" class="tgtSentence">Configuración de IRM para OneDrive para la Empresa</caps:sentence>
                </title>
                <content>
                  <para>
                    <caps:sentence sentenceid="cbecbfa5c801fae2da45f8282310e29f" id="tgt72" class="tgtSentence">Después de haber habilitado el servicio IRM para SharePoint Online, la biblioteca de documentos OneDrive para la Empresa de los usuarios se puede configurar para la protección de Rights Management.</caps:sentence>
                    <caps:sentence sentenceid="56420843401e46832618c3ae454857df" id="tgt73" class="tgtSentence">  Los usuarios pueden configurarlo por sí mismos con el icono <ui>Configuración</ui> de su OneDrive.</caps:sentence>
                    <caps:sentence sentenceid="cb32c6d23e2632712cd320676e835a80" id="tgt74" class="tgtSentence"> Aunque los administradores no pueden configurar Rights Management para OneDrive para la Empresa mediante el centro de administración de SharePoint, pueden hacerlo con Windows PowerShell.</caps:sentence>
                  </para>
                  <alert class="note">
                    <para>
                      <caps:sentence sentenceid="45f031349ea717e8cedd185171cf5e20" id="tgt75" class="tgtSentence">Para obtener más información acerca de cómo configurar OneDrive para la Empresa, consulte la documentación de Office,<externalLink><linkText>Configurar OneDrive para el negocio en Office 365</linkText><linkUri>https://support.office.com/article/Set-up-OneDrive-for-Business-in-Office-365-3e21f8f0-e0a1-43be-aa3e-8c0236bf11bb</linkUri></externalLink>.</caps:sentence>
                    </para>
                  </alert>
                </content>
                <sections>
                  <section>
                    <title>
                      <caps:sentence sentenceid="604ce35f46a0cfe529aea1ba590e8c86" id="tgt76" class="tgtSentence">Configuración de los usuarios</caps:sentence>
                    </title>
                    <content>
                      <para>
                        <caps:sentence sentenceid="7e1b1daa51c3f28a3015386be04d146a" id="tgt77" class="tgtSentence">Dé a los usuarios estas instrucciones para que puedan configurar su OneDrive para la Empresa y para proteger mediante IRM los archivos de su empresa.</caps:sentence>
                      </para>
                      <list class="ordered">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="ed3351322e8bc30d961baefb0f0c09ee" id="tgt78" class="tgtSentence">En OneDrive, haga clic en el icono <ui>Configuración</ui> para abrir el menú de configuración y, luego, haga clic en <ui>Contenido del sitio</ui>.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="f174ce634f98e9522873d5ed2d2e73e2" id="tgt79" class="tgtSentence">Mantenga el mouse sobre el icono <ui>Documentos</ui>, elija el botón de puntos suspensivos (<ui>...</ui>) y, luego, haga clic en <ui>CONFIGURACIÓN</ui>.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt80" class="tgtSentence">En la página <ui>Configuración</ui>, en la sección <ui>Permisos y administración</ui>, haga clic en <ui>Information Rights Management</ui>.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt81" class="tgtSentence">En la página <ui>Configuración de Information Rights Management</ui>, seleccione la casilla <ui>Limitar permisos de descarga de esta biblioteca</ui>, especifique la elección del nombre y una descripción de los permisos y, si lo desea, haga clic en <ui>MOSTRAR OPCIONES</ui> para realizar configuraciones opcionales. A continuación, haga clic en <ui>Aceptar</ui>.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence sentenceid="65d2aacf99ad2f0026727627b93ed56f" id="tgt82" class="tgtSentence">Para obtener más información sobre las opciones de configuración, consulte las instrucciones que se indican en <externalLink><linkText>Aplicación de Information Rights Management a una lista o biblioteca</linkText><linkUri>https://support.office.com/article/Apply-Information-Rights-Management-to-a-list-or-library-3bdb5c4e-94fc-4741-b02f-4e7cc3c54aa1</linkUri></externalLink> de la documentación de Office.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                      <para>
                        <caps:sentence sentenceid="43b4da4b6c87c3d6385a64368b1bf893" id="tgt83" class="tgtSentence">Dado que esta configuración confía en los usuarios, en lugar de en el administrador, para proteger con IRM su biblioteca OneDrive para la Empresa, muestre a los usuarios las ventajas de proteger sus archivos y cómo hacerlo.</caps:sentence>
                        <caps:sentence sentenceid="2b4cd61422610017710400cf426eb466" id="tgt84" class="tgtSentence"> Por ejemplo, explique que cuando comparten un documento de OneDrive para la Empresa, solo las personas que ellos autorizan pueden tener a él acceso con cualquier restricción que configuren, incluso si se cambia el nombre del archivo o se copia en otra parte.</caps:sentence>
                      </para>
                    </content>
                  </section>
                  <section>
                    <title>
                      <caps:sentence sentenceid="3da9b1957d51404e59a969d9ef584d22" id="tgt85" class="tgtSentence">Configuración para administradores</caps:sentence>
                    </title>
                    <content>
                      <para>
                        <caps:sentence sentenceid="10bfb0c08ded3fb36e34c1c3c20bdd9d" id="tgt86" class="tgtSentence">Aunque IRM no se puede configurar para OneDrive para la Empresa de los usuarios mediante el centro de administración de SharePoint, se puede hacer con Windows PowerShell.</caps:sentence>
                        <caps:sentence sentenceid="5cbb53951e2920f932519dcdf472d183" id="tgt87" class="tgtSentence"> Para habilitar IRM en estas bibliotecas, siga estos pasos:</caps:sentence>
                      </para>
                      <list class="ordered">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="599f968755b3fd6fb4191c3386a799f0" id="tgt88" class="tgtSentence">Descargue e instale el <externalLink><linkText>SDK de componentes del cliente de SharePoint Online</linkText><linkUri>http://www.microsoft.com/en-us/download/details.aspx?id=42038</linkUri></externalLink>.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="599f968755b3fd6fb4191c3386a799f0" id="tgt89" class="tgtSentence">Descargue e instale el <externalLink><linkText>shell de administración de SharePoint Online</linkText><linkUri>http://www.microsoft.com/en-us/download/details.aspx?id=35588</linkUri></externalLink>.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="55e9b999429f1e68d6d185ae2d1d1a01" id="tgt90" class="tgtSentence">Copie el contenido del siguiente script y denomine Set-IRMOnOneDriveForBusiness.ps1 al archivo en el equipo.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence sentenceid="18eedc5da80094e0ab3d004c93476602" id="tgt91" class="tgtSentence">
                              <legacyItalic>
                                <embeddedLabel>Declinación de responsabilidades</embeddedLabel>
                              </legacyItalic>: Este script de ejemplo no es compatible en ningún servicio o programa de soporte estándar de Microsoft.</caps:sentence>
                            <caps:sentence sentenceid="c62eb79717d2870aba23b3fa99ed9aa4" id="tgt92" class="tgtSentence"> Este script de ejemplo se proporciona TAL CUAL sin garantía de ningún tipo.</caps:sentence>
                          </para>
                          <code># Requires Windows PowerShell version 3 &lt;# Description: Configures IRM policy settings for OneDrive for Business and can also be used for SharePoint Online libraries and lists Script Installation Requirements: SharePoint Online Client Components SDK http://www.microsoft.com/en-us/download/details.aspx?id=42038 SharePoint Online Management Shell http://www.microsoft.com/en-us/download/details.aspx?id=35588 ============================================================== #&gt; # URL will be in the format https://&lt;tenant-name&gt;-admin.sharepoint.com $sharepointAdminCenterUrl = "https://contoso-admin.sharepoint.com" $tenantAdmin = "admin@contoso.com" $webUrls = @("https://contoso-my.sharepoint.com/personal/user1_contoso_com", "https://contoso-my.sharepoint.com/personal/user2_contoso_com", "https://contoso-my.sharepoint.com/personal/user3_contoso_com") &lt;# As an alternative to specifying the URLs as an array, you can import them from a CSV file (no header, single value per row). Then, use: $webUrls = Get-Content -Path "File_path_and_name.csv" #&gt; $listTitle = "Documents" function Load-SharePointOnlineClientComponentAssemblies { [cmdletbinding()] param() process { # assembly location: C:\Program Files\Common Files\microsoft shared\Web Server Extensions\16\ISAPI try { Write-Verbose "Loading Assembly: Microsoft.Office.Client.Policy, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" [System.Reflection.Assembly]::Load("Microsoft.Office.Client.Policy, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c") | Out-Null Write-Verbose "Loading Assembly: Microsoft.Office.Client.TranslationServices, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" [System.Reflection.Assembly]::Load("Microsoft.Office.Client.TranslationServices, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c") | Out-Null Write-Verbose "Loading Assembly: Microsoft.SharePoint.Client, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" [System.Reflection.Assembly]::Load("Microsoft.SharePoint.Client, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c") | Out-Null Write-Verbose "Loading Assembly: Microsoft.SharePoint.Client.DocumentManagement, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" [System.Reflection.Assembly]::Load("Microsoft.SharePoint.Client.DocumentManagement, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c") | Out-Null Write-Verbose "Loading Assembly: Microsoft.SharePoint.Client.Publishing, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" [System.Reflection.Assembly]::Load("Microsoft.SharePoint.Client.Publishing, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c") | Out-Null Write-Verbose "Loading Assembly: Microsoft.SharePoint.Client.Runtime, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" [System.Reflection.Assembly]::Load("Microsoft.SharePoint.Client.Runtime, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c") | Out-Null Write-Verbose "Loading Assembly: Microsoft.SharePoint.Client.Search.Applications, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" [System.Reflection.Assembly]::Load("Microsoft.SharePoint.Client.Search.Applications, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c") | Out-Null Write-Verbose "Loading Assembly: Microsoft.SharePoint.Client.Search, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" [System.Reflection.Assembly]::Load("Microsoft.SharePoint.Client.Search, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c") | Out-Null Write-Verbose "Loading Assembly: Microsoft.SharePoint.Client.Taxonomy, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" [System.Reflection.Assembly]::Load("Microsoft.SharePoint.Client.Taxonomy, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c") | Out-Null Write-Verbose "Loading Assembly: Microsoft.SharePoint.Client.UserProfiles, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" [System.Reflection.Assembly]::Load("Microsoft.SharePoint.Client.UserProfiles, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c") | Out-Null return $true } catch { if($_.Exception.Message -match "Could not load file or assembly") { Write-Error -Message "Unable to load the SharePoint Server 2013 Client Components.`nDownload Location: http://www.microsoft.com/en-us/download/details.aspx?id=42038" } else { Write-Error -Exception $_.Exception } return $false } } } function Load-SharePointOnlineModule { [cmdletbinding()] param() process { do { # Installation location: C:\Program Files\SharePoint Online Management Shell\Microsoft.Online.SharePoint.PowerShell $spoModule = Get-Module -Name Microsoft.Online.SharePoint.PowerShell -ErrorAction SilentlyContinue if(-not $spoModule) { try { Import-Module Microsoft.Online.SharePoint.PowerShell -DisableNameChecking return $true } catch { if($_.Exception.Message -match "Could not load file or assembly") { Write-Error -Message "Unable to load the SharePoint Online Management Shell.`nDownload Location: http://www.microsoft.com/en-us/download/details.aspx?id=35588" } else { Write-Error -Exception $_.Exception } return $false } } else { return $true } } while(-not $spoModule) } } function Set-IrmConfiguration { [cmdletbinding()] param( [parameter(Mandatory=$true)][Microsoft.SharePoint.Client.List]$List, [parameter(Mandatory=$true)][string]$PolicyTitle, [parameter(Mandatory=$true)][string]$PolicyDescription, [parameter(Mandatory=$false)][switch]$IrmReject, [parameter(Mandatory=$false)][DateTime]$ProtectionExpirationDate, [parameter(Mandatory=$false)][switch]$DisableDocumentBrowserView, [parameter(Mandatory=$false)][switch]$AllowPrint, [parameter(Mandatory=$false)][switch]$AllowScript, [parameter(Mandatory=$false)][switch]$AllowWriteCopy, [parameter(Mandatory=$false)][int]$DocumentAccessExpireDays, [parameter(Mandatory=$false)][int]$LicenseCacheExpireDays, [parameter(Mandatory=$false)][string]$GroupName ) process { Write-Verbose "Applying IRM Configuration on '$($List.Title)'" # reset the value to the default settings $list.InformationRightsManagementSettings.Reset() $list.IrmEnabled = $true # IRM Policy title and description $list.InformationRightsManagementSettings.PolicyTitle       = $PolicyTitle $list.InformationRightsManagementSettings.PolicyDescription = $PolicyDescription # Set additional IRM library settings # Do not allow users to upload documents that do not support IRM $list.IrmReject = $IrmReject.IsPresent $parsedDate = Get-Date if([DateTime]::TryParse($ProtectionExpirationDate, [ref]$parsedDate)) { # Stop restricting access to the library at &lt;date&gt; $list.IrmExpire = $true $list.InformationRightsManagementSettings.DocumentLibraryProtectionExpireDate = $ProtectionExpirationDate } # Prevent opening documents in the browser for this Document Library $list.InformationRightsManagementSettings.DisableDocumentBrowserView = $DisableDocumentBrowserView.IsPresent # Configure document access rights # Allow viewers to print $list.InformationRightsManagementSettings.AllowPrint = $AllowPrint.IsPresent # Allow viewers to run script and screen reader to function on downloaded documents $list.InformationRightsManagementSettings.AllowScript = $AllowScript.IsPresent # Allow viewers to write on a copy of the downloaded document $list.InformationRightsManagementSettings.AllowWriteCopy = $AllowWriteCopy.IsPresent if($DocumentAccessExpireDays) { # After download, document access rights will expire after these number of days (1-365) $list.InformationRightsManagementSettings.EnableDocumentAccessExpire = $true $list.InformationRightsManagementSettings.DocumentAccessExpireDays   = $DocumentAccessExpireDays } # Set group protection and credentials interval if($LicenseCacheExpireDays) { # Users must verify their credentials using this interval (days) $list.InformationRightsManagementSettings.EnableLicenseCacheExpire = $true $list.InformationRightsManagementSettings.LicenseCacheExpireDays   = $LicenseCacheExpireDays } if($GroupName) { # Allow group protection. Default group: $list.InformationRightsManagementSettings.EnableGroupProtection = $true $list.InformationRightsManagementSettings.GroupName             = $GroupName } } end { if($list) { Write-Verbose "Committing IRM configuration settings on '$($list.Title)'" $list.InformationRightsManagementSettings.Update() $list.Update() $script:clientContext.Load($list) $script:clientContext.ExecuteQuery() } } } function Get-CredentialFromCredentialCache { [cmdletbinding()] param([string]$CredentialName) #if( Test-Path variable:\global:CredentialCache ) if( Get-Variable O365TenantAdminCredentialCache -Scope Global -ErrorAction SilentlyContinue ) { if($global:O365TenantAdminCredentialCache.ContainsKey($CredentialName)) { Write-Verbose "Credential Cache Hit: $CredentialName" return $global:O365TenantAdminCredentialCache[$CredentialName] } } Write-Verbose "Credential Cache Miss: $CredentialName" return $null } function Add-CredentialToCredentialCache { [cmdletbinding()] param([System.Management.Automation.PSCredential]$Credential) if(-not (Get-Variable CredentialCache -Scope Global -ErrorAction SilentlyContinue)) { Write-Verbose "Initializing the Credential Cache" $global:O365TenantAdminCredentialCache = @{} } Write-Verbose "Adding Credential to the Credential Cache" $global:O365TenantAdminCredentialCache[$Credential.UserName] = $Credential } # load the required assemblies and Windows PowerShell modules if(-not ((Load-SharePointOnlineClientComponentAssemblies) -and (Load-SharePointOnlineModule)) ) { return } # Add the credentials to the client context and SharePoint Online service connection # check for cached credentials to use $o365TenantAdminCredential = Get-CredentialFromCredentialCache -CredentialName $tenantAdmin if(-not $o365TenantAdminCredential) { # when credentials are not cached, prompt for the tenant admin credentials $o365TenantAdminCredential = Get-Credential -UserName $tenantAdmin -Message "Enter the password for the Office 365 admin" if(-not $o365TenantAdminCredential -or -not $o365TenantAdminCredential.UserName -or $o365TenantAdminCredential.Password.Length -eq 0 ) { Write-Error -Message "Could not validate the supplied tenant admin credentials" return } # add the credentials to the cache Add-CredentialToCredentialCache -Credential $o365TenantAdminCredential } # connect to Office365 first, required for SharePoint Online cmdlets to run Connect-SPOService -Url $sharepointAdminCenterUrl -Credential $o365TenantAdminCredential # enumerate each of the specified site URLs foreach($webUrl in $webUrls) { $grantedSiteCollectionAdmin = $false try { # establish the client context and set the credentials to connect to the site $script:clientContext = New-Object Microsoft.SharePoint.Client.ClientContext($webUrl) $script:clientContext.Credentials = New-Object Microsoft.SharePoint.Client.SharePointOnlineCredentials($o365TenantAdminCredential.UserName, $o365TenantAdminCredential.Password) # initialize the site and web context $script:clientContext.Load($script:clientContext.Site) $script:clientContext.Load($script:clientContext.Web) $script:clientContext.ExecuteQuery() # load and ensure the tenant admin user account if present on the target SharePoint site $tenantAdminUser = $script:clientContext.Web.EnsureUser($o365TenantAdminCredential.UserName) $script:clientContext.Load($tenantAdminUser) $script:clientContext.ExecuteQuery() # check if the tenant admin is a site admin if( -not $tenantAdminUser.IsSiteAdmin ) { try { # grant the tenant admin temporary admin rights to the site collection Set-SPOUser -Site $script:clientContext.Site.Url -LoginName $o365TenantAdminCredential.UserName -IsSiteCollectionAdmin $true | Out-Null $grantedSiteCollectionAdmin = $true } catch { Write-Error $_.Exception return } } try { # load the list orlibrary using CSOM $list = $null $list = $script:clientContext.Web.Lists.GetByTitle($listTitle) $script:clientContext.Load($list) $script:clientContext.ExecuteQuery() # **************  ADMIN INSTRUCTIONS  ************** # If necessary, modify the following Set-IrmConfiguration parameters to match your required values # The supplied options and values are for example only # Example that shows the Set-IrmConfiguration command with all parameters: Set-IrmConfiguration -List $list -PolicyTitle "Protected Files" -PolicyDescription "This policy restricts access to authorized users" -IrmReject -ProtectionExpirationDate $(Get-Date).AddDays(180) -DisableDocumentBrowserView -AllowPrint -AllowScript -AllowWriteCopy -LicenseCacheExpireDays 25 -DocumentAccessExpireDays 90 Set-IrmConfiguration -List $list -PolicyTitle "Protected Files" -PolicyDescription "This policy restricts access to authorized users" } catch { Write-Error -Message "Error setting IRM configuration on site: $webUrl.`nError Details: $($_.Exception.ToString())" } } finally { if($grantedSiteCollectionAdmin) { # remove the temporary admin rights to the site collection Set-SPOUser -Site $script:clientContext.Site.Url -LoginName $o365TenantAdminCredential.UserName -IsSiteCollectionAdmin $false | Out-Null } } } Disconnect-SPOService -ErrorAction SilentlyContinue

</code>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="3e5c8bfb50e79b38e3ce2e66ac8ccff9" id="tgt93" class="tgtSentence">Revise el script y realice los cambios siguientes:</caps:sentence>
                          </para>
                          <list class="ordered">
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="7455cdf3a433c60318c9243b472a767f" id="tgt94" class="tgtSentence">Busque <codeInline>$sharepointAdminCenterUrl</codeInline> y reemplace el valor de ejemplo con su propia dirección URL del centro de administración de SharePoint.</caps:sentence>
                              </para>
                              <para>
                                <caps:sentence sentenceid="d8a77b4f9310ec9c769bcbd28d2a46b4" id="tgt95" class="tgtSentence">Este valor aparecerá como URL base al entrar en el centro de administración de SharePoint y tendrá el siguiente formato: https://<placeholder>&lt;nombre_inquilino&gt;</placeholder>-admin.sharepoint.com</caps:sentence>
                              </para>
                              <para>
                                <caps:sentence sentenceid="045d32f423a1593c5bf047a636ec37cc" id="tgt96" class="tgtSentence">Por ejemplo, si el nombre de inquilino es "contoso", debería especificar: <userInput>https://contoso-admin.sharepoint.com</userInput></caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="7455cdf3a433c60318c9243b472a767f" id="tgt97" class="tgtSentence">Busque <codeInline>$tenantAdmin</codeInline> y reemplazar el valor de ejemplo por su propia cuenta de administrador global completa para Office 365.</caps:sentence>
                              </para>
                              <para>
                                <caps:sentence sentenceid="50c859674ade3781e9d966c7cd4018b4" id="tgt98" class="tgtSentence">Este valor es el mismo que se utiliza para iniciar sesión en el portal de administración de Office 365 como administrador global y tiene el siguiente formato: nombre_usuario@<placeholder>&lt;nombre_de_dominio_de inquilino&gt;</placeholder>.com</caps:sentence>
                              </para>
                              <para>
                                <caps:sentence sentenceid="4e1c04d223ee528ddc8297427e948ccb" id="tgt99" class="tgtSentence">Por ejemplo, si el nombre de usuario de administrador global de Office 365 es "admin" en el dominio de inquilino "contoso.com.", especificaría: <userInput>admin@contoso.com</userInput></caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="7455cdf3a433c60318c9243b472a767f" id="tgt100" class="tgtSentence">Busque <codeInline>$webUrls</codeInline> y reemplace los valores del ejemplo por las direcciones URL de la web de OneDrive para la Empresa de los usuarios y agregue o elimine tantas entradas como necesite.</caps:sentence>
                              </para>
                              <para>
                                <caps:sentence sentenceid="07c34d3baddb4e9edbbe99c8c5f18486" id="tgt101" class="tgtSentence">Como alternativa, vea los comentarios del script sobre cómo reemplazar esta matriz mediante la importación de un archivo .CSV que contiene todas las direcciones URL que es preciso configurar.</caps:sentence>
                                <caps:sentence sentenceid="0c576054df022bad478bed6e2da947fe" id="tgt102" class="tgtSentence">  Hemos proporcionado otro script de ejemplo para buscar y extraer automáticamente las direcciones URL para rellenar este archivo .CSV.</caps:sentence>
                                <caps:sentence sentenceid="5b35ade59ec147c9e2ffdd9e004da4bc" id="tgt103" class="tgtSentence"> Cuando esté listo para hacerlo, expanda la sección <link xlink:href="#BKMK_Script_OD4B_URLS">Additional script to output all OneDrive for Business URLs to a .CSV file</link> sección inmediatamente después de estos pasos.</caps:sentence>
                              </para>
                              <para>
                                <caps:sentence sentenceid="b9289b5a140d41f96707e9b9fe98770c" id="tgt104" class="tgtSentence">La dirección URL de la web de OneDrive para Empresa del usuario tiene el siguiente formato: https://<placeholder>&lt;nombre de inquilino&gt;</placeholder>-my.sharepoint.com/personal/<placeholder>&lt;nombre_usuario&gt;</placeholder>_<placeholder>&lt;nombre de inquilino&gt;</placeholder>_com</caps:sentence>
                              </para>
                              <para>
                                <caps:sentence sentenceid="dcf3dfeb47bdcb617232d7cab51dde55" id="tgt105" class="tgtSentence">Por ejemplo, si el usuario del inquilino contoso tiene el nombre de usuario "rsimone", especificaría: <userInput>https://contoso-my.sharepoint.com/personal/rsimone_contoso_com</userInput></caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="e84d5aca5708dc3a0969294f0a6715ee" id="tgt106" class="tgtSentence">Dado que vamos a usar el script para configurar OneDrive para la Empresa, no cambie el valor de <system>Documents</system> en la variable <codeInline>$listTitle</codeInline>.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="7455cdf3a433c60318c9243b472a767f" id="tgt107" class="tgtSentence">Busque <codeInline>ADMIN INSTRUCTIONS</codeInline>.</caps:sentence>
                                <caps:sentence sentenceid="044267b6b052c228f3d813f50c542558" id="tgt108" class="tgtSentence"> Si no realiza cambios en esta sección, OneDrive para la Empresa del usuario se configurará IRM con el título de directiva "Archivos protegidos" y la descripción "Esta directiva restringe el acceso a usuarios autorizados".</caps:sentence>
                                <caps:sentence sentenceid="42854179c3701c3f9c1f815a2fdc6dcc" id="tgt109" class="tgtSentence">  No se configurarán otras opciones de IRM, ya que es probable que sea lo más apropiado para la mayoría de los entornos.</caps:sentence>
                                <caps:sentence sentenceid="d97e6fb47004fe814efa78969fe2eced" id="tgt110" class="tgtSentence"> Sin embargo, es posible cambiar tanto el título de la directiva como la descripción sugeridos, así como agregar otras opciones de IRM que sean apropiados para su entorno.</caps:sentence>
                                <caps:sentence sentenceid="c6af5b71d2057fb4a61a7061965bb238" id="tgt111" class="tgtSentence"> Consulte el ejemplo comentado en el script, ya que le ayudará a construir su propio conjunto de parámetros para el comando Set-IrmConfiguration.</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="6bcf417db3e139c3710f10b2373805b0" id="tgt112" class="tgtSentence">Guarde el script y fírmelo.</caps:sentence>
                            <caps:sentence sentenceid="9c76010d742843df62369945526a3b64" id="tgt113" class="tgtSentence"> Si no firma el guión (más seguro), Windows PowerShell deben estar configurado en el equipo para ejecutar scripts sin firmar.</caps:sentence>
                            <caps:sentence sentenceid="dbf5079f216c42f1ed060be48f977ec3" id="tgt114" class="tgtSentence"> Para ello, ejecute una sesión de Windows PowerShell con la opción <ui>Ejecutar como administrador</ui> y escriba: <userInput>Set-ExecutionPolicy sin restricciones</userInput>.</caps:sentence>
                            <caps:sentence sentenceid="60745ffc42a2b47c904074b0c30d8868" id="tgt115" class="tgtSentence"> Sin embargo, esta configuración permite la ejecución de todos los scripts sin firmar (menos seguro).</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence sentenceid="bdb735148f45a643cc3c943abf34cbd6" id="tgt116" class="tgtSentence">Para obtener más información acerca de la firma de scripts de Windows PowerShell, consulte <externalLink><linkText>about_Signing</linkText><linkUri>https://technet.microsoft.com/library/hh847874.aspx</linkUri></externalLink> en la biblioteca de documentación de PowerShell.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="02b5aaa2669a81b79179df5e7984cbce" id="tgt117" class="tgtSentence">Ejecute el script y si se le solicita, especifique la contraseña de la cuenta de administrador de Office 365.</caps:sentence>
                            <caps:sentence sentenceid="78d2d726b6558931e5ba62c2541c4cf8" id="tgt118" class="tgtSentence"> Si modifica el script y lo ejecuta en la misma sesión de Windows PowerShell, no se le pedirán credenciales.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                      <alert class="tip">
                        <para>
                          <caps:sentence sentenceid="fb83e4b3e9ad802a8eafc50399a12e02" id="tgt119" class="tgtSentence">Este script también se puede utilizar para configurar IRM para una biblioteca de SharePoint Online.</caps:sentence>
                          <caps:sentence sentenceid="bd4d3c69223e645fb4cd511b9f0afd94" id="tgt120" class="tgtSentence"> Para esta configuración, es probable que desee habilitar la opción adicional <ui>No permitir a los usuarios cargar documentos que no admitan IRM</ui>, con el fin de asegurarse de que la biblioteca solo contiene documentos protegidos.</caps:sentence>
                          <caps:sentence sentenceid="790db6bdc88e19be4b76f28c3ba99f3b" id="tgt121" class="tgtSentence">    Para ello, agregue el parámetro <codeInline>-IrmReject</codeInline> parámetro al comando Set-IrmConfiguration del script.</caps:sentence>
                        </para>
                        <para>
                          <caps:sentence sentenceid="cb7ff485229813d93782e646bdbe734b" id="tgt122" class="tgtSentence">También tendría que modificar la variable <codeInline>$webUrls</codeInline> (por ejemplo, <userInput>https://contoso.sharepoint.com</userInput>) y la variable <codeInline>$listTitle</codeInline> (por ejemplo, <userInput>$Reports</userInput>).</caps:sentence>
                        </para>
                      </alert>
                      <para>
                        <caps:sentence sentenceid="e71a2a48cdcf03bbd4d79513ab2dfa4e" id="tgt123" class="tgtSentence">Si desea deshabilitar IRM en las bibliotecas de OneDrive para la Empresa del usuario, expanda la sección <link xlink:href="#BKMK_Script_OD4B_DisableIRM">Script to disable IRM for OneDrive for Business</link>.</caps:sentence>
                      </para>
                    </content>
                    <sections>
                      <section expanded="false" address="BKMK_Script_OD4B_URLS">
                        <title>
                          <caps:sentence sentenceid="311f137e886dd676bb77895fb5a851db" id="tgt124" class="tgtSentence">Script adicional para enviar todas las direcciones URL de OneDrive para la Empresa a un archivo .CSV</caps:sentence>
                        </title>
                        <content>
                          <para>
                            <caps:sentence sentenceid="c2c656b8d65506ea1f0a0f959a8ba7cc" id="tgt125" class="tgtSentence">En el paso 4c, puede utilizar el siguiente script de Windows PowerShell para extraer las direcciones URL de las bibliotecas de OneDrive para la Empresa de todos los usuarios y posteriormente podrá comprobar, editar si es necesario e importar en el script principal.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence sentenceid="61ab981dbfa41ac8decde98e5ec349ba" id="tgt126" class="tgtSentence">Este script también requiere tanto el <externalLink><linkText>SDK de componentes del cliente de SharePoint Online</linkText><linkUri>http://www.microsoft.com/en-us/download/details.aspx?id=42038</linkUri></externalLink> como el <externalLink><linkText>shell de administración de SharePoint Online</linkText><linkUri>http://www.microsoft.com/en-us/download/details.aspx?id=35588</linkUri></externalLink>.</caps:sentence>
                            <caps:sentence sentenceid="5bf9082a8fe02e4f1cf19855943d9a6b" id="tgt127" class="tgtSentence"> Siga las mismas instrucciones para copiarlo y pegarlo, guarde el archivo localmente (por ejemplo, "Report-OneDriveForBusinessSiteInfo.ps1"), modifique los valores <codeInline>$sharepointAdminCenterUrl</codeInline> y <codeInline>$tenantAdmin</codeInline> como antes y, a continuación, ejecute el script.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence sentenceid="18eedc5da80094e0ab3d004c93476602" id="tgt128" class="tgtSentence">
                              <legacyItalic>
                                <embeddedLabel>Declinación de responsabilidades</embeddedLabel>
                              </legacyItalic>: Este script de ejemplo no es compatible en ningún servicio o programa de soporte estándar de Microsoft.</caps:sentence>
                            <caps:sentence sentenceid="c62eb79717d2870aba23b3fa99ed9aa4" id="tgt129" class="tgtSentence"> Este script de ejemplo se proporciona TAL CUAL sin garantía de ningún tipo.</caps:sentence>
                          </para>
                          <code># Requires Windows PowerShell version 3 &lt;# Description: Queries the search service of an Office 365 tenant to retrieve all OneDrive for Business sites. Details of the discovered sites are written to a .CSV file (by default,"OneDriveForBusinessSiteInfo_&lt;date&gt;.csv"). Script Installation Requirements: SharePoint Online Client Components SDK http://www.microsoft.com/en-us/download/details.aspx?id=42038 SharePoint Online Management Shell http://www.microsoft.com/en-us/download/details.aspx?id=35588 ============================================================== #&gt; # URL will be in the format https://&lt;tenant-name&gt;-admin.sharepoint.com $sharepointAdminCenterUrl = "https://contoso-admin.sharepoint.com" $tenantAdmin = "admin@contoso.onmicrosoft.com" $reportName = "OneDriveForBusinessSiteInfo_$((Get-Date).ToString("yyyy-MM-dd_hh.mm.ss")).csv" $oneDriveForBusinessSiteUrls= @() $resultsProcessed = 0 function Load-SharePointOnlineClientComponentAssemblies { [cmdletbinding()] param() process { # assembly location: C:\Program Files\Common Files\microsoft shared\Web Server Extensions\16\ISAPI try { Write-Verbose "Loading Assembly: Microsoft.Office.Client.Policy, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" [System.Reflection.Assembly]::Load("Microsoft.Office.Client.Policy, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c") | Out-Null Write-Verbose "Loading Assembly: Microsoft.Office.Client.TranslationServices, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" [System.Reflection.Assembly]::Load("Microsoft.Office.Client.TranslationServices, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c") | Out-Null Write-Verbose "Loading Assembly: Microsoft.SharePoint.Client, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" [System.Reflection.Assembly]::Load("Microsoft.SharePoint.Client, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c") | Out-Null Write-Verbose "Loading Assembly: Microsoft.SharePoint.Client.DocumentManagement, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" [System.Reflection.Assembly]::Load("Microsoft.SharePoint.Client.DocumentManagement, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c") | Out-Null Write-Verbose "Loading Assembly: Microsoft.SharePoint.Client.Publishing, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" [System.Reflection.Assembly]::Load("Microsoft.SharePoint.Client.Publishing, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c") | Out-Null Write-Verbose "Loading Assembly: Microsoft.SharePoint.Client.Runtime, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" [System.Reflection.Assembly]::Load("Microsoft.SharePoint.Client.Runtime, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c") | Out-Null Write-Verbose "Loading Assembly: Microsoft.SharePoint.Client.Search.Applications, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" [System.Reflection.Assembly]::Load("Microsoft.SharePoint.Client.Search.Applications, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c") | Out-Null Write-Verbose "Loading Assembly: Microsoft.SharePoint.Client.Search, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" [System.Reflection.Assembly]::Load("Microsoft.SharePoint.Client.Search, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c") | Out-Null Write-Verbose "Loading Assembly: Microsoft.SharePoint.Client.Taxonomy, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" [System.Reflection.Assembly]::Load("Microsoft.SharePoint.Client.Taxonomy, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c") | Out-Null Write-Verbose "Loading Assembly: Microsoft.SharePoint.Client.UserProfiles, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" [System.Reflection.Assembly]::Load("Microsoft.SharePoint.Client.UserProfiles, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c") | Out-Null return $true } catch { if($_.Exception.Message -match "Could not load file or assembly") { Write-Error -Message "Unable to load the SharePoint Server 2013 Client Components.`nDownload Location: http://www.microsoft.com/en-us/download/details.aspx?id=42038" } else { Write-Error -Exception $_.Exception } return $false } } } function Load-SharePointOnlineModule { [cmdletbinding()] param() process { do { # Installation location: C:\Program Files\SharePoint Online Management Shell\Microsoft.Online.SharePoint.PowerShell $spoModule = Get-Module -Name Microsoft.Online.SharePoint.PowerShell -ErrorAction SilentlyContinue if(-not $spoModule) { try { Import-Module Microsoft.Online.SharePoint.PowerShell -DisableNameChecking return $true } catch { if($_.Exception.Message -match "Could not load file or assembly") { Write-Error -Message "Unable to load the SharePoint Online Management Shell.`nDownload Location: http://www.microsoft.com/en-us/download/details.aspx?id=35588" } else { Write-Error -Exception $_.Exception } return $false } } else { return $true } } while(-not $spoModule) } } function Get-CredentialFromCredentialCache { [cmdletbinding()] param([string]$CredentialName) #if( Test-Path variable:\global:CredentialCache ) if( Get-Variable O365TenantAdminCredentialCache -Scope Global -ErrorAction SilentlyContinue ) { if($global:O365TenantAdminCredentialCache.ContainsKey($CredentialName)) { Write-Verbose "Credential Cache Hit: $CredentialName" return $global:O365TenantAdminCredentialCache[$CredentialName] } } Write-Verbose "Credential Cache Miss: $CredentialName" return $null } function Add-CredentialToCredentialCache { [cmdletbinding()] param([System.Management.Automation.PSCredential]$Credential) if(-not (Get-Variable CredentialCache -Scope Global -ErrorAction SilentlyContinue)) { Write-Verbose "Initializing the Credential Cache" $global:O365TenantAdminCredentialCache = @{} } Write-Verbose "Adding Credential to the Credential Cache" $global:O365TenantAdminCredentialCache[$Credential.UserName] = $Credential } # load the required assemblies and Windows PowerShell modules if(-not ((Load-SharePointOnlineClientComponentAssemblies) -and (Load-SharePointOnlineModule)) ) { return } # Add the credentials to the client context and SharePoint Online service connection # check for cached credentials to use $o365TenantAdminCredential = Get-CredentialFromCredentialCache -CredentialName $tenantAdmin if(-not $o365TenantAdminCredential) { # when credentials are not cached, prompt for the tenant admin credentials $o365TenantAdminCredential = Get-Credential -UserName $tenantAdmin -Message "Enter the password for the Office 365 admin" if(-not $o365TenantAdminCredential -or -not $o365TenantAdminCredential.UserName -or $o365TenantAdminCredential.Password.Length -eq 0 ) { Write-Error -Message "Could not validate the supplied tenant admin credentials" return } # add the credentials to the cache Add-CredentialToCredentialCache -Credential $o365TenantAdminCredential } # establish the client context and set the credentials to connect to the site $clientContext = New-Object Microsoft.SharePoint.Client.ClientContext($sharepointAdminCenterUrl) $clientContext.Credentials = New-Object Microsoft.SharePoint.Client.SharePointOnlineCredentials($o365TenantAdminCredential.UserName, $o365TenantAdminCredential.Password) # run a query against the Office 365 tenant search service to retrieve all OneDrive for Business URLs do { # build the query object $query = New-Object Microsoft.SharePoint.Client.Search.Query.KeywordQuery($clientContext) $query.TrimDuplicates        = $false $query.RowLimit              = 500 $query.QueryText             = "SPSiteUrl:'/personal/' AND contentclass:STS_Site" $query.StartRow              = $resultsProcessed $query.TotalRowsExactMinimum = 500000 # run the query $searchExecutor = New-Object Microsoft.SharePoint.Client.Search.Query.SearchExecutor($clientContext) $queryResults = $searchExecutor.ExecuteQuery($query) $clientContext.ExecuteQuery() # enumerate the search results and store the site URLs $queryResults.Value[0].ResultRows | % { $oneDriveForBusinessSiteUrls += $_.Path $resultsProcessed++ } } while($resultsProcessed -lt $queryResults.Value.TotalRows) $oneDriveForBusinessSiteUrls | Out-File -FilePath $reportName
</code>
                        </content>
                      </section>
                      <section expanded="false" address="BKMK_Script_OD4B_DisableIRM">
                        <title>
                          <caps:sentence sentenceid="41f71f295aa37b42692661d3881e1b9f" id="tgt130" class="tgtSentence">Script para deshabilitar IRM en OneDrive para la Empresa</caps:sentence>
                        </title>
                        <content>
                          <para>
                            <caps:sentence sentenceid="fea92055ebf888574d9b9599a157e1c5" id="tgt131" class="tgtSentence">Utilice el siguiente script de ejemplo si necesita deshabilitar IRM en OneDrive para la Empresa de los usuarios.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence sentenceid="61ab981dbfa41ac8decde98e5ec349ba" id="tgt132" class="tgtSentence">Este script también requiere tanto el <externalLink><linkText>SDK de componentes del cliente de SharePoint Online</linkText><linkUri>http://www.microsoft.com/en-us/download/details.aspx?id=42038</linkUri></externalLink> como el <externalLink><linkText>shell de administración de SharePoint Online</linkText><linkUri>http://www.microsoft.com/en-us/download/details.aspx?id=35588</linkUri></externalLink>.</caps:sentence>
                            <caps:sentence sentenceid="4ebd529900d517e9138baeee3cbc56c3" id="tgt133" class="tgtSentence"> Copie y pegue el contenido, guarde el archivo localmente (por ejemplo, "Disable-IRMOnOneDriveForBusiness.ps1") y modifique los valores <codeInline>$sharepointAdminCenterUrl</codeInline> y <codeInline>$tenantAdmin</codeInline>.</caps:sentence>
                            <caps:sentence sentenceid="caf8b2bdb41229744aac5776ed09c646" id="tgt134" class="tgtSentence"> Especifique manualmente las direcciones URL de OneDrive para la Empresa o use el script de la sección anterior para poder importarlos y, a continuación, ejecute el script.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence sentenceid="18eedc5da80094e0ab3d004c93476602" id="tgt135" class="tgtSentence">
                              <legacyItalic>
                                <embeddedLabel>Declinación de responsabilidades</embeddedLabel>
                              </legacyItalic>: Este script de ejemplo no es compatible en ningún servicio o programa de soporte estándar de Microsoft.</caps:sentence>
                            <caps:sentence sentenceid="c62eb79717d2870aba23b3fa99ed9aa4" id="tgt136" class="tgtSentence"> Este script de ejemplo se proporciona TAL CUAL sin garantía de ningún tipo.</caps:sentence>
                          </para>
                          <code># Requires Windows PowerShell version 3 &lt;# Description: Disables IRM for OneDrive for Business and can also be used for SharePoint Online libraries and lists Script Installation Requirements: SharePoint Online Client Components SDK http://www.microsoft.com/en-us/download/details.aspx?id=42038 SharePoint Online Management Shell http://www.microsoft.com/en-us/download/details.aspx?id=35588 ============================================================== #&gt; $sharepointAdminCenterUrl = "https://contoso-admin.sharepoint.com" $tenantAdmin = "admin@contoso.com" $webUrls = @("https://contoso-my.sharepoint.com/personal/user1_contoso_com", "https://contoso-my.sharepoint.com/personal/user2_contoso_com", "https://contoso-my.sharepoint.com/personal/person3_contoso_com") &lt;# As an alternative to specifying the URLs as an array, you can import them from a CSV file (no header, single value per row). Then, use: $webUrls = Get-Content -Path "File_path_and_name.csv" #&gt; $listTitle = "Documents" function Load-SharePointOnlineClientComponentAssemblies { [cmdletbinding()] param() process { # assembly location: C:\Program Files\Common Files\microsoft shared\Web Server Extensions\16\ISAPI try { Write-Verbose "Loading Assembly: Microsoft.Office.Client.Policy, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" [System.Reflection.Assembly]::Load("Microsoft.Office.Client.Policy, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c") | Out-Null Write-Verbose "Loading Assembly: Microsoft.Office.Client.TranslationServices, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" [System.Reflection.Assembly]::Load("Microsoft.Office.Client.TranslationServices, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c") | Out-Null Write-Verbose "Loading Assembly: Microsoft.SharePoint.Client, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" [System.Reflection.Assembly]::Load("Microsoft.SharePoint.Client, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c") | Out-Null Write-Verbose "Loading Assembly: Microsoft.SharePoint.Client.DocumentManagement, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" [System.Reflection.Assembly]::Load("Microsoft.SharePoint.Client.DocumentManagement, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c") | Out-Null Write-Verbose "Loading Assembly: Microsoft.SharePoint.Client.Publishing, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" [System.Reflection.Assembly]::Load("Microsoft.SharePoint.Client.Publishing, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c") | Out-Null Write-Verbose "Loading Assembly: Microsoft.SharePoint.Client.Runtime, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" [System.Reflection.Assembly]::Load("Microsoft.SharePoint.Client.Runtime, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c") | Out-Null Write-Verbose "Loading Assembly: Microsoft.SharePoint.Client.Search.Applications, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" [System.Reflection.Assembly]::Load("Microsoft.SharePoint.Client.Search.Applications, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c") | Out-Null Write-Verbose "Loading Assembly: Microsoft.SharePoint.Client.Search, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" [System.Reflection.Assembly]::Load("Microsoft.SharePoint.Client.Search, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c") | Out-Null Write-Verbose "Loading Assembly: Microsoft.SharePoint.Client.Taxonomy, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" [System.Reflection.Assembly]::Load("Microsoft.SharePoint.Client.Taxonomy, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c") | Out-Null Write-Verbose "Loading Assembly: Microsoft.SharePoint.Client.UserProfiles, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" [System.Reflection.Assembly]::Load("Microsoft.SharePoint.Client.UserProfiles, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c") | Out-Null return $true } catch { if($_.Exception.Message -match "Could not load file or assembly") { Write-Error -Message "Unable to load the SharePoint Server 2013 Client Components.`nDownload Location: http://www.microsoft.com/en-us/download/details.aspx?id=42038" } else { Write-Error -Exception $_.Exception } return $false } } } function Load-SharePointOnlineModule { [cmdletbinding()] param() process { do { # Installation location: C:\Program Files\SharePoint Online Management Shell\Microsoft.Online.SharePoint.PowerShell $spoModule = Get-Module -Name Microsoft.Online.SharePoint.PowerShell -ErrorAction SilentlyContinue if(-not $spoModule) { try { Import-Module Microsoft.Online.SharePoint.PowerShell -DisableNameChecking return $true } catch { if($_.Exception.Message -match "Could not load file or assembly") { Write-Error -Message "Unable to load the SharePoint Online Management Shell.`nDownload Location: http://www.microsoft.com/en-us/download/details.aspx?id=35588" } else { Write-Error -Exception $_.Exception } return $false } } else { return $true } } while(-not $spoModule) } } function Remove-IrmConfiguration { [cmdletbinding()] param( [parameter(Mandatory=$true)][Microsoft.SharePoint.Client.List]$List ) process { Write-Verbose "Disabling IRM Configuration on '$($List.Title)'" $List.IrmEnabled = $false $List.IrmExpire  = $false $List.IrmReject  = $false $List.InformationRightsManagementSettings.Reset() } end { if($List) { Write-Verbose "Committing IRM configuration settings on '$($list.Title)'" $list.InformationRightsManagementSettings.Update() $list.Update() $script:clientContext.Load($list) $script:clientContext.ExecuteQuery() } } } function Get-CredentialFromCredentialCache { [cmdletbinding()] param([string]$CredentialName) #if( Test-Path variable:\global:CredentialCache ) if( Get-Variable O365TenantAdminCredentialCache -Scope Global -ErrorAction SilentlyContinue ) { if($global:O365TenantAdminCredentialCache.ContainsKey($CredentialName)) { Write-Verbose "Credential Cache Hit: $CredentialName" return $global:O365TenantAdminCredentialCache[$CredentialName] } } Write-Verbose "Credential Cache Miss: $CredentialName" return $null } function Add-CredentialToCredentialCache { [cmdletbinding()] param([System.Management.Automation.PSCredential]$Credential) if(-not (Get-Variable CredentialCache -Scope Global -ErrorAction SilentlyContinue)) { Write-Verbose "Initializing the Credential Cache" $global:O365TenantAdminCredentialCache = @{} } Write-Verbose "Adding Credential to the Credential Cache" $global:O365TenantAdminCredentialCache[$Credential.UserName] = $Credential } # load the required assemblies and Windows PowerShell modules if(-not ((Load-SharePointOnlineClientComponentAssemblies) -and (Load-SharePointOnlineModule)) ) { return } # Add the credentials to the client context and SharePoint Online service connection # check for cached credentials to use $o365TenantAdminCredential = Get-CredentialFromCredentialCache -CredentialName $tenantAdmin if(-not $o365TenantAdminCredential) { # when credentials are not cached, prompt for the tenant admin credentials $o365TenantAdminCredential = Get-Credential -UserName $tenantAdmin -Message "Enter the password for the Office 365 admin" if(-not $o365TenantAdminCredential -or -not $o365TenantAdminCredential.UserName -or $o365TenantAdminCredential.Password.Length -eq 0 ) { Write-Error -Message "Could not validate the supplied tenant admin credentials" return } # add the credentials to the cache Add-CredentialToCredentialCache -Credential $o365TenantAdminCredential } # connect to Office365 first, required for SharePoint Online cmdlets to run Connect-SPOService -Url $sharepointAdminCenterUrl -Credential $o365TenantAdminCredential # enumerate each of the specified site URLs foreach($webUrl in $webUrls) { $grantedSiteCollectionAdmin = $false try { # establish the client context and set the credentials to connect to the site $script:clientContext = New-Object Microsoft.SharePoint.Client.ClientContext($webUrl) $script:clientContext.Credentials = New-Object Microsoft.SharePoint.Client.SharePointOnlineCredentials($o365TenantAdminCredential.UserName, $o365TenantAdminCredential.Password) # initialize the site and web context $script:clientContext.Load($script:clientContext.Site) $script:clientContext.Load($script:clientContext.Web) $script:clientContext.ExecuteQuery() # load and ensure the tenant admin user account if present on the target SharePoint site $tenantAdminUser = $script:clientContext.Web.EnsureUser($o365TenantAdminCredential.UserName) $script:clientContext.Load($tenantAdminUser) $script:clientContext.ExecuteQuery() # check if the tenant admin is a site admin if( -not $tenantAdminUser.IsSiteAdmin ) { try { # grant the tenant admin temporary admin rights to the site collection Set-SPOUser -Site $script:clientContext.Site.Url -LoginName $o365TenantAdminCredential.UserName -IsSiteCollectionAdmin $true | Out-Null $grantedSiteCollectionAdmin = $true } catch { Write-Error $_.Exception return } } try { # load the list orlibrary using CSOM $list = $null $list = $script:clientContext.Web.Lists.GetByTitle($listTitle) $script:clientContext.Load($list) $script:clientContext.ExecuteQuery() Remove-IrmConfiguration -List $list } catch { Write-Error -Message "Error setting IRM configuration on site: $webUrl.`nError Details: $($_.Exception.ToString())" } } finally { if($grantedSiteCollectionAdmin) { # remove the temporary admin rights to the site collection Set-SPOUser -Site $script:clientContext.Site.Url -LoginName $o365TenantAdminCredential.UserName -IsSiteCollectionAdmin $false | Out-Null } } } Disconnect-SPOService -ErrorAction SilentlyContinue
</code>
                        </content>
                      </section>
                    </sections>
                  </section>
                </sections>
              </section>
            </sections>
          </section>
        </sections>
      </section>
      <section address="BKMK_Office2013Configuration">
        <title>
          <caps:sentence sentenceid="807d182e2678bdbe277f0b4450f1585a" id="tgt137" class="tgtSentence">Office 2016 y Office 2013: Configuración para clientes</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="090bbe92b656a35fe216289600f184c2" id="tgt138" class="tgtSentence">Como estas últimas versiones de Office son compatibles de forma nativa con Azure RMS, no es necesario configurar el equipo para admitir las características de Information Rights Management (IRM) para aplicaciones como Word, Excel, PowerPoint, Outlook y la aplicación web de Outlook.</caps:sentence>
            <caps:sentence sentenceid="7b0cbc296279057ff1cbc36c965674f9" id="tgt139" class="tgtSentence"> Todo lo que tienen que hacer los usuarios es iniciar sesión en sus aplicaciones Office con sus credenciales de <token>o365_1</token> y pueden proteger archivos y correos electrónicos, así como usar los que hayan sido protegidos por otros usuarios.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="bbbb6b8e8569e4f708b6559ae443d771" id="tgt140" class="tgtSentence">Sin embargo, se recomienda que complemente estas aplicaciones con la aplicación de uso compartido Rights Management, para que los usuarios obtengan los beneficios del complemento de Office.</caps:sentence>
            <caps:sentence sentenceid="be021ab36c2c99a549fc25f5fcee238c" id="tgt141" class="tgtSentence"> Para obtener más información, consulte la sección <link xlink:href="ea09cbc5-b98b-444e-8b60-5bc3cb199c36#BKMK_SharingApp">Rights Management sharing application: Installation and configuration for clients</link> de este tema.</caps:sentence>
          </para>
        </content>
      </section>
      <section address="BKMK_Office2010Configuration">
        <title>
          <caps:sentence sentenceid="351643db43d76843d60abd4335586fa6" id="tgt142" class="tgtSentence">Office 2010: Configuración para clientes</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="6603dda46c18bcd0717e2a25c74dbc5d" id="tgt143" class="tgtSentence">Para equipos cliente que usen Azure RMS con Office 2010, deben tener instalado la aplicación de uso compartido Rights Management para Windows.</caps:sentence>
            <caps:sentence sentenceid="34156c369bbdc51184788e5336dbc9e2" id="tgt144" class="tgtSentence"> No es preciso implementar ninguna otra configuración; los usuarios deben iniciar sesión con sus credenciales de <token>o365_1</token> y pueden proteger los archivos, así como usar los que hayan sido protegidos por otros usuarios.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="2850c7b4c3f0d0a6e268a673b33bc99e" id="tgt145" class="tgtSentence">Para obtener más información acerca de la aplicación de Rights Management sharing, consulte la sección <link xlink:href="ea09cbc5-b98b-444e-8b60-5bc3cb199c36#BKMK_SharingApp">Rights Management sharing application: Installation and configuration for clients</link> de este tema.</caps:sentence>
          </para>
        </content>
      </section>
      <section address="BKMK_SharingApp">
        <title>
          <caps:sentence sentenceid="63616ab4f69be5e85b2a1ce0b42848ab" id="tgt146" class="tgtSentence">Aplicación de uso compartido Rights Management Instalación y configuración para clientes</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="cae075513daca706903ed600e35be2cd" id="tgt147" class="tgtSentence">Es precisa la aplicación de uso compartido Rights Management (RMS) para equipos cliente que usen Azure RMS con Office 2010, y se es recomienda para todos los equipos y dispositivos móviles compatibles con Azure RMS.</caps:sentence>
            <caps:sentence sentenceid="9a0b43739dcd18f5646bdd117ddcdd40" id="tgt148" class="tgtSentence"> La aplicación de uso compartido RMS se integra con aplicaciones Office mediante la instalación de un complemento Office para que los usuarios puedan proteger fácilmente los archivos y correos electrónicos directamente desde la cinta.</caps:sentence>
            <caps:sentence sentenceid="2256a245c6f9158999bf86aa273d4991" id="tgt149" class="tgtSentence"> También ofrece protección genérica para tipos de archivo que no son compatibles de forma nativa con Azure RMS, y un sitio de seguimiento de documentos para que los usuarios controlen y revoquen los archivos que hayan protegido.</caps:sentence>
          </para>
        </content>
        <sections>
          <section address="BKMK_SharingAppforWindows" expanded="false">
            <title>
              <caps:sentence sentenceid="7cd1a87a0375852bec9b59281e1579b1" id="tgt150" class="tgtSentence">La aplicación de uso compartido de RMS para Windows: Instalación y configuración</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="52bccbe65fb33dbf164c879a5b448073" id="tgt151" class="tgtSentence">Para instalar y configurar la aplicación de RMS sharing para Windows para una implementación empresarial, consulte la <externalLink><linkText>Guía del administrador de la aplicación de Rights Management sharing</linkText><linkUri>http://technet.microsoft.com/library/dn339003.aspx</linkUri></externalLink>.</caps:sentence>
              </para>
              <alert class="tip">
                <para>
                  <caps:sentence sentenceid="d478aa26f20f994b7d90a88ce9c4fffc" id="tgt152" class="tgtSentence">Si desea instalar y probar rápidamente la aplicación de RMS sharing para un equipo único, consulte <externalLink><linkText>Descarga e instalación de la aplicación de Rights Management sharing</linkText><linkUri>http://technet.microsoft.com/library/dn574734.aspx</linkUri></externalLink> en la <externalLink><linkText>Guía de usuario de la aplicación de Rights Management sharing</linkText><linkUri>http://technet.microsoft.com/library/dn339006.aspx</linkUri></externalLink>.</caps:sentence>
                </para>
              </alert>
            </content>
          </section>
          <section address="BKMK_SharingAppMovileDevices" expanded="false">
            <title>
              <caps:sentence sentenceid="db20a8e59b92fc24a7993299bd304491" id="tgt153" class="tgtSentence">La aplicación de uso compartido de RMS para plataformas móviles: Instalación</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="79015786b07c158ea703cfcb4f3f0685" id="tgt154" class="tgtSentence">Para instalar la aplicación de uso compartido de RMS en plataformas móviles, descargue la aplicación pertinente mediante los vínculos de la <externalLink><linkText>página de Microsoft Rights Management</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=303970</linkUri></externalLink>.</caps:sentence>
                <caps:sentence sentenceid="8339ddfcd1a8686ffbbba73233901ba3" id="tgt155" class="tgtSentence"> No es necesaria ninguna configuración para usar Azure RMS con esta aplicación.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </section>
      <section address="BKMK_RMSAPIs">
        <title>
          <caps:sentence sentenceid="1aedd98b8755a6fa8ed3bdc6b994c6e8" id="tgt156" class="tgtSentence">Otras aplicaciones compatibles con las API de RMS: Instalación y configuración</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="e1ca7b6c5acc0e07a0f35a135fb17c12" id="tgt157" class="tgtSentence">Esta categoría incluye aplicaciones de línea de negocio que se han diseñado internamente mediante el SDK de RMS y aplicaciones de proveedores de software que se han diseñado mediante el SDK de RMS.</caps:sentence>
            <caps:sentence sentenceid="296465e504a1a68e1ea87b5d9793f818" id="tgt158" class="tgtSentence"> Para estas aplicaciones, sigue las instrucciones suministradas junto a la aplicación.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="0a4f90ce90fc062c4fc00532513d86da" id="tgt159" class="tgtSentence">Pasos siguientes</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="e029000d4b572b3aa0d94b10d412c0d8" id="tgt160" class="tgtSentence">Después de haber configurado las aplicaciones para admitir Azure Rights Management, use el <link xlink:href="086600c2-c5d8-47ec-a4c0-c782e1797486">Azure Rights Management Deployment Roadmap</link> para comprobar si hay otros pasos de configuración que puedan ser necesarios antes de revertir <token>aad_rightsmanagement_1</token> a usuarios y administradores.</caps:sentence>
            <caps:sentence sentenceid="78d532987bb841ddcab6e790ab58bf27" id="tgt161" class="tgtSentence"> Si no es así, consulte <link xlink:href="18564e4a-9364-4ed2-8f17-89d24fc0d878">Using Azure Rights Management</link> para conocer los pasos siguientes.</caps:sentence>
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
        <alert class="note">
          <para>
            <caps:sentence id="src1" class="srcSentence">This information is for IT administrators and consultants who have deployed Azure Rights Management.</caps:sentence>
            <caps:sentence id="src2" class="srcSentence"> If you are looking for user help and information about how to use Rights Management for a specific application or how to open a file that is rights-protected, use the help and guidance that accompanies your application.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src3" class="srcSentence">For example, for Office applications, click the Help icon and enter search terms such as <userInput>Rights Management</userInput> or <userInput>IRM</userInput>.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> For the RMS sharing application for Windows, see the <externalLink><linkText>Rights Management sharing application user guide</linkText><linkUri>http://technet.microsoft.com/library/dn339006.aspx</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence id="src5" class="srcSentence">After you have deployed Azure Rights Management (Azure RMS) for your organization, use the following information to configure applications and services to support Azure RMS.</caps:sentence>
          <caps:sentence id="src6" class="srcSentence"> These include Office applications such as Word 2013 and Word 2010, and services such as Exchange Online (transport rules, data loss prevention, do not forward, and message encryption) and SharePoint Online (protected libraries).</caps:sentence>
          <caps:sentence id="src7" class="srcSentence"> For information about how these applications and services support Rights Management, see <link xlink:href="2cdc7bde-4044-4021-b887-11476f99afd9">How Applications Support Azure Rights Management</link>.</caps:sentence>
        </para>
        <alert class="important">
          <para>
            <caps:sentence id="src8" class="srcSentence">For information about supported versions and other requirements, see <link xlink:href="dc78321d-d759-4653-8818-80da74b6cdeb">Requirements for Azure Rights Management</link>.</caps:sentence>
          </para>
        </alert>
        <list class="bullet">
          <listItem>
            <para>
              <link xlink:href="ea09cbc5-b98b-444e-8b60-5bc3cb199c36#BKMK_O365">Office 365: Configuration for clients and online services</link>
            </para>
            <list class="bullet">
              <listItem>
                <para>
                  <link xlink:href="ea09cbc5-b98b-444e-8b60-5bc3cb199c36#BKMK_ExchangeOnline">Exchange Online: IRM Configuration</link>
                </para>
              </listItem>
              <listItem>
                <para>
                  <link xlink:href="#BKMK_SharePointOnline">SharePoint Online and OneDrive for Business: IRM Configuration</link>
                </para>
              </listItem>
            </list>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="#BKMK_Office2013Configuration">Office 2016 and Office 2013: Configuration for clients</link>
            </para>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="ea09cbc5-b98b-444e-8b60-5bc3cb199c36#BKMK_Office2010Configuration">Office 2010: Configuration for clients</link>
            </para>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="ea09cbc5-b98b-444e-8b60-5bc3cb199c36#BKMK_SharingApp">Rights Management sharing application: Installation and configuration for clients</link>
            </para>
            <list class="bullet">
              <listItem>
                <para>
                  <link xlink:href="ea09cbc5-b98b-444e-8b60-5bc3cb199c36#BKMK_SharingAppforWindows">The RMS sharing application for Windows: Installation and configuration</link>
                </para>
              </listItem>
              <listItem>
                <para>
                  <link xlink:href="ea09cbc5-b98b-444e-8b60-5bc3cb199c36#BKMK_SharingAppMovileDevices">The RMS sharing application for mobile platforms: Installation</link>
                </para>
              </listItem>
            </list>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="ea09cbc5-b98b-444e-8b60-5bc3cb199c36#BKMK_RMSAPIs">Other applications that support the RMS APIs: Installation and configuration</link>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence id="src9" class="srcSentence">To configure on-premises servers such as Exchange Server and SharePoint Server, see <link xlink:href="90e7e33f-9ecc-497b-89c5-09205ffc5066">Deploying the Azure Rights Management Connector</link>.</caps:sentence>
        </para>
        <alert class="tip">
          <para>
            <caps:sentence id="src10" class="srcSentence">For high-level examples and screenshots of applications configured to use Azure RMS, see the <link xlink:href="aeeebcd7-6646-4405-addf-ee1cc74df5df#BKMK_RMSpictures">Azure RMS in action: What administrators and users see</link> section from the <link xlink:href="aeeebcd7-6646-4405-addf-ee1cc74df5df">What is Azure Rights Management?</link> topic.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <section address="BKMK_O365">
        <title>
          <caps:sentence id="src11" class="srcSentence">Office 365: Configuration for clients and online services</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src12" class="srcSentence">Because Office 365 natively supports Azure RMS, no client computer configuration is required to support the information rights management (IRM) features for applications such as Word, Excel, PowerPoint, Outlook and the Outlook Web App.</caps:sentence>
            <caps:sentence id="src13" class="srcSentence"> All users have to do is sign in to their Office applications with their <token>o365_1</token> credentials and they can protect files and emails, and use files and emails that have been protected by others.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src14" class="srcSentence">However, we recommend that you supplement these applications with the Rights Management sharing application, so that users get the benefit of the Office add-in.</caps:sentence>
            <caps:sentence id="src15" class="srcSentence"> For more information, see the <link xlink:href="ea09cbc5-b98b-444e-8b60-5bc3cb199c36#BKMK_SharingApp">Rights Management sharing application: Installation and configuration for clients</link> section in this topic.</caps:sentence>
          </para>
        </content>
        <sections>
          <section address="BKMK_ExchangeOnline" expanded="false">
            <title>
              <caps:sentence id="src16" class="srcSentence">Exchange Online: IRM Configuration</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src17" class="srcSentence">To configure Exchange Online to support Azure RMS, you must configure the information rights management (IRM) service for Exchange Online.</caps:sentence>
                <caps:sentence id="src18" class="srcSentence"> To do this, you use Windows PowerShell (no need to install a separate module), and run <externalLink><linkText>PowerShell commands for Exchange Online</linkText><linkUri>https://technet.microsoft.com/library/jj200677.aspx</linkUri></externalLink>.</caps:sentence>
              </para>
              <alert class="note">
                <para>
                  <caps:sentence id="src19" class="srcSentence">You cannot currently configure Exchange Online to support Azure RMS if you are using a customer-managed tenant key (BYOK) for Azure RMS, rather than the default configuration of a Microsoft-managed tenant key.</caps:sentence>
                  <caps:sentence id="src20" class="srcSentence"> For more information, see the <link xlink:href="f0d33c5f-a6a6-44a1-bdec-5be1bc8e1e14#BKMK_Pricing">BYOK pricing and restrictions</link> section in the <link xlink:href="f0d33c5f-a6a6-44a1-bdec-5be1bc8e1e14">Planning and Implementing Your Azure Rights Management Tenant Key</link> topic.</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src21" class="srcSentence">If you try to configure Exchange Online when Azure RMS is using BYOK, the command to import the key (step 5,  in the following procedure) fails with the error message <ui>[FailureCategory=Cmdlet-FailedToGetTrustedPublishingDomainFromRmsOnlineException]</ui>.</caps:sentence>
                </para>
              </alert>
              <para>
                <caps:sentence id="src22" class="srcSentence">The following steps provide a typical set of commands that you would run to enable Exchange Online to use Azure RMS:</caps:sentence>
              </para>
              <list class="ordered">
                <listItem>
                  <para>
                    <caps:sentence id="src23" class="srcSentence">If this is the first time that you have used Windows PowerShell for Exchange Online on your computer, you must configure Windows PowerShell to run signed scripts.</caps:sentence>
                    <caps:sentence id="src24" class="srcSentence"> Start your Windows PowerShell session by using the <ui>Run as administrator</ui> option, and then type:</caps:sentence>
                  </para>
                  <code>
Set-ExecutionPolicy RemoteSigned </code>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src25" class="srcSentence">In your Windows PowerShell session, sign in to Exchange Online by using an account that is enabled for remote Shell access.</caps:sentence>
                    <caps:sentence id="src26" class="srcSentence"> By default, all accounts that are created in Exchange Online are enabled for remote Shell access but this can be disabled  (and enabled) by using the   <externalLink><linkText>Set-User &lt;UserIdentity&gt; -RemotePowerShellEnabled</linkText><linkUri>https://technet.microsoft.com/library/jj984292(v=exchg.160).aspx</linkUri></externalLink> command.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src27" class="srcSentence">To sign in, type:</caps:sentence>
                  </para>
                  <code>$Cred = Get-Credential</code>
                  <para>
                    <caps:sentence id="src28" class="srcSentence">In the <ui>Windows PowerShell credential request</ui> dialog box, supply your Office 365 user name and password.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src29" class="srcSentence">Connect to the Exchange Online service by running the following two commands:</caps:sentence>
                  </para>
                  <code>$Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.outlook.com/powershell/ -Credential $Cred -Authentication Basic –AllowRedirection</code>
                  <code>Import-PSSession $Session</code>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src30" class="srcSentence">Specify the location of the Azure RMS tenant key, according to your region:</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src31" class="srcSentence">For North America (and government subscriptions):</caps:sentence>
                  </para>
                  <code>Set-IRMConfiguration -RMSOnlineKeySharingLocation "https://sp-rms.na.aadrm.com/TenantManagement/ServicePartner.svc"</code>
                  <para>
                    <caps:sentence id="src32" class="srcSentence">For Europe:</caps:sentence>
                  </para>
                  <code>Set-IRMConfiguration -RMSOnlineKeySharingLocation "https://sp-rms.eu.aadrm.com/TenantManagement/ServicePartner.svc"</code>
                  <para>
                    <caps:sentence id="src33" class="srcSentence">For Asia:</caps:sentence>
                  </para>
                  <code>Set-IRMConfiguration -RMSOnlineKeySharingLocation "https://sp-rms.ap.aadrm.com/TenantManagement/ServicePartner.svc"</code>
                  <para>
                    <caps:sentence id="src34" class="srcSentence">For South America:</caps:sentence>
                  </para>
                  <code>Set-IRMConfiguration -RMSOnlineKeySharingLocation "https://sp-rms.sa.aadrm.com/TenantManagement/ServicePartner.svc"</code>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src35" class="srcSentence">Import configuration data from Azure RMS to Exchange Online, in the form of the trusted publishing domain (TPD).</caps:sentence>
                    <caps:sentence id="src36" class="srcSentence"> This includes the Azure RMS tenant key and Azure RMS templates:</caps:sentence>
                  </para>
                  <code>Import-RMSTrustedPublishingDomain -RMSOnline -name "RMS Online"</code>
                  <para>
                    <caps:sentence id="src37" class="srcSentence">In this command, we used the name of <ui>RMS Online</ui>  for the base name of the TPD for Azure RMS in Exchange Online.</caps:sentence>
                    <caps:sentence id="src38" class="srcSentence"> After the TPD is imported, it is named <system>RMS Online - 1</system> in Exchange Online.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src39" class="srcSentence">Enable Azure RMS functionality so that IRM features are available for Exchange Online:</caps:sentence>
                  </para>
                  <code>Set-IRMConfiguration -InternalLicensingEnabled $true</code>
                  <para>
                    <caps:sentence id="src40" class="srcSentence">After running this command, Rights Management is automatically enabled for the Outlook client, the Outlook Web app, and Exchange Active Sync.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src41" class="srcSentence">Optionally, test that this configuration is successful by using the following command:</caps:sentence>
                  </para>
                  <code>Test-IRMConfiguration -Sender &lt;user email address&gt;</code>
                  <para>
                    <caps:sentence id="src42" class="srcSentence">For example: <userInput>Test-IRMConfiguration -Sender  adams@contoso.com</userInput></caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src43" class="srcSentence">This command runs a series of checks that includes verifying connectivity to the service, retrieving the configuration, retrieving URIs, licenses, and any templates.</caps:sentence>
                    <caps:sentence id="src44" class="srcSentence"> In the Windows PowerShell session, you will see the results of each and at the end, if everything passes these checks: <ui>OVERALL RESULT: PASS</ui></caps:sentence> </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src45" class="srcSentence">Disconnect your remote PowerShell session:</caps:sentence>
                  </para>
                  <code>Remove-PSSession $Session</code>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src46" class="srcSentence">Users can now protect their email messages by using Azure RMS.</caps:sentence>
                <caps:sentence id="src47" class="srcSentence"> For example,  in the Outlook Web App, select <ui>Set permissions</ui> from the extended menu (<ui>...</ui>), and then choose <ui>Do Not Forward</ui> or one of the available templates to apply information protection to the email message and any attachments.</caps:sentence>
                <caps:sentence id="src48" class="srcSentence"> However, because the Outlook Web App caches the UI for a day, wait for this time period to elapse before you try applying information protection to email messages and after running these configuration commands.</caps:sentence>
                <caps:sentence id="src49" class="srcSentence"> Before the UI updates to reflect the new configuration, you will not see any options from the <ui>Set permissions</ui> menu.</caps:sentence>
              </para>
              <alert class="important">
                <para>
                  <caps:sentence id="src50" class="srcSentence">If you create new <externalLink><linkText>custom templates</linkText><linkUri>https://technet.microsoft.com/library/dn642472.aspx</linkUri></externalLink> for Azure RMS or update the templates, each time, you must run the following Exchange Online PowerShell command (if necessary, run steps 2 and 3 first) to synchronize these changes to Exchange Online: <codeInline>Import-RMSTrustedPublishingDomain -Name "RMS Online - 1" -RefreshTemplates –RMSOnline</codeInline></caps:sentence>
                </para>
              </alert>
              <para>
                <caps:sentence id="src51" class="srcSentence">As an Exchange administrator, you can now configure features that apply information protection automatically, such as <externalLink><linkText>transport rules</linkText><linkUri>https://technet.microsoft.com/library/dd302432.aspx</linkUri></externalLink>, <externalLink><linkText>data loss prevention (DLP) policies</linkText><linkUri>https://technet.microsoft.com/library/jj150527(v=exchg.150).aspx</linkUri></externalLink>, and <externalLink><linkText>protected voice mail</linkText><linkUri>https://technet.microsoft.com/library/dn198211(v=exchg.150).aspx</linkUri></externalLink> (Unified Messaging).</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src52" class="srcSentence"> For detailed instructions to configure Exchange Online to enable IRM functionality, see the documentation in the Exchange library.</caps:sentence>
                <caps:sentence id="src53" class="srcSentence"> For example:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <externalLink>
                      <linkText>
                        <caps:sentence id="src54" class="srcSentence">Connect to Exchange Online using remote PowerShell</caps:sentence>
                      </linkText>
                      <linkUri>https://technet.microsoft.com/library/jj984289(v=exchg.160).aspx</linkUri>
                    </externalLink>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <externalLink>
                      <linkText>
                        <caps:sentence id="src55" class="srcSentence">Configure IRM to use Azure Rights Management</caps:sentence>
                      </linkText>
                      <linkUri>https://technet.microsoft.com/library/dn151475(v=exchg.150).aspx</linkUri>
                    </externalLink>
                  </para>
                </listItem>
              </list>
            </content>
            <sections>
              <section>
                <title>
                  <caps:sentence id="src56" class="srcSentence">Office 365 Message Encryption</caps:sentence>
                </title>
                <content>
                  <para>
                    <caps:sentence id="src57" class="srcSentence">Run the same steps as documented in the previous section, but if you don't want templates to be displayed, before step 6,  run the following command to prevent IRM templates from being available in the Outlook Web App and Outlook client: <codeInline>Set-IRMConfiguration -ClientAccessServerEnabled $false</codeInline></caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src58" class="srcSentence">Then, you're ready to configure <externalLink><linkText>transport rules</linkText><linkUri>https://technet.microsoft.com/library/dd302432.aspx</linkUri></externalLink> to automatically modify the message security when recipients are located outside the organization, and select the <ui>Apply Office 365 Message Encryption</ui> option.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src59" class="srcSentence">For more information about message encryption, see <externalLink><linkText>Encryption in Office 365</linkText><linkUri>https://technet.microsoft.com/library/dn569286.aspx</linkUri></externalLink> in the Exchange library.</caps:sentence>
                  </para>
                </content>
              </section>
            </sections>
          </section>
          <section address="BKMK_SharePointOnline" expanded="false">
            <title>
              <caps:sentence id="src60" class="srcSentence">SharePoint Online and OneDrive for Business: IRM Configuration</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src61" class="srcSentence">To configure SharePoint Online and OneDrive for Business to support Azure RMS, you must first enable the information rights management (IRM) service for SharePoint Online by using the SharePoint admin center.</caps:sentence>
                <caps:sentence id="src62" class="srcSentence"> Then, site owners can  IRM-protect their SharePoint lists and document libraries, and users can IRM-protect their OneDrive for Business library so that documents that are saved there, and shared with others, are automatically protected by Azure RMS.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src63" class="srcSentence">To enable the  information rights management (IRM) service for SharePoint Online, see the following instructions from the Office website:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <externalLink>
                      <linkText>
                        <caps:sentence id="src64" class="srcSentence">Set up Information Rights Management (IRM) in SharePoint admin center</caps:sentence>
                      </linkText>
                      <linkUri>http://office.microsoft.com/office365-sharepoint-online-enterprise-help/set-up-information-rights-management-irm-insharepoint-online-HA102895193.aspx</linkUri>
                    </externalLink>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src65" class="srcSentence">This configuration is done by the Office 365 administrator.</caps:sentence>
              </para>
            </content>
            <sections>
              <section>
                <title>
                  <caps:sentence id="src66" class="srcSentence">Configuring IRM for libraries and lists</caps:sentence>
                </title>
                <content>
                  <para>
                    <caps:sentence id="src67" class="srcSentence">After you have enabled the   IRM service for SharePoint, site owners can  IRM-protect their SharePoint document libraries and lists.</caps:sentence>
                    <caps:sentence id="src68" class="srcSentence"> For instructions, see the following from the Office website:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src69" class="srcSentence"> <externalLink><linkText>Apply Information Rights Management to a list or library</linkText><linkUri>http://office.microsoft.com/sharepoint-help/apply-information-rights-management-to-a-list-or-library-HA102891460.aspx</linkUri></externalLink></caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence id="src70" class="srcSentence">This configuration is done by the SharePoint site administrator.</caps:sentence>
                  </para>
                </content>
              </section>
              <section address="BKMK_OneDrive" expanded="true">
                <title>
                  <caps:sentence id="src71" class="srcSentence">Configuring IRM for OneDrive for Business</caps:sentence>
                </title>
                <content>
                  <para>
                    <caps:sentence id="src72" class="srcSentence">After you have enabled the   IRM service for SharePoint Online, users' OneDrive for Business document library can then be configured for  Rights Management protection.</caps:sentence>
                    <caps:sentence id="src73" class="srcSentence">  Users can configure this for themselves by using the <ui>Settings</ui> icon in their OneDrive.</caps:sentence>
                    <caps:sentence id="src74" class="srcSentence"> Although administrators cannot configure Rights Management for users' OneDrive for Business by using the SharePoint admin center, you can do this by using Windows PowerShell.</caps:sentence>
                  </para>
                  <alert class="note">
                    <para>
                      <caps:sentence id="src75" class="srcSentence">For more information about configuring OneDrive for Business, see the Office documentation,<externalLink><linkText>Set up OneDrive for Business in Office 365</linkText><linkUri>https://support.office.com/article/Set-up-OneDrive-for-Business-in-Office-365-3e21f8f0-e0a1-43be-aa3e-8c0236bf11bb</linkUri></externalLink>.</caps:sentence>
                    </para>
                  </alert>
                </content>
                <sections>
                  <section>
                    <title>
                      <caps:sentence id="src76" class="srcSentence">Configuration for users</caps:sentence>
                    </title>
                    <content>
                      <para>
                        <caps:sentence id="src77" class="srcSentence">Give users these instructions so that they can configure their OneDrive for Business and IRM-protect their business files.</caps:sentence>
                      </para>
                      <list class="ordered">
                        <listItem>
                          <para>
                            <caps:sentence id="src78" class="srcSentence">In OneDrive, click the <ui>Settings</ui> icon, to open the Settings menu, and then click <ui>Site Contents</ui>.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src79" class="srcSentence">Hover on the <ui>Documents</ui> tile, chose the ellipses (<ui>...</ui>), and then click <ui>SETTINGS.</ui></caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src80" class="srcSentence">On the <ui>Settings</ui> page, in the <ui>Permissions and Management</ui> section, click <ui>Information Rights Management</ui>.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src81" class="srcSentence">On the <ui>Information Rights Management Settings</ui> page, select <ui>Restrict permissions on this library on download</ui> check box, specify your choice of  name and a description for the permissions, and optionally, click <ui>SHOW OPTIONS</ui> to configure optional configurations, and then click <ui>OK</ui>.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence id="src82" class="srcSentence">For more information about the configuration options, see the instructions in <externalLink><linkText>Apply Information Rights Management to a list or library</linkText><linkUri>https://support.office.com/article/Apply-Information-Rights-Management-to-a-list-or-library-3bdb5c4e-94fc-4741-b02f-4e7cc3c54aa1</linkUri></externalLink> from the Office documentation.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                      <para>
                        <caps:sentence id="src83" class="srcSentence">Because this configuration relies on users rather than an administrator to IRM-protect their OneDrive for Business library, educate users about the  benefits of protecting their files and how to do this.</caps:sentence>
                        <caps:sentence id="src84" class="srcSentence"> For example, explain that when they share a document from OneDrive for Business, only people they authorize can access it with  any restrictions that they configure, even if the file is renamed and copied somewhere else.</caps:sentence>
                      </para>
                    </content>
                  </section>
                  <section>
                    <title>
                      <caps:sentence id="src85" class="srcSentence">Configuration for administrators</caps:sentence>
                    </title>
                    <content>
                      <para>
                        <caps:sentence id="src86" class="srcSentence">Although you cannot configure IRM for users' OneDrive for Business by using the SharePoint admin center, you can do this by using Windows PowerShell.</caps:sentence>
                        <caps:sentence id="src87" class="srcSentence"> To enable IRM for these libraries, follow these steps:</caps:sentence>
                      </para>
                      <list class="ordered">
                        <listItem>
                          <para>
                            <caps:sentence id="src88" class="srcSentence">Download and install the <externalLink><linkText>SharePoint Online Client Components SDK</linkText><linkUri>http://www.microsoft.com/en-us/download/details.aspx?id=42038</linkUri></externalLink>.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src89" class="srcSentence">Download and install the <externalLink><linkText>SharePoint Online Management Shell</linkText><linkUri>http://www.microsoft.com/en-us/download/details.aspx?id=35588</linkUri></externalLink>.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src90" class="srcSentence">Copy the contents of the following script and name the file Set-IRMOnOneDriveForBusiness.ps1 on your computer.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence id="src91" class="srcSentence">
                              <legacyItalic>
                                <embeddedLabel>Disclaimer</embeddedLabel>
                              </legacyItalic>: This sample script is not supported under any Microsoft standard support program or service.</caps:sentence>
                            <caps:sentence id="src92" class="srcSentence"> This sample script is provided AS IS without warranty of any kind.</caps:sentence>
                          </para>
                          <code># Requires Windows PowerShell version 3 &lt;# Description: Configures IRM policy settings for OneDrive for Business and can also be used for SharePoint Online libraries and lists Script Installation Requirements: SharePoint Online Client Components SDK http://www.microsoft.com/en-us/download/details.aspx?id=42038 SharePoint Online Management Shell http://www.microsoft.com/en-us/download/details.aspx?id=35588 ============================================================== #&gt; # URL will be in the format https://&lt;tenant-name&gt;-admin.sharepoint.com $sharepointAdminCenterUrl = "https://contoso-admin.sharepoint.com" $tenantAdmin = "admin@contoso.com" $webUrls = @("https://contoso-my.sharepoint.com/personal/user1_contoso_com", "https://contoso-my.sharepoint.com/personal/user2_contoso_com", "https://contoso-my.sharepoint.com/personal/user3_contoso_com") &lt;# As an alternative to specifying the URLs as an array, you can import them from a CSV file (no header, single value per row). Then, use: $webUrls = Get-Content -Path "File_path_and_name.csv" #&gt; $listTitle = "Documents" function Load-SharePointOnlineClientComponentAssemblies { [cmdletbinding()] param() process { # assembly location: C:\Program Files\Common Files\microsoft shared\Web Server Extensions\16\ISAPI try { Write-Verbose "Loading Assembly: Microsoft.Office.Client.Policy, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" [System.Reflection.Assembly]::Load("Microsoft.Office.Client.Policy, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c") | Out-Null Write-Verbose "Loading Assembly: Microsoft.Office.Client.TranslationServices, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" [System.Reflection.Assembly]::Load("Microsoft.Office.Client.TranslationServices, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c") | Out-Null Write-Verbose "Loading Assembly: Microsoft.SharePoint.Client, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" [System.Reflection.Assembly]::Load("Microsoft.SharePoint.Client, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c") | Out-Null Write-Verbose "Loading Assembly: Microsoft.SharePoint.Client.DocumentManagement, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" [System.Reflection.Assembly]::Load("Microsoft.SharePoint.Client.DocumentManagement, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c") | Out-Null Write-Verbose "Loading Assembly: Microsoft.SharePoint.Client.Publishing, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" [System.Reflection.Assembly]::Load("Microsoft.SharePoint.Client.Publishing, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c") | Out-Null Write-Verbose "Loading Assembly: Microsoft.SharePoint.Client.Runtime, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" [System.Reflection.Assembly]::Load("Microsoft.SharePoint.Client.Runtime, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c") | Out-Null Write-Verbose "Loading Assembly: Microsoft.SharePoint.Client.Search.Applications, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" [System.Reflection.Assembly]::Load("Microsoft.SharePoint.Client.Search.Applications, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c") | Out-Null Write-Verbose "Loading Assembly: Microsoft.SharePoint.Client.Search, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" [System.Reflection.Assembly]::Load("Microsoft.SharePoint.Client.Search, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c") | Out-Null Write-Verbose "Loading Assembly: Microsoft.SharePoint.Client.Taxonomy, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" [System.Reflection.Assembly]::Load("Microsoft.SharePoint.Client.Taxonomy, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c") | Out-Null Write-Verbose "Loading Assembly: Microsoft.SharePoint.Client.UserProfiles, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" [System.Reflection.Assembly]::Load("Microsoft.SharePoint.Client.UserProfiles, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c") | Out-Null return $true } catch { if($_.Exception.Message -match "Could not load file or assembly") { Write-Error -Message "Unable to load the SharePoint Server 2013 Client Components.`nDownload Location: http://www.microsoft.com/en-us/download/details.aspx?id=42038" } else { Write-Error -Exception $_.Exception } return $false } } } function Load-SharePointOnlineModule { [cmdletbinding()] param() process { do { # Installation location: C:\Program Files\SharePoint Online Management Shell\Microsoft.Online.SharePoint.PowerShell $spoModule = Get-Module -Name Microsoft.Online.SharePoint.PowerShell -ErrorAction SilentlyContinue if(-not $spoModule) { try { Import-Module Microsoft.Online.SharePoint.PowerShell -DisableNameChecking return $true } catch { if($_.Exception.Message -match "Could not load file or assembly") { Write-Error -Message "Unable to load the SharePoint Online Management Shell.`nDownload Location: http://www.microsoft.com/en-us/download/details.aspx?id=35588" } else { Write-Error -Exception $_.Exception } return $false } } else { return $true } } while(-not $spoModule) } } function Set-IrmConfiguration { [cmdletbinding()] param( [parameter(Mandatory=$true)][Microsoft.SharePoint.Client.List]$List, [parameter(Mandatory=$true)][string]$PolicyTitle, [parameter(Mandatory=$true)][string]$PolicyDescription, [parameter(Mandatory=$false)][switch]$IrmReject, [parameter(Mandatory=$false)][DateTime]$ProtectionExpirationDate, [parameter(Mandatory=$false)][switch]$DisableDocumentBrowserView, [parameter(Mandatory=$false)][switch]$AllowPrint, [parameter(Mandatory=$false)][switch]$AllowScript, [parameter(Mandatory=$false)][switch]$AllowWriteCopy, [parameter(Mandatory=$false)][int]$DocumentAccessExpireDays, [parameter(Mandatory=$false)][int]$LicenseCacheExpireDays, [parameter(Mandatory=$false)][string]$GroupName ) process { Write-Verbose "Applying IRM Configuration on '$($List.Title)'" # reset the value to the default settings $list.InformationRightsManagementSettings.Reset() $list.IrmEnabled = $true # IRM Policy title and description $list.InformationRightsManagementSettings.PolicyTitle       = $PolicyTitle $list.InformationRightsManagementSettings.PolicyDescription = $PolicyDescription # Set additional IRM library settings # Do not allow users to upload documents that do not support IRM $list.IrmReject = $IrmReject.IsPresent $parsedDate = Get-Date if([DateTime]::TryParse($ProtectionExpirationDate, [ref]$parsedDate)) { # Stop restricting access to the library at &lt;date&gt; $list.IrmExpire = $true $list.InformationRightsManagementSettings.DocumentLibraryProtectionExpireDate = $ProtectionExpirationDate } # Prevent opening documents in the browser for this Document Library $list.InformationRightsManagementSettings.DisableDocumentBrowserView = $DisableDocumentBrowserView.IsPresent # Configure document access rights # Allow viewers to print $list.InformationRightsManagementSettings.AllowPrint = $AllowPrint.IsPresent # Allow viewers to run script and screen reader to function on downloaded documents $list.InformationRightsManagementSettings.AllowScript = $AllowScript.IsPresent # Allow viewers to write on a copy of the downloaded document $list.InformationRightsManagementSettings.AllowWriteCopy = $AllowWriteCopy.IsPresent if($DocumentAccessExpireDays) { # After download, document access rights will expire after these number of days (1-365) $list.InformationRightsManagementSettings.EnableDocumentAccessExpire = $true $list.InformationRightsManagementSettings.DocumentAccessExpireDays   = $DocumentAccessExpireDays } # Set group protection and credentials interval if($LicenseCacheExpireDays) { # Users must verify their credentials using this interval (days) $list.InformationRightsManagementSettings.EnableLicenseCacheExpire = $true $list.InformationRightsManagementSettings.LicenseCacheExpireDays   = $LicenseCacheExpireDays } if($GroupName) { # Allow group protection. Default group: $list.InformationRightsManagementSettings.EnableGroupProtection = $true $list.InformationRightsManagementSettings.GroupName             = $GroupName } } end { if($list) { Write-Verbose "Committing IRM configuration settings on '$($list.Title)'" $list.InformationRightsManagementSettings.Update() $list.Update() $script:clientContext.Load($list) $script:clientContext.ExecuteQuery() } } } function Get-CredentialFromCredentialCache { [cmdletbinding()] param([string]$CredentialName) #if( Test-Path variable:\global:CredentialCache ) if( Get-Variable O365TenantAdminCredentialCache -Scope Global -ErrorAction SilentlyContinue ) { if($global:O365TenantAdminCredentialCache.ContainsKey($CredentialName)) { Write-Verbose "Credential Cache Hit: $CredentialName" return $global:O365TenantAdminCredentialCache[$CredentialName] } } Write-Verbose "Credential Cache Miss: $CredentialName" return $null } function Add-CredentialToCredentialCache { [cmdletbinding()] param([System.Management.Automation.PSCredential]$Credential) if(-not (Get-Variable CredentialCache -Scope Global -ErrorAction SilentlyContinue)) { Write-Verbose "Initializing the Credential Cache" $global:O365TenantAdminCredentialCache = @{} } Write-Verbose "Adding Credential to the Credential Cache" $global:O365TenantAdminCredentialCache[$Credential.UserName] = $Credential } # load the required assemblies and Windows PowerShell modules if(-not ((Load-SharePointOnlineClientComponentAssemblies) -and (Load-SharePointOnlineModule)) ) { return } # Add the credentials to the client context and SharePoint Online service connection # check for cached credentials to use $o365TenantAdminCredential = Get-CredentialFromCredentialCache -CredentialName $tenantAdmin if(-not $o365TenantAdminCredential) { # when credentials are not cached, prompt for the tenant admin credentials $o365TenantAdminCredential = Get-Credential -UserName $tenantAdmin -Message "Enter the password for the Office 365 admin" if(-not $o365TenantAdminCredential -or -not $o365TenantAdminCredential.UserName -or $o365TenantAdminCredential.Password.Length -eq 0 ) { Write-Error -Message "Could not validate the supplied tenant admin credentials" return } # add the credentials to the cache Add-CredentialToCredentialCache -Credential $o365TenantAdminCredential } # connect to Office365 first, required for SharePoint Online cmdlets to run Connect-SPOService -Url $sharepointAdminCenterUrl -Credential $o365TenantAdminCredential # enumerate each of the specified site URLs foreach($webUrl in $webUrls) { $grantedSiteCollectionAdmin = $false try { # establish the client context and set the credentials to connect to the site $script:clientContext = New-Object Microsoft.SharePoint.Client.ClientContext($webUrl) $script:clientContext.Credentials = New-Object Microsoft.SharePoint.Client.SharePointOnlineCredentials($o365TenantAdminCredential.UserName, $o365TenantAdminCredential.Password) # initialize the site and web context $script:clientContext.Load($script:clientContext.Site) $script:clientContext.Load($script:clientContext.Web) $script:clientContext.ExecuteQuery() # load and ensure the tenant admin user account if present on the target SharePoint site $tenantAdminUser = $script:clientContext.Web.EnsureUser($o365TenantAdminCredential.UserName) $script:clientContext.Load($tenantAdminUser) $script:clientContext.ExecuteQuery() # check if the tenant admin is a site admin if( -not $tenantAdminUser.IsSiteAdmin ) { try { # grant the tenant admin temporary admin rights to the site collection Set-SPOUser -Site $script:clientContext.Site.Url -LoginName $o365TenantAdminCredential.UserName -IsSiteCollectionAdmin $true | Out-Null $grantedSiteCollectionAdmin = $true } catch { Write-Error $_.Exception return } } try { # load the list orlibrary using CSOM $list = $null $list = $script:clientContext.Web.Lists.GetByTitle($listTitle) $script:clientContext.Load($list) $script:clientContext.ExecuteQuery() # **************  ADMIN INSTRUCTIONS  ************** # If necessary, modify the following Set-IrmConfiguration parameters to match your required values # The supplied options and values are for example only # Example that shows the Set-IrmConfiguration command with all parameters: Set-IrmConfiguration -List $list -PolicyTitle "Protected Files" -PolicyDescription "This policy restricts access to authorized users" -IrmReject -ProtectionExpirationDate $(Get-Date).AddDays(180) -DisableDocumentBrowserView -AllowPrint -AllowScript -AllowWriteCopy -LicenseCacheExpireDays 25 -DocumentAccessExpireDays 90 Set-IrmConfiguration -List $list -PolicyTitle "Protected Files" -PolicyDescription "This policy restricts access to authorized users" } catch { Write-Error -Message "Error setting IRM configuration on site: $webUrl.`nError Details: $($_.Exception.ToString())" } } finally { if($grantedSiteCollectionAdmin) { # remove the temporary admin rights to the site collection Set-SPOUser -Site $script:clientContext.Site.Url -LoginName $o365TenantAdminCredential.UserName -IsSiteCollectionAdmin $false | Out-Null } } } Disconnect-SPOService -ErrorAction SilentlyContinue

</code>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src93" class="srcSentence">Review the script and make the following changes:</caps:sentence>
                          </para>
                          <list class="ordered">
                            <listItem>
                              <para>
                                <caps:sentence id="src94" class="srcSentence">Search for <codeInline>$sharepointAdminCenterUrl</codeInline> and replace the example value with your own SharePoint admin center URL.</caps:sentence>
                              </para>
                              <para>
                                <caps:sentence id="src95" class="srcSentence">You'll find this value as the base URL when you go into the SharePoint admin center, and it has the following format: https://<placeholder>&lt;tenant_name&gt;</placeholder>-admin.sharepoint.com</caps:sentence>
                              </para>
                              <para>
                                <caps:sentence id="src96" class="srcSentence">For example, if the tenant name is "contoso", then you would specify: <userInput>https://contoso-admin.sharepoint.com</userInput></caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src97" class="srcSentence">Search for <codeInline>$tenantAdmin</codeInline> and replace the example value with your own fully qualified global administrator account for Office 365.</caps:sentence>
                              </para>
                              <para>
                                <caps:sentence id="src98" class="srcSentence">This value is the same as the one you use to sign in to the Office 365 admin portal as the global administrator and has the following format: user_name@<placeholder>&lt;tenant domain name&gt;</placeholder>.com</caps:sentence>
                              </para>
                              <para>
                                <caps:sentence id="src99" class="srcSentence">For example, if the Office 365 global administrator user name is "admin" for the "contoso.com" tenant domain, you would specify: <userInput>admin@contoso.com</userInput></caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src100" class="srcSentence">Search for <codeInline>$webUrls</codeInline> and replace the example values with your users' OneDrive for Business web URLs, adding or deleting as many entries as you need.</caps:sentence>
                              </para>
                              <para>
                                <caps:sentence id="src101" class="srcSentence">Alternatively, see the comments in the script about how to replace this array by importing a .CSV file that contains all the URLs you need to configure.</caps:sentence>
                                <caps:sentence id="src102" class="srcSentence">  We've provided another sample script to automatically search for and extract the URLs to populate this .CSV file.</caps:sentence>
                                <caps:sentence id="src103" class="srcSentence"> When you're ready to do this, expand the <link xlink:href="#BKMK_Script_OD4B_URLS">Additional script to output all OneDrive for Business URLs to a .CSV file</link> section immediately after these steps.</caps:sentence>
                              </para>
                              <para>
                                <caps:sentence id="src104" class="srcSentence">The web URL for the user's OneDrive for Business is in the following format: https://<placeholder>&lt;tenant name&gt;</placeholder>-my.sharepoint.com/personal/<placeholder>&lt;user_name&gt;</placeholder>_<placeholder>&lt;tenant name&gt;</placeholder>_com</caps:sentence>
                              </para>
                              <para>
                                <caps:sentence id="src105" class="srcSentence">For example, if the user in the contoso tenant has a user name of "rsimone", you would specify: <userInput>https://contoso-my.sharepoint.com/personal/rsimone_contoso_com</userInput></caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src106" class="srcSentence">Because we are using the script to configure OneDrive for Business, do not change the value of <system>Documents</system> for the <codeInline>$listTitle</codeInline> variable.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src107" class="srcSentence">Search for <codeInline>ADMIN INSTRUCTIONS</codeInline>.</caps:sentence>
                                <caps:sentence id="src108" class="srcSentence"> If you make no changes to this section, the user's OneDrive for Business will be configured for IRM with the policy title of "Protected Files" and the description of "This policy restricts access to authorized users".</caps:sentence>
                                <caps:sentence id="src109" class="srcSentence">  No other IRM options will be set, which is probably appropriate for most environments.</caps:sentence>
                                <caps:sentence id="src110" class="srcSentence"> However, you can change the suggested policy title and description, and also add any other IRM options that are appropriate for your environment.</caps:sentence>
                                <caps:sentence id="src111" class="srcSentence"> See the commented example in the script to help you construct your own set of parameters for the Set-IrmConfiguration command.</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src112" class="srcSentence">Save the script and sign it.</caps:sentence>
                            <caps:sentence id="src113" class="srcSentence"> If you do not sign the script (more secure), Windows PowerShell must be configured on your computer to run unsigned scripts.</caps:sentence>
                            <caps:sentence id="src114" class="srcSentence"> To do this, run a Windows PowerShell session with the <ui>Run as Administrator</ui> option, and type: <userInput>Set-ExecutionPolicy Unrestricted</userInput>.</caps:sentence>
                            <caps:sentence id="src115" class="srcSentence"> However, this configuration lets all unsigned scripts run (less secure).</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence id="src116" class="srcSentence">For more information about signing Windows PowerShell scripts, see <externalLink><linkText>about_Signing</linkText><linkUri>https://technet.microsoft.com/library/hh847874.aspx</linkUri></externalLink> in the PowerShell documentation library.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src117" class="srcSentence">Run the script and if prompted, supply the password for the Office 365 admin account.</caps:sentence>
                            <caps:sentence id="src118" class="srcSentence"> If you modify the script and run it in the same Windows PowerShell session, you won't be prompted for credentials.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                      <alert class="tip">
                        <para>
                          <caps:sentence id="src119" class="srcSentence">You can also use this script to configure IRM for a SharePoint Online library.</caps:sentence>
                          <caps:sentence id="src120" class="srcSentence"> For this configuration, you will likely want to enable the additional option <ui>Do not allow users to upload documents that do not support IRM</ui>, to ensure that the library contains only protected documents.</caps:sentence>
                          <caps:sentence id="src121" class="srcSentence">    To do that, add the <codeInline>-IrmReject</codeInline> parameter to the Set-IrmConfiguration command in the script.</caps:sentence>
                        </para>
                        <para>
                          <caps:sentence id="src122" class="srcSentence">You would also need to modify the <codeInline>$webUrls</codeInline> variable (for example, <userInput>https://contoso.sharepoint.com</userInput>) and  <codeInline>$listTitle</codeInline> variable (for example, <userInput>$Reports</userInput>).</caps:sentence>
                        </para>
                      </alert>
                      <para>
                        <caps:sentence id="src123" class="srcSentence">If you need to disable IRM for user's OneDrive for Business libraries, expand the <link xlink:href="#BKMK_Script_OD4B_DisableIRM">Script to disable IRM for OneDrive for Business</link> section.</caps:sentence>
                      </para>
                    </content>
                    <sections>
                      <section expanded="false" address="BKMK_Script_OD4B_URLS">
                        <title>
                          <caps:sentence id="src124" class="srcSentence">Additional script to output all OneDrive for Business URLs to a .CSV file</caps:sentence>
                        </title>
                        <content>
                          <para>
                            <caps:sentence id="src125" class="srcSentence">For step 4c above, you can use the following Windows PowerShell script to extract the URLs for all users' OneDrive for Business libraries, which you can then check, edit if necessary, and then import into the main script.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence id="src126" class="srcSentence">This script also requires the <externalLink><linkText>SharePoint Online Client Components SDK</linkText><linkUri>http://www.microsoft.com/en-us/download/details.aspx?id=42038</linkUri></externalLink> and the <externalLink><linkText>SharePoint Online Management Shell</linkText><linkUri>http://www.microsoft.com/en-us/download/details.aspx?id=35588</linkUri></externalLink>.</caps:sentence>
                            <caps:sentence id="src127" class="srcSentence"> Follow the same instructions to copy and paste it, save the file locally (for example, "Report-OneDriveForBusinessSiteInfo.ps1"), modify the   <codeInline>$sharepointAdminCenterUrl</codeInline> and <codeInline>$tenantAdmin</codeInline> values as before, and then run the script.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence id="src128" class="srcSentence">
                              <legacyItalic>
                                <embeddedLabel>Disclaimer</embeddedLabel>
                              </legacyItalic>: This sample script is not supported under any Microsoft standard support program or service.</caps:sentence>
                            <caps:sentence id="src129" class="srcSentence"> This sample script is provided AS IS without warranty of any kind.</caps:sentence>
                          </para>
                          <code># Requires Windows PowerShell version 3 &lt;# Description: Queries the search service of an Office 365 tenant to retrieve all OneDrive for Business sites. Details of the discovered sites are written to a .CSV file (by default,"OneDriveForBusinessSiteInfo_&lt;date&gt;.csv"). Script Installation Requirements: SharePoint Online Client Components SDK http://www.microsoft.com/en-us/download/details.aspx?id=42038 SharePoint Online Management Shell http://www.microsoft.com/en-us/download/details.aspx?id=35588 ============================================================== #&gt; # URL will be in the format https://&lt;tenant-name&gt;-admin.sharepoint.com $sharepointAdminCenterUrl = "https://contoso-admin.sharepoint.com" $tenantAdmin = "admin@contoso.onmicrosoft.com" $reportName = "OneDriveForBusinessSiteInfo_$((Get-Date).ToString("yyyy-MM-dd_hh.mm.ss")).csv" $oneDriveForBusinessSiteUrls= @() $resultsProcessed = 0 function Load-SharePointOnlineClientComponentAssemblies { [cmdletbinding()] param() process { # assembly location: C:\Program Files\Common Files\microsoft shared\Web Server Extensions\16\ISAPI try { Write-Verbose "Loading Assembly: Microsoft.Office.Client.Policy, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" [System.Reflection.Assembly]::Load("Microsoft.Office.Client.Policy, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c") | Out-Null Write-Verbose "Loading Assembly: Microsoft.Office.Client.TranslationServices, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" [System.Reflection.Assembly]::Load("Microsoft.Office.Client.TranslationServices, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c") | Out-Null Write-Verbose "Loading Assembly: Microsoft.SharePoint.Client, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" [System.Reflection.Assembly]::Load("Microsoft.SharePoint.Client, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c") | Out-Null Write-Verbose "Loading Assembly: Microsoft.SharePoint.Client.DocumentManagement, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" [System.Reflection.Assembly]::Load("Microsoft.SharePoint.Client.DocumentManagement, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c") | Out-Null Write-Verbose "Loading Assembly: Microsoft.SharePoint.Client.Publishing, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" [System.Reflection.Assembly]::Load("Microsoft.SharePoint.Client.Publishing, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c") | Out-Null Write-Verbose "Loading Assembly: Microsoft.SharePoint.Client.Runtime, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" [System.Reflection.Assembly]::Load("Microsoft.SharePoint.Client.Runtime, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c") | Out-Null Write-Verbose "Loading Assembly: Microsoft.SharePoint.Client.Search.Applications, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" [System.Reflection.Assembly]::Load("Microsoft.SharePoint.Client.Search.Applications, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c") | Out-Null Write-Verbose "Loading Assembly: Microsoft.SharePoint.Client.Search, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" [System.Reflection.Assembly]::Load("Microsoft.SharePoint.Client.Search, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c") | Out-Null Write-Verbose "Loading Assembly: Microsoft.SharePoint.Client.Taxonomy, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" [System.Reflection.Assembly]::Load("Microsoft.SharePoint.Client.Taxonomy, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c") | Out-Null Write-Verbose "Loading Assembly: Microsoft.SharePoint.Client.UserProfiles, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" [System.Reflection.Assembly]::Load("Microsoft.SharePoint.Client.UserProfiles, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c") | Out-Null return $true } catch { if($_.Exception.Message -match "Could not load file or assembly") { Write-Error -Message "Unable to load the SharePoint Server 2013 Client Components.`nDownload Location: http://www.microsoft.com/en-us/download/details.aspx?id=42038" } else { Write-Error -Exception $_.Exception } return $false } } } function Load-SharePointOnlineModule { [cmdletbinding()] param() process { do { # Installation location: C:\Program Files\SharePoint Online Management Shell\Microsoft.Online.SharePoint.PowerShell $spoModule = Get-Module -Name Microsoft.Online.SharePoint.PowerShell -ErrorAction SilentlyContinue if(-not $spoModule) { try { Import-Module Microsoft.Online.SharePoint.PowerShell -DisableNameChecking return $true } catch { if($_.Exception.Message -match "Could not load file or assembly") { Write-Error -Message "Unable to load the SharePoint Online Management Shell.`nDownload Location: http://www.microsoft.com/en-us/download/details.aspx?id=35588" } else { Write-Error -Exception $_.Exception } return $false } } else { return $true } } while(-not $spoModule) } } function Get-CredentialFromCredentialCache { [cmdletbinding()] param([string]$CredentialName) #if( Test-Path variable:\global:CredentialCache ) if( Get-Variable O365TenantAdminCredentialCache -Scope Global -ErrorAction SilentlyContinue ) { if($global:O365TenantAdminCredentialCache.ContainsKey($CredentialName)) { Write-Verbose "Credential Cache Hit: $CredentialName" return $global:O365TenantAdminCredentialCache[$CredentialName] } } Write-Verbose "Credential Cache Miss: $CredentialName" return $null } function Add-CredentialToCredentialCache { [cmdletbinding()] param([System.Management.Automation.PSCredential]$Credential) if(-not (Get-Variable CredentialCache -Scope Global -ErrorAction SilentlyContinue)) { Write-Verbose "Initializing the Credential Cache" $global:O365TenantAdminCredentialCache = @{} } Write-Verbose "Adding Credential to the Credential Cache" $global:O365TenantAdminCredentialCache[$Credential.UserName] = $Credential } # load the required assemblies and Windows PowerShell modules if(-not ((Load-SharePointOnlineClientComponentAssemblies) -and (Load-SharePointOnlineModule)) ) { return } # Add the credentials to the client context and SharePoint Online service connection # check for cached credentials to use $o365TenantAdminCredential = Get-CredentialFromCredentialCache -CredentialName $tenantAdmin if(-not $o365TenantAdminCredential) { # when credentials are not cached, prompt for the tenant admin credentials $o365TenantAdminCredential = Get-Credential -UserName $tenantAdmin -Message "Enter the password for the Office 365 admin" if(-not $o365TenantAdminCredential -or -not $o365TenantAdminCredential.UserName -or $o365TenantAdminCredential.Password.Length -eq 0 ) { Write-Error -Message "Could not validate the supplied tenant admin credentials" return } # add the credentials to the cache Add-CredentialToCredentialCache -Credential $o365TenantAdminCredential } # establish the client context and set the credentials to connect to the site $clientContext = New-Object Microsoft.SharePoint.Client.ClientContext($sharepointAdminCenterUrl) $clientContext.Credentials = New-Object Microsoft.SharePoint.Client.SharePointOnlineCredentials($o365TenantAdminCredential.UserName, $o365TenantAdminCredential.Password) # run a query against the Office 365 tenant search service to retrieve all OneDrive for Business URLs do { # build the query object $query = New-Object Microsoft.SharePoint.Client.Search.Query.KeywordQuery($clientContext) $query.TrimDuplicates        = $false $query.RowLimit              = 500 $query.QueryText             = "SPSiteUrl:'/personal/' AND contentclass:STS_Site" $query.StartRow              = $resultsProcessed $query.TotalRowsExactMinimum = 500000 # run the query $searchExecutor = New-Object Microsoft.SharePoint.Client.Search.Query.SearchExecutor($clientContext) $queryResults = $searchExecutor.ExecuteQuery($query) $clientContext.ExecuteQuery() # enumerate the search results and store the site URLs $queryResults.Value[0].ResultRows | % { $oneDriveForBusinessSiteUrls += $_.Path $resultsProcessed++ } } while($resultsProcessed -lt $queryResults.Value.TotalRows) $oneDriveForBusinessSiteUrls | Out-File -FilePath $reportName
</code>
                        </content>
                      </section>
                      <section expanded="false" address="BKMK_Script_OD4B_DisableIRM">
                        <title>
                          <caps:sentence id="src130" class="srcSentence">Script to disable IRM for OneDrive for Business</caps:sentence>
                        </title>
                        <content>
                          <para>
                            <caps:sentence id="src131" class="srcSentence">Use the following sample script if you need to disable IRM for users' OneDrive for Business.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence id="src132" class="srcSentence">This script also requires the <externalLink><linkText>SharePoint Online Client Components SDK</linkText><linkUri>http://www.microsoft.com/en-us/download/details.aspx?id=42038</linkUri></externalLink> and the <externalLink><linkText>SharePoint Online Management Shell</linkText><linkUri>http://www.microsoft.com/en-us/download/details.aspx?id=35588</linkUri></externalLink>.</caps:sentence>
                            <caps:sentence id="src133" class="srcSentence"> Copy and paste the contents, save the file locally (for example, "Disable-IRMOnOneDriveForBusiness.ps1"), and modify the   <codeInline>$sharepointAdminCenterUrl</codeInline> and <codeInline>$tenantAdmin</codeInline> values.</caps:sentence>
                            <caps:sentence id="src134" class="srcSentence"> Manually specify the OneDrive for Business URLs or use the script in the previous section so that you can import these, and then run the script.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence id="src135" class="srcSentence">
                              <legacyItalic>
                                <embeddedLabel>Disclaimer</embeddedLabel>
                              </legacyItalic>: This sample script is not supported under any Microsoft standard support program or service.</caps:sentence>
                            <caps:sentence id="src136" class="srcSentence"> This sample script is provided AS IS without warranty of any kind.</caps:sentence>
                          </para>
                          <code># Requires Windows PowerShell version 3 &lt;# Description: Disables IRM for OneDrive for Business and can also be used for SharePoint Online libraries and lists Script Installation Requirements: SharePoint Online Client Components SDK http://www.microsoft.com/en-us/download/details.aspx?id=42038 SharePoint Online Management Shell http://www.microsoft.com/en-us/download/details.aspx?id=35588 ============================================================== #&gt; $sharepointAdminCenterUrl = "https://contoso-admin.sharepoint.com" $tenantAdmin = "admin@contoso.com" $webUrls = @("https://contoso-my.sharepoint.com/personal/user1_contoso_com", "https://contoso-my.sharepoint.com/personal/user2_contoso_com", "https://contoso-my.sharepoint.com/personal/person3_contoso_com") &lt;# As an alternative to specifying the URLs as an array, you can import them from a CSV file (no header, single value per row). Then, use: $webUrls = Get-Content -Path "File_path_and_name.csv" #&gt; $listTitle = "Documents" function Load-SharePointOnlineClientComponentAssemblies { [cmdletbinding()] param() process { # assembly location: C:\Program Files\Common Files\microsoft shared\Web Server Extensions\16\ISAPI try { Write-Verbose "Loading Assembly: Microsoft.Office.Client.Policy, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" [System.Reflection.Assembly]::Load("Microsoft.Office.Client.Policy, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c") | Out-Null Write-Verbose "Loading Assembly: Microsoft.Office.Client.TranslationServices, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" [System.Reflection.Assembly]::Load("Microsoft.Office.Client.TranslationServices, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c") | Out-Null Write-Verbose "Loading Assembly: Microsoft.SharePoint.Client, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" [System.Reflection.Assembly]::Load("Microsoft.SharePoint.Client, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c") | Out-Null Write-Verbose "Loading Assembly: Microsoft.SharePoint.Client.DocumentManagement, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" [System.Reflection.Assembly]::Load("Microsoft.SharePoint.Client.DocumentManagement, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c") | Out-Null Write-Verbose "Loading Assembly: Microsoft.SharePoint.Client.Publishing, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" [System.Reflection.Assembly]::Load("Microsoft.SharePoint.Client.Publishing, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c") | Out-Null Write-Verbose "Loading Assembly: Microsoft.SharePoint.Client.Runtime, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" [System.Reflection.Assembly]::Load("Microsoft.SharePoint.Client.Runtime, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c") | Out-Null Write-Verbose "Loading Assembly: Microsoft.SharePoint.Client.Search.Applications, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" [System.Reflection.Assembly]::Load("Microsoft.SharePoint.Client.Search.Applications, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c") | Out-Null Write-Verbose "Loading Assembly: Microsoft.SharePoint.Client.Search, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" [System.Reflection.Assembly]::Load("Microsoft.SharePoint.Client.Search, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c") | Out-Null Write-Verbose "Loading Assembly: Microsoft.SharePoint.Client.Taxonomy, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" [System.Reflection.Assembly]::Load("Microsoft.SharePoint.Client.Taxonomy, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c") | Out-Null Write-Verbose "Loading Assembly: Microsoft.SharePoint.Client.UserProfiles, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" [System.Reflection.Assembly]::Load("Microsoft.SharePoint.Client.UserProfiles, Version=16.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c") | Out-Null return $true } catch { if($_.Exception.Message -match "Could not load file or assembly") { Write-Error -Message "Unable to load the SharePoint Server 2013 Client Components.`nDownload Location: http://www.microsoft.com/en-us/download/details.aspx?id=42038" } else { Write-Error -Exception $_.Exception } return $false } } } function Load-SharePointOnlineModule { [cmdletbinding()] param() process { do { # Installation location: C:\Program Files\SharePoint Online Management Shell\Microsoft.Online.SharePoint.PowerShell $spoModule = Get-Module -Name Microsoft.Online.SharePoint.PowerShell -ErrorAction SilentlyContinue if(-not $spoModule) { try { Import-Module Microsoft.Online.SharePoint.PowerShell -DisableNameChecking return $true } catch { if($_.Exception.Message -match "Could not load file or assembly") { Write-Error -Message "Unable to load the SharePoint Online Management Shell.`nDownload Location: http://www.microsoft.com/en-us/download/details.aspx?id=35588" } else { Write-Error -Exception $_.Exception } return $false } } else { return $true } } while(-not $spoModule) } } function Remove-IrmConfiguration { [cmdletbinding()] param( [parameter(Mandatory=$true)][Microsoft.SharePoint.Client.List]$List ) process { Write-Verbose "Disabling IRM Configuration on '$($List.Title)'" $List.IrmEnabled = $false $List.IrmExpire  = $false $List.IrmReject  = $false $List.InformationRightsManagementSettings.Reset() } end { if($List) { Write-Verbose "Committing IRM configuration settings on '$($list.Title)'" $list.InformationRightsManagementSettings.Update() $list.Update() $script:clientContext.Load($list) $script:clientContext.ExecuteQuery() } } } function Get-CredentialFromCredentialCache { [cmdletbinding()] param([string]$CredentialName) #if( Test-Path variable:\global:CredentialCache ) if( Get-Variable O365TenantAdminCredentialCache -Scope Global -ErrorAction SilentlyContinue ) { if($global:O365TenantAdminCredentialCache.ContainsKey($CredentialName)) { Write-Verbose "Credential Cache Hit: $CredentialName" return $global:O365TenantAdminCredentialCache[$CredentialName] } } Write-Verbose "Credential Cache Miss: $CredentialName" return $null } function Add-CredentialToCredentialCache { [cmdletbinding()] param([System.Management.Automation.PSCredential]$Credential) if(-not (Get-Variable CredentialCache -Scope Global -ErrorAction SilentlyContinue)) { Write-Verbose "Initializing the Credential Cache" $global:O365TenantAdminCredentialCache = @{} } Write-Verbose "Adding Credential to the Credential Cache" $global:O365TenantAdminCredentialCache[$Credential.UserName] = $Credential } # load the required assemblies and Windows PowerShell modules if(-not ((Load-SharePointOnlineClientComponentAssemblies) -and (Load-SharePointOnlineModule)) ) { return } # Add the credentials to the client context and SharePoint Online service connection # check for cached credentials to use $o365TenantAdminCredential = Get-CredentialFromCredentialCache -CredentialName $tenantAdmin if(-not $o365TenantAdminCredential) { # when credentials are not cached, prompt for the tenant admin credentials $o365TenantAdminCredential = Get-Credential -UserName $tenantAdmin -Message "Enter the password for the Office 365 admin" if(-not $o365TenantAdminCredential -or -not $o365TenantAdminCredential.UserName -or $o365TenantAdminCredential.Password.Length -eq 0 ) { Write-Error -Message "Could not validate the supplied tenant admin credentials" return } # add the credentials to the cache Add-CredentialToCredentialCache -Credential $o365TenantAdminCredential } # connect to Office365 first, required for SharePoint Online cmdlets to run Connect-SPOService -Url $sharepointAdminCenterUrl -Credential $o365TenantAdminCredential # enumerate each of the specified site URLs foreach($webUrl in $webUrls) { $grantedSiteCollectionAdmin = $false try { # establish the client context and set the credentials to connect to the site $script:clientContext = New-Object Microsoft.SharePoint.Client.ClientContext($webUrl) $script:clientContext.Credentials = New-Object Microsoft.SharePoint.Client.SharePointOnlineCredentials($o365TenantAdminCredential.UserName, $o365TenantAdminCredential.Password) # initialize the site and web context $script:clientContext.Load($script:clientContext.Site) $script:clientContext.Load($script:clientContext.Web) $script:clientContext.ExecuteQuery() # load and ensure the tenant admin user account if present on the target SharePoint site $tenantAdminUser = $script:clientContext.Web.EnsureUser($o365TenantAdminCredential.UserName) $script:clientContext.Load($tenantAdminUser) $script:clientContext.ExecuteQuery() # check if the tenant admin is a site admin if( -not $tenantAdminUser.IsSiteAdmin ) { try { # grant the tenant admin temporary admin rights to the site collection Set-SPOUser -Site $script:clientContext.Site.Url -LoginName $o365TenantAdminCredential.UserName -IsSiteCollectionAdmin $true | Out-Null $grantedSiteCollectionAdmin = $true } catch { Write-Error $_.Exception return } } try { # load the list orlibrary using CSOM $list = $null $list = $script:clientContext.Web.Lists.GetByTitle($listTitle) $script:clientContext.Load($list) $script:clientContext.ExecuteQuery() Remove-IrmConfiguration -List $list } catch { Write-Error -Message "Error setting IRM configuration on site: $webUrl.`nError Details: $($_.Exception.ToString())" } } finally { if($grantedSiteCollectionAdmin) { # remove the temporary admin rights to the site collection Set-SPOUser -Site $script:clientContext.Site.Url -LoginName $o365TenantAdminCredential.UserName -IsSiteCollectionAdmin $false | Out-Null } } } Disconnect-SPOService -ErrorAction SilentlyContinue
</code>
                        </content>
                      </section>
                    </sections>
                  </section>
                </sections>
              </section>
            </sections>
          </section>
        </sections>
      </section>
      <section address="BKMK_Office2013Configuration">
        <title>
          <caps:sentence id="src137" class="srcSentence">Office 2016 and Office 2013: Configuration for clients</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src138" class="srcSentence">Because these later versions of Office  natively support Azure RMS, no client computer configuration is required to support the information rights management (IRM) features for applications such as Word, Excel, PowerPoint, Outlook and the Outlook Web App.</caps:sentence>
            <caps:sentence id="src139" class="srcSentence"> All users have to do is sign in to their Office applications with their <token>o365_1</token> credentials and they can protect files and emails, and use files and emails that have been protected by others.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src140" class="srcSentence">However, we recommend that you supplement these applications with the Rights Management sharing application, so that users get the benefit of the Office add-in.</caps:sentence>
            <caps:sentence id="src141" class="srcSentence"> For more information, see the <link xlink:href="ea09cbc5-b98b-444e-8b60-5bc3cb199c36#BKMK_SharingApp">Rights Management sharing application: Installation and configuration for clients</link> section in this topic.</caps:sentence>
          </para>
        </content>
      </section>
      <section address="BKMK_Office2010Configuration">
        <title>
          <caps:sentence id="src142" class="srcSentence">Office 2010: Configuration for clients</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src143" class="srcSentence">For client computers to use Azure RMS with Office 2010, they must have installed the Rights Management sharing application for Windows.</caps:sentence>
            <caps:sentence id="src144" class="srcSentence"> No further configuration is required other than users must sign in with their <token>o365_1</token> credentials and they can then protect files and use files that have been protected by others.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src145" class="srcSentence">For more information about the Rights Management sharing application, see the <link xlink:href="ea09cbc5-b98b-444e-8b60-5bc3cb199c36#BKMK_SharingApp">Rights Management sharing application: Installation and configuration for clients</link> section in this topic.</caps:sentence>
          </para>
        </content>
      </section>
      <section address="BKMK_SharingApp">
        <title>
          <caps:sentence id="src146" class="srcSentence">Rights Management sharing application: Installation and configuration for clients</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src147" class="srcSentence">The Rights Management (RMS) sharing application is required for client computers to use Azure RMS with Office 2010, and recommended for all computers and mobile devices that support Azure RMS.</caps:sentence>
            <caps:sentence id="src148" class="srcSentence"> The RMS sharing application integrates with Office applications by installing an Office add-in so that users can easily protect files and emails directly from the ribbon.</caps:sentence>
            <caps:sentence id="src149" class="srcSentence"> It also offers generic protection for files types that are not natively supported by Azure RMS, and a document tracking site for users to track and revoke files that they have protected.</caps:sentence>
          </para>
        </content>
        <sections>
          <section address="BKMK_SharingAppforWindows" expanded="false">
            <title>
              <caps:sentence id="src150" class="srcSentence">The RMS sharing application for Windows: Installation and configuration</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src151" class="srcSentence">To install and configure the RMS sharing application for Windows for an enterprise deployment, see the <externalLink><linkText>Rights Management sharing application administrator guide</linkText><linkUri>http://technet.microsoft.com/library/dn339003.aspx</linkUri></externalLink>.</caps:sentence>
              </para>
              <alert class="tip">
                <para>
                  <caps:sentence id="src152" class="srcSentence">If you want to quickly install and test the RMS sharing application for a single computer, see <externalLink><linkText>Download and install the Rights Management sharing application</linkText><linkUri>http://technet.microsoft.com/library/dn574734.aspx</linkUri></externalLink> from the <externalLink><linkText>Rights Management sharing application user guide</linkText><linkUri>http://technet.microsoft.com/library/dn339006.aspx</linkUri></externalLink>.</caps:sentence>
                </para>
              </alert>
            </content>
          </section>
          <section address="BKMK_SharingAppMovileDevices" expanded="false">
            <title>
              <caps:sentence id="src153" class="srcSentence">The RMS sharing application for mobile platforms: Installation</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src154" class="srcSentence">To install the RMS sharing application for mobile platforms, you can download the relevant app by using the links on the <externalLink><linkText>Microsoft Rights Management page</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=303970</linkUri></externalLink>.</caps:sentence>
                <caps:sentence id="src155" class="srcSentence"> No configuration is required to use Azure RMS with this app.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </section>
      <section address="BKMK_RMSAPIs">
        <title>
          <caps:sentence id="src156" class="srcSentence">Other applications that support the RMS APIs: Installation and configuration</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src157" class="srcSentence">This category includes line-of-business applications that are written in-house by using the RMS SDK, and applications from software vendors that are written by using the RMS SDK.</caps:sentence>
            <caps:sentence id="src158" class="srcSentence"> For these applications, follow the instructions that are provided with the application.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src159" class="srcSentence">Next steps</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src160" class="srcSentence">After you’ve configured your applications to support Azure Rights Management, use the <link xlink:href="086600c2-c5d8-47ec-a4c0-c782e1797486">Azure Rights Management Deployment Roadmap</link> to check whether there are other configuration steps that you might want to do before you roll out <token>aad_rightsmanagement_1</token> to users and administrators.</caps:sentence>
            <caps:sentence id="src161" class="srcSentence"> If not, see <link xlink:href="18564e4a-9364-4ed2-8f17-89d24fc0d878">Using Azure Rights Management</link> for your next steps.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="206a0bfe-0912-4e0e-aa15-484b000b264c">Configuring rights management</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>