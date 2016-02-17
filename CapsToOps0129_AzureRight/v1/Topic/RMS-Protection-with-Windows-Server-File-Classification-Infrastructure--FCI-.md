---
title: Protecci&#243;n de RMS con la infraestructura de clasificaci&#243;n de archivos (FCI) de Windows Server
ms.custom: na
ms.reviewer: na
ms.service: rights-management
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9aa693db-9727-4284-9f64-867681e114c9
---
# Protecci&#243;n de RMS con la infraestructura de clasificaci&#243;n de archivos (FCI) de Windows Server
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="es-ES">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xlink="http://www.w3.org/1999/xlink">
      <introduction>
        <para>
          <caps:sentence sentenceid="f1978bfefaaf68d08811f06c777ef26a" id="tgt1" class="tgtSentence">Use este artículo para obtener instrucciones y un script para utilizar el cliente de Rights Management (RMS) con la herramienta de protección de RMS para configurar el Administrador de recursos del servidor de archivos y la infraestructura de clasificación de archivos (FCI).</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="653ebb8f23b36d8614d145b7fbf37ebf" id="tgt2" class="tgtSentence">Esta solución le permite proteger automáticamente todos los archivos en una carpeta de un servidor de archivos que ejecuta Windows Server o bien proteger automáticamente archivos que cumplen criterios específicos.</caps:sentence>
          <caps:sentence sentenceid="e221f1826b69d3ed7c5485e237e7a73d" id="tgt3" class="tgtSentence"> Por ejemplo, los archivos que se han clasificado como poseedores de información confidencial.</caps:sentence>
          <caps:sentence sentenceid="480e05529df3cb57a6ef08bf1f047b04" id="tgt4" class="tgtSentence"> Esta solución usa <link xlink:href="965581c8-be3c-43b4-8145-5cefd29c7636">Azure Rights Management</link> (Azure RMS) para proteger los archivos, de modo que debe tener esta tecnología implementada en su organización.</caps:sentence>
        </para>
        <alert class="note">
          <para>
            <caps:sentence sentenceid="98c3cfe05c5d2b12c850f38222d50191" id="tgt5" class="tgtSentence">Aunque Azure RMS incluye un <externalLink><linkText>conector</linkText><linkUri>https://technet.microsoft.com/library/dn375964.aspx</linkUri></externalLink> que admite la infraestructura de clasificación de archivos, dicha solución admite solo la protección nativa (por ejemplo, archivos de Office).</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="260e09019810550b7661e136156d9c3b" id="tgt6" class="tgtSentence">Para admitir todos los tipos de archivo con infraestructura de clasificación de archivos, debe usar el módulo <embeddedLabel>Protección de RMS</embeddedLabel> de Windows PowerShell, tal como se describe en este artículo.</caps:sentence>
            <caps:sentence sentenceid="e823c60f1362932c2ce00601d65c79ab" id="tgt7" class="tgtSentence"> Los cmdlets de protección de RMS, al igual que la aplicación de uso compartido de RMS, admite protección genérica, así como protección nativa, lo que significa que se pueden proteger todos los archivos.</caps:sentence>
            <caps:sentence sentenceid="9034fbbdd49b2280db4600cb9deb2ebe" id="tgt8" class="tgtSentence"> Para obtener más información acerca de todos estos niveles de protección, consulte la sección <link xlink:href="d9992e30-f3d1-48d5-aedc-4e721f7d7c25#BKMK_LevelsofProtection">Levels of protection – native and generic</link> en <link xlink:href="d9992e30-f3d1-48d5-aedc-4e721f7d7c25">Rights Management sharing application administrator guide</link>.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence sentenceid="0e4dfdfcc53d4854ed8aa2afdc2808bc" id="tgt9" class="tgtSentence">Las instrucciones siguientes sirven para Windows Server 2012 R2 o Windows Server 2012.</caps:sentence>
          <caps:sentence sentenceid="9ab7e37c03597a5b82a10ff992b9b856" id="tgt10" class="tgtSentence"> Si ejecuta otras versiones compatibles de Windows, es posible que tenga que adaptar algunos de los pasos por las diferencias entre la versión de su sistema operativo y la descrita en este artículo.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="d2299eac7d6a85ce258d812a93eb0211" id="tgt11" class="tgtSentence">Requisitos previos de la protección de Azure RMS con FCI de Windows Server</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="a509e6aa075b304ea8281efc81ac0ca0" id="tgt12" class="tgtSentence">Requisitos previos de estas instrucciones: </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="7b9332077fc5a4a5185c4512a2bf0298" id="tgt13" class="tgtSentence">En cada servidor de archivos donde ejecutará el Administrador de recursos de archivos con la infraestructura de clasificación de archivos:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="f0839a1ed9dc5f1a517671fa5ac764b7" id="tgt14" class="tgtSentence">Ha instalado el Administrador de recursos del servidor de archivos como uno de los servicios de rol para el rol Servicios de archivo.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="a42b827e9e14dd0546967b455c388054" id="tgt15" class="tgtSentence">Ha identificado una carpeta local que contiene archivos para proteger con Rights Management.</caps:sentence>
                    <caps:sentence sentenceid="c9fa4ea43829158ecc6e3ab421fb48b4" id="tgt16" class="tgtSentence"> Por ejemplo, C:\FileShare.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="21315f242952866769c2fae95ab81c05" id="tgt17" class="tgtSentence">Ha instalado la herramienta de protección de RMS, incluidos los requisitos previos de la herramienta (como el cliente RMS) y de Azure RMS (como la cuenta principal de servicio).</caps:sentence>
                    <caps:sentence sentenceid="1070f425823a6e05a98eb2d747f0c53d" id="tgt18" class="tgtSentence"> Para obtener más información, consulte <externalLink><linkText>Cmdlets de protección de RMS</linkText><linkUri>https://msdn.microsoft.com/library/azure/mt433195.aspx</linkUri></externalLink>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="d16139385a2964e8c8f4fef6a9a769ec" id="tgt19" class="tgtSentence">Si desea cambiar el nivel predeterminado de protección de RMS (nativo o genérico) para las extensiones de nombre de archivo específicas, ha editado el registro como se describe en la página <externalLink><linkText>Configuración de API de archivo</linkText><linkUri>https://msdn.microsoft.com/library/dn197834(v=vs.85).aspx</linkUri></externalLink>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="e02d660051081660e1c0d6e5c2d0cbf3" id="tgt20" class="tgtSentence">Tiene conexión a Internet, con los ajustes del equipo configurados si es necesario para un servidor proxy.</caps:sentence>
                    <caps:sentence sentenceid="407e8379b5443b7c0092c35c8bab7f29" id="tgt21" class="tgtSentence"> Por ejemplo: <codeInline>netsh winhttp import proxy source=ie</codeInline></caps:sentence>
                  </para>
                </listItem>
              </list>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="81cdf8b2a561660d033462b3c9d7e450" id="tgt22" class="tgtSentence">Ha configurado los requisitos previos adicionales de la implementación de Azure Rights Management, como se describe en <externalLink><linkText>about_RMSProtection_AzureRMS</linkText><linkUri>https://msdn.microsoft.com/library/mt433202.aspx</linkUri></externalLink>.</caps:sentence>
                <caps:sentence sentenceid="cd9e861b4d93ba46f1992374b597528c" id="tgt23" class="tgtSentence"> En concreto, tiene los siguientes valores para conectarse a Azure RMS mediante el uso de una entidad de servicio:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="8dda7f4712571824366f949a7b331480" id="tgt24" class="tgtSentence">BposTenantId</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="e77cd3164d0bd728c19df766001d0d79" id="tgt25" class="tgtSentence">AppPrincipalId</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="ed923d237ad88bd3bd9639039a77853a" id="tgt26" class="tgtSentence">Clave simétrica</caps:sentence>
                  </para>
                </listItem>
              </list>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="ea6fe3b8f532cc6d367ab83c34311d9b" id="tgt27" class="tgtSentence">Ha sincronizado sus cuentas de usuario de Active Directory locales con Azure Active Directory u Office 365, incluyendo su dirección de correo electrónico.</caps:sentence>
                <caps:sentence sentenceid="52500c333d674e3d392bc819ecf395b6" id="tgt28" class="tgtSentence"> Esto es necesario para todos los usuarios que puedan necesitar acceder a los archivos después de que FCI y Azure RMS los hayan protegido.</caps:sentence>
                <caps:sentence sentenceid="84150f76dba6d6c067d048c2fbe0e085" id="tgt29" class="tgtSentence"> Si no realiza este paso (por ejemplo, en un entorno de prueba), existe la posibilidad de que se bloquee el acceso de los usuarios a estos archivos.</caps:sentence>
                <caps:sentence sentenceid="457e0843ac4e5c6a5f1767f11e2b5ee2" id="tgt30" class="tgtSentence"> Si necesita más información sobre la configuración de esta cuenta, consulte <link xlink:href="afbca2d6-32a7-4bda-8aaf-9f93f5da5abc">Preparing for Azure Rights Management</link>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="08a3e8e995845f2b31e8f8b03f81cf22" id="tgt31" class="tgtSentence">Ha identificado la plantilla Rights Management para su utilización, que protegerá los archivos.</caps:sentence>
                <caps:sentence sentenceid="203377d9d70dbecef91db9de38462857" id="tgt32" class="tgtSentence"> Asegúrese de que conoce el identificador de esta plantilla usando el cmdlet <externalLink><linkText>Get-RMSTemplate</linkText><linkUri>https://msdn.microsoft.com/library/azure/mt433197.aspx</linkUri></externalLink>.</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="d15dedc49509d0cb5aecc51c563f2ea5" id="tgt33" class="tgtSentence">Instrucciones para configurar FCI del Administrador de recursos del servidor de archivos para la protección de Azure RMS </caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="0b51fd69cbc78d9921f7bed015eef54f" id="tgt34" class="tgtSentence">Siga estas instrucciones para proteger automáticamente todos los archivos en una carpeta mediante un script de Windows PowerShell como una tarea personalizada.</caps:sentence>
            <caps:sentence sentenceid="018f86b2f112666121b038e73ad029ca" id="tgt35" class="tgtSentence"> Lleve a cabo estos procedimientos en este orden:</caps:sentence>
          </para>
          <list class="ordered">
            <listItem>
              <para>
                <caps:sentence sentenceid="235fefb02b544dd883d399238b405b4a" id="tgt36" class="tgtSentence">Guardar el script de Windows PowerShell</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="fb3ae979ef63d5c42e7ef8e52ba5d833" id="tgt37" class="tgtSentence">Crear una propiedad de clasificación para Rights Management (RMS)</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="1a2496a9ed68e322aec986295f6517c4" id="tgt38" class="tgtSentence">Crear una regla de clasificación (clasificar para RMS)</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="df57e97ebf4f7ef4ad475c132db39f5f" id="tgt39" class="tgtSentence">Configurar la programación de clasificación</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="e885d131972edd81cda09b5d5accd1e9" id="tgt40" class="tgtSentence">Crear una tarea de administración de archivos personalizada (proteger los archivos con RMS)</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="1ff4133565bf3c38a3b244616a4fa588" id="tgt41" class="tgtSentence">Probar la configuración ejecutando manualmente la regla y la tarea</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="b390fa11a33d3962df60ff118a95ba3b" id="tgt42" class="tgtSentence">Al final de estas instrucciones, todos los archivos de su carpeta seleccionada se clasificarán con la propiedad personalizada de RMS y, a continuación, Rights Management protegerá estos archivos.</caps:sentence>
            <caps:sentence sentenceid="ef5bbdc828207c921d1b8caa55d8f262" id="tgt43" class="tgtSentence"> Para una configuración más compleja que protege de forma selectiva algunos archivos y no otros, puede crear o usar una regla y una propiedad de clasificación diferentes con una tarea de administración de archivos que protege solo esos archivos.</caps:sentence>
          </para>
          <procedure>
            <title>
              <caps:sentence sentenceid="235fefb02b544dd883d399238b405b4a" id="tgt44" class="tgtSentence">Guardar el script de Windows PowerShell</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="fdcc4fa280e08d732d92c3b912f16628" id="tgt45" class="tgtSentence">Expanda la sección <link xlink:href="#BKMK_RMSProtection_Script">Windows PowerShell Script</link> de este artículo y copie su contenido.</caps:sentence>
                    <caps:sentence sentenceid="a7317d46b59dd03d06a948ecbf05daf9" id="tgt46" class="tgtSentence"> Pegue el contenido del script y ponga al archivo el nombre <system>RMS-Protect-FCI.ps1</system> en su propio equipo.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="3e5c8bfb50e79b38e3ce2e66ac8ccff9" id="tgt47" class="tgtSentence">Revise el script y realice los cambios siguientes:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="0877026490683b13351acf65902eeead" id="tgt48" class="tgtSentence">Busque la siguiente cadena y reemplácela por su propio AppPrincipalId, que utiliza con el cmdlet <externalLink><linkText>Set-RMSServerAuthentication</linkText><linkUri>https://msdn.microsoft.com/library/mt433199.aspx</linkUri></externalLink> para conectarse a Azure RMS:</caps:sentence>
                      </para>
                      <code>&lt;enter your AppPrincipalId here&gt;</code>
                      <para>
                        <caps:sentence sentenceid="e2b35422e18254a04dc723c6a0a240fc" id="tgt49" class="tgtSentence">Por ejemplo, es posible que el script tenga el aspecto siguiente:</caps:sentence>
                      </para>
                      <para>
                        <codeInline>[Parameter(Mandatory = $false)]
            </codeInline>
                      </para>
                      <para>
                        <codeInline>[Parameter(Mandatory = $false)] [string]$AppPrincipalId = "b5e3f76a-b5c2-4c96-a594-a0807f65bba4",</codeInline>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="c56f6fc6d0f40cc82c9831e3a0b9c840" id="tgt50" class="tgtSentence">Busque la siguiente cadena y reemplácela por su propia clave simétrica, que utiliza con el cmdlet <externalLink><linkText>Set-RMSServerAuthentication</linkText><linkUri>https://msdn.microsoft.com/library/mt433199.aspx</linkUri></externalLink> para conectarse a Azure RMS:</caps:sentence>
                      </para>
                      <code>&lt;enter your key here&gt;</code>
                      <para>
                        <caps:sentence sentenceid="e2b35422e18254a04dc723c6a0a240fc" id="tgt51" class="tgtSentence">Por ejemplo, es posible que el script tenga el aspecto siguiente:</caps:sentence>
                      </para>
                      <para>
                        <codeInline>[Parameter(Mandatory = $false)]
            </codeInline>
                      </para>
                      <para>
                        <codeInline>[string]$SymmetricKey = "zIeMu8zNJ6U377CLtppkhkbl4gjodmYSXUVwAO5ycgA="</codeInline>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="7a720d32fce2c7be139ed51ee40aa6c1" id="tgt52" class="tgtSentence">Busque la siguiente cadena y reemplácela por su propio BposTenantId (identificador de inquilino), que utiliza con el cmdlet <externalLink><linkText>Set-RMSServerAuthentication</linkText><linkUri>https://msdn.microsoft.com/library/mt433199.aspx</linkUri></externalLink> para conectarse a Azure RMS:</caps:sentence>
                      </para>
                      <code>&lt;enter your BposTenantId here&gt;</code>
                      <para>
                        <caps:sentence sentenceid="e2b35422e18254a04dc723c6a0a240fc" id="tgt53" class="tgtSentence">Por ejemplo, es posible que el script tenga el aspecto siguiente:</caps:sentence>
                      </para>
                      <para>
                        <codeInline>[Parameter(Mandatory = $false)]
            </codeInline>
                      </para>
                      <para>
                        <codeInline>[string]$BposTenantId = "23976bc6-dcd4-4173-9d96-dad1f48efd42",</codeInline>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="ada294e5218bd88593a76c89f35f7268" id="tgt54" class="tgtSentence">Si su servidor ejecuta Windows Server 2012, es posible que tenga que cargar manualmente el módulo RMSProtection al principio del script.</caps:sentence>
                        <caps:sentence sentenceid="920b2fee2658e46a351a921675fe5533" id="tgt55" class="tgtSentence"> Agregue el siguiente comando (o equivalente si la carpeta "Archivos de programa" está en una unidad distinta de la unidad C:</caps:sentence>
                      </para>
                      <code>Import-Module "C:\Program Files\WindowsPowerShell\Modules\RMSProtection\RMSProtection.dll"</code>
                    </listItem>
                  </list>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="4651b11b80347d39d69638158f8d33e6" id="tgt56" class="tgtSentence">Firme el script.</caps:sentence>
                    <caps:sentence sentenceid="f047e948670a398b6c2f4e029b3636dd" id="tgt57" class="tgtSentence"> Si no firma el script (más seguro), debe configurar Windows PowerShell en los servidores que lo ejecutan.</caps:sentence>
                    <caps:sentence sentenceid="f21f2d18bac473499f5df04fe824e43f" id="tgt58" class="tgtSentence"> Por ejemplo, ejecute una sesión de Windows PowerShell mediante la opción <ui>Ejecutar como administrador</ui> y escriba: <userInput>Set-ExecutionPolicy sin restricciones</userInput>.</caps:sentence>
                    <caps:sentence sentenceid="60745ffc42a2b47c904074b0c30d8868" id="tgt59" class="tgtSentence"> Sin embargo, esta configuración permite la ejecución de todos los scripts sin firmar (menos seguro).</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="bdb735148f45a643cc3c943abf34cbd6" id="tgt60" class="tgtSentence">Para obtener más información acerca de la firma de scripts de Windows PowerShell, consulte <externalLink><linkText>about_Signing</linkText><linkUri>https://technet.microsoft.com/library/hh847874.aspx</linkUri></externalLink> en la biblioteca de documentación de PowerShell.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="2a8d7bd94d42105122416d2be2f945d9" id="tgt61" class="tgtSentence">Guarde el archivo localmente en cada servidor de archivos que ejecute el Administrador de recursos de archivos con la infraestructura de clasificación de archivos.</caps:sentence>
                    <caps:sentence sentenceid="380c4475b301f142acdfdd11f7dd8cd6" id="tgt62" class="tgtSentence"> Por ejemplo, guarde el archivo en <system>C:\RMS-Protection</system>.</caps:sentence>
                    <caps:sentence sentenceid="8c7b927903537e8566202741e49e37a5" id="tgt63" class="tgtSentence"> Proteja este archivo mediante permisos NTFS para que los usuarios no autorizados no puedan modificarlo.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence sentenceid="1e900b76654e8ece4cb397b21023398b" id="tgt64" class="tgtSentence">Ahora está listo para empezar a configurar el Administrador de recursos del servidor de archivos.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
          <procedure>
            <title>
              <caps:sentence sentenceid="fb3ae979ef63d5c42e7ef8e52ba5d833" id="tgt65" class="tgtSentence">Crear una propiedad de clasificación para Rights Management (RMS)</caps:sentence>
            </title>
            <steps class="bullet">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="3e6c1f60d0ceabf3769f30946c89ca39" id="tgt66" class="tgtSentence">En el Administrador de recursos del servidor de archivos, en Administración de clasificaciones, cree una nueva propiedad local:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="fef8d1696dea20a8cd2a8b759e74a3f1" id="tgt67" class="tgtSentence">
                          <ui>Nombre</ui>: Escribir <userInput>RMS</userInput></caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="48d653e215605a52408d563e79974d09" id="tgt68" class="tgtSentence">
                          <ui>Descripción</ui>:   Escribir <userInput>protección de Rights Management</userInput></caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="4281ddfd144e2840410d083f59f98edc" id="tgt69" class="tgtSentence">
                          <ui>Tipo de propiedad</ui>: Seleccionar <ui>Sí/No</ui></caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="4281ddfd144e2840410d083f59f98edc" id="tgt70" class="tgtSentence">
                          <ui>Valor</ui>: Seleccionar <ui>Sí</ui></caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence sentenceid="ee3ca119563033e02f441bb12b150cdc" id="tgt71" class="tgtSentence">Ahora podemos crear una regla de clasificación que usa esta propiedad.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
          <procedure>
            <title>
              <caps:sentence sentenceid="1a2496a9ed68e322aec986295f6517c4" id="tgt72" class="tgtSentence">Crear una regla de clasificación (clasificar para RMS)</caps:sentence>
            </title>
            <steps class="bullet">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="9863137161f6f630639c1ea9dad3314e" id="tgt73" class="tgtSentence">Cree una nueva regla de clasificación:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt74" class="tgtSentence">En la pestaña <ui>General</ui>:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="651df6c9203f03052cbec366476e7ae2" id="tgt75" class="tgtSentence">
                              <ui>Nombre</ui>: Escribir<userInput> Clasificar para RMS</userInput></caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="5d3b307b3b4b75d45e97dfb1b4bb6ad5" id="tgt76" class="tgtSentence">
                              <ui>Habilitado</ui>: Mantenga el valor predeterminado, que es por lo que esta casilla de verificación está seleccionada.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="fef8d1696dea20a8cd2a8b759e74a3f1" id="tgt77" class="tgtSentence">
                              <ui>Descripción</ui>: Escriba <userInput>Clasificar todos los archivos en la carpeta &lt;nombre de carpeta&gt; para Rights Management</userInput>.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence sentenceid="05d18373e30d5a4c6a58e6f3b2e3e7ab" id="tgt78" class="tgtSentence">Reemplace <placeholder>&lt;nombre de carpeta&gt;</placeholder> por su nombre elegido para la carpeta.</caps:sentence>
                            <caps:sentence sentenceid="4eee3758f1bf4073d94deae936dd0a13" id="tgt79" class="tgtSentence"> Por ejemplo, <ui>Clasificar todos los archivos en la carpeta C:\FileShare para Rights Management</ui></caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="c94ad9bb0714a5540c5b79ec72c3c04b" id="tgt80" class="tgtSentence">
                              <ui>Ámbito</ui>: Agregue su carpeta elegida.</caps:sentence>
                            <caps:sentence sentenceid="4eee3758f1bf4073d94deae936dd0a13" id="tgt81" class="tgtSentence"> Por ejemplo, <ui>C:\FileShare</ui>.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence sentenceid="24e121b32086c6d0a2f7a65edf0fa704" id="tgt82" class="tgtSentence">No seleccione las casillas de verificación.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt83" class="tgtSentence">En la pestaña <ui>Clasificación</ui>:</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="4281ddfd144e2840410d083f59f98edc" id="tgt84" class="tgtSentence">
                          <ui>Método de clasificación</ui>: Seleccionar <ui>Clasificador de carpetas</ui></caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="fdc0fcd4332187a47e6a86c3698c11b7" id="tgt85" class="tgtSentence">Nombre de <ui>propiedad</ui>: Seleccionar <ui>RMS</ui></caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="5d9025399a7d70af989cb67b959d50fc" id="tgt86" class="tgtSentence">
                          <ui>Valor</ui> de la propiedad: Seleccionar <ui>Sí</ui></caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence sentenceid="957b5d660fe24ad385e2973b1846acd0" id="tgt87" class="tgtSentence">Aunque puede ejecutar las reglas de clasificación manualmente, para las operaciones en curso, deseará que esta regla se ejecute en una programación de modo que los nuevos archivos se clasifiquen con la propiedad RMS.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
          <procedure>
            <title>
              <caps:sentence sentenceid="df57e97ebf4f7ef4ad475c132db39f5f" id="tgt88" class="tgtSentence">Configurar la programación de clasificación</caps:sentence>
            </title>
            <steps class="bullet">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt89" class="tgtSentence">En la pestaña <ui>Clasificación automática</ui>:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="91d34ca7099aa951a878689301e7dae5" id="tgt90" class="tgtSentence">
                          <ui>Habilitar programación fija</ui>: Seleccione esta casilla de verificación.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="1c7bbacee9ecb35844b0359c12c6d5c9" id="tgt91" class="tgtSentence">Configure la programación para que se ejecuten todas las reglas de clasificación, lo que incluye nuestra nueva regla para clasificar archivos con la propiedad RMS.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="07e04ac173431e78e6ae55bd52e03419" id="tgt92" class="tgtSentence">
                          <ui>Permitir clasificación continua de nuevos archivos</ui>: Seleccione esta casilla de verificación de modo que se clasifiquen nuevos archivos.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="b8beafecf8d342791369941c4eb52fa4" id="tgt93" class="tgtSentence">Opcional: Realice cualquier otro cambios que desee, como configurar opciones para informes y notificaciones.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence sentenceid="2a6f41af5bcebcc6a2d84dd5bd685185" id="tgt94" class="tgtSentence">Ahora que ha completado la configuración de clasificación, está listo para configurar una tarea de administración para aplicar la protección de RMS a los archivos.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
          <procedure>
            <title>
              <caps:sentence sentenceid="e885d131972edd81cda09b5d5accd1e9" id="tgt95" class="tgtSentence">Crear una tarea de administración de archivos personalizada (proteger los archivos con RMS)</caps:sentence>
            </title>
            <steps class="bullet">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="2d5a4eebfaf348c097ce2509288ef568" id="tgt96" class="tgtSentence">En <ui>Tareas de administración de archivos</ui>, cree una nueva tarea de administración de archivos:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt97" class="tgtSentence">En la pestaña <ui>General</ui>:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="fef8d1696dea20a8cd2a8b759e74a3f1" id="tgt98" class="tgtSentence">
                              <ui>Nombre de la tarea</ui>: Escribir <userInput>Proteger archivos con RMS</userInput></caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="f97cf85beeb765c9124aa8192882cb3f" id="tgt99" class="tgtSentence">Mantener la casilla de verificación <ui>Habilitar</ui> seleccionada.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="fef8d1696dea20a8cd2a8b759e74a3f1" id="tgt100" class="tgtSentence">
                              <ui>Descripción</ui>: Escriba <userInput>Proteger archivos en &lt;nombre de carpeta&gt; con Rights Management y una plantilla mediante un script de Windows PowerShell. </userInput></caps:sentence>
                          </para>
                          <para>
                            <caps:sentence sentenceid="05d18373e30d5a4c6a58e6f3b2e3e7ab" id="tgt101" class="tgtSentence">Reemplace <placeholder>&lt;nombre de carpeta&gt;</placeholder> por su nombre elegido para la carpeta.</caps:sentence>
                            <caps:sentence sentenceid="4eee3758f1bf4073d94deae936dd0a13" id="tgt102" class="tgtSentence"> Por ejemplo, <ui>Proteger archivos en C:\FileShare con Rights Management y una plantilla mediante un script de Windows PowerShell</ui></caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="af9b1e322f4a999a04d919fa14bd437a" id="tgt103" class="tgtSentence">
                              <ui>Ámbito</ui>: Seleccione su carpeta elegida.</caps:sentence>
                            <caps:sentence sentenceid="4eee3758f1bf4073d94deae936dd0a13" id="tgt104" class="tgtSentence"> Por ejemplo, <ui>C:\FileShare</ui>.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence sentenceid="24e121b32086c6d0a2f7a65edf0fa704" id="tgt105" class="tgtSentence">No seleccione las casillas de verificación.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt106" class="tgtSentence">En la pestaña <ui>Acción</ui>:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="4281ddfd144e2840410d083f59f98edc" id="tgt107" class="tgtSentence">
                              <ui>Tipo</ui>: Seleccionar <ui>Personalizado</ui></caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="01b581bc71b70f83101d927e6a3293a4" id="tgt108" class="tgtSentence">
                              <ui>Ejecutable</ui>: Especifique lo siguiente:</caps:sentence>
                          </para>
                          <code>C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe</code>
                          <para>
                            <caps:sentence sentenceid="a6d53222666bfe4d6e6062bad6dd93fe" id="tgt109" class="tgtSentence">Si Windows no está en la unidad C:, modifique esta ruta de acceso o vaya a este archivo.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="71f36901c386ab223d1e35c48cb169a7" id="tgt110" class="tgtSentence">
                              <ui>Argumento</ui>: Especifique lo siguiente, proporcionando sus propios valores para &lt;ruta de acceso&gt; e &lt;identificador de plantilla&gt;:</caps:sentence>
                          </para>
                          <code>-Noprofile -Command "&lt;path&gt;\RMS-Protect-FCI.ps1 -File '[Source File Path]' -TemplateID &lt;template GUID&gt; -OwnerMail [Source File Owner Email]"</code>
                          <para>
                            <caps:sentence sentenceid="8664dc091627973e755c4fdd0c7c9122" id="tgt111" class="tgtSentence">Por ejemplo, si ha copiado el script en C:\RMS-Protection y el identificador de plantilla que ha identificado en los requisitos previos es e6ee2481-26b9-45e5-b34a-f744eacd53b0, especifique lo siguiente: </caps:sentence>
                          </para>
                          <para>
                            <codeInline>-Noprofile -Command "C:\RMS-Protection\RMS-Protect-FCI.ps1 -File '[Source File Path]' -TemplateID e6ee2481-26b9-45e5-b34a-f744eacd53b0 -OwnerMail [Source File Owner Email]"</codeInline>
                          </para>
                          <para>
                            <caps:sentence sentenceid="87b9aa7d3e4d8a93fd8fd576f587b073" id="tgt112" class="tgtSentence">En este comando, tanto <ui>[Source File Path]</ui> como <ui>[Source File Owner Email]</ui> son variables específicas de FCI, así que escríbalas exactamente como aparecen en el comando anterior.</caps:sentence>
                            <caps:sentence sentenceid="348a35b094d1566f5da1cf1ec6cab2c5" id="tgt113" class="tgtSentence"> La primera la usa FCI para especificar automáticamente el archivo identificado en la carpeta y la segunda es para que FCI recupere automáticamente la dirección de correo electrónico del propietario designado del archivo identificado.</caps:sentence>
                            <caps:sentence sentenceid="718081dbd9cc74ed5d3a72315d7f5635" id="tgt114" class="tgtSentence"> Este comando se repite para cada archivo en la carpeta que, en nuestro ejemplo, es cada archivo de la carpeta C:\FileShare que, de forma adicional, tiene RMS como propiedad de clasificación de archivos.</caps:sentence>
                          </para>
                          <alert class="note">
                            <para>
                              <caps:sentence sentenceid="8fc42c6ddf9966db3b09e84365034357" id="tgt115" class="tgtSentence">El parámetro y el valor de <system> -OwnerMail [Source File Owner Email]</system> aseguran que al propietario original del archivo se le otorga al propietario de Rights Management del archivo después de que esté protegido.</caps:sentence>
                              <caps:sentence sentenceid="8d1d9ed09c0677336753d10d4be4e547" id="tgt116" class="tgtSentence"> Esto asegura que el propietario del archivo original tiene todos los derechos de Rights Management en sus propios archivos.</caps:sentence>
                              <caps:sentence sentenceid="b874c9dd5992305bf9b918fe4e4fc9b3" id="tgt117" class="tgtSentence"> Cuando un usuario de dominio crea archivos, la dirección de correo electrónico se recupera automáticamente desde Active Directory con el nombre de la cuenta de usuario de la propiedad Owner del archivo.</caps:sentence>
                              <caps:sentence sentenceid="6daac165494076dcccd238926bcdc18e" id="tgt118" class="tgtSentence"> Para ello, el servidor de archivos debe estar en el mismo dominio o dominio de confianza que el usuario.</caps:sentence>
                            </para>
                            <para>
                              <caps:sentence sentenceid="b6a5bf21d5f94af5431a857030f3a3fe" id="tgt119" class="tgtSentence">Siempre que sea posible, asigne los propietarios originales a documentos protegidos para asegurarse de que estos usuarios continúan teniendo control total sobre los archivos que han creado.</caps:sentence>
                              <caps:sentence sentenceid="66b625d73e4690a64a49ff0f57bc4751" id="tgt120" class="tgtSentence"> Sin embargo, si utiliza la variable [Source File Owner Email] igual como se ha hecho anteriormente y un archivo no tiene un usuario de dominio definido como propietario (por ejemplo, se utilizó una cuenta local para crear el archivo, por lo que el usuario aparece como SISTEMA), se producirá un error en el script.</caps:sentence>
                            </para>
                            <para>
                              <caps:sentence sentenceid="bd7516b91c9592a6397f9a2712d9f1b7" id="tgt121" class="tgtSentence">Para los archivos que no tienen un usuario de dominio como propietario, puede copiar y guardar estos archivos usted mismo como usuario de dominio, de modo que se convierta en el propietario de solo estos archivos.</caps:sentence>
                              <caps:sentence sentenceid="361437bc37fa5921415b1611314e219d" id="tgt122" class="tgtSentence"> O bien, si dispone de permisos, puede cambiar manualmente el propietario.</caps:sentence>
                              <caps:sentence sentenceid="8c184412d8f7b51cd1754be342b79915" id="tgt123" class="tgtSentence">  Como alternativa, puede especificar una dirección de correo electrónico específica (como la suya propia o una dirección de grupo del departamento de TI) en lugar de la variable [Source File Owner Email], lo que significa que todos los archivos que protege mediante este script utilizarán esta dirección de correo electrónico para definir el nuevo propietario.</caps:sentence>
                            </para>
                          </alert>
                        </listItem>
                      </list>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="4281ddfd144e2840410d083f59f98edc" id="tgt124" class="tgtSentence">
                          <ui>Ejecutar el comando como</ui>: Seleccionar <ui>Sistema local</ui></caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt125" class="tgtSentence">En la pestaña <ui>Condición</ui>:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="4281ddfd144e2840410d083f59f98edc" id="tgt126" class="tgtSentence">
                              <ui>Propiedad</ui>: Seleccionar <ui>RMS</ui> </caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="4281ddfd144e2840410d083f59f98edc" id="tgt127" class="tgtSentence">
                              <ui>Operador</ui>: Seleccionar <ui>Igual</ui> </caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="4281ddfd144e2840410d083f59f98edc" id="tgt128" class="tgtSentence">
                              <ui>Valor</ui>: Seleccionar <ui>Sí</ui> </caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt129" class="tgtSentence">En la pestaña <ui>Programación</ui>:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="23c6e5f971f0eb826551c86d4e6c0bde" id="tgt130" class="tgtSentence">
                              <ui>Ejecutar en</ui>: Configure su programación preferida.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence sentenceid="e788d9dc338429796f1fe0c5280e6507" id="tgt131" class="tgtSentence">Conceda al script tiempo de sobra para completarse.</caps:sentence>
                            <caps:sentence sentenceid="481cefbbbcc5379e63c80ea6529da00b" id="tgt132" class="tgtSentence"> Aunque esta solución protege todos los archivos de la carpeta, el script se ejecuta una vez para cada archivo cada vez.</caps:sentence>
                            <caps:sentence sentenceid="4ae07fe9dd935ca1fc2e4c21d86c7cc6" id="tgt133" class="tgtSentence"> Aunque este proceso tarda más que proteger todos los archivos al mismo tiempo, lo que es compatible con la herramienta de protección de RMS, esta configuración de cada archivo para FCI es más eficaz.</caps:sentence>
                            <caps:sentence sentenceid="d517b890868482d8e09982d6c295d7e5" id="tgt134" class="tgtSentence"> Por ejemplo, los archivos protegidos pueden tener distintos propietarios (conservar el propietario original) cuando utiliza la variable [Source File Owner Email] y esta acción de cada archivo será necesaria si posteriormente cambia la configuración para proteger archivos de forma selectiva en lugar de todos los archivos de una carpeta.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="91d34ca7099aa951a878689301e7dae5" id="tgt135" class="tgtSentence">
                              <ui>Ejecutarse continuamente en nuevos archivos</ui>: Seleccione esta casilla de verificación.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </listItem>
                  </list>
                </content>
              </step>
            </steps>
          </procedure>
          <procedure>
            <title>
              <caps:sentence sentenceid="1ff4133565bf3c38a3b244616a4fa588" id="tgt136" class="tgtSentence">Probar la configuración ejecutando manualmente la regla y la tarea</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="bbe765eb485159dec33428731ac5c231" id="tgt137" class="tgtSentence">Ejecute la regla de clasificación: </caps:sentence>
                  </para>
                  <list class="ordered">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="ccbe2a6c96a5df5e1966988e40064061" id="tgt138" class="tgtSentence">Haga clic en <ui>Reglas de clasificación</ui> &gt; <ui>Ejecutar clasificación con todas las reglas ahora</ui></caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="ccbe2a6c96a5df5e1966988e40064061" id="tgt139" class="tgtSentence">Haga clic en <ui>Esperar a que termine la clasificación</ui> y, a continuación, haga clic en <ui>Aceptar</ui>.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="9e34974a14ae2c6a958a4ff3f2459b27" id="tgt140" class="tgtSentence">Espere a que se cierre el cuadro de diálogo <ui>Ejecutando clasificación</ui> para cerrar y, a continuación, ver los resultados en el informe que se muestra automáticamente.</caps:sentence>
                    <caps:sentence sentenceid="584cb8cf69690ba8a0aeaf9c284ba57f" id="tgt141" class="tgtSentence"> Debe ver <ui>1</ui> para el campo <ui>Propiedades</ui> y el número de archivos de su carpeta.</caps:sentence>
                    <caps:sentence sentenceid="e6da0c100d35d9d353c85a4c7a8c8424" id="tgt142" class="tgtSentence"> Confírmelo mediante el Explorador de archivos y comprobando las propiedades de archivos de su carpeta elegida.</caps:sentence>
                    <caps:sentence sentenceid="94898649863bca08a3420d208bbe0015" id="tgt143" class="tgtSentence"> En la pestaña <ui>Clasificación</ui> ficha, debe ver <ui>RMS</ui> como nombre de la propiedad y <ui>Sí</ui> para su <ui>Valor</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="b36221f649cd6bc3cf61a47c61e1199a" id="tgt144" class="tgtSentence">Ejecute la tarea de administración de archivos: </caps:sentence>
                  </para>
                  <list class="ordered">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="ccbe2a6c96a5df5e1966988e40064061" id="tgt145" class="tgtSentence">Haga clic en <ui>Tareas de administración de archivos</ui> &gt; <ui>Proteger archivos con RMS</ui>  &gt; <ui>Ejecutar tarea de administración de archivos ahora</ui></caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="ccbe2a6c96a5df5e1966988e40064061" id="tgt146" class="tgtSentence">Haga clic en <ui>Esperar a que termine la clasificación</ui> y, a continuación, haga clic en <ui>Aceptar</ui>.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="9e34974a14ae2c6a958a4ff3f2459b27" id="tgt147" class="tgtSentence">Espere a que se cierre el cuadro de diálogo <ui>Ejecutando tarea de administración de archivos</ui> para cerrar y, a continuación, ver los resultados en el informe que se muestra automáticamente.</caps:sentence>
                    <caps:sentence sentenceid="a297040c198c733f646732185a257282" id="tgt148" class="tgtSentence"> Debe ver el número de archivos que se encuentran en su carpeta elegida en el campo <ui>Archivos</ui>.</caps:sentence>
                    <caps:sentence sentenceid="c579be2a327560df9a410b6e0b9bf961" id="tgt149" class="tgtSentence"> Confirme que los archivos de su carpeta elegida están actualmente protegidos por RMS.</caps:sentence>
                    <caps:sentence sentenceid="d27955bf281806217cd1ec29e2180d63" id="tgt150" class="tgtSentence"> Por ejemplo, si su carpeta elegida es C:\FileShare, escriba lo siguiente en una sesión de Windows PowerShell y confirme que no hay ningún archivo con el estado <ui>Sin proteger</ui>:</caps:sentence>
                  </para>
                  <code>foreach ($file in (Get-ChildItem -Path C:\FileShare -Force | where {!$_.PSIsContainer})) {Get-RMSFileStatus -f $file.PSPath}</code>
                  <alert class="tip">
                    <para>
                      <caps:sentence sentenceid="2ac79ac1045726e36ce944838864228a" id="tgt151" class="tgtSentence">Algunas sugerencias para la solución de problemas:</caps:sentence>
                    </para>
                    <list class="bullet">
                      <listItem>
                        <para>
                          <caps:sentence sentenceid="40faa0b00520e4c33d49b109faeb2eca" id="tgt152" class="tgtSentence">Si ve <ui>0</ui> en el informe, en lugar del número de archivos de su carpeta, esto indica que el script no se ha ejecutado.</caps:sentence>
                          <caps:sentence sentenceid="b76b27be6321b3a4b7782789549894a1" id="tgt153" class="tgtSentence"> En primer lugar, compruebe el propio script cargándolo en ISE de Windows PowerShell para validar el contenido del script e intenta ejecutarlo para ver si se muestra algún error.</caps:sentence>
                          <caps:sentence sentenceid="8d42945dd21fce5251f58005884c1761" id="tgt154" class="tgtSentence"> Sin argumentos especificados, el script intentará conectarse y autenticarse en Azure RMS.</caps:sentence>
                        </para>
                        <list class="bullet">
                          <listItem>
                            <para>
                              <caps:sentence sentenceid="e2606d931bfd85917a5a8786a170f72a" id="tgt155" class="tgtSentence">Si el script informa de que no ha podido conectarse a Azure RMS, compruebe los valores que muestra para la cuenta de entidad de servicio, que ha especificado en el script.</caps:sentence>
                              <caps:sentence sentenceid="2a34748acadb4f1aab8af9348b430184" id="tgt156" class="tgtSentence">  Para obtener más información sobre cómo crear esta cuenta de entidad de servicio, consulte el segundo requisito previo en <externalLink><linkText>about_RMSProtection_AzureRMS</linkText><linkUri>https://msdn.microsoft.com/library/mt433202.aspx</linkUri></externalLink></caps:sentence>
                            </para>
                          </listItem>
                          <listItem>
                            <para>
                              <caps:sentence sentenceid="36400741606c2f520eb51b611dd77d67" id="tgt157" class="tgtSentence">Si el script informa de que ha podido conectarse a Azure RMS y su región de Azure está fuera de Norteamérica, compruebe que ha modificado el Registro correctamente para esta configuración.</caps:sentence>
                              <caps:sentence sentenceid="90662c14417be6b186cf386cdee97bd5" id="tgt158" class="tgtSentence"> Una buena prueba de esto es ejecutar Get-RMSTemplate directamente desde Windows PowerShell en el servidor.</caps:sentence>
                              <caps:sentence sentenceid="2cef37a2853cc192b977fef1ceef877c" id="tgt159" class="tgtSentence"> Para obtener más información acerca de las modificaciones del Registro, consulte el tercer requisito previo en <externalLink><linkText>about_RMSProtection_AzureRMS</linkText><linkUri>https://msdn.microsoft.com/library/mt433202.aspx</linkUri></externalLink>.</caps:sentence>
                            </para>
                          </listItem>
                        </list>
                      </listItem>
                      <listItem>
                        <para>
                          <caps:sentence sentenceid="9a0aa1bdc8ad8daa5b616aca2133147d" id="tgt160" class="tgtSentence">Si el script por sí solo se ejecuta en ISE de Windows PowerShell sin errores, intente ejecutarlo como se indica a continuación en una sesión de PowerShell, especificando un nombre de archivo para proteger y sin el parámetro - OwnerEmail:</caps:sentence>
                        </para>
                        <code>powershell.exe -Noprofile -Command "&lt;path&gt;\RMS-Protect-FCI.ps1 -File &lt;full path and name of a file&gt;' -TemplateID &lt;template GUID&gt;"</code>
                        <list class="bullet">
                          <listItem>
                            <para>
                              <caps:sentence sentenceid="78c1f2606bb17ee48d09d6732cb4b4b0" id="tgt161" class="tgtSentence">Si el script se ejecuta correctamente en esta sesión de Windows PowerShell, compruebe sus entradas para <ui>Ejecutivo</ui> y <ui>Argumento</ui> en la acción de tarea de administración de archivos.</caps:sentence>
                              <caps:sentence sentenceid="63adce836a33805d362c6b97775b3ed5" id="tgt162" class="tgtSentence">  Si ha especificado <ui> - OwnerEmail [Source File Owner Email]</ui>, pruebe a quitar este parámetro.</caps:sentence>
                            </para>
                            <para>
                              <caps:sentence sentenceid="350d6d8e01270f9f874da9e49d0025c5" id="tgt163" class="tgtSentence">Si la tarea de administración de archivos funciona correctamente sin <ui> -OwnerEmail [Source File Owner Email]</ui>, compruebe que los archivos no protegidos tienen un usuario de dominio que aparece como el propietario del archivo, en lugar de <ui>SISTEMA</ui>.</caps:sentence>
                              <caps:sentence sentenceid="399fb74ed10d95eea1e8f6a29d6a1a33" id="tgt164" class="tgtSentence">  Para ello, utilice las pestaña <ui>Seguridad</ui> ficha de las propiedades del archivo y haga clic en <ui>Opciones avanzadas</ui>.</caps:sentence>
                              <caps:sentence sentenceid="90adbbe7112a5ab0269194573e650cc6" id="tgt165" class="tgtSentence"> El valor <ui>Propietario</ui> se muestra inmediatamente después del <ui>Nombre</ui> del archivo.</caps:sentence>
                              <caps:sentence sentenceid="e72e4fd3288508b4fa313bca3977a09e" id="tgt166" class="tgtSentence"> Verifique también que el servidor de archivos está en el mismo dominio o en un dominio de confianza para buscar la dirección de correo electrónico del usuario de Servicios de dominio de Active Directory.</caps:sentence>
                            </para>
                          </listItem>
                        </list>
                      </listItem>
                      <listItem>
                        <para>
                          <caps:sentence sentenceid="77c6afe82ef0354e9991ad671b39b871" id="tgt167" class="tgtSentence">Si ve el número correcto de archivos en el informe, pero los archivos no están protegidos, intente proteger los archivos manualmente mediante el uso del cmdlet <externalLink><linkText>Protect-RMSFile</linkText><linkUri>https://msdn.microsoft.com/library/azure/mt433201.aspx</linkUri></externalLink> para ver si aparece algún error.</caps:sentence>
                        </para>
                      </listItem>
                    </list>
                  </alert>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence sentenceid="2b5f3c3abb6ce45a3e50e5e8d7c110b2" id="tgt168" class="tgtSentence">Cuando haya confirmado que estas tareas se ejecutan satisfactoriamente, puede cerrar el Administrador de recursos de archivo.</caps:sentence>
                  <caps:sentence sentenceid="63bc7f50fb641e27e0b7b0b4b317b466" id="tgt169" class="tgtSentence"> Los archivos nuevos se protegerán automáticamente y todos los archivos se protegerán de nuevo cuando se ejecuten las programaciones.</caps:sentence>
                  <caps:sentence sentenceid="87a0074c18370eb2792a08ed58887018" id="tgt170" class="tgtSentence"> Volver a proteger los archivos garantiza que todos los cambios realizados en la plantilla se aplican a los archivos.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
        </content>
        <sections>
          <section expanded="false" address="BKMK_RMSProtection_Script">
            <title>
              <caps:sentence sentenceid="5a1d953d666e2bac952c1c9083935236" id="tgt171" class="tgtSentence">Script de Windows PowerShell para la protección de Azure RMS con FCI del Administrador de recursos del servidor de archivos</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="13c1f77b9a5fa277cd1ee77094e85296" id="tgt172" class="tgtSentence">Esta sección contiene el script de ejemplo para copiar y editar, como se describe en la sección anterior.</caps:sentence>
              </para>
              <para>
                <legacyItalic>
                  <caps:sentence sentenceid="18eedc5da80094e0ab3d004c93476602" id="tgt173" class="tgtSentence">
                    <legacyBold>Renuncia</legacyBold>: Este script de ejemplo no es compatible en ningún servicio o programa de soporte estándar de Microsoft.</caps:sentence>
                  <caps:sentence sentenceid="c62eb79717d2870aba23b3fa99ed9aa4" id="tgt174" class="tgtSentence"> Este script de ejemplo se proporciona TAL CUAL sin garantía de ningún tipo.</caps:sentence>
                </legacyItalic>
              </para>
              <code>&lt;# .SYNOPSIS Helper script to protect all file types with Azure RMS and FCI. .DESCRIPTION Protect files with Azure RMS and Windows Server FCI, using an RMS template ID. #&gt; param( [Parameter(Mandatory = $false)] [ValidateScript({ If($_ -eq "") {$true} else { if (Test-Path -Path $_ -PathType Leaf) {$true} else {throw "Can't find file specified"} } })] [string]$File, [Parameter(Mandatory = $false)] [string]$TemplateID, [Parameter(Mandatory = $false)] [string]$OwnerMail, [Parameter(Mandatory = $false)] [string]$AppPrincipalId = "&lt;enter your AppPrincipalId here&gt;", [Parameter(Mandatory = $false)] [string]$SymmetricKey = "&lt;enter your key here&gt;", [Parameter(Mandatory = $false)] [string]$BposTenantId = "&lt;enter your BposTenantId here&gt;" ) # script information [String] $Script:Version = 'version 1.0' [String] $Script:Name = "RMS-Protect-FCI.ps1" #global working variables [switch] $Script:isScriptProcess = $False # Controls the script process. If false, the script gracefully stops running. #**Functions (general helper)*************************************** function Get-ScriptName(){ return $MyInvocation.ScriptName.Substring($MyInvocation.ScriptName.LastIndexOf('\') + 1, $MyInvocation.ScriptName.LastIndexOf('.') - $MyInvocation.ScriptName.LastIndexOf('\') - 1) } #**Functions (script specific)************************************** function Check-Module{ param ([String]$Module = $(Throw "Module name not specified")) [bool]$isResult = $False #try to load the module if (get-module -list -name $Module) { import-module $Module if (get-module -name $Module ) { $isResult = $True } else { $isResult = $False } } else { $isResult = $False } return $isResult } function Protect-File ($ffile, $ftemplateId, $fownermail) { [bool] $returnValue = $false try { If ($OwnerMail -eq $null -or $OwnerMail -eq "") { $protectReturn = Protect-RMSFile -File $ffile -TemplateID $ftemplateId $returnValue = $true Write-Host ( "Information: " + "Protected File: $ffile with Template: $ftemplateId") } else { $protectReturn = Protect-RMSFile -File $ffile -TemplateID $ftemplateId -OwnerEmail $fownermail $returnValue = $true Write-Host ( "Information: " + "Protected File: $ffile with Template: $ftemplateId, set Owner: $fownermail") } } catch { Write-Host ( "ERROR" + "During protection of file: $ffile with Template: $ftemplateId") } return $returnValue } function Set-RMSConnection ($fappId, $fkey, $fbposId) { [bool] $returnValue = $false try { Set-RMSServerAuthentication -AppPrincipalId $fappId -Key $fkey -BposTenantId $fbposId Write-Host ("Information: " + "Connected to Azure RMS Service with BposTenantId: $fbposId using AppPrincipalId: $fappId") $returnValue = $true } catch { Write-Host ("ERROR" + "During connection to Azure RMS Service with BposTenantId: $fbposId using AppPrincipalId: $fappId") } return $returnValue } #**Main Script (Script)********************************************* Write-Host ("-== " + $Script:Name + " " + $Version + " ==-") $Script:isScriptProcess = $True # Validate Azure RMS connection by checking the module and then connection if ($Script:isScriptProcess) { if (Check-Module -Module RMSProtection){ $Script:isScriptProcess = $True } else { Write-Host ("The RMSProtection module is not loaded") -foregroundcolor "yellow" -backgroundcolor "black" $Script:isScriptProcess = $False } } if ($Script:isScriptProcess) { #Write-Host ("Try to connect to Azure RMS with AppId: $AppPrincipalId and BPOSID: $BposTenantId" ) if (Set-RMSConnection $AppPrincipalId $SymmetricKey $BposTenantId) { Write-Host ("Connected to Azure RMS") } else { Write-Host ("Couldn't connect to Azure RMS") -foregroundcolor "yellow" -backgroundcolor "black" $Script:isScriptProcess = $False } } #  Start working loop if ($Script:isScriptProcess) { if ( !(($File -eq $null) -or ($File -eq "")) ) { if (!(Protect-File -ffile $File -ftemplateId $TemplateID -fownermail $OwnerMail)) { $Script:isScriptProcess = $False } } } # Closing if (!$Script:isScriptProcess) { Write-Host "ERROR occurred during script process" -foregroundcolor "red" -backgroundcolor "black"} write-host ("-== " + $Script:Name + " " + $Version + "  ==-") if (!$Script:isScriptProcess) { exit(-1) } else {exit(0)}</code>
            </content>
          </section>
        </sections>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="97eb8e00ef102ee58cc612d3103a3574" id="tgt175" class="tgtSentence">Modificar las instrucciones para proteger archivos de forma selectiva</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="be055d726acb56bff5b9557264f7b81a" id="tgt176" class="tgtSentence">Cuando tenga las instrucciones anteriores funcionando, será muy fácil modificarlas para obtener una configuración más sofisticada.</caps:sentence>
            <caps:sentence sentenceid="40d5c9641850abddacba2b1c69bcc92b" id="tgt177" class="tgtSentence"> Por ejemplo, proteja archivos mediante el uso del mismo script, pero solo para los archivos que contienen información de identificación personal y seleccione quizás una plantilla con permisos más restrictivos.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="a6a47442228acaf3eedde192b6db01db" id="tgt178" class="tgtSentence">Para ello, utilice una de las propiedades de clasificación integradas (por ejemplo, <ui>Información de identificación personal</ui>) o cree su propia nueva propiedad.</caps:sentence>
            <caps:sentence sentenceid="4c7dfc020e759c77dbe00bb2196d0493" id="tgt179" class="tgtSentence"> A continuación, cree una nueva regla que utilice esta propiedad.</caps:sentence>
            <caps:sentence sentenceid="1da561b1d05eb93b079e70905fa5c48c" id="tgt180" class="tgtSentence"> Por ejemplo, puede seleccionar <ui>Clasificador de contenido</ui>, elija la propiedad <ui>Información de identificación personal</ui> con un valor de <ui>Alto</ui> y configure el modelo de expresiones o cadenas que identifica el archivo que se va a configurar para esta propiedad (como la cadena "<userInputLocalizable>Fecha de nacimiento</userInputLocalizable>").</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="ed9008e52b11bbec4d123ba05ee6a116" id="tgt181" class="tgtSentence">Ahora todo lo que debe hacer es crear una nueva tarea de administración de archivos que utilice el mismo script, aunque quizás con una plantilla diferente, así como configurar la condición para la propiedad de clasificación que acaba de configurar.</caps:sentence>
            <caps:sentence sentenceid="40ff6667e422fd313fba19dac423cf33" id="tgt182" class="tgtSentence"> Por ejemplo, en lugar de la condición que hemos configurado previamente (propiedad <ui>RMS</ui>, <ui>Igual</ui>, <ui>Sí</ui>), seleccione la propiedad <ui>Información de identificación personal</ui> con el valor <ui>Operador</ui> establecido en <ui>Igual</ui> y el <ui>Valor</ui> de <ui>Alto</ui>.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xlink="http://www.w3.org/1999/xlink">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Use this article for instructions and a script to use the Rights Management (RMS) client with the RMS Protection tool to configure File Server Resource Manager and file classification infrastructure (FCI).</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src2" class="srcSentence">This solutions lets you automatically protect all files in a folder on a file server running Windows Server, or automatically protect files that meet a specific criteria.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> For example, files that have been classified as containing confidential or sensitive information.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> This solution uses <link xlink:href="965581c8-be3c-43b4-8145-5cefd29c7636">Azure Rights Management</link> (Azure RMS) to protect the files, so you must have this technology deployed in your organization.</caps:sentence>
        </para>
        <alert class="note">
          <para>
            <caps:sentence id="src5" class="srcSentence">Although Azure RMS includes a <externalLink><linkText>connector</linkText><linkUri>https://technet.microsoft.com/library/dn375964.aspx</linkUri></externalLink> that supports file classification infrastructure, that solution supports native protection only—for example, Office files.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src6" class="srcSentence">To support all file types with file classification infrastructure, you must use the Windows PowerShell <embeddedLabel>RMS Protection</embeddedLabel> module, as documented in this article.</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> The RMS Protection cmdlets, like the RMS sharing application, support generic protection as well as native protection, which means that all files can be protected.</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> For more information about these different protection levels, see the <link xlink:href="d9992e30-f3d1-48d5-aedc-4e721f7d7c25#BKMK_LevelsofProtection">Levels of protection – native and generic</link> section in the <link xlink:href="d9992e30-f3d1-48d5-aedc-4e721f7d7c25">Rights Management sharing application administrator guide</link>.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence id="src9" class="srcSentence">The instructions that follow are for Windows Server 2012 R2 or Windows Server 2012.</caps:sentence>
          <caps:sentence id="src10" class="srcSentence"> If you run other supported versions of Windows, you might need to adapt some of the steps for differences between your operating system version and the one documented in this article.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src11" class="srcSentence">Prerequisites for Azure RMS protection with Windows Server FCI</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src12" class="srcSentence">Prerequisites for these instructions: </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src13" class="srcSentence">On each file server where you will run File Resource Manager with file classification infrastructure:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src14" class="srcSentence">You have installed File Server Resource Manager as one of the role services for the File Services role.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src15" class="srcSentence">You have identified a local folder that contains files to protect with Rights Management.</caps:sentence>
                    <caps:sentence id="src16" class="srcSentence"> For example, C:\FileShare.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src17" class="srcSentence">You have installed the RMS Protection tool, including the prerequisites for the tool (such as the RMS client) and for Azure RMS (such as the service principal account).</caps:sentence>
                    <caps:sentence id="src18" class="srcSentence"> For more information, see <externalLink><linkText>RMS Protection Cmdlets</linkText><linkUri>https://msdn.microsoft.com/library/azure/mt433195.aspx</linkUri></externalLink>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src19" class="srcSentence">If you want to change the default level of RMS protection (native or generic) for specific file name extensions, you have edited the registry as described in the <externalLink><linkText>File API configuration</linkText><linkUri>https://msdn.microsoft.com/library/dn197834(v=vs.85).aspx</linkUri></externalLink> page.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src20" class="srcSentence">You have an Internet connection, with configured computer settings if required for a proxy server.</caps:sentence>
                    <caps:sentence id="src21" class="srcSentence"> For example: <codeInline>netsh winhttp import proxy source=ie</codeInline></caps:sentence>
                  </para>
                </listItem>
              </list>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src22" class="srcSentence">You have configured the additional prerequisites for your Azure Rights Management deployment, as described in <externalLink><linkText>about_RMSProtection_AzureRMS</linkText><linkUri>https://msdn.microsoft.com/library/mt433202.aspx</linkUri></externalLink>.</caps:sentence>
                <caps:sentence id="src23" class="srcSentence"> Specifically, you have the following values to connect to Azure RMS by using a service principal:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src24" class="srcSentence">BposTenantId</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src25" class="srcSentence">AppPrincipalId</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src26" class="srcSentence">Symmetric key</caps:sentence>
                  </para>
                </listItem>
              </list>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src27" class="srcSentence">You have synchronized your on-premises Active Directory user accounts with Azure Active Directory or Office 365, including their email address.</caps:sentence>
                <caps:sentence id="src28" class="srcSentence"> This is required for all users that might need to access files after they are protected by FCI and Azure RMS.</caps:sentence>
                <caps:sentence id="src29" class="srcSentence"> If you do not  do this step (for example, in a test environment), users might be blocked from accessing these files.</caps:sentence>
                <caps:sentence id="src30" class="srcSentence"> If you need more information about this account configuration, see <link xlink:href="afbca2d6-32a7-4bda-8aaf-9f93f5da5abc">Preparing for Azure Rights Management</link>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src31" class="srcSentence">You have identified the Rights Management template to use, which will protect the files.</caps:sentence>
                <caps:sentence id="src32" class="srcSentence"> Make sure that you know the ID for this template by using the <externalLink><linkText>Get-RMSTemplate</linkText><linkUri>https://msdn.microsoft.com/library/azure/mt433197.aspx</linkUri></externalLink> cmdlet.</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src33" class="srcSentence">Instructions to configure File Server Resource Manager FCI for Azure RMS protection </caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src34" class="srcSentence">Follow these instructions to automatically protect all files in a folder, by using a Windows PowerShell script as a custom task.</caps:sentence>
            <caps:sentence id="src35" class="srcSentence"> Do these procedures in this order:</caps:sentence>
          </para>
          <list class="ordered">
            <listItem>
              <para>
                <caps:sentence id="src36" class="srcSentence">Save the Windows PowerShell script</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src37" class="srcSentence">Create a classification property for Rights Management (RMS)</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src38" class="srcSentence">Create a classification rule (Classify for RMS)</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src39" class="srcSentence">Configure the classification schedule</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src40" class="srcSentence">Create a custom file management task (Protect files with RMS)</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src41" class="srcSentence">Test the configuration by manually running the rule and task</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src42" class="srcSentence">At the end of these instructions, all files in your selected folder will be classified with the custom property of RMS, and these files will then be protected by Rights Management.</caps:sentence>
            <caps:sentence id="src43" class="srcSentence"> For a more complex configuration that selectively protects some files and not others, you can then create or use a different classification property and rule, with a file management task that protects just those files.</caps:sentence>
          </para>
          <procedure>
            <title>
              <caps:sentence id="src44" class="srcSentence">Save the Windows PowerShell script</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src45" class="srcSentence">Expand the <link xlink:href="#BKMK_RMSProtection_Script">Windows PowerShell Script</link> section in this article, and copy its contents.</caps:sentence>
                    <caps:sentence id="src46" class="srcSentence"> Paste the contents of the script and  name the file <system>RMS-Protect-FCI.ps1</system> on your own computer.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src47" class="srcSentence">Review the script and make the following changes:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src48" class="srcSentence">Search for the following string and replace it with your own AppPrincipalId that you use with the <externalLink><linkText>Set-RMSServerAuthentication</linkText><linkUri>https://msdn.microsoft.com/library/mt433199.aspx</linkUri></externalLink> cmdlet to connect to Azure RMS:</caps:sentence>
                      </para>
                      <code>&lt;enter your AppPrincipalId here&gt;</code>
                      <para>
                        <caps:sentence id="src49" class="srcSentence">For example, the script might look like this:</caps:sentence>
                      </para>
                      <para>
                        <codeInline>[Parameter(Mandatory = $false)]
            </codeInline>
                      </para>
                      <para>
                        <codeInline>[Parameter(Mandatory = $false)] [string]$AppPrincipalId = "b5e3f76a-b5c2-4c96-a594-a0807f65bba4",</codeInline>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src50" class="srcSentence">Search for the following string and replace it with your own symmetric key that you use with the <externalLink><linkText>Set-RMSServerAuthentication</linkText><linkUri>https://msdn.microsoft.com/library/mt433199.aspx</linkUri></externalLink> cmdlet to connect to Azure RMS:</caps:sentence>
                      </para>
                      <code>&lt;enter your key here&gt;</code>
                      <para>
                        <caps:sentence id="src51" class="srcSentence">For example, the script might look like this:</caps:sentence>
                      </para>
                      <para>
                        <codeInline>[Parameter(Mandatory = $false)]
            </codeInline>
                      </para>
                      <para>
                        <codeInline>[string]$SymmetricKey = "zIeMu8zNJ6U377CLtppkhkbl4gjodmYSXUVwAO5ycgA="</codeInline>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src52" class="srcSentence">Search for the following string and replace it with your own BposTenantId (tenant ID) that you use with the <externalLink><linkText>Set-RMSServerAuthentication</linkText><linkUri>https://msdn.microsoft.com/library/mt433199.aspx</linkUri></externalLink> cmdlet to connect to Azure RMS:</caps:sentence>
                      </para>
                      <code>&lt;enter your BposTenantId here&gt;</code>
                      <para>
                        <caps:sentence id="src53" class="srcSentence">For example, the script might look like this:</caps:sentence>
                      </para>
                      <para>
                        <codeInline>[Parameter(Mandatory = $false)]
            </codeInline>
                      </para>
                      <para>
                        <codeInline>[string]$BposTenantId = "23976bc6-dcd4-4173-9d96-dad1f48efd42",</codeInline>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src54" class="srcSentence">If your server is running Windows Server 2012, you might have to manually load the RMSProtection module at the beginning of the script.</caps:sentence>
                        <caps:sentence id="src55" class="srcSentence"> Add the following command (or equivalent if  the "Program Files"  folder is  on a drive other than the  C: drive :</caps:sentence>
                      </para>
                      <code>Import-Module "C:\Program Files\WindowsPowerShell\Modules\RMSProtection\RMSProtection.dll"</code>
                    </listItem>
                  </list>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src56" class="srcSentence">Sign the script.</caps:sentence>
                    <caps:sentence id="src57" class="srcSentence"> If you do not sign the script (more secure), you must configure Windows PowerShell on the servers that run it.</caps:sentence>
                    <caps:sentence id="src58" class="srcSentence"> For example, run a Windows PowerShell session with the <ui>Run as Administrator</ui> option, and type: <userInput>Set-ExecutionPolicy Unrestricted</userInput>.</caps:sentence>
                    <caps:sentence id="src59" class="srcSentence"> However, this configuration lets all unsigned scripts run (less secure).</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src60" class="srcSentence">For more information about signing Windows PowerShell scripts, see <externalLink><linkText>about_Signing</linkText><linkUri>https://technet.microsoft.com/library/hh847874.aspx</linkUri></externalLink> in the PowerShell documentation library.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src61" class="srcSentence">Save the file locally on each file server that will run File Resource Manager with file classification infrastructure.</caps:sentence>
                    <caps:sentence id="src62" class="srcSentence"> For example, save the file in <system>C:\RMS-Protection</system>.</caps:sentence>
                    <caps:sentence id="src63" class="srcSentence"> Secure this file by using NTFS permissions so that unauthorized users cannot modify it.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence id="src64" class="srcSentence">You're now ready to start configuring File Server Resource Manager.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
          <procedure>
            <title>
              <caps:sentence id="src65" class="srcSentence">Create a classification property for Rights Management (RMS)</caps:sentence>
            </title>
            <steps class="bullet">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src66" class="srcSentence">In File Server Resource Manager, Classification Management, create a new local property:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src67" class="srcSentence">
                          <ui>Name</ui>: Type <userInput>RMS</userInput></caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src68" class="srcSentence">
                          <ui>Description</ui>:   Type <userInput>Rights Management protection</userInput></caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src69" class="srcSentence">
                          <ui>Property Type</ui>: Select <ui>Yes/No</ui></caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src70" class="srcSentence">
                          <ui>Value</ui>: Select <ui>Yes</ui></caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence id="src71" class="srcSentence">We can now create a classification rule that uses this property.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
          <procedure>
            <title>
              <caps:sentence id="src72" class="srcSentence">Create a classification rule (Classify for RMS)</caps:sentence>
            </title>
            <steps class="bullet">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src73" class="srcSentence">Create a new classification rule:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src74" class="srcSentence">On the <ui>General</ui> tab:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence id="src75" class="srcSentence">
                              <ui>Name</ui>: Type<userInput> Classify for RMS</userInput></caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src76" class="srcSentence">
                              <ui>Enabled</ui>: Keep the default, which is that this checkbox is selected.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src77" class="srcSentence">
                              <ui>Description</ui>: Type <userInput>Classify all files in the &lt;folder name&gt; folder for Rights Management</userInput>.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence id="src78" class="srcSentence">Replace <placeholder>&lt;folder name&gt;</placeholder> with your chosen folder name.</caps:sentence>
                            <caps:sentence id="src79" class="srcSentence"> For example, <ui>Classify all files in the C:\FileShare folder for Rights Management</ui></caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src80" class="srcSentence">
                              <ui>Scope</ui>: Add your chosen folder.</caps:sentence>
                            <caps:sentence id="src81" class="srcSentence"> For example, <ui>C:\FileShare</ui>.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence id="src82" class="srcSentence">Do not select the checkboxes.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src83" class="srcSentence">On the <ui>Classification</ui> tab:</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src84" class="srcSentence">
                          <ui>Classification method</ui>: Select <ui>Folder Classifier</ui></caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src85" class="srcSentence">
                          <ui>Property</ui> name: Select <ui>RMS</ui></caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src86" class="srcSentence">Property <ui>value</ui>: Select <ui>Yes</ui></caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence id="src87" class="srcSentence">Although you can run the classification rules manually, for ongoing operations, you will want this rule to run on a schedule so that new files will be classified with the RMS property.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
          <procedure>
            <title>
              <caps:sentence id="src88" class="srcSentence">Configure the classification schedule</caps:sentence>
            </title>
            <steps class="bullet">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src89" class="srcSentence">On the <ui>Automatic Classification</ui> tab:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src90" class="srcSentence">
                          <ui>Enable fixed schedule</ui>: Select this checkbox.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src91" class="srcSentence">Configure the schedule for all classification rules to run, which includes our new rule to classify files with the RMS property.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src92" class="srcSentence">
                          <ui>Allow continuous classification for new files</ui>: Select this checkbox so that new files will be classified.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src93" class="srcSentence">Optional: Make any other changes that you want, such as configuring options for reports and notifications.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence id="src94" class="srcSentence">Now you've completed the classification configuration, you're ready to configure a management task to apply the RMS protection to the files.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
          <procedure>
            <title>
              <caps:sentence id="src95" class="srcSentence">Create a custom file management task (Protect files with RMS)</caps:sentence>
            </title>
            <steps class="bullet">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src96" class="srcSentence">In <ui>File Management Tasks</ui>, create a new file management task:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src97" class="srcSentence">On the <ui>General</ui> tab:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence id="src98" class="srcSentence">
                              <ui>Task name</ui>: Type <userInput>Protect files with RMS</userInput></caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src99" class="srcSentence">Keep the <ui>Enable</ui> checkbox selected.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src100" class="srcSentence">
                              <ui>Description</ui>: Type <userInput>Protect files in &lt;folder name&gt; with Rights Management and a template by using a Windows PowerShell script. </userInput></caps:sentence>
                          </para>
                          <para>
                            <caps:sentence id="src101" class="srcSentence">Replace <placeholder>&lt;folder name&gt;</placeholder> with your chosen folder name.</caps:sentence>
                            <caps:sentence id="src102" class="srcSentence"> For example, <ui>Protect files in C:\FileShare with Rights Management and a template by using a Windows PowerShell script</ui></caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src103" class="srcSentence">
                              <ui>Scope</ui>: Select your chosen folder.</caps:sentence>
                            <caps:sentence id="src104" class="srcSentence"> For example, <ui>C:\FileShare</ui>.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence id="src105" class="srcSentence">Do not select the checkboxes.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src106" class="srcSentence">On the <ui>Action</ui> tab:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence id="src107" class="srcSentence">
                              <ui>Type</ui>: Select <ui>Custom</ui></caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src108" class="srcSentence">
                              <ui>Executable</ui>: Specify the following:</caps:sentence>
                          </para>
                          <code>C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe</code>
                          <para>
                            <caps:sentence id="src109" class="srcSentence">If Windows is not on your C: drive, modify this path or browse to this file.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src110" class="srcSentence">
                              <ui>Argument</ui>: Specify the following, supplying your own values for &lt;path&gt; and &lt;template ID&gt;:</caps:sentence>
                          </para>
                          <code>-Noprofile -Command "&lt;path&gt;\RMS-Protect-FCI.ps1 -File '[Source File Path]' -TemplateID &lt;template GUID&gt; -OwnerMail [Source File Owner Email]"</code>
                          <para>
                            <caps:sentence id="src111" class="srcSentence">For example, if you copied the script to C:\RMS-Protection and the template ID you identified from the prerequisites is e6ee2481-26b9-45e5-b34a-f744eacd53b0, specify the following: </caps:sentence>
                          </para>
                          <para>
                            <codeInline>-Noprofile -Command "C:\RMS-Protection\RMS-Protect-FCI.ps1 -File '[Source File Path]' -TemplateID e6ee2481-26b9-45e5-b34a-f744eacd53b0 -OwnerMail [Source File Owner Email]"</codeInline>
                          </para>
                          <para>
                            <caps:sentence id="src112" class="srcSentence">In this command, <ui>[Source File Path]</ui> and <ui>[Source File Owner Email]</ui> are both FCI-specific variables, so type these exactly as they appear in the command above.</caps:sentence>
                            <caps:sentence id="src113" class="srcSentence"> The first one is used by FCI to automatically specify the identified file in the folder, and the second is for FCI to automatically retrieve the email address of the named Owner of the identified file.</caps:sentence>
                            <caps:sentence id="src114" class="srcSentence"> This command is repeated for each file in the folder, which in our example, is each file in the C:\FileShare folder that additionally, has RMS as a file classification property.</caps:sentence>
                          </para>
                          <alert class="note">
                            <para>
                              <caps:sentence id="src115" class="srcSentence">The<system> -OwnerMail [Source File Owner Email]</system> parameter and value ensures that the original owner of the file is granted the Rights Management owner of the file after it is protected.</caps:sentence>
                              <caps:sentence id="src116" class="srcSentence"> This ensures that the original file owner has all Rights Management rights to their own files.</caps:sentence>
                              <caps:sentence id="src117" class="srcSentence"> When files are created by a domain user, the email address is  automatically retrieved from Active Directory by using the user account name in the file's Owner property.</caps:sentence>
                              <caps:sentence id="src118" class="srcSentence"> To do this, the file server must be in the same domain or trusted domain as the user.</caps:sentence>
                            </para>
                            <para>
                              <caps:sentence id="src119" class="srcSentence">Whenever possible, assign the original owners to protected documents, to ensure that these users continue to have full control over the files that they created.</caps:sentence>
                              <caps:sentence id="src120" class="srcSentence"> However, if you use the [Source File Owner Email] variable as above, and a file does not have a domain user defined as the owner (for example, a local account was used to create the file, so the owner displays SYSTEM), the script will fail.</caps:sentence>
                            </para>
                            <para>
                              <caps:sentence id="src121" class="srcSentence">For files that do not have a domain user as owner, you can either copy and save these files yourself as a domain user, so that you become the owner for just these files.</caps:sentence>
                              <caps:sentence id="src122" class="srcSentence"> Or, if you have permissions, you can manually change the owner.</caps:sentence>
                              <caps:sentence id="src123" class="srcSentence">  Or alternatively, you can supply a specific email address (such as your own or a group address for the IT department) instead of the [Source File Owner Email] variable, which means that all files you protect by using this script will use this email address to define the new owner.</caps:sentence>
                            </para>
                          </alert>
                        </listItem>
                      </list>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src124" class="srcSentence">
                          <ui>Run the command as</ui>: Select <ui>Local System</ui></caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src125" class="srcSentence">On the <ui>Condition</ui> tab:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence id="src126" class="srcSentence">
                              <ui>Property</ui>: Select <ui>RMS</ui> </caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src127" class="srcSentence">
                              <ui>Operator</ui>: Select <ui>Equal</ui> </caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src128" class="srcSentence">
                              <ui>Value</ui>: Select <ui>Yes</ui> </caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src129" class="srcSentence">On the <ui>Schedule</ui> tab:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence id="src130" class="srcSentence">
                              <ui>Run at</ui>: Configure your preferred schedule.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence id="src131" class="srcSentence">Allow plenty of time for the script to complete.</caps:sentence>
                            <caps:sentence id="src132" class="srcSentence"> Although this solution  protects all files in the folder, the script runs once for each file, each time.</caps:sentence>
                            <caps:sentence id="src133" class="srcSentence"> Although this takes longer than protecting all the files at the same time, which the RMS Protection tool supports, this file-by-file configuration for FCI is more powerful.</caps:sentence>
                            <caps:sentence id="src134" class="srcSentence"> For example, the protected files can have different owners (retain the original owner) when you use the   [Source File Owner Email] variable, and this file-by-file action will be required if you later change the configuration to selectively protect files rather than all files in a folder.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src135" class="srcSentence">
                              <ui>Run continuously on new files</ui>: Select this checkbox.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </listItem>
                  </list>
                </content>
              </step>
            </steps>
          </procedure>
          <procedure>
            <title>
              <caps:sentence id="src136" class="srcSentence">Test the configuration by manually running the rule and task</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src137" class="srcSentence">Run the classification rule: </caps:sentence>
                  </para>
                  <list class="ordered">
                    <listItem>
                      <para>
                        <caps:sentence id="src138" class="srcSentence">Click <ui>Classification Rules</ui> &gt; <ui>Run Classification With All Rules Now</ui></caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src139" class="srcSentence">Click <ui>Wait for classification to complete</ui>, and then click <ui>OK</ui>.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src140" class="srcSentence">Wait for the <ui>Running Classification</ui> dialog box to close and then view the results in the automatically displayed report.</caps:sentence>
                    <caps:sentence id="src141" class="srcSentence"> You should see <ui>1</ui> for the <ui>Properties</ui> field and the number of files in your folder.</caps:sentence>
                    <caps:sentence id="src142" class="srcSentence"> Confirm by using File Explorer and checking the properties of files in your chosen folder.</caps:sentence>
                    <caps:sentence id="src143" class="srcSentence"> On the <ui>Classification</ui> tab, you should see <ui>RMS</ui> as a property name and <ui>Yes</ui> for its <ui>Value</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src144" class="srcSentence">Run the file management task: </caps:sentence>
                  </para>
                  <list class="ordered">
                    <listItem>
                      <para>
                        <caps:sentence id="src145" class="srcSentence">Click <ui>File Management Tasks</ui> &gt; <ui>Protect files with RMS</ui>  &gt; <ui>Run File Management Task Now</ui></caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src146" class="srcSentence">Click <ui>Wait for the task to complete</ui>, and then click <ui>OK</ui>.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src147" class="srcSentence">Wait for the <ui>Running File Management Task</ui> dialog box to close and then view the results in the automatically displayed report.</caps:sentence>
                    <caps:sentence id="src148" class="srcSentence"> You should see the number of files that are in your chosen folder in the <ui>Files</ui> field.</caps:sentence>
                    <caps:sentence id="src149" class="srcSentence"> Confirm that the files in your chosen folder are now protected by RMS.</caps:sentence>
                    <caps:sentence id="src150" class="srcSentence"> For example, if your chosen folder is C:\FileShare, type the following in a Windows PowerShell session and confirm that no files have a status of <ui>UnProtected</ui>:</caps:sentence>
                  </para>
                  <code>foreach ($file in (Get-ChildItem -Path C:\FileShare -Force | where {!$_.PSIsContainer})) {Get-RMSFileStatus -f $file.PSPath}</code>
                  <alert class="tip">
                    <para>
                      <caps:sentence id="src151" class="srcSentence">Some troubleshooting tips:</caps:sentence>
                    </para>
                    <list class="bullet">
                      <listItem>
                        <para>
                          <caps:sentence id="src152" class="srcSentence">If you see <ui>0</ui> in the report, instead of the number of files in your folder, this indicates that the script did not run.</caps:sentence>
                          <caps:sentence id="src153" class="srcSentence"> First, check the script itself by loading it in Windows PowerShell ISE to validate the script contents and try running it to see if any errors are displayed.</caps:sentence>
                          <caps:sentence id="src154" class="srcSentence"> With no arguments specified, the script will try to connect and authenticate to Azure RMS.</caps:sentence>
                        </para>
                        <list class="bullet">
                          <listItem>
                            <para>
                              <caps:sentence id="src155" class="srcSentence">If the script reports that it couldn't connect to Azure RMS, check the values it displays for the service principal account, which you specified in the script.</caps:sentence>
                              <caps:sentence id="src156" class="srcSentence">  For more information about how to create this service principal account, see the second prerequisite in <externalLink><linkText>about_RMSProtection_AzureRMS</linkText><linkUri>https://msdn.microsoft.com/library/mt433202.aspx</linkUri></externalLink></caps:sentence>
                            </para>
                          </listItem>
                          <listItem>
                            <para>
                              <caps:sentence id="src157" class="srcSentence">If the script reports that it could connect to Azure RMS and your Azure region is outside North America, check that you have edited the registry correctly for this configuration.</caps:sentence>
                              <caps:sentence id="src158" class="srcSentence"> A good test for this is to run Get-RMSTemplate directly from Windows PowerShell on the server.</caps:sentence>
                              <caps:sentence id="src159" class="srcSentence"> For more information about the registry edits, see the third prerequisite in <externalLink><linkText>about_RMSProtection_AzureRMS</linkText><linkUri>https://msdn.microsoft.com/library/mt433202.aspx</linkUri></externalLink>.</caps:sentence>
                            </para>
                          </listItem>
                        </list>
                      </listItem>
                      <listItem>
                        <para>
                          <caps:sentence id="src160" class="srcSentence">If the script by itself runs in Windows PowerShell ISE without errors, try running it as follows from a  PowerShell session, specifying a file name to protect and without the -OwnerEmail parameter:</caps:sentence>
                        </para>
                        <code>powershell.exe -Noprofile -Command "&lt;path&gt;\RMS-Protect-FCI.ps1 -File &lt;full path and name of a file&gt;' -TemplateID &lt;template GUID&gt;"</code>
                        <list class="bullet">
                          <listItem>
                            <para>
                              <caps:sentence id="src161" class="srcSentence">If the script runs successfully in this Windows PowerShell session, check  your entries for <ui>Executive</ui> and <ui>Argument</ui> in the file management task action.</caps:sentence>
                              <caps:sentence id="src162" class="srcSentence">  If you have specified<ui> -OwnerEmail [Source File Owner Email]</ui>, try removing this parameter.</caps:sentence>
                            </para>
                            <para>
                              <caps:sentence id="src163" class="srcSentence">If the file management task works successfully without <ui> -OwnerEmail [Source File Owner Email]</ui>, check that the unprotected files have a domain user listed as the file owner, rather than <ui>SYSTEM</ui>.</caps:sentence>
                              <caps:sentence id="src164" class="srcSentence">  To do this, use the <ui>Security</ui> tab for the file's properties, and then click <ui>Advanced</ui>.</caps:sentence>
                              <caps:sentence id="src165" class="srcSentence"> The <ui>Owner</ui> value is displayed immediately after the file <ui>Name</ui>.</caps:sentence>
                              <caps:sentence id="src166" class="srcSentence"> Also, verify that the file server is in the same domain or a trusted domain to lookup the user's email address from Active Directory Domain Services.</caps:sentence>
                            </para>
                          </listItem>
                        </list>
                      </listItem>
                      <listItem>
                        <para>
                          <caps:sentence id="src167" class="srcSentence">If you see the correct number of files in the report but the files are not protected, try protecting the files manually by using the <externalLink><linkText>Protect-RMSFile</linkText><linkUri>https://msdn.microsoft.com/library/azure/mt433201.aspx</linkUri></externalLink> cmdlet, to see if any errors are displayed.</caps:sentence>
                        </para>
                      </listItem>
                    </list>
                  </alert>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence id="src168" class="srcSentence">When you have confirmed that these tasks run successfully, you can close File Resource Manager.</caps:sentence>
                  <caps:sentence id="src169" class="srcSentence"> New files will be automatically protected and all files will be protected again when the schedules run.</caps:sentence>
                  <caps:sentence id="src170" class="srcSentence"> Re-protecting files ensures that any changes to the template are applied to the files.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
        </content>
        <sections>
          <section expanded="false" address="BKMK_RMSProtection_Script">
            <title>
              <caps:sentence id="src171" class="srcSentence">Windows PowerShell Script for Azure RMS protection by using File Server Resource Manager FCI</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src172" class="srcSentence">This section contains the sample script to copy and edit, as described in the preceding section.</caps:sentence>
              </para>
              <para>
                <legacyItalic>
                  <caps:sentence id="src173" class="srcSentence">
                    <legacyBold>Disclaimer</legacyBold>: This sample script is not supported under any Microsoft standard support program or service.</caps:sentence>
                  <caps:sentence id="src174" class="srcSentence"> This sample script is provided AS IS without warranty of any kind.</caps:sentence>
                </legacyItalic>
              </para>
              <code>&lt;# .SYNOPSIS Helper script to protect all file types with Azure RMS and FCI. .DESCRIPTION Protect files with Azure RMS and Windows Server FCI, using an RMS template ID. #&gt; param( [Parameter(Mandatory = $false)] [ValidateScript({ If($_ -eq "") {$true} else { if (Test-Path -Path $_ -PathType Leaf) {$true} else {throw "Can't find file specified"} } })] [string]$File, [Parameter(Mandatory = $false)] [string]$TemplateID, [Parameter(Mandatory = $false)] [string]$OwnerMail, [Parameter(Mandatory = $false)] [string]$AppPrincipalId = "&lt;enter your AppPrincipalId here&gt;", [Parameter(Mandatory = $false)] [string]$SymmetricKey = "&lt;enter your key here&gt;", [Parameter(Mandatory = $false)] [string]$BposTenantId = "&lt;enter your BposTenantId here&gt;" ) # script information [String] $Script:Version = 'version 1.0' [String] $Script:Name = "RMS-Protect-FCI.ps1" #global working variables [switch] $Script:isScriptProcess = $False # Controls the script process. If false, the script gracefully stops running. #**Functions (general helper)*************************************** function Get-ScriptName(){ return $MyInvocation.ScriptName.Substring($MyInvocation.ScriptName.LastIndexOf('\') + 1, $MyInvocation.ScriptName.LastIndexOf('.') - $MyInvocation.ScriptName.LastIndexOf('\') - 1) } #**Functions (script specific)************************************** function Check-Module{ param ([String]$Module = $(Throw "Module name not specified")) [bool]$isResult = $False #try to load the module if (get-module -list -name $Module) { import-module $Module if (get-module -name $Module ) { $isResult = $True } else { $isResult = $False } } else { $isResult = $False } return $isResult } function Protect-File ($ffile, $ftemplateId, $fownermail) { [bool] $returnValue = $false try { If ($OwnerMail -eq $null -or $OwnerMail -eq "") { $protectReturn = Protect-RMSFile -File $ffile -TemplateID $ftemplateId $returnValue = $true Write-Host ( "Information: " + "Protected File: $ffile with Template: $ftemplateId") } else { $protectReturn = Protect-RMSFile -File $ffile -TemplateID $ftemplateId -OwnerEmail $fownermail $returnValue = $true Write-Host ( "Information: " + "Protected File: $ffile with Template: $ftemplateId, set Owner: $fownermail") } } catch { Write-Host ( "ERROR" + "During protection of file: $ffile with Template: $ftemplateId") } return $returnValue } function Set-RMSConnection ($fappId, $fkey, $fbposId) { [bool] $returnValue = $false try { Set-RMSServerAuthentication -AppPrincipalId $fappId -Key $fkey -BposTenantId $fbposId Write-Host ("Information: " + "Connected to Azure RMS Service with BposTenantId: $fbposId using AppPrincipalId: $fappId") $returnValue = $true } catch { Write-Host ("ERROR" + "During connection to Azure RMS Service with BposTenantId: $fbposId using AppPrincipalId: $fappId") } return $returnValue } #**Main Script (Script)********************************************* Write-Host ("-== " + $Script:Name + " " + $Version + " ==-") $Script:isScriptProcess = $True # Validate Azure RMS connection by checking the module and then connection if ($Script:isScriptProcess) { if (Check-Module -Module RMSProtection){ $Script:isScriptProcess = $True } else { Write-Host ("The RMSProtection module is not loaded") -foregroundcolor "yellow" -backgroundcolor "black" $Script:isScriptProcess = $False } } if ($Script:isScriptProcess) { #Write-Host ("Try to connect to Azure RMS with AppId: $AppPrincipalId and BPOSID: $BposTenantId" ) if (Set-RMSConnection $AppPrincipalId $SymmetricKey $BposTenantId) { Write-Host ("Connected to Azure RMS") } else { Write-Host ("Couldn't connect to Azure RMS") -foregroundcolor "yellow" -backgroundcolor "black" $Script:isScriptProcess = $False } } #  Start working loop if ($Script:isScriptProcess) { if ( !(($File -eq $null) -or ($File -eq "")) ) { if (!(Protect-File -ffile $File -ftemplateId $TemplateID -fownermail $OwnerMail)) { $Script:isScriptProcess = $False } } } # Closing if (!$Script:isScriptProcess) { Write-Host "ERROR occurred during script process" -foregroundcolor "red" -backgroundcolor "black"} write-host ("-== " + $Script:Name + " " + $Version + "  ==-") if (!$Script:isScriptProcess) { exit(-1) } else {exit(0)}</code>
            </content>
          </section>
        </sections>
      </section>
      <section>
        <title>
          <caps:sentence id="src175" class="srcSentence">Modifying the instructions to selectively protect files</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src176" class="srcSentence">When you have the preceding instructions working, it's then very easy to modify them for a more sophisticated configuration.</caps:sentence>
            <caps:sentence id="src177" class="srcSentence"> For example, protect files by using the same script but only for files that contain personal identifiable information, and perhaps select a template that has more restrictive rights.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src178" class="srcSentence">To do this, use one of the built-in classification properties (for example, <ui>Personally Identifiable Information</ui>) or create your own new property.</caps:sentence>
            <caps:sentence id="src179" class="srcSentence"> Then create a new rule that uses this property.</caps:sentence>
            <caps:sentence id="src180" class="srcSentence"> For example, you might select the <ui>Content Classifier</ui>, choose the <ui>Personally Identifiable Information</ui> property with a value of <ui>High</ui>, and configure the string or expression pattern that identifies the file to be configured for this property (such as the  string "<userInputLocalizable>Date of Birth</userInputLocalizable>").</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src181" class="srcSentence">Now all you need to do is create a new file management task that uses the same script but perhaps with a different template, and configure the condition for the classification property that you have just configured.</caps:sentence>
            <caps:sentence id="src182" class="srcSentence"> For example, instead of the condition that we configured previously (<ui>RMS</ui> property, <ui>Equal</ui>, <ui>Yes</ui>), select the <ui>Personally Identifiable Information</ui> property with the <ui>Operator</ui> value set to <ui>Equal</ui> and the <ui>Value</ui> of <ui>High</ui>.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>