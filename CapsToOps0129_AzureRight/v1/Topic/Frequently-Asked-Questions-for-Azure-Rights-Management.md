---
title: Preguntas m&#225;s frecuentes de Azure Rights Management
ms.custom: na
ms.reviewer: na
ms.service: rights-management
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 71ce491f-41c1-4d15-9646-455a6eaa157d
---
# Preguntas m&#225;s frecuentes de Azure Rights Management
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="es-ES">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="4d96c857b012f7cec7f214c980a386a0" id="tgt1" class="tgtSentence">Algunas de las preguntas más frecuentes sobre Microsoft <token>aad_rightsmanagement_1</token>, también conocido como Azure RMS:</caps:sentence>
        </para>
      </introduction>
      <section expanded="false">
        <title>
          <caps:sentence sentenceid="66e97ac10718c1ed4aae97664b9ceeba" id="tgt2" class="tgtSentence">¿Qué necesito para implementar Azure RMS y cómo lo hago?</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="c5ecce72374861c6f7864f49edc30a66" id="tgt3" class="tgtSentence">En primer lugar, consulte en <link xlink:href="dc78321d-d759-4653-8818-80da74b6cdeb">Requirements for Azure Rights Management</link> información sobre las opciones de suscripción en la nube, cómo puede usar los servidores locales con Azure RMS, qué escenarios de implementación no se admiten actualmente, qué dispositivos y aplicaciones admiten Azure RMS y un vínculo si necesita una lista de direcciones IP y nombres de domino para firewalls o servidores proxy.</caps:sentence>
            <caps:sentence sentenceid="7fcb498824e3a6ec60b27e5c4f90f964" id="tgt4" class="tgtSentence"> También puede consultar otros temas en la sección <link xlink:href="5214667c-ec69-42ca-8bbf-8cb22da8c62e">Getting Started with Azure Rights Management</link> para comprender los aspectos básicos de cómo <token>aad_rightsmanagement_1</token> puede ayudar a proteger los datos de su organización, cómo funciona con las aplicaciones y cómo es en comparación con la versión local de Active Directory Rights Management, así como los términos y las abreviaturas específicas de <token>aad_rightsmanagement_1</token>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="cb5bcd6fd4323cdf9e14a549035020aa" id="tgt5" class="tgtSentence">Cuando esté listo para probar Azure RMS por su cuenta o implementarlo en su organización, consulte el <link xlink:href="086600c2-c5d8-47ec-a4c0-c782e1797486">Azure Rights Management Deployment Roadmap</link> para ver una lista de pasos con vínculos a más información e instrucciones de procedimientos.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="bc3599c8ee34fa8327e1205df41b7331" id="tgt6" class="tgtSentence">Si necesita más información, recursos y opciones de soporte, consulte <link xlink:href="7cc73d92-27d6-49ff-a8ab-2fae73519b4b">Information and Support for Azure Rights Management</link>.</caps:sentence>
          </para>
        </content>
      </section>
      <section expanded="false">
        <title>
          <caps:sentence sentenceid="1b22c8a140757b30729701e444aa51d0" id="tgt7" class="tgtSentence">¿Puedo integrar Azure RMS con mis servidores locales?</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="4f7b50bec76bcf2b862eeb2140701427" id="tgt8" class="tgtSentence">Sí.</caps:sentence>
            <caps:sentence sentenceid="ebde2dbae9729f4683d3fadee4dcc5bb" id="tgt9" class="tgtSentence"> Azure RMS se puede integrar con sus servidores locales, como servidores de archivos de Exchange Server, SharePoint y Windows.</caps:sentence>
            <caps:sentence sentenceid="8a7d645e64fa2354daac80a268a1f82c" id="tgt10" class="tgtSentence"> Para hacerlo, use el <externalLink><linkText>conector de Rights Management</linkText><linkUri>https://technet.microsoft.com/library/dn375964.aspx</linkUri></externalLink>.</caps:sentence>
            <caps:sentence sentenceid="8c7d68d1fd238ed28b87fb4c6c045969" id="tgt11" class="tgtSentence"> O bien, si solo le interesa usar la infraestructura de clasificación de archivos (FC) con Windows Server, puede usar los <externalLink><linkText>cmdlets de protección de RMS</linkText><linkUri>https://technet.microsoft.com/library/mt601315(v=ws.10).aspx</linkUri></externalLink>.</caps:sentence>
            <caps:sentence sentenceid="23b91fac6d3e35a66220626bd4f811e9" id="tgt12" class="tgtSentence"> También puede sincronizar y federar los controladores de dominio de Active Directory con Azure AD para ofrecer una experiencia de autenticación más sencilla a los usuarios, por ejemplo, mediante el uso de <externalLink><linkText>Azure AD Connect</linkText><linkUri>http://azure.microsoft.com/documentation/articles/active-directory-aadconnect/</linkUri></externalLink>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="b6ba4a812957a7f9524040e4ae9898e3" id="tgt13" class="tgtSentence">Azure RMS genera automáticamente y administra los certificados XrML según sea necesario, por lo que no usa una PKI local.</caps:sentence>
            <caps:sentence sentenceid="081e850b6866d79dcee8c7a027e44089" id="tgt14" class="tgtSentence"> Para obtener más información sobre la manera en que Azure RMS usa los certificados, vea la sección <link xlink:href="aeeebcd7-6646-4405-addf-ee1cc74df5df#BKMK_Walthrough">Walkthrough of how Azure RMS works: First use, content protection, content consumption</link> del tema <link xlink:href="aeeebcd7-6646-4405-addf-ee1cc74df5df">What is Azure Rights Management?</link>.</caps:sentence>
          </para>
        </content>
      </section>
      <section expanded="false">
        <title>
          <caps:sentence sentenceid="c8014cba12cbd17f666b2c2fb53e9da2" id="tgt15" class="tgtSentence">Tengo una implementación híbrida de Exchange con algunos usuarios de Exchange Online y otros de Exchange Server. ¿Es compatible con Azure RMS?</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="89e8d84f8a5f0199c7f288e46ffa29dc" id="tgt16" class="tgtSentence">Desde luego, y lo mejor es que los usuarios podrán proteger sin problemas y consumir correos electrónicos y archivos adjuntos protegidos en las dos implementaciones de Exchange.</caps:sentence>
            <caps:sentence sentenceid="46e591e54fe9343b34c22f4433261d0f" id="tgt17" class="tgtSentence"> Para esta configuración, <externalLink><linkText>active Azure RMS</linkText><linkUri>https://technet.microsoft.com/library/jj658941.aspx</linkUri></externalLink> y <externalLink><linkText>habilite IRM para Exchange Online</linkText><linkUri>https://technet.microsoft.com/library/dn151475(v=exchg.150).aspx</linkUri></externalLink>. A continuación, <externalLink><linkText>implemente y configure el conector RMS</linkText><linkUri>https://technet.microsoft.com/library/dn375964.aspx</linkUri></externalLink> para Exchange Server.</caps:sentence>
          </para>
          <para></para>
        </content>
      </section>
      <section expanded="false">
        <title>
          <caps:sentence sentenceid="7e48ebc350fc47296a3eeecc3a0f7eb7" id="tgt18" class="tgtSentence">Si implemento Azure RMS en producción, ¿estará mi empresa atada a la solución o se arriesgará a perder el acceso a los contenidos que protegimos con Azure RMS?</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="6790155640269df973548e83a49b5474" id="tgt19" class="tgtSentence">No, siempre tendrá el control de los datos y seguirá teniendo acceso a ellos, incluso si decide dejar de usar Azure RMS.</caps:sentence>
            <caps:sentence sentenceid="41acc90190a372092e38a45226932109" id="tgt20" class="tgtSentence"> Para obtener más información, vea <link xlink:href="0b1c2064-0d01-45ae-a541-cebd7fd762ad">Decommissioning and Deactivating Azure Rights Management</link>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="682e5165d1c1dbc9e6a1724dd5654952" id="tgt21" class="tgtSentence">Sin embargo, antes de retirar la implementación de Azure RMS, nos gustaría conocer su opinión y comprender por qué tomó esta decisión.</caps:sentence>
            <caps:sentence sentenceid="aa5bc97fbf1dc93d73bf9a13e9ec5747" id="tgt22" class="tgtSentence"> Si Azure RMS no satisface sus requisitos empresariales, consúltenos para informarse de si planeamos una funcionalidad nueva para el futuro cercano o si hay alternativas.</caps:sentence>
            <caps:sentence sentenceid="e18f41ac96a2f389622734cd84d43883" id="tgt23" class="tgtSentence"> Envíe un mensaje de correo electrónico a <externalLink><linkText>AskIPTeam@Microsoft.com</linkText><linkUri>mailto:askipteam@microsoft.com?subject=Planning%20to%20decommission%20Azure%20RMS</linkUri></externalLink>. Estaremos encantados de analizar sus requisitos técnicos y empresariales.</caps:sentence>
          </para>
        </content>
      </section>
      <section expanded="false">
        <title>
          <caps:sentence sentenceid="c6222a06b98b2c25c2abed1a67f82f0a" id="tgt24" class="tgtSentence">¿Puedo controlar quiénes de mis usuarios pueden usar Azure RMS para proteger el contenido?</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="83e1de908181d50a284ea38c65bf5f05" id="tgt25" class="tgtSentence">Sí, Azure RMS tiene controles de incorporación de usuario para este escenario.</caps:sentence>
            <caps:sentence sentenceid="45f94fee671a4226aa16794673588fc6" id="tgt26" class="tgtSentence"> Para obtener más información, consulte la sección <link xlink:href="f8707e01-b239-4d1a-a1ea-0d1cf9a8d214#BKMK_OnboardingControls">Configuring onboarding controls for a phased deployment</link> en el tema <link xlink:href="f8707e01-b239-4d1a-a1ea-0d1cf9a8d214">Activating Azure Rights Management</link>.</caps:sentence>
          </para>
        </content>
      </section>
      <section expanded="false">
        <title>
          <caps:sentence sentenceid="84c2eeeb418e723ee15acd26e69a0fa7" id="tgt27" class="tgtSentence">¿Se puede impedir que los usuarios compartan documentos protegidos con organizaciones específicas?</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="f3c1f7441a84b9022a16ac1fb1197c03" id="tgt28" class="tgtSentence">Una de las mayores ventajas de Azure RMS es que admite la colaboración de negocio a negocio sin tener que configurar relaciones de confianza explícitas para cada organización asociada, ya que Azure AD se encarga de la autenticación.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="1ff73e65215686a087cbbb35d17dd780" id="tgt29" class="tgtSentence">No hay ninguna opción de administración para impedir que los usuarios compartan documentos con organizaciones específicas de forma segura.</caps:sentence>
            <caps:sentence sentenceid="e6d3a6d7acc1fcdaf2159e3395d84868" id="tgt30" class="tgtSentence"> Por ejemplo, supongamos que desea bloquear una organización en la que no confía o que tiene un negocio en competencia.</caps:sentence>
            <caps:sentence sentenceid="c4b81dd3d2e76ea1d85e1bc649ae27a4" id="tgt31" class="tgtSentence"> Impedir que Azure RMS envíe documentos protegidos a los usuarios de estas organizaciones no tendría sentido, ya que los usuarios compartirían los documentos sin protección, lo que probablemente sea lo último que desea que ocurra en este escenario.</caps:sentence>
            <caps:sentence sentenceid="d61dba8dbf048174d56c5ad6fc76cd31" id="tgt32" class="tgtSentence"> Por ejemplo, no podría identificar quién comparte documentos confidenciales de la compañía ni con qué usuarios de esas organizaciones lo está haciendo, lo que sí es posible cuando el documento (o correo electrónico) está protegido con Azure RMS.</caps:sentence>
          </para>
        </content>
      </section>
      <section expanded="false">
        <title>
          <caps:sentence sentenceid="df3090f3d0e98d052437ea89c22d1443" id="tgt33" class="tgtSentence">Cuando comparto un documento protegido con una persona ajena a mi organización, ¿cómo se autentica ese usuario?</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="c9f4806d21bfa786778a36cc75adc9c7" id="tgt34" class="tgtSentence">Azure RMS siempre usa una cuenta de Azure Active Directory y una dirección de correo electrónico asociada para la autenticación de usuarios, lo que facilita a los administradores la colaboración de negocio a negocio.</caps:sentence>
            <caps:sentence sentenceid="dba8742d75f22de08b0212c977f47aed" id="tgt35" class="tgtSentence"> Si la otra organización usa servicios de Azure, los usuarios ya tendrán cuentas en Azure Active Directory, incluso si dichas cuentas se crearon y se administraron localmente y después se sincronizaron con Azure.</caps:sentence>
            <caps:sentence sentenceid="a3f01ff5af1e49f799f967e235a42e93" id="tgt36" class="tgtSentence">  Si la organización tiene Office 365 de forma encubierta, este servicio también usa Azure Active Directory para las cuentas de usuario.</caps:sentence>
            <caps:sentence sentenceid="b753ec1f95a4f59d5bf6664f33ea9318" id="tgt37" class="tgtSentence">  Si la organización del usuario no tiene cuentas administradas en Azure, los usuarios pueden suscribirse a <externalLink><linkText>RMS para usuarios</linkText><linkUri>https://technet.microsoft.com/library/dn592127.aspx</linkUri></externalLink>, que crea un inquilino y un directorio de Azure no administrados para la organización con una cuenta para el usuario, de modo que este usuario se pueda autenticar para Azure RMS.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="cdb24e579b3c1f6657a898e7b9932bb6" id="tgt38" class="tgtSentence">El método de autenticación de estas cuentas puede variar, en función de cómo configurase el administrador de la otra organización las cuentas de Azure Active Directory.</caps:sentence>
            <caps:sentence sentenceid="a198155cd20332111965af00518202a2" id="tgt39" class="tgtSentence"> Por ejemplo, podrían usar contraseñas creadas para estas cuentas, Multi-Factor Authentication (MFA), federación o contraseñas creadas en Servicios de dominio de Active Directory y después sincronizadas con Active Directory de Azure.</caps:sentence>
          </para>
        </content>
      </section>
      <section expanded="false">
        <title>
          <caps:sentence sentenceid="9ccd2e033533c18ef21c1fe22fa7bcb7" id="tgt40" class="tgtSentence">¿Puedo agregar usuarios ajenos a mi empresa a plantillas personalizadas?</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="4f7b50bec76bcf2b862eeb2140701427" id="tgt41" class="tgtSentence">Sí.</caps:sentence>
            <caps:sentence sentenceid="1c1829ebbd5fe2541bc2b0b3a9ebd548" id="tgt42" class="tgtSentence">  Si crea plantillas personalizadas que los usuarios finales (y los administradores) puedan seleccionar desde las aplicaciones, hará que les resulte más rápido y sencillo aplicar la protección de la información mediante las directivas predefinidas que especifique.</caps:sentence>
            <caps:sentence sentenceid="3af81fe0f8f0e08ea7e7a420f3f7b563" id="tgt43" class="tgtSentence"> Uno de los valores de la plantilla define quién puede acceder al contenido, y puede especificar usuarios y grupos de su organización y usuarios ajenos a su organización.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="6d7650435f018fbde17dd23ab76eab34" id="tgt44" class="tgtSentence">Para especificar usuarios de fuera de su organización, use el <externalLink><linkText>módulo de Windows PowerShell para Azure Rights Management</linkText><linkUri>https://technet.microsoft.com/library/jj585012.aspx</linkUri></externalLink>: </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="c74daf49e8552e917d5220f663e6f184" id="tgt45" class="tgtSentence">
                  <embeddedLabel>Use un objeto de Rights Definition para crear o actualizar una plantilla</embeddedLabel>.</caps:sentence>
                <caps:sentence sentenceid="015c7094d3511e4d1d805d366615b5f8" id="tgt46" class="tgtSentence">    especifique las direcciones de correo electrónico externas y sus derechos en un objeto de Rights Definition, que después usará para crear o actualizar una plantilla.</caps:sentence>
                <caps:sentence sentenceid="bbca5d1c6ffa325d2c59e24a01f11ee1" id="tgt47" class="tgtSentence"> Especifique el objeto de Rights Definition mediante el cmdlet <externalLink><linkText>New-AadrmRightsDefinition</linkText><linkUri>https://msdn.microsoft.com/library/azure/dn727080.aspx</linkUri></externalLink> para crear una variable y, a continuación, suministrar esta variable al parámetro -RightsDefinition con el cmdlet <externalLink><linkText>Add-AadrmTemplateProperty</linkText><linkUri>https://msdn.microsoft.com/library/azure/dn727075.aspx</linkUri></externalLink> (para una nueva plantilla) o <externalLink><linkText>Set-AadrmTemplateProperty</linkText><linkUri>https://msdn.microsoft.com/library/azure/dn727076.aspx</linkUri></externalLink> (si modifica una plantilla existente).</caps:sentence>
                <caps:sentence sentenceid="a293e7820e4687b9b9e81e7ece359ce6" id="tgt48" class="tgtSentence"> Sin embargo, si agrega estos usuarios a una plantilla existente, tendrá que definir objetos de Rights Definition para los grupos existentes en las plantillas y no solo los usuarios externos.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="8c8621193341ff5a7694aec1db18e98c" id="tgt49" class="tgtSentence">Para obtener más información sobre las plantillas personalizadas, consulte <link xlink:href="1775d8d0-9a59-42c8-914f-ce285b71ac1c">Configuring Custom Templates for Azure Rights Management</link>.</caps:sentence>
          </para>
        </content>
      </section>
      <section expanded="false">
        <title>
          <caps:sentence sentenceid="3f66f4ab6ebff3e2e2d8050222e45306" id="tgt50" class="tgtSentence">¿Qué dispositivos y tipos de archivo admite Azure RMS?</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="e355ec3a33c4cc385e086c9d6b2d821d" id="tgt51" class="tgtSentence">Para obtener una lista de dispositivos compatibles, consulte la sección <link xlink:href="dc78321d-d759-4653-8818-80da74b6cdeb#BKMK_SupportedDevices">Client devices that support Azure RMS</link> en el tema <link xlink:href="dc78321d-d759-4653-8818-80da74b6cdeb">Requirements for Azure Rights Management</link>.</caps:sentence>
            <caps:sentence sentenceid="999a47c3434239e19cc823dcdac26c56" id="tgt52" class="tgtSentence"> Dado que, actualmente, no todos los dispositivos compatibles admiten todas las funciones de RMS, consulte también la tabla <link xlink:href="dc78321d-d759-4653-8818-80da74b6cdeb#BKMK_ClientCapabilities">Client device capabilities</link> de este mismo tema.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="6d4d1bffbc1e352b767cbdf8a2219bb3" id="tgt53" class="tgtSentence">Azure RMS admite todos los tipos de archivo.</caps:sentence>
            <caps:sentence sentenceid="8fdac9a6a1537847209c06148b89dfcf" id="tgt54" class="tgtSentence"> Para archivos de texto, imagen, Microsoft Office (Word, Excel, PowerPoint), archivos .pdf y otros tipos de archivo de aplicaciones, Azure RMS proporciona protección nativa que incluye cifrado y cumplimiento de derechos (permisos).</caps:sentence>
            <caps:sentence sentenceid="ed009ac3bc4655e965b15d1549f808d4" id="tgt55" class="tgtSentence"> Para las demás aplicaciones y tipos de archivo, la protección genérica proporciona encapsulación de archivos y autenticación para comprobar si un usuario está autorizado para abrir el archivo.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="107b51ebb845de0e0d95e3df90d63406" id="tgt56" class="tgtSentence">Para obtener una lista de extensiones de nombre de archivo que se admiten de forma nativa en Azure RMS, consulte la sección <externalLink><linkText>Tipos de archivo y extensiones de nombre de archivo compatibles</linkText><linkUri>http://technet.microsoft.com/library/dn339003.aspx</linkUri></externalLink> en la <externalLink><linkText>Guía del administrador de la aplicación de uso compartido de Rights Management</linkText><linkUri>http://technet.microsoft.com/library/dn339003.aspx</linkUri></externalLink>.</caps:sentence>
            <caps:sentence sentenceid="2431cba45924083b6773d3ee8e72a814" id="tgt57" class="tgtSentence"> Se admiten las extensiones de nombre de archivo que no están enumeradas si se usa la aplicación para uso compartido de RMS, que aplica automáticamente la protección genérica a estos archivos.</caps:sentence>
          </para>
        </content>
      </section>
      <section expanded="false">
        <title>
          <caps:sentence sentenceid="fe22b5c484b0dc62441e36b985f02d28" id="tgt58" class="tgtSentence">¿Cuándo se admitirá la migración de AD RMS?</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="412e0d72645731f0af67d46701800e7c" id="tgt59" class="tgtSentence">Inicialmente, Azure RMS no admitía la migración de una implementación local de Rights Management, como AD RMS.</caps:sentence>
            <caps:sentence sentenceid="75b3ded7e5c9dcc9482c5af191ea48b1" id="tgt60" class="tgtSentence"> Pero ahora sí se admite.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="d2efb72ac933673a55e3c729d3415e80" id="tgt61" class="tgtSentence">Para obtener más información, vea <link xlink:href="828cf1f7-d0e7-4edf-8525-91896dbe3172">Migrating from AD RMS to Azure Rights Management</link>.</caps:sentence>
          </para>
        </content>
      </section>
      <section expanded="false">
        <title>
          <caps:sentence sentenceid="b54518f2fbc3f6f457defcf5b367b403" id="tgt62" class="tgtSentence">Nos interesa usar BYOK con Azure RMS, pero por lo visto no es compatible con Exchange Online. ¿Qué nos aconsejan?</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="9f403e1848ea4c4c366bf3ffe28e6753" id="tgt63" class="tgtSentence">No permitan que esta limitación actual retrase su implementación de Azure RMS.</caps:sentence>
            <caps:sentence sentenceid="04d902db517618a7b9131144662f0c31" id="tgt64" class="tgtSentence"> Si tiene Exchange Online y desea usar Aportar su propia clave (BYOK), se recomienda implementar ahora Azure RMS en el modo de administración de claves predeterminado, donde Microsoft genera y administra su clave.</caps:sentence>
            <caps:sentence sentenceid="8e821538be483d04f7dc1dbcb26a131f" id="tgt65" class="tgtSentence"> De este modo, obtendrá todas las ventajas que supone proteger ahora sus archivos y mensajes de correo electrónico importantes, con la opción de pasarse a BYOK más adelante (por ejemplo, cuando Exchange Online admita BYOK).</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="037e12350dbfd149117746fd73dea849" id="tgt66" class="tgtSentence">Sin embargo, si las directivas de la empresa requieren que se use un módulo de seguridad de hardware (HSM) y esto podría bloquear la implementación de Azure RMS, otra opción es implementar ahora Azure RMS con BYOK, con una funcionalidad de RMS reducida para Exchange.</caps:sentence>
            <caps:sentence sentenceid="43557a0c9c4412ee3bd2f0adf297da7e" id="tgt67" class="tgtSentence"> Para obtener más información, consulte la sección <link xlink:href="f0d33c5f-a6a6-44a1-bdec-5be1bc8e1e14#BKMK_Pricing">BYOK pricing and restrictions</link> en el tema <link xlink:href="f0d33c5f-a6a6-44a1-bdec-5be1bc8e1e14">Planning and Implementing Your Azure Rights Management Tenant Key</link>.</caps:sentence>
          </para>
        </content>
      </section>
      <section expanded="false">
        <title>
          <caps:sentence sentenceid="9a1298ce82e67b41b6557655da7fa899" id="tgt68" class="tgtSentence">Una característica que me interesa no funciona con las bibliotecas protegidas de SharePoint. ¿Está prevista la compatibilidad con esta característica?</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="ccf3f9ba13728f3d5687a0ee5c399a29" id="tgt69" class="tgtSentence">Actualmente, SharePoint es compatible con documentos protegidos de RMS mediante las bibliotecas protegidas de IRM, que no son compatibles con las plantillas personalizadas, el seguimiento de documentos y otras capacidades.</caps:sentence>
            <caps:sentence sentenceid="da4af3fd5aadbb2591cdf6561c2e662c" id="tgt70" class="tgtSentence">  Para obtener más información, expanda la sección <link xlink:href="ea09cbc5-b98b-444e-8b60-5bc3cb199c36#BKMK_SharePointOnline">SharePoint Online and OneDrive for Business: IRM Configuration</link> del tema <link xlink:href="2cdc7bde-4044-4021-b887-11476f99afd9">How Applications Support Azure Rights Management</link>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="03e93bb69ac4e3d8c55e9ee450ee0248" id="tgt71" class="tgtSentence">Si está interesado en una función específica que todavía no es compatible, no se pierda los anuncios que se publican en el <externalLink><linkText>blog del equipo de RMS</linkText><linkUri>http://blogs.technet.com/b/rms/</linkUri></externalLink>.</caps:sentence>
          </para>
        </content>
      </section>
      <section expanded="false">
        <title>
          <caps:sentence sentenceid="d48718cc268184e64552069dcea78f35" id="tgt72" class="tgtSentence">¿Cómo configuro OneDrive para la Empresa en SharePoint Online para que los usuarios puedan compartir con seguridad sus archivos con personas de dentro y fuera de la empresa?</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="4f0da6314a8b90c6eda3f92fa3669851" id="tgt73" class="tgtSentence">De forma predeterminada, como administrador de Office 365, no es usted quien lo configura; lo hacen los usuarios.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="7a1b1f7d42509e3a2807cf175e2d68b8" id="tgt74" class="tgtSentence">Del mismo modo que el administrador del sitio de SharePoint habilita y configura IRM para una biblioteca de SharePoint de su propiedad, OneDrive para la Empresa se ha diseñado para que los usuarios habiliten y configuren IRM para su propia biblioteca de OneDrive para la Empresa.</caps:sentence>
            <caps:sentence sentenceid="1fcba590d90f67460e61d310d5c659c6" id="tgt75" class="tgtSentence">  Sin embargo, gracias a PowerShell, puede hacerlo por ellos.</caps:sentence>
            <caps:sentence sentenceid="e0403bbc51682027a61dff6479d80953" id="tgt76" class="tgtSentence"> Para obtener instrucciones, expanda la sección <link xlink:href="ea09cbc5-b98b-444e-8b60-5bc3cb199c36#BKMK_SharePointOnline">SharePoint Online and OneDrive for Business: IRM Configuration</link> del artículo <link xlink:href="ea09cbc5-b98b-444e-8b60-5bc3cb199c36">Configuring Applications for Azure Rights Management</link>.</caps:sentence>
          </para>
        </content>
      </section>
      <section expanded="false">
        <title>
          <caps:sentence sentenceid="b77bdcff0dfba49de85c2aadb2595a0a" id="tgt77" class="tgtSentence">¿Hay trucos o sugerencias para una correcta implementación de RMS?</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="8d81df08da0f16f8b4cece4d795b1181" id="tgt78" class="tgtSentence">Después de supervisar muchas implementaciones y escuchar a nuestros clientes, socios, asesores e ingenieros de soporte, una de las mayores sugerencias que le podemos dar por la experiencia es: <legacyBold>Diseño e implementación de directivas de permisos sencillas</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="c467021ec53d51a7fd74ca4208f7235e" id="tgt79" class="tgtSentence">Dado que Azure RMS admite el uso compartido seguro con cualquiera, puede ser ambicioso con el alcance de la protección de la información.</caps:sentence>
            <caps:sentence sentenceid="b01d59d6c85881e54410eda3d20c8d86" id="tgt80" class="tgtSentence"> Pero debe ser conservador en cuanto a las directivas de derechos.</caps:sentence>
            <caps:sentence sentenceid="3a99033be49fa1839b8378894d1b0e29" id="tgt81" class="tgtSentence"> Para muchas organizaciones, el mayor impacto comercial se centra en evitar las pérdidas de datos mediante la plantilla predeterminada de directivas de derechos que restringe el acceso a las personas de su organización.</caps:sentence>
            <caps:sentence sentenceid="313d4553abbd081c0def61ab0a6d2cba" id="tgt82" class="tgtSentence"> Claro que puede alcanzar un nivel mucho más pormenorizado si es necesario (evitar que los usuarios impriman, editen, etc.). Pero las restricciones más pormenorizadas deben ser la excepción para los documentos que realmente necesitan un alto nivel de seguridad. Además, no debe implementar estas directivas más restrictivas desde el primer día, sino que conviene planificar un enfoque más escalonado.</caps:sentence>
          </para>
        </content>
      </section>
      <section expanded="false">
        <title>
          <caps:sentence sentenceid="eb1fa3db8ac747ad8cc849aa7c3267d0" id="tgt83" class="tgtSentence">¿Qué características se pueden usar y cuáles no con las diferentes suscripciones de Azure RMS?</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="01ac793622ae26ffa5e03967638328d2" id="tgt84" class="tgtSentence">Para la suscripciones de pago que admiten Azure RMS (Office 365, Azure RMS Premium y Enterprise Mobility Suite), hay algunas diferencias en las características RMS que se admiten.</caps:sentence>
            <caps:sentence sentenceid="1fd7bc4e552e216f11e24cd8c2ecdfe4" id="tgt85" class="tgtSentence"> Para obtener una lista, consulte <externalLink><linkText>Comparación de las ofertas de Rights Management Services (RMS)</linkText><linkUri>http://technet.microsoft.com/dn858608</linkUri></externalLink>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="6a966ec301895f59ee36fb5e06a52881" id="tgt86" class="tgtSentence">La suscripción gratuita compatible con Azure RMS (RMS Para individuos) admite el consumo de contenido que se ha protegido mediante Azure RMS.</caps:sentence>
            <caps:sentence sentenceid="012ce4626edad7510c0e7a2f19406b64" id="tgt87" class="tgtSentence"> Para obtener más información, vea <link xlink:href="2efcb440-fefd-45e9-872b-f471573aadf2">RMS for Individuals and Azure Rights Management</link>.</caps:sentence>
          </para>
        </content>
      </section>
      <section expanded="false">
        <title>
          <caps:sentence sentenceid="5b78ef16b7af2eaa36d347ce97036b8c" id="tgt88" class="tgtSentence">¿Dónde puedo obtener información técnica sobre la suscripción gratuita de Azure RMS (RMS para usuarios), por ejemplo sobre cómo funciona, cómo controlar las cuentas y qué dominios no se pueden utilizar?</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="e8d0e22dea68cffd2ed1f89dd299a84f" id="tgt89" class="tgtSentence">Encontrará respuestas a estas preguntas en el tema <link xlink:href="2efcb440-fefd-45e9-872b-f471573aadf2">RMS for Individuals and Azure Rights Management</link>.</caps:sentence>
          </para>
        </content>
      </section>
      <section expanded="false">
        <title>
          <caps:sentence sentenceid="b3f526c04ff9371c9aa39b019b4b33c7" id="tgt90" class="tgtSentence">¿Cómo recupero el acceso a los archivos que protegió un empleado que ya no trabaja en la organización?</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="0aec1192fb6556e951374a7acd0ac3d1" id="tgt91" class="tgtSentence">Use la característica de superusuario de Azure RMS, que permite que los usuarios autorizados tengan derechos de propietario completos para todas las licencias de uso concedidas por el inquilino de RMS de su organización.</caps:sentence>
            <caps:sentence sentenceid="2039f6db660b10183044be2f62ddc42b" id="tgt92" class="tgtSentence"> Esta misma función permite que los servicios autorizados indicen e inspeccionen archivos, según sea necesario.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="c1303fab43eb1931fed4ebea080ea6d3" id="tgt93" class="tgtSentence">Para obtener más información, vea <link xlink:href="acb4c00b-d3a9-4d74-94fe-91eeb481f7e3">Configuring Super Users for Azure Rights Management and Discovery Services or Data Recovery</link>.</caps:sentence>
          </para>
        </content>
      </section>
      <section expanded="false">
        <title>
          <caps:sentence sentenceid="49a27bce910581cb71979b0d80091b77" id="tgt94" class="tgtSentence">¿Puede impedir Rights Management las capturas de pantalla?</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="76c02cc38b332d0f345ccd0ebb8d95e9" id="tgt95" class="tgtSentence">Rights Management bloquea las capturas de pantalla de la mayoría de las herramientas de captura de pantalla que se utilizan habitualmente, lo que puede ayudar a evitar la divulgación accidental o por negligencia de información confidencial.</caps:sentence>
            <caps:sentence sentenceid="bea5f521ac8c215c2ade0dbd40aab59d" id="tgt96" class="tgtSentence"> Sin embargo, existen muchas formas en que un usuario puede compartir datos que se muestran en una pantalla y hacer una captura de pantalla es solo un método.</caps:sentence>
            <caps:sentence sentenceid="f76115b2526bdfa63dbe91aa6c31e1a2" id="tgt97" class="tgtSentence"> Por ejemplo, un usuario decidido a compartir la información mostrada puede tomar una foto de ella con su teléfono con cámara, volver a escribir los datos o simplemente transmitírsela verbalmente a alguien.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="05d71a7f430be36cf381d4fe0adafc37" id="tgt98" class="tgtSentence">Como demuestran estos ejemplos, la tecnología por sí sola no siempre puede impedir que los usuarios compartan datos que no deberían.</caps:sentence>
            <caps:sentence sentenceid="4d76bf3ba8449ef2a0e4d786a77d3140" id="tgt99" class="tgtSentence"> Aunque Rights Management puede ayudar a proteger sus datos importantes mediante directivas de autorización y uso, esta solución de administración de derechos empresariales debe utilizarse con otros controles.</caps:sentence>
            <caps:sentence sentenceid="7f351cedcf8c8f73242f71a01657a592" id="tgt100" class="tgtSentence"> Por ejemplo, implemente seguridad física, preste especial atención a aquellas personas con acceso autorizado a los datos de su organización e invierta en la educación de los usuarios para que sepan qué datos no deben compartir.</caps:sentence>
          </para>
        </content>
      </section>
      <section expanded="false">
        <title>
          <caps:sentence sentenceid="d27c144c572eb860768eac4e1058714b" id="tgt101" class="tgtSentence">¿Dónde puedo encontrar información complementaria para Azure RMS, como información de tipo legal, de cumplimiento y contratos de nivel de servicio (SLA)?</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="56ef49ae0fc7e5b87e4af6a2164f68de" id="tgt102" class="tgtSentence">Azure RMS admite otros servicios y también se basa en otros servicios.</caps:sentence>
            <caps:sentence sentenceid="5bee4ed4452fcc7b27072e98986a833e" id="tgt103" class="tgtSentence"> Si está buscando información relacionada con Azure RMS pero no acerca de cómo utilizar el servicio Azure RMS, compruebe los recursos siguientes:</caps:sentence>
          </para>
          <para>
            <embeddedLabel>
              <caps:sentence sentenceid="89043590189b057ac4e9ec90f1e74bb2" id="tgt104" class="tgtSentence">Información legal y privacidad:</caps:sentence>
            </embeddedLabel>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="20b7e653d85bae085b74ebcc1d28f2e2" id="tgt105" class="tgtSentence">Para información contractual de Microsoft Azure: <externalLink><linkText>Contrato de Microsoft Azure</linkText><linkUri>http://azure.microsoft.com/support/legal/subscription-agreement/</linkUri></externalLink></caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="0c7b4288bfc709282b0c9cce4fef2aa3" id="tgt106" class="tgtSentence">Para información de privacidad de Microsoft Azure: <externalLink><linkText>Declaración de privacidad de Microsoft Azure</linkText><linkUri>http://azure.microsoft.com/support/legal/privacy-statement/</linkUri></externalLink></caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <embeddedLabel>
              <caps:sentence sentenceid="11c6431e2060fc45be8319d264707565" id="tgt107" class="tgtSentence">Seguridad, cumplimiento y auditoría:</caps:sentence>
            </embeddedLabel>
          </para>
          <para>
            <caps:sentence sentenceid="2de56792e8f9a8b3af24f7c997c4e216" id="tgt108" class="tgtSentence">Vea la sección <link xlink:href="aeeebcd7-6646-4405-addf-ee1cc74df5df#BKMK_RMScompliance">Security, compliance, and regulatory requirements</link> del tema <link xlink:href="aeeebcd7-6646-4405-addf-ee1cc74df5df">What is Azure Rights Management?</link>.</caps:sentence>
            <caps:sentence sentenceid="e7fff03a157bc33b1fd16558fd9b5d0b" id="tgt109" class="tgtSentence"> Además:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="6bef01bcc0e06cc805a3165641c15c63" id="tgt110" class="tgtSentence">Para certificaciones externas de Azure RMS: <externalLink><linkText>Centro de confianza de Microsoft Azure</linkText><linkUri>http://azure.microsoft.com/support/trust-center/</linkUri></externalLink></caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="5cb179fb3cb3bd2f96d302e4ef1163df" id="tgt111" class="tgtSentence">Para obtener información sobre FIPS 140: <externalLink><linkText>Validación conforme a FIPS 140</linkText><linkUri>https://technet.microsoft.com/library/security/cc750357.aspx</linkUri></externalLink></caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <embeddedLabel>
              <caps:sentence sentenceid="64fc3324d3d4f36ac64377372a054808" id="tgt112" class="tgtSentence">Contratos de nivel de servicio:</caps:sentence>
            </embeddedLabel>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="f9b35ed91b30a06e94c8a213dfd88cc4" id="tgt113" class="tgtSentence">Contrato de nivel de servicio para Azure RMS, por país seleccionado: <externalLink><linkText>Contrato de nivel de servicio</linkText><linkUri>http://microsoftvolumelicensing.com/DocumentSearch.aspx?Mode=3&amp;DocumentTypeId=37</linkUri></externalLink> </caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="0ce46c44915c2458208255706d1aa89b" id="tgt114" class="tgtSentence">Contrato de nivel de servicio para Azure Active Directory: <externalLink><linkText>Contratos de nivel de servicio</linkText><linkUri>http://azure.microsoft.com/support/legal/sla/</linkUri></externalLink></caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <embeddedLabel>
              <caps:sentence sentenceid="63adb321a0c16bdb196adb991267517c" id="tgt115" class="tgtSentence">Documentación:</caps:sentence>
            </embeddedLabel>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="9e835b66867919def9cd636df3121a23" id="tgt116" class="tgtSentence">Sitio de documentación de Azure Active Directory: <externalLink><linkText>Azure Active Directory</linkText><linkUri>http://azure.microsoft.com/documentation/services/active-directory/</linkUri></externalLink></caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="cc24df7dd92a4d204790388bf237937c" id="tgt117" class="tgtSentence">Biblioteca de Azure Active Directory: <externalLink><linkText>Azure Active Directory</linkText><linkUri>http://msdn.microsoft.com/library/azure/jj673460.aspx</linkUri></externalLink></caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="a34f85bd547e2cc541c86e584132f8c9" id="tgt118" class="tgtSentence">Biblioteca de Office 365: <externalLink><linkText>Office 365</linkText><linkUri>http://technet.microsoft.com/library/dn127064(v=office.14).aspx</linkUri></externalLink></caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <section expanded="false">
        <title>
          <caps:sentence sentenceid="0398fda84f59464004e2d12dfab70ebf" id="tgt119" class="tgtSentence">¿Qué debo hacer si mi pregunta no aparece aquí?</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="3cd784595e484e8b8b784e21a2d5c34b" id="tgt120" class="tgtSentence">Use los vínculos y recursos que aparecen en <link xlink:href="7cc73d92-27d6-49ff-a8ab-2fae73519b4b">Information and Support for Azure Rights Management</link>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="98e956464cfc5e2037df20ecfd1b6293" id="tgt121" class="tgtSentence">Además, hay preguntas frecuentes diseñadas para usuarios finales:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <externalLink>
                  <linkText>
                    <caps:sentence sentenceid="6e530ad535055e4acc7229493acc5ba7" id="tgt122" class="tgtSentence">Preguntas más frecuentes sobre la aplicación de uso compartido de Rights Management para Windows</caps:sentence>
                  </linkText>
                  <linkUri>https://technet.microsoft.com/dn467883</linkUri>
                </externalLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <externalLink>
                  <linkText>
                    <caps:sentence sentenceid="1aa2fbb155957558f8fdd797f7e74a8b" id="tgt123" class="tgtSentence"> Preguntas frecuentes sobre la aplicación Rights Management sharing para plataformas Mac y móviles</caps:sentence>
                  </linkText>
                  <linkUri>https://technet.microsoft.com/dn451248</linkUri>
                </externalLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <externalLink>
                  <linkText>
                    <caps:sentence sentenceid="1ea15bf16350f6bd7bee6a3388afa295" id="tgt124" class="tgtSentence">Preguntas más frecuentes sobre seguimiento de documentos</caps:sentence>
                  </linkText>
                  <linkUri>http://go.microsoft.com/fwlink/?LinkId=523977</linkUri>
                </externalLink>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="909ecfe0b7499cd7bc240656d3b624cf" id="tgt125" class="tgtSentence">Esta página de Preguntas más frecuentes se actualizará regularmente, con nuevas adiciones enumeradas en los anuncios mensuales de actualización de la documentación en el blog del <externalLink><linkText>equipo de Rights Management (RMS) de Microsoft</linkText><linkUri>http://blogs.technet.com/b/rms/</linkUri></externalLink>.</caps:sentence>
          </para>
          <alert class="tip">
            <para>
              <caps:sentence sentenceid="bc4408162aed259521c2777b35c973e4" id="tgt126" class="tgtSentence">Utilice la <externalLink><linkText>etiqueta docs</linkText><linkUri>http://blogs.technet.com/b/rms/archive/tags/docs/</linkUri></externalLink> en el blog para encontrar estos anuncios sobre la documentación con más facilidad.</caps:sentence>
            </para>
          </alert>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="5214667c-ec69-42ca-8bbf-8cb22da8c62e">Getting Started with Azure Rights Management</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Some frequently asked questions for Microsoft <token>aad_rightsmanagement_1</token>, also known as Azure RMS:</caps:sentence>
        </para>
      </introduction>
      <section expanded="false">
        <title>
          <caps:sentence id="src2" class="srcSentence">What do I need to deploy Azure RMS and how do I get going?</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">First, check <link xlink:href="dc78321d-d759-4653-8818-80da74b6cdeb">Requirements for Azure Rights Management</link>, which has information about the cloud subscription options, how you can use your on-premises servers with Azure RMS, which deployment scenarios are not currently supported, which devices and applications support Azure RMS, and a link if you need a list of IP addresses and domain names for firewalls or proxy servers.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> You might also want to check the other topics in the <link xlink:href="5214667c-ec69-42ca-8bbf-8cb22da8c62e">Getting Started with Azure Rights Management</link> section, to get a basic understanding of how <token>aad_rightsmanagement_1</token> can help protect your organization’s data, how it works with applications, how it compares with the on-premises version of Active Directory Rights Management, and understand the terms and abbreviations that are specific to <token>aad_rightsmanagement_1</token>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src5" class="srcSentence">Then when you’re ready to test Azure RMS for yourself, or deploy it for your organization, use the <link xlink:href="086600c2-c5d8-47ec-a4c0-c782e1797486">Azure Rights Management Deployment Roadmap</link> for a list of steps with links for more information and how-to instructions.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src6" class="srcSentence">If you need additional information, resources, and support options, see <link xlink:href="7cc73d92-27d6-49ff-a8ab-2fae73519b4b">Information and Support for Azure Rights Management</link>.</caps:sentence>
          </para>
        </content>
      </section>
      <section expanded="false">
        <title>
          <caps:sentence id="src7" class="srcSentence">Can I integrate Azure RMS with my on-premises servers?</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src8" class="srcSentence">Yes.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence"> Azure RMS can be integrated with your on-premises servers, such as Exchange Server, SharePoint, and Windows file servers.</caps:sentence>
            <caps:sentence id="src10" class="srcSentence"> To do this, you use the <externalLink><linkText>Rights Management connector</linkText><linkUri>https://technet.microsoft.com/library/dn375964.aspx</linkUri></externalLink>.</caps:sentence>
            <caps:sentence id="src11" class="srcSentence"> Or, if you're just interested in using File Classification Infrastructure (FC) with Windows Server, you can use the <externalLink><linkText>RMS Protection cmdlets</linkText><linkUri>https://technet.microsoft.com/library/mt601315(v=ws.10).aspx</linkUri></externalLink>.</caps:sentence>
            <caps:sentence id="src12" class="srcSentence"> You can also synchronize and federate your Active Directory domain controllers with Azure AD for a more seamless authentication experience for users, for example, by using <externalLink><linkText>Azure AD Connect</linkText><linkUri>http://azure.microsoft.com/documentation/articles/active-directory-aadconnect/</linkUri></externalLink>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src13" class="srcSentence">Azure RMS automatically generates and manages XrML certificates as required, so it doesn’t use an on-premises PKI.</caps:sentence>
            <caps:sentence id="src14" class="srcSentence"> For more information about how Azure RMS uses certificates, see the <link xlink:href="aeeebcd7-6646-4405-addf-ee1cc74df5df#BKMK_Walthrough">Walkthrough of how Azure RMS works: First use, content protection, content consumption</link> section in the <link xlink:href="aeeebcd7-6646-4405-addf-ee1cc74df5df">What is Azure Rights Management?</link> topic.</caps:sentence>
          </para>
        </content>
      </section>
      <section expanded="false">
        <title>
          <caps:sentence id="src15" class="srcSentence">I have a hybrid deployment of Exchange with some users on Exchange Online and others on Exchange Server—is this supported by Azure RMS?</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src16" class="srcSentence">Absolutely, and the nice thing is, users will be able to seamlessly protect and consume protected emails and attachments across the two Exchange deployments.</caps:sentence>
            <caps:sentence id="src17" class="srcSentence"> For this configuration, <externalLink><linkText>activate Azure RMS</linkText><linkUri>https://technet.microsoft.com/library/jj658941.aspx</linkUri></externalLink> and <externalLink><linkText>enable IRM for Exchange Online</linkText><linkUri>https://technet.microsoft.com/library/dn151475(v=exchg.150).aspx</linkUri></externalLink>, then <externalLink><linkText>deploy and configure the RMS connector</linkText><linkUri>https://technet.microsoft.com/library/dn375964.aspx</linkUri></externalLink> for Exchange Server.</caps:sentence>
          </para>
          <para></para>
        </content>
      </section>
      <section expanded="false">
        <title>
          <caps:sentence id="src18" class="srcSentence">If I deploy Azure RMS in production, is my company then locked into the solution or risk losing access to content that we protected with Azure RMS?</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src19" class="srcSentence">No, you always remain in control of your data and can continue to access it, even if you decide to no longer use Azure RMS.</caps:sentence>
            <caps:sentence id="src20" class="srcSentence"> For more information, see <link xlink:href="0b1c2064-0d01-45ae-a541-cebd7fd762ad">Decommissioning and Deactivating Azure Rights Management</link>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src21" class="srcSentence">However, before you decommission your Azure RMS deployment, we would like to hear from you and understand why you made this decision.</caps:sentence>
            <caps:sentence id="src22" class="srcSentence"> If Azure RMS does not fulfil your business requirements, check with us in case new functionality is planned for the near-future or if there are alternatives.</caps:sentence>
            <caps:sentence id="src23" class="srcSentence"> Send an email message to <externalLink><linkText>AskIPTeam@Microsoft.com</linkText><linkUri>mailto:askipteam@microsoft.com?subject=Planning%20to%20decommission%20Azure%20RMS</linkUri></externalLink> and we’ll be happy to discuss your technical and business requirements.</caps:sentence>
          </para>
        </content>
      </section>
      <section expanded="false">
        <title>
          <caps:sentence id="src24" class="srcSentence">Can I control which of my users can use Azure RMS to protect content?</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src25" class="srcSentence">Yes, Azure RMS has user onboarding controls for this scenario.</caps:sentence>
            <caps:sentence id="src26" class="srcSentence"> For more information, see the <link xlink:href="f8707e01-b239-4d1a-a1ea-0d1cf9a8d214#BKMK_OnboardingControls">Configuring onboarding controls for a phased deployment</link> section in the <link xlink:href="f8707e01-b239-4d1a-a1ea-0d1cf9a8d214">Activating Azure Rights Management</link> topic.</caps:sentence>
          </para>
        </content>
      </section>
      <section expanded="false">
        <title>
          <caps:sentence id="src27" class="srcSentence">Can I prevent users from sharing protected documents with specific organizations?</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src28" class="srcSentence">One of the biggest benefits of Azure RMS is that it supports business-to-business collaboration without you having to configure explicit trusts for each partner organization, because Azure AD takes care of the authentication for you.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src29" class="srcSentence">There is no administration option to prevent users from securely sharing documents with specific organizations.</caps:sentence>
            <caps:sentence id="src30" class="srcSentence"> For example, you want to block an organization that you don’t trust or that has a competing business.</caps:sentence>
            <caps:sentence id="src31" class="srcSentence"> Preventing Azure RMS from sending protected documents to users in these organizations wouldn’t make sense because your users would then share their documents unprotected, which is probably the last thing you want to happen in this scenario!</caps:sentence>
            <caps:sentence id="src32" class="srcSentence"> For example, you wouldn’t be able to identify who is sharing company-confidential documents with which users in these organizations, which you can do when the document (or email) is protected by Azure RMS.</caps:sentence>
          </para>
        </content>
      </section>
      <section expanded="false">
        <title>
          <caps:sentence id="src33" class="srcSentence">When I share a protected document with somebody outside my company, how does that user get authenticated?</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src34" class="srcSentence">Azure RMS always uses an Azure Active Directory account and an associated email address for user authentication, which makes business-to-business collaboration seamless for administrators.</caps:sentence>
            <caps:sentence id="src35" class="srcSentence"> If the other organization uses Azure services, users will already have accounts in Azure Active Directory, even if these accounts are created and managed on-premises and then synchronized to Azure.</caps:sentence>
            <caps:sentence id="src36" class="srcSentence">  If the organization has Office 365, under the covers, this service also uses Azure Active Directory for the user accounts.</caps:sentence>
            <caps:sentence id="src37" class="srcSentence">  If the user’s organization doesn’t have managed accounts in Azure, users can sign up for <externalLink><linkText>RMS for individuals</linkText><linkUri>https://technet.microsoft.com/library/dn592127.aspx</linkUri></externalLink>, which creates an unmanaged Azure tenant and directory for the organization with an account for the user, so that this user can then be authenticated for Azure RMS.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src38" class="srcSentence">The authentication method for these accounts can vary, depending on how the administrator in the other organization has configured the Azure Active Directory accounts.</caps:sentence>
            <caps:sentence id="src39" class="srcSentence"> For example, they could use passwords that were created for these accounts, multi-factor authentication (MFA), federation, or passwords that were created in Active Directory Domain Services and then synchronized to Azure Active Directory.</caps:sentence>
          </para>
        </content>
      </section>
      <section expanded="false">
        <title>
          <caps:sentence id="src40" class="srcSentence">Can I add users from outside my company to custom templates?</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src41" class="srcSentence">Yes.</caps:sentence>
            <caps:sentence id="src42" class="srcSentence">  Creating custom templates that end users (and administrators) can select from applications makes it quick and easily for them to apply information protection, using predefined policies that you specify.</caps:sentence>
            <caps:sentence id="src43" class="srcSentence"> One of the settings in the template is who is able to access the content, and you can specify users and groups from within your organization, and users from outside your organization.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src44" class="srcSentence">To specify users from outside your organization, use <externalLink><linkText>Windows PowerShell module for Azure Rights Management</linkText><linkUri>https://technet.microsoft.com/library/jj585012.aspx</linkUri></externalLink>: </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src45" class="srcSentence">
                  <embeddedLabel>Use a rights definition object to create or update a template</embeddedLabel>.</caps:sentence>
                <caps:sentence id="src46" class="srcSentence">    Specify the external email addresses and their rights in a rights definition object, which you then use to create or update a template.</caps:sentence>
                <caps:sentence id="src47" class="srcSentence"> You specify the rights definition object by using the <externalLink><linkText>New-AadrmRightsDefinition</linkText><linkUri>https://msdn.microsoft.com/library/azure/dn727080.aspx</linkUri></externalLink> cmdlet to create a variable and then supply this variable to the  -RightsDefinition parameter with the <externalLink><linkText>Add-AadrmTemplate</linkText><linkUri>https://msdn.microsoft.com/library/azure/dn727075.aspx</linkUri></externalLink> cmdlet (for a new template) or <externalLink><linkText>Set-AadrmTemplateProperty</linkText><linkUri>https://msdn.microsoft.com/library/azure/dn727076.aspx</linkUri></externalLink> cmdlet (if you're modifying an existing template).</caps:sentence>
                <caps:sentence id="src48" class="srcSentence"> However, if you're adding these users to an existing template, you will need to define rights definition objects for the existing groups in the templates and not just the external users.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src49" class="srcSentence">For more information about custom templates, see <link xlink:href="1775d8d0-9a59-42c8-914f-ce285b71ac1c">Configuring Custom Templates for Azure Rights Management</link>.</caps:sentence>
          </para>
        </content>
      </section>
      <section expanded="false">
        <title>
          <caps:sentence id="src50" class="srcSentence">What devices and which file types are supported by Azure RMS?</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src51" class="srcSentence">For a list of supported devices, see the <link xlink:href="dc78321d-d759-4653-8818-80da74b6cdeb#BKMK_SupportedDevices">Client devices that support Azure RMS</link> section in the <link xlink:href="dc78321d-d759-4653-8818-80da74b6cdeb">Requirements for Azure Rights Management</link> topic.</caps:sentence>
            <caps:sentence id="src52" class="srcSentence"> Because not all supported devices can currently support all RMS capabilities, be sure to also check the <link xlink:href="dc78321d-d759-4653-8818-80da74b6cdeb#BKMK_ClientCapabilities">Client device capabilities</link> table in the same topic.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src53" class="srcSentence">Azure RMS can support all file types.</caps:sentence>
            <caps:sentence id="src54" class="srcSentence"> For text, image, Microsoft Office (Word, Excel, PowerPoint) files, .pdf files, and some other application file types, Azure RMS provides native protection that includes both encryption and enforcement of rights (permissions).</caps:sentence>
            <caps:sentence id="src55" class="srcSentence"> For all other applications and file types, generic protection provides file encapsulation and authentication to verify if a user is authorized to open the file.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src56" class="srcSentence">For a list of file name extensions that are natively supported by Azure RMS, see the <externalLink><linkText>Supported file types and file name extensions</linkText><linkUri>http://technet.microsoft.com/library/dn339003.aspx</linkUri></externalLink> section of the <externalLink><linkText>Rights Management sharing application administrator guide</linkText><linkUri>http://technet.microsoft.com/library/dn339003.aspx</linkUri></externalLink>.</caps:sentence>
            <caps:sentence id="src57" class="srcSentence"> File name extensions not listed are supported by using the RMS sharing application that automatically applies generic protection to these files.</caps:sentence>
          </para>
        </content>
      </section>
      <section expanded="false">
        <title>
          <caps:sentence id="src58" class="srcSentence">When will you support migration from AD RMS?</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src59" class="srcSentence">Initially, Azure RMS didn’t support migration from an on-premises deployment of Rights Management, such as AD RMS.</caps:sentence>
            <caps:sentence id="src60" class="srcSentence"> But it’s supported now.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src61" class="srcSentence">For more information, see <link xlink:href="828cf1f7-d0e7-4edf-8525-91896dbe3172">Migrating from AD RMS to Azure Rights Management</link>.</caps:sentence>
          </para>
        </content>
      </section>
      <section expanded="false">
        <title>
          <caps:sentence id="src62" class="srcSentence">We really want to use BYOK with Azure RMS but learned that this isn’t compatible with Exchange Online—what’s your advice?</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src63" class="srcSentence">Don’t let this current limitation delay your Azure RMS deployment.</caps:sentence>
            <caps:sentence id="src64" class="srcSentence"> If you have Exchange Online and want to use bring your own key (BYOK), we recommend that you deploy Azure RMS in the default key management mode now, where Microsoft generates and manages your key.</caps:sentence>
            <caps:sentence id="src65" class="srcSentence"> That way, you get all the benefits of protecting your important files and emails now, with the option to move to BYOK later (for example, when Exchange Online does support BYOK).</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src66" class="srcSentence">However, if your company policies require you to use a hardware security module (HSM) and this would otherwise block your Azure RMS deployment, another option is to deploy Azure RMS with BYOK now, with reduced RMS functionality for Exchange.</caps:sentence>
            <caps:sentence id="src67" class="srcSentence"> For more information, see the <link xlink:href="f0d33c5f-a6a6-44a1-bdec-5be1bc8e1e14#BKMK_Pricing">BYOK pricing and restrictions</link> section in the <link xlink:href="f0d33c5f-a6a6-44a1-bdec-5be1bc8e1e14">Planning and Implementing Your Azure Rights Management Tenant Key</link> topic.</caps:sentence>
          </para>
        </content>
      </section>
      <section expanded="false">
        <title>
          <caps:sentence id="src68" class="srcSentence">A feature I am looking for doesn’t seem to work with SharePoint protected libraries—is support for my feature planned?</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src69" class="srcSentence">Currently, SharePoint supports RMS protected documents by using IRM protected libraries, which do not support custom templates, document tracking, and some other capabilities.</caps:sentence>
            <caps:sentence id="src70" class="srcSentence">  For more information, expand the   <link xlink:href="ea09cbc5-b98b-444e-8b60-5bc3cb199c36#BKMK_SharePointOnline">SharePoint Online and OneDrive for Business: IRM Configuration</link> section in the <link xlink:href="2cdc7bde-4044-4021-b887-11476f99afd9">How Applications Support Azure Rights Management</link> topic .</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src71" class="srcSentence">If you are interested in a specific  capability that isn't yet supported,  be sure to keep an eye on announcements on the <externalLink><linkText>RMS team blog</linkText><linkUri>http://blogs.technet.com/b/rms/</linkUri></externalLink>.</caps:sentence>
          </para>
        </content>
      </section>
      <section expanded="false">
        <title>
          <caps:sentence id="src72" class="srcSentence">How do I configure One Drive for Business in SharePoint Online, so that users can safely share their files with people inside and outside the company?</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src73" class="srcSentence">By default, as an Office 365 administrator, you don’t configure this; users do.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src74" class="srcSentence">Just as a SharePoint site administrator enables and configures IRM for a SharePoint library that they own, OneDrive for Business is designed for users to enable and configure IRM for their own OneDrive for Business library.</caps:sentence>
            <caps:sentence id="src75" class="srcSentence">  However, by using PowerShell, you can do this for them.</caps:sentence>
            <caps:sentence id="src76" class="srcSentence"> For instructions, expand the <link xlink:href="ea09cbc5-b98b-444e-8b60-5bc3cb199c36#BKMK_SharePointOnline">SharePoint Online and OneDrive for Business: IRM Configuration</link>  section in the <link xlink:href="ea09cbc5-b98b-444e-8b60-5bc3cb199c36">Configuring Applications for Azure Rights Management</link> article.</caps:sentence>
          </para>
        </content>
      </section>
      <section expanded="false">
        <title>
          <caps:sentence id="src77" class="srcSentence">Do you have any tips or tricks for a successful RMS deployment?</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src78" class="srcSentence">After overseeing many deployments and listening to our customers, partners, consultants, and support engineers – one of the biggest tips we can pass on from experience: <legacyBold>Design and deploy simple rights policies</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src79" class="srcSentence">Because Azure RMS supports sharing securely with anyone, you can afford to be ambitious with your information protection reach.</caps:sentence>
            <caps:sentence id="src80" class="srcSentence"> But be conservative with your rights policies.</caps:sentence>
            <caps:sentence id="src81" class="srcSentence"> For many organizations, the biggest business impact comes from preventing data leakage by applying the default rights policy template that restricts access to people in your organization.</caps:sentence>
            <caps:sentence id="src82" class="srcSentence"> Of course, you can get much more granular than that if you need to – prevent people from printing, editing etc. But keep the more granular restrictions as the exception for documents that really need high-level security, and don’t implement these more restrictive policies on day one, but plan for a more phased approach.</caps:sentence>
          </para>
        </content>
      </section>
      <section expanded="false">
        <title>
          <caps:sentence id="src83" class="srcSentence">What features can or can’t be used with the different subscriptions for Azure RMS?</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src84" class="srcSentence">For the paid subscriptions that support Azure RMS (Office 365, Azure RMS Premium, and Enterprise Mobility Suite), there are some differences in the RMS features that are supported.</caps:sentence>
            <caps:sentence id="src85" class="srcSentence"> For a list of these, see <externalLink><linkText>Comparison of Rights Management Services (RMS) Offerings</linkText><linkUri>http://technet.microsoft.com/dn858608</linkUri></externalLink>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src86" class="srcSentence">The free subscription that supports Azure RMS (RMS for individuals) supports consuming content that has been protected by Azure RMS.</caps:sentence>
            <caps:sentence id="src87" class="srcSentence"> For more information, see <link xlink:href="2efcb440-fefd-45e9-872b-f471573aadf2">RMS for Individuals and Azure Rights Management</link>.</caps:sentence>
          </para>
        </content>
      </section>
      <section expanded="false">
        <title>
          <caps:sentence id="src88" class="srcSentence">Where can I get technical information about the free Azure RMS subscription (RMS for individuals)—for example, how it really works, how to take control of the accounts, and which domains can’t be used?</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src89" class="srcSentence">You’ll find answers to these questions in the <link xlink:href="2efcb440-fefd-45e9-872b-f471573aadf2">RMS for Individuals and Azure Rights Management</link> topic.</caps:sentence>
          </para>
        </content>
      </section>
      <section expanded="false">
        <title>
          <caps:sentence id="src90" class="srcSentence">How do we regain access to files that were protected by an employee who has now left the organization?</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src91" class="srcSentence">Use the super user feature of Azure RMS, which lets authorized users have full owner rights for all use licenses that were granted by your organization’s RMS tenant.</caps:sentence>
            <caps:sentence id="src92" class="srcSentence"> This same feature lets authorized services index and inspect files, as needed.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src93" class="srcSentence">For more information, see <link xlink:href="acb4c00b-d3a9-4d74-94fe-91eeb481f7e3">Configuring Super Users for Azure Rights Management and Discovery Services or Data Recovery</link>.</caps:sentence>
          </para>
        </content>
      </section>
      <section expanded="false">
        <title>
          <caps:sentence id="src94" class="srcSentence">Can Rights Management prevent screen captures?</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src95" class="srcSentence">Rights Management does block screen captures from most of the commonly used screen capture tools, which can help to avoid accidental or negligent disclosure of confidential or sensitive information.</caps:sentence>
            <caps:sentence id="src96" class="srcSentence"> However, there are many ways that a user can share data that is displayed on a screen, and taking a screen shot is only one method.</caps:sentence>
            <caps:sentence id="src97" class="srcSentence"> For example, a user intent on sharing displayed information can take a picture of it using their camera phone, retype the data, or simply verbally relay it to somebody.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src98" class="srcSentence">As these examples demonstrate, technology alone cannot always prevent users from sharing data that they should not.</caps:sentence>
            <caps:sentence id="src99" class="srcSentence"> While Rights Management can help to safeguard your important data by using authorization and usage policies, this enterprise rights management solution should be used with other controls.</caps:sentence>
            <caps:sentence id="src100" class="srcSentence"> For example, implement physical security, carefully screen and monitor people who have authorized access to your organization's data, and invest in user education so users understand what data should not be shared.</caps:sentence>
          </para>
        </content>
      </section>
      <section expanded="false">
        <title>
          <caps:sentence id="src101" class="srcSentence">Where can I find supporting information for Azure RMS—such as legal, compliance, and SLAs?</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src102" class="srcSentence">Azure RMS supports other services and also relies on other services.</caps:sentence>
            <caps:sentence id="src103" class="srcSentence"> If you’re looking for information that is related to Azure RMS but not about how to use the Azure RMS service, check the following resources:</caps:sentence>
          </para>
          <para>
            <embeddedLabel>
              <caps:sentence id="src104" class="srcSentence">Legal and privacy:</caps:sentence>
            </embeddedLabel>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src105" class="srcSentence">For Microsoft Azure agreement information: <externalLink><linkText>Microsoft Azure Agreement</linkText><linkUri>http://azure.microsoft.com/support/legal/subscription-agreement/</linkUri></externalLink></caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src106" class="srcSentence">For Microsoft Azure privacy information: <externalLink><linkText>Microsoft Azure Privacy Statement</linkText><linkUri>http://azure.microsoft.com/support/legal/privacy-statement/</linkUri></externalLink></caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <embeddedLabel>
              <caps:sentence id="src107" class="srcSentence">Security, compliance, and auditing:</caps:sentence>
            </embeddedLabel>
          </para>
          <para>
            <caps:sentence id="src108" class="srcSentence">See the <link xlink:href="aeeebcd7-6646-4405-addf-ee1cc74df5df#BKMK_RMScompliance">Security, compliance, and regulatory requirements</link> section in the <link xlink:href="aeeebcd7-6646-4405-addf-ee1cc74df5df">What is Azure Rights Management?</link> topic.</caps:sentence>
            <caps:sentence id="src109" class="srcSentence"> In addition:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src110" class="srcSentence">For external certifications for Azure RMS: <externalLink><linkText>Microsoft Azure Trust Center</linkText><linkUri>http://azure.microsoft.com/support/trust-center/</linkUri></externalLink></caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src111" class="srcSentence">For FIPS 140 information: <externalLink><linkText>FIPS 140 Validation</linkText><linkUri>https://technet.microsoft.com/library/security/cc750357.aspx</linkUri></externalLink></caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <embeddedLabel>
              <caps:sentence id="src112" class="srcSentence">Service level agreements:</caps:sentence>
            </embeddedLabel>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src113" class="srcSentence">Service level agreement for Azure RMS, by selected country: <externalLink><linkText>Service level agreement</linkText><linkUri>http://microsoftvolumelicensing.com/DocumentSearch.aspx?Mode=3&amp;DocumentTypeId=37</linkUri></externalLink> </caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src114" class="srcSentence">Service level agreement for Azure Active Directory: <externalLink><linkText>Service Level Agreements</linkText><linkUri>http://azure.microsoft.com/support/legal/sla/</linkUri></externalLink></caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <embeddedLabel>
              <caps:sentence id="src115" class="srcSentence">Documentation:</caps:sentence>
            </embeddedLabel>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src116" class="srcSentence">Azure Active Directory Documentation site: <externalLink><linkText>Azure Active Directory</linkText><linkUri>http://azure.microsoft.com/documentation/services/active-directory/</linkUri></externalLink></caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src117" class="srcSentence">Azure Active Directory Library: <externalLink><linkText>Azure Active Directory</linkText><linkUri>http://msdn.microsoft.com/library/azure/jj673460.aspx</linkUri></externalLink></caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src118" class="srcSentence">Office 365 Library: <externalLink><linkText>Office 365</linkText><linkUri>http://technet.microsoft.com/library/dn127064(v=office.14).aspx</linkUri></externalLink></caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <section expanded="false">
        <title>
          <caps:sentence id="src119" class="srcSentence">What do I do if my question isn’t here?</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src120" class="srcSentence">Use the links and resources listed in <link xlink:href="7cc73d92-27d6-49ff-a8ab-2fae73519b4b">Information and Support for Azure Rights Management</link>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src121" class="srcSentence">In addition, there are FAQs designed for end-users:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <externalLink>
                  <linkText>
                    <caps:sentence id="src122" class="srcSentence">FAQ for Rights Management Sharing Application for Windows</caps:sentence>
                  </linkText>
                  <linkUri>https://technet.microsoft.com/dn467883</linkUri>
                </externalLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <externalLink>
                  <linkText>
                    <caps:sentence id="src123" class="srcSentence"> FAQ for Rights Management Sharing Application for Mobile and Mac Platforms</caps:sentence>
                  </linkText>
                  <linkUri>https://technet.microsoft.com/dn451248</linkUri>
                </externalLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <externalLink>
                  <linkText>
                    <caps:sentence id="src124" class="srcSentence">FAQ for Document Tracking</caps:sentence>
                  </linkText>
                  <linkUri>http://go.microsoft.com/fwlink/?LinkId=523977</linkUri>
                </externalLink>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src125" class="srcSentence">This FAQ page will be updated regularly, with new additions listed in the monthly documentation update announcements on the <externalLink><linkText>Microsoft Rights Management (RMS) Team</linkText><linkUri>http://blogs.technet.com/b/rms/</linkUri></externalLink> blog.</caps:sentence>
          </para>
          <alert class="tip">
            <para>
              <caps:sentence id="src126" class="srcSentence">You can use the <externalLink><linkText>docs tag</linkText><linkUri>http://blogs.technet.com/b/rms/archive/tags/docs/</linkUri></externalLink> on the blog, to more easily find these documentation announcements.</caps:sentence>
            </para>
          </alert>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="5214667c-ec69-42ca-8bbf-8cb22da8c62e">Getting Started with Azure Rights Management</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>