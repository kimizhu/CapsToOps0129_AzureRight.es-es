---
title: Configuraci&#243;n de plantillas personalizadas para Azure Rights Management
ms.custom: na
ms.reviewer: na
ms.service: rights-management
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1775d8d0-9a59-42c8-914f-ce285b71ac1c
---
# Configuraci&#243;n de plantillas personalizadas para Azure Rights Management
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="es-ES">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="59f34f5737aeb9bd43ce6edab7570275" id="tgt1" class="tgtSentence">Tras activar Azure Rights Management (Azure RMS), los usuarios pueden automáticamente usar dos plantillas predeterminadas, lo que les facilita la aplicación de directivas para archivos confidenciales para los que desean restringir el acceso solamente a usuarios autorizados de su organización.</caps:sentence>
          <caps:sentence sentenceid="e0963451d364756468514ac4c45dbb9d" id="tgt2" class="tgtSentence"> Estas dos plantillas presentan las restricciones de directivas de derechos siguientes:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="f564a1ad34624859873e9267e8b516ad" id="tgt3" class="tgtSentence">Visualización de solo lectura para el contenido protegido</caps:sentence>
            </para>
            <list class="bullet">
              <listItem>
                <para>
                  <caps:sentence sentenceid="b71fa3883a5b02ed47352fddc9905b72" id="tgt4" class="tgtSentence">Nombre para mostrar: <ui>&lt;nombre de organización&gt; - Solo vista confidencial</ui></caps:sentence>
                </para>
              </listItem>
              <listItem>
                <para>
                  <caps:sentence sentenceid="faffb7c4ba724dd000b98b5b20f53f86" id="tgt5" class="tgtSentence">Permiso específico: Ver contenido</caps:sentence>
                </para>
              </listItem>
            </list>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="058853c04abaf2c05a8e9e119079a58e" id="tgt6" class="tgtSentence">Lectura o modificación de permisos de contenido protegido</caps:sentence>
            </para>
            <list class="bullet">
              <listItem>
                <para>
                  <caps:sentence sentenceid="57dbb58f27bbefc2e6054c86fb8a9c3d" id="tgt7" class="tgtSentence">Nombre para mostrar: <ui>&lt;nombre de organización&gt; - Confidencial</ui></caps:sentence>
                </para>
              </listItem>
              <listItem>
                <para>
                  <caps:sentence sentenceid="954945239f512845947cc3d50a9ac6cd" id="tgt8" class="tgtSentence">Permisos específicos: Ver contenido, Guardar archivo, Editar contenido, Ver derechos asignados, Permitir macros, Reenviar, Responder y Responder a todos</caps:sentence>
                </para>
              </listItem>
            </list>
          </listItem>
        </list>
        <para>
          <caps:sentence sentenceid="41c9e6408632c07f06cab6613b276a15" id="tgt9" class="tgtSentence">Además, la <externalLink><linkText>aplicación RMS sharing</linkText><linkUri>http://technet.microsoft.com/library/dn339006.aspx</linkUri></externalLink> permite a los usuarios definir su propio conjunto de permisos.</caps:sentence>
          <caps:sentence sentenceid="a21a3bd7d9b2a138b6f802d9a54d3fca" id="tgt10" class="tgtSentence"> Y, para el cliente de Outlook y Outlook Web Access, los usuarios pueden seleccionar la opción <ui>No reenviar</ui> para los mensajes de correo electrónico.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="9fc3938913954161007026a9373a6956" id="tgt11" class="tgtSentence">Para muchas organizaciones, las plantillas predeterminadas pueden ser suficientes.</caps:sentence>
          <caps:sentence sentenceid="162325146963ae87a3e6f51c098b33fa" id="tgt12" class="tgtSentence"> Pero si quieres crear tus propias plantillas de directivas de derechos personalizadas, puedes hacerlo.</caps:sentence>
          <caps:sentence sentenceid="ebd5fe053eca6f3ce32999b63d86e4cd" id="tgt13" class="tgtSentence"> Entre los motivos para crear una plantilla personalizada encontramos los siguientes:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="b73755a35b5ff091a25bfc30a3db59f4" id="tgt14" class="tgtSentence">Quieres una plantilla que garantice los derechos a una red secundaria de usuarios de la organización, más que a todos los usuarios.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="14d8201fbac142eff9cb2e90ad65200c" id="tgt15" class="tgtSentence">Desea que solo un subconjunto de usuarios puedan ver y seleccionar una plantilla (plantilla de departamento) de las aplicaciones, en lugar de que todos los usuarios de la organización vean y puedan seleccionar la plantilla.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="4010f3407c0b9c54f6922855ba8522a9" id="tgt16" class="tgtSentence">Quieres definir un derecho personalizado para una plantilla, como Ver y Editar, pero no Copiar e Imprimir.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="005649d2839ddbe099187e2e6ccbf5a8" id="tgt17" class="tgtSentence">Quieres configurar opciones adicionales en una plantilla, entre las cuales se incluye una fecha de caducidad y si se puede acceder al contenido sin conexión a Internet.</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence sentenceid="64bd2ff7b46e5977bb8df33465e3dc5b" id="tgt18" class="tgtSentence">Para que los usuarios puedan seleccionar una plantilla personalizada que contenga una configuración como estas, en primer lugar, debes crear una plantilla personalizada, configurarla y, a continuación, publicarla.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="8d348ecd1f2cf86a8c8713c113c55c14" id="tgt19" class="tgtSentence">Usa las secciones siguientes para tratar de configurar y usar plantillas personalizadas:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <link xlink:href="1775d8d0-9a59-42c8-914f-ce285b71ac1c#BKMK_HowToConfigureCustomTemplates">How to create, configure, and publish a custom template</link>
            </para>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="1775d8d0-9a59-42c8-914f-ce285b71ac1c#BKMK_HowToCopyTemplates">How to copy a template</link>
            </para>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="1775d8d0-9a59-42c8-914f-ce285b71ac1c#BKMK_HowToArchiveTemplates">How to remove (archive) templates</link>
            </para>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="1775d8d0-9a59-42c8-914f-ce285b71ac1c#BKMK_RefreshingTemplates">Refreshing templates for users</link>
            </para>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="1775d8d0-9a59-42c8-914f-ce285b71ac1c#BKMK_PowerShellTemplates">Windows PowerShell reference</link>
            </para>
          </listItem>
        </list>
      </introduction>
      <section address="BKMK_HowToConfigureCustomTemplates">
        <title>
          <caps:sentence sentenceid="4afb1d98fe0047fd6a983bde369d0ee8" id="tgt20" class="tgtSentence">Cómo crear, configurar y publicar una plantilla personalizada</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="55d030f534db985b2367c3486b0dc44c" id="tgt21" class="tgtSentence">En el Portal de Azure clásico puede crear y administrar plantillas personalizada.</caps:sentence>
            <caps:sentence sentenceid="81a49779685e919d2396d70c51695531" id="tgt22" class="tgtSentence"> Puede hacerlo directamente desde el Portal de Azure clásico o puede iniciar sesión en el Centro de administración de Office 365 y elegir <ui>Características avanzadas</ui> para Rights Management, lo que le redirigirá al Portal de Azure clásico.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="68a187d8d7d1791d222a5b2c8349d139" id="tgt23" class="tgtSentence">Usa los procedimientos siguientes para crear, configurar y publicar plantillas personalizadas para Rights Management.</caps:sentence>
          </para>
          <procedure>
            <title>
              <caps:sentence sentenceid="c72c19a9b285cbb4308f21aa2959a43b" id="tgt24" class="tgtSentence">Para crear una plantilla personalizada</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="087d136f89f4568a8dff8c62688d02dc" id="tgt25" class="tgtSentence">En función de si inicia sesión en el Centro de administración de Office 365 o en el Portal de Azure clásico, emplee uno de los siguientes procedimientos:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="fa4d6cdcb3bd5910e14ffbc770ccf9b1" id="tgt26" class="tgtSentence">En el <externalLink><linkText>Centro de administración de Office 365</linkText><linkUri>https://portal.office.com/</linkUri></externalLink>:</caps:sentence>
                      </para>
                      <list class="ordered">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="03fc4535a09ba638aefd9eca093a4456" id="tgt27" class="tgtSentence">En el panel izquierdo, haga clic en<ui>Configuración del servicio</ui>.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="b006a68383f6bc4f3d01d3f2bbef41bc" id="tgt28" class="tgtSentence">En la página <ui>Configuración del servicio</ui>, haga clic en <ui>Rights Management</ui>.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="153f28316f09d4a35c68fa6b41701202" id="tgt29" class="tgtSentence">En la sección <ui>Proteja su información</ui>, haga clic en <ui>Administrar</ui>.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="1991af03e54aed6f6a60d7ede615b446" id="tgt30" class="tgtSentence">En la sección <ui>Rights Management</ui>, haga clic en <ui>Características avanzadas</ui>.</caps:sentence>
                          </para>
                          <alert class="note">
                            <para>
                              <caps:sentence sentenceid="171fcdd455ffab093869003ea1bee163" id="tgt31" class="tgtSentence">Si no ha activado todavía Rights Management, haga clic primero en <ui>Activar</ui> y confirme la acción.</caps:sentence>
                              <caps:sentence sentenceid="2165a043f4d02f3b0aa7c134ab18fe7c" id="tgt32" class="tgtSentence"> Para obtener más información, vea <link xlink:href="f8707e01-b239-4d1a-a1ea-0d1cf9a8d214">Activating Azure Rights Management</link>.</caps:sentence>
                            </para>
                            <para>
                              <caps:sentence sentenceid="0900624dab3b561b81cd9a422853073f" id="tgt33" class="tgtSentence">Si no ha hecho clic en <ui>Características avanzadas</ui> antes, después de activar Rights Management, siga las instrucciones que aparecen en pantalla para obtener una suscripción gratuita de Azure, necesaria para poder acceder al Portal de Azure clásico.</caps:sentence>
                            </para>
                          </alert>
                          <para>
                            <caps:sentence sentenceid="feaa1ab7c76ebb73d56ca6cb5919f12b" id="tgt34" class="tgtSentence">Al hacer clic en <ui>Características avanzadas</ui>, se carga el Portal de Azure clásico, donde puede administrar <ui>RIGHTS MANAGEMENT</ui> para Azure Active Directory de su organización.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="364cda3879b6aed6f23084e886ec4dd0" id="tgt35" class="tgtSentence">Desde el <externalLink><linkText>Portal de Azure clásico</linkText><linkUri>http://go.microsoft.com/fwlink/p/?LinkID=275081</linkUri></externalLink>:</caps:sentence>
                      </para>
                      <list class="ordered">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="754a9e159cb4f6ee8e17958f8431ca5b" id="tgt36" class="tgtSentence">En el panel izquierdo, haga clic en <ui>ACTIVE DIRECTORY</ui>.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="0a119846f95f1b3e868eae5ffcdd23f4" id="tgt37" class="tgtSentence">En la página <ui>Active Directory</ui>, haga clic en <ui>RIGHTS MANAGEMENT</ui>.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="ccaa0c9c4788db0bf0fb6fd749a9d990" id="tgt38" class="tgtSentence">Selecciona el directorio que administrarás para Rights Management.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="0d2534e8ac7847129a6830a1791f04a7" id="tgt39" class="tgtSentence">Si no ha activado todavía Rights Management, haga clic en <ui>ACTIVAR</ui> y confirme la acción.</caps:sentence>
                          </para>
                          <alert class="note">
                            <para>
                              <caps:sentence sentenceid="2d80c1dcdb8c5016aaa9fa6efe6e3cf2" id="tgt40" class="tgtSentence">Para obtener más información, vea <link xlink:href="f8707e01-b239-4d1a-a1ea-0d1cf9a8d214">Activating Azure Rights Management</link>.</caps:sentence>
                            </para>
                          </alert>
                        </listItem>
                      </list>
                    </listItem>
                  </list>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="40fe772d5895d4e48e5e5c5aa07745b8" id="tgt41" class="tgtSentence">Crea una plantilla nueva: </caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="c5764e5062dc45472e3d7147e64d43ac" id="tgt42" class="tgtSentence">En el Portal de Azure clásico, en la página de inicio rápido <ui>Introducción a Rights Management</ui>, haga clic en <ui>Crear una nueva plantilla de directiva de permisos</ui>.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="13a4ef3ad3d0f4600871595d3968a0a8" id="tgt43" class="tgtSentence">Si no ve inmediatamente esta página tras seguir las instrucciones de Office 365, use las instrucciones de navegación del Portal de Azure clásico, enumeradas anteriormente.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="a5aadb6cf420d97607bbb9a7d1ade350" id="tgt44" class="tgtSentence">En la página <ui>Agregar una nueva plantilla de directiva de permisos</ui>, seleccione un idioma en el que tendrá que escribir el nombre de la plantilla y la descripción que verán los usuarios (puede agregar más idiomas más adelante).</caps:sentence>
                    <caps:sentence sentenceid="1a7a5ab7ef93c5c44314700212cc6421" id="tgt45" class="tgtSentence"> A continuación, escribe un nombre y una descripción únicos, y haz clic en el botón Completado.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence sentenceid="df16418eb39ff1f1436d1a649732e224" id="tgt46" class="tgtSentence">En la página de inicio rápido <ui>Empiece a trabajar con Rights Management</ui>, haga clic en <ui>Administrar sus plantillas de directivas de permisos</ui>.</caps:sentence>
                  <caps:sentence sentenceid="a28294158647b574e49cdd6ce1b5b0aa" id="tgt47" class="tgtSentence"> Verá la plantilla recién creada agregada a la lista de plantillas, con el estado <ui>Archivada</ui>.</caps:sentence>
                  <caps:sentence sentenceid="0687736c3d35940ec2ec21425558f764" id="tgt48" class="tgtSentence"> En esta fase, la plantilla se ha creado pero no se ha configurado, y no es visible para los usuarios.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
          <procedure>
            <title>
              <caps:sentence sentenceid="b3821612b33ea4b13e7612622f025e22" id="tgt49" class="tgtSentence">Para configurar y publicar una plantilla personalizada</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="58b06c1c86aa8ad455fbf6a2b5b84f9c" id="tgt50" class="tgtSentence">Seleccione la plantilla recién creada en la página <ui>PLANTILLAS</ui> del Portal de Azure clásico.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="1ce1a1f453f170cf5455c567e3b5631e" id="tgt51" class="tgtSentence">En la página de inicio rápido <ui>Se ha agregado la plantilla</ui>, haga clic en <ui>Introducción</ui> en el paso 1, <ui>Configurar permisos de usuarios y grupos</ui>, elija <ui>EMPEZAR AHORA</ui> o <ui>AGREGAR</ui> y seleccione los usuarios y grupos que tendrán permisos para usar el contenido protegido con la nueva plantilla.</caps:sentence>
                  </para>
                  <alert class="note">
                    <para>
                      <caps:sentence sentenceid="ff5f903f22498c04a729e6d02496971a" id="tgt52" class="tgtSentence">Los usuarios o grupos que selecciones deben disponer de una dirección de correo electrónico.</caps:sentence>
                      <caps:sentence sentenceid="61d86fa6c41a0e44a29e76272b77a195" id="tgt53" class="tgtSentence"> En un entorno productivo, no será un problema, pero en un entorno de pruebas simple, es posible que tengas que agregar direcciones de correo electrónico para cuentas de usuario o grupos.</caps:sentence>
                    </para>
                  </alert>
                  <para>
                    <caps:sentence sentenceid="d30099cc202b2d4edbf75348d2a10180" id="tgt54" class="tgtSentence">Se recomienda usar grupos más que usuarios, lo cual simplifica la administración de las plantillas.</caps:sentence>
                    <caps:sentence sentenceid="28d5a90f60cba04f9ad4692b89d4a6fe" id="tgt55" class="tgtSentence"> Si tiene Active Directory localmente y está sincronizando con Azure AD, puede usar grupos habilitados para correo electrónico que sean grupos de seguridad o grupos de distribución.</caps:sentence>
                    <caps:sentence sentenceid="406d17db11f9335a3ac34fd4d046044c" id="tgt56" class="tgtSentence"> Sin embargo, si desea conceder derechos a todos los usuarios de la organización, resultará más eficiente copiar una de las plantillas predeterminadas en lugar de especificar varios grupos.</caps:sentence>
                    <caps:sentence sentenceid="6b2a797d6490fe8b0e1dd6a9f59f00ab" id="tgt57" class="tgtSentence"> Para obtener más información, consulte la sección <link xlink:href="1775d8d0-9a59-42c8-914f-ce285b71ac1c#BKMK_HowToCopyTemplates">How to copy a template</link> de este tema.</caps:sentence>
                  </para>
                  <alert class="tip">
                    <para>
                      <caps:sentence sentenceid="af07e06a8123ad62d31909a4dccc822a" id="tgt58" class="tgtSentence">Más tarde puede agregar usuarios de fuera de su organización a la plantilla mediante el <externalLink><linkText>módulo Windows PowerShell para Azure Rights Management</linkText><linkUri>https://technet.microsoft.com/library/jj585012.aspx</linkUri></externalLink> y uno de los métodos siguientes:</caps:sentence>
                    </para>
                    <list class="bullet">
                      <listItem>
                        <para>
                          <caps:sentence sentenceid="59b2418d0ffd6285b09b8ba8e32e6796" id="tgt59" class="tgtSentence">
                            <embeddedLabel>Use un objeto de Rights Definition para actualizar una plantilla</embeddedLabel>:    especifique las direcciones de correo electrónico externas y sus derechos en un objeto de Rights Definition, que después usará para actualizar su plantilla.</caps:sentence>
                          <caps:sentence sentenceid="646b82cc6b4624ad4ef87706e188b83d" id="tgt60" class="tgtSentence"> Especifique el objeto de Rights Definition mediante el cmdlet <externalLink><linkText>New-AadrmRightsDefinition</linkText><linkUri>https://msdn.microsoft.com/library/azure/dn727080.aspx</linkUri></externalLink> para crear una variable y, a continuación, suministrar esta variable al parámetro -RightsDefinition con el cmdlet <externalLink><linkText>Set-AadrmTemplateProperty</linkText><linkUri>https://msdn.microsoft.com/library/azure/dn727076.aspx</linkUri></externalLink> para modificar una plantilla existente.</caps:sentence>
                          <caps:sentence sentenceid="f3229c4844c485e77a4b89ec85bfd862" id="tgt61" class="tgtSentence"> Sin embargo, si agrega estos usuarios a una plantilla existente, también tendrá que definir objetos de Rights Definition para los grupos existentes en las plantillas y no solo los usuarios externos nuevos.</caps:sentence>
                        </para>
                      </listItem>
                      <listItem>
                        <para>
                          <caps:sentence sentenceid="0e981289fdf790853c66e0bd9fa5647a" id="tgt62" class="tgtSentence">
                            <embeddedLabel>Exportar, editar e importar la plantilla actualizada</embeddedLabel>: use el cmdlet <externalLink><linkText>Export-AadrmTemplate</linkText><linkUri>https://msdn.microsoft.com/library/azure/dn727078.aspx</linkUri></externalLink> para exportar la plantilla en un archivo que pueda editar para agregar las direcciones de correo electrónico externas de estos usuarios y sus derechos en los grupos y derechos existentes.</caps:sentence>
                          <caps:sentence sentenceid="5618d8d5b9a582a739c0cc27e02dea66" id="tgt63" class="tgtSentence"> A continuación, use el cmdlet <externalLink><linkText>Import-AadrmTemplate</linkText><linkUri>https://msdn.microsoft.com/library/azure/dn727077.aspx</linkUri></externalLink> para importar este cambio de nuevo en Azure RMS.</caps:sentence>
                        </para>
                      </listItem>
                    </list>
                  </alert>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="b288a28c2b701a9ac2949e929b937a1e" id="tgt64" class="tgtSentence">Haz clic en el botón Siguiente y, a continuación, asigna uno de los derechos enumerados a tus usuarios y grupos seleccionados.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="3f4537631ca8d3fd4ae7d45c529be912" id="tgt65" class="tgtSentence">Use la descripción mostrada para obtener más información acerca de cada derecho (y para derechos personalizados).</caps:sentence>
                    <caps:sentence sentenceid="7b7735df672ca19a0db0ea3839fddd82" id="tgt66" class="tgtSentence"> También hay información más detallada disponible en <link xlink:href="97ddde38-b91b-42a5-8eb4-3ce6ce15393d">Configuring Usage Rights for Azure Rights Management</link>.</caps:sentence>
                    <caps:sentence sentenceid="fa1bdfcbf78bb24306b50cec6bf3ceb7" id="tgt67" class="tgtSentence"> Sin embargo, las aplicaciones que son compatibles con RMS pueden variar en la forma de aplicar estos derechos.</caps:sentence>
                    <caps:sentence sentenceid="06858b47263ec5f7deff92c51e9827b6" id="tgt68" class="tgtSentence"> Consulte su documentación y realice sus propias pruebas con las aplicaciones que usan los usuarios para comprobar el comportamiento antes de implementar la plantilla para los usuarios.</caps:sentence>
                    <caps:sentence sentenceid="f6b92da83ef76bffdc014c974db58ee6" id="tgt69" class="tgtSentence"> Para hacer que esta plantilla solo puedan verla los administradores para la realización de las pruebas, defínala como una plantilla de departamento (paso 6).</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="3ceaeea7205cfc1af36fc4a7edad3920" id="tgt70" class="tgtSentence">Si seleccionó <ui>Personalizar</ui>, haga clic en el botón Siguiente y seleccione permisos personalizados.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="f66d68cd5e40866ed1abb8a0c7fad317" id="tgt71" class="tgtSentence">Aunque puedas usar cualquier combinación de derechos individuales disponible, en algunas aplicaciones, hay derechos que pueden depender de otros derechos individuales.</caps:sentence>
                    <caps:sentence sentenceid="5a31e4123de105dfe253341a60432d24" id="tgt72" class="tgtSentence"> Cuando es sí, se seleccionan de forma automática los derechos dependientes.</caps:sentence>
                  </para>
                  <alert class="tip">
                    <para>
                      <caps:sentence sentenceid="ab01ed2d4f7aa8cd18b12faa20ca8c22" id="tgt73" class="tgtSentence">Considere la posibilidad de agregar el permiso <ui>Copiar y extraer contenido</ui> y concedérselo a algunos administradores o personal de otros roles que sean responsables de la recuperación de información.</caps:sentence>
                      <caps:sentence sentenceid="fceb3273073851cdc7930738fcb4b21a" id="tgt74" class="tgtSentence"> Este derecho les permite quitar la protección, si es necesario, de archivos y correos electrónicos que se protegerán con esta plantilla.</caps:sentence>
                      <caps:sentence sentenceid="8845381d02f0d11f2b462bf0afc18184" id="tgt75" class="tgtSentence"> Esta capacidad de quitar la protección en el nivel de plantilla proporciona un control más minucioso que el uso de la característica de superusuario.</caps:sentence>
                    </para>
                  </alert>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="ffd18c170bef4abaced4788e9cb131cf" id="tgt76" class="tgtSentence">Haz clic en el botón Completar.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="ca96ad534259301550a541c5dd176902" id="tgt77" class="tgtSentence">En cambio, si desea que la plantilla pueda verla solo un subconjunto de usuarios cuando vean una lista de plantillas en las aplicaciones: Haga clic en <ui>ÁMBITO</ui> para configurar esto como una plantilla de departamento y haga clic en <ui>COMENZAR AHORA</ui>.</caps:sentence>
                    <caps:sentence sentenceid="45553c55d1340725c742c3027932f211" id="tgt78" class="tgtSentence"> De lo contrario, vaya al paso 9.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="555786c76edb5a0db141723cf5f156cc" id="tgt79" class="tgtSentence">Obtener más información acerca de las plantillas de departamento: De forma predeterminada, todos los usuarios del directorio de Azure verán todas las plantillas publicadas y, a continuación, pueden seleccionarlas en las aplicaciones cuando deseen proteger el contenido.</caps:sentence>
                    <caps:sentence sentenceid="848f8aa09eb714b9613fd6b8d286488e" id="tgt80" class="tgtSentence"> Si desea que solo usuarios específicos vean algunas de las plantillas publicadas, debe definir el ámbito de las plantillas para estos usuarios.</caps:sentence>
                    <caps:sentence sentenceid="dc622cb36abea61d42df03e35b44b798" id="tgt81" class="tgtSentence"> A continuación, solo dichos usuarios podrán seleccionar estas plantillas.</caps:sentence>
                    <caps:sentence sentenceid="f1f229070d5bc5804b78915226ad4ff5" id="tgt82" class="tgtSentence"> Los usuarios no especificados no verán las plantillas y por lo tanto, no pueden seleccionarlas.</caps:sentence>
                    <caps:sentence sentenceid="8a47dfa6a7fa4f9ad47a16dd05434179" id="tgt83" class="tgtSentence"> Esta técnica puede facilitar a los usuarios la elección de la plantilla adecuada, especialmente al crear plantillas que están diseñadas para que las usen grupos o departamentos concretos.</caps:sentence>
                    <caps:sentence sentenceid="ec6e49de83a248bea28fe58673550077" id="tgt84" class="tgtSentence"> Por tanto, los usuarios solo pueden ver las plantillas que se les han designado.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="7deee202a02d376ed16fa08da8a8584c" id="tgt85" class="tgtSentence">Por ejemplo, ha creado una plantilla para el departamento de recursos humanos que aplica el permiso de solo lectura a los miembros del departamento de finanzas.</caps:sentence>
                    <caps:sentence sentenceid="4daffa5eed5745fa6d2ceb7eb4897a9f" id="tgt86" class="tgtSentence"> Para que solo los miembros del departamento de recursos humanos puedan aplicar esta plantilla al usar la aplicación de uso compartido de Administración de derechos, debe definir el ámbito de la plantilla para el grupo habilitado para correo electrónico denominado RecursosHumanos.</caps:sentence>
                    <caps:sentence sentenceid="caae64cfde62b121c88083777f1ff4cf" id="tgt87" class="tgtSentence"> A continuación, solo los miembros de este grupo pueden ver y aplicar esta plantilla.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="f7a3c42aa78bb2ab22b521b021fb3ab8" id="tgt88" class="tgtSentence">En <ui>VISIBILIDAD DE PLANTILLA</ui>, seleccione los usuarios y grupos que podrán ver y seleccionar la plantilla desde las aplicaciones habilitadas para RMS.</caps:sentence>
                    <caps:sentence sentenceid="2fdd2c3534e31a05d05348e35e1cd337" id="tgt89" class="tgtSentence"> Como antes, como procedimiento recomendado, utilice grupos en lugar de usuarios, y los grupos o usuarios que seleccione deben tener una dirección de correo electrónico.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="8368fc060694766cfef27279fc22f704" id="tgt90" class="tgtSentence">Haga clic en el botón Siguiente y decida si es necesario configurar la compatibilidad de aplicaciones para la plantilla de departamento.</caps:sentence>
                    <caps:sentence sentenceid="af9d3773918552718a5b45f45658c84e" id="tgt91" class="tgtSentence"> Si lo hace, haga clic en <ui>COMPATIBILIDAD DE APLICACIÓN</ui>, active la casilla y haga clic en <ui>Completa</ui>.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="e919acce9511c88be81aaf8e74c68467" id="tgt92" class="tgtSentence">¿Por qué debe configurar la compatibilidad de aplicaciones?</caps:sentence>
                    <caps:sentence sentenceid="031d5d2878b49c82cb6bc2ab6420e84e" id="tgt93" class="tgtSentence"> No todas las aplicaciones pueden admitir plantillas de departamento.</caps:sentence>
                    <caps:sentence sentenceid="6bd4f47bb9d16534fdbe45a74d318b2c" id="tgt94" class="tgtSentence"> Para ello, la aplicación debe autenticarse primero con el servicio RMS antes de descargar las plantillas.</caps:sentence>
                    <caps:sentence sentenceid="b04c2886a1a31858bb8ae80430da5047" id="tgt95" class="tgtSentence"> Si el proceso de autenticación no se realiza, de forma predeterminada, ninguna de las plantillas de departamento se descargan.</caps:sentence>
                    <caps:sentence sentenceid="1db80321bb6293654b3ab13d56775ee2" id="tgt96" class="tgtSentence"> Puede invalidar este comportamiento especificando que se deberían descargar todas las plantillas departamentales. Para ello, configure la compatibilidad de aplicaciones y active la casilla <ui>Mostrar esta plantilla a todos los usuarios cuando las aplicaciones no admiten la identidad de usuario</ui>.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="2d9ba0de1e6cf67a22a5beb379fdca76" id="tgt97" class="tgtSentence">Por ejemplo, si no configura la compatibilidad de aplicaciones para la plantilla de departamento en nuestro ejemplo de recursos humanos, solo los usuarios del departamento de recursos humanos verán la plantilla de departamento cuando utilizan la aplicación de uso compartido de RMS, pero ningún usuario verá la plantilla de departamento al usar Outlook Web Access (OWA) de Exchange Server 2013 porque Exchange OWA y Exchange ActiveSync no son compatibles actualmente con las plantillas de departamento.</caps:sentence>
                    <caps:sentence sentenceid="469502518979496e46eccc4bd9e69ff0" id="tgt98" class="tgtSentence"> Si invalida este comportamiento predeterminado mediante la configuración de la compatibilidad de aplicaciones, solo los usuarios del departamento de recursos humanos verán la plantilla de departamento cuando usen la aplicación de uso compartido de RMS, pero todos los usuarios podrán ver la plantilla de departamento al usar Outlook Web Access (OWA).</caps:sentence>
                    <caps:sentence sentenceid="72a2dcee44f6795a9c342a7e0dd165d5" id="tgt99" class="tgtSentence"> Si los usuarios utilizan OWA o Exchange ActiveSync desde Exchange Online, las plantillas de departamento las verán todos los usuarios o bien ninguno, en función del estado de la plantilla (archivado o publicado) en Exchange Online.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="fb123bdbaf59437a7017ea52f3903803" id="tgt100" class="tgtSentence">Office 2016 admite de forma nativa plantillas de departamento, y Office 2013 también con las últimas actualizaciones de Office (<externalLink><linkText>KB 3054853</linkText><linkUri>https://support.microsoft.com/kb/3054853</linkUri></externalLink>).</caps:sentence>
                  </para>
                  <alert class="note">
                    <para>
                      <caps:sentence sentenceid="d939e293f8221ff45038b309fcaa641b" id="tgt101" class="tgtSentence"> Si tiene aplicaciones que aún no admiten de forma nativa las plantillas departamentales, use un script personalizado de descarga de plantillas RMS u otras herramientas para implementar estas plantillas en la carpeta local del cliente de RMS.</caps:sentence>
                      <caps:sentence sentenceid="bee20a780b14de3d6e3e5ba51c938179" id="tgt102" class="tgtSentence"> A continuación, estas aplicaciones mostrarán correctamente las plantillas de departamento solo a los usuarios y grupos que ha seleccionado para el ámbito de la plantilla:</caps:sentence>
                    </para>
                    <list class="bullet">
                      <listItem>
                        <para>
                          <caps:sentence sentenceid="671c3b1f7f9762140ba785dde5f3b21e" id="tgt103" class="tgtSentence">Para Office 2010, la carpeta de cliente es <system>%localappdata%\Microsoft\DRM\Templates</system>.</caps:sentence>
                        </para>
                      </listItem>
                      <listItem>
                        <para>
                          <caps:sentence sentenceid="c1a22d4fbe0d8f95bd10ca76287c89ec" id="tgt104" class="tgtSentence">Desde un equipo cliente que ha descargado todas las plantillas, puede copiar los archivos de plantilla y pegarlos en otros equipos.</caps:sentence>
                        </para>
                      </listItem>
                    </list>
                    <para> </para>
                    <para>
                      <caps:sentence sentenceid="f97f42e5f0b002c0f83bc199e037a6a9" id="tgt105" class="tgtSentence">Puede <externalLink><linkText>descargar el script de plantillas personalizadas de RMS desde el sitio de Microsoft Connect</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=524506</linkUri></externalLink>.</caps:sentence>
                      <caps:sentence sentenceid="ed5ec2f8133ab6c6d9f71fdbb5b8553e" id="tgt106" class="tgtSentence"> Si ve un error al hacer clic en este vínculo, probablemente no se haya registrado en Microsoft Connect.</caps:sentence>
                      <caps:sentence sentenceid="5d20b5fd49f6afdf9f1f2aad4e1dd9a4" id="tgt107" class="tgtSentence">   Para registrarse:</caps:sentence>
                    </para>
                    <list class="ordered">
                      <listItem>
                        <para>
                          <caps:sentence sentenceid="0e5b854bb128eca185c0a7dc7d59dde5" id="tgt108" class="tgtSentence">Vaya al <externalLink><linkText>sitio de Microsoft Connect</linkText><linkUri>http://www.connect.microsoft.com</linkUri></externalLink> e inicie sesión con su cuenta Microsoft.</caps:sentence>
                        </para>
                      </listItem>
                      <listItem>
                        <para>
                          <caps:sentence sentenceid="f41c898ce7a79fff10bc9dba7f817763" id="tgt109" class="tgtSentence">Haga clic en <ui>Directorio</ui> y seleccione la categoría <ui>Ver los productos Connect que no aceptan comentarios</ui>.</caps:sentence>
                        </para>
                      </listItem>
                      <listItem>
                        <para>
                          <caps:sentence sentenceid="943a33c3378576995b8023a255ae2dbd" id="tgt110" class="tgtSentence">Busque <userInput>Rights Management Services</userInput> y, para el programa <ui>Microsoft RMS Enterprise Features</ui>, haga clic en <ui>Unirse</ui>.</caps:sentence>
                        </para>
                      </listItem>
                    </list>
                  </alert>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="9b392ca8ae2341d531c5d4ba8aebfa9d" id="tgt111" class="tgtSentence">Haz clic en <ui>CONFIGURAR</ui> y agrega los idiomas adicionales que usen los usuarios, junto con el nombre y la descripción de esta plantilla en ese idioma.</caps:sentence>
                    <caps:sentence sentenceid="84e18c0cd331dee536bdf0c9c1796362" id="tgt112" class="tgtSentence"> Cuando tienes usuarios multilingües, es importante agregar todos los idiomas que usen; además debes proporcionar un nombre y una descripción en ese idioma.</caps:sentence>
                    <caps:sentence sentenceid="af6ff730b86a1e55fe1e96f9cfae78ef" id="tgt113" class="tgtSentence"> Los usuarios verán entonces el nombre y la descripción de la plantilla en el mismo idioma que su sistema operativo, lo cual garantiza que entenderán la directiva que se aplica a un documento o a un mensaje de correo electrónico.</caps:sentence>
                    <caps:sentence sentenceid="81dbb53e706711bb22bb0177d025e9ea" id="tgt114" class="tgtSentence"> Si no coinciden con el idioma del sistema operativo cliente, el nombre y la descripción que ven se cambiarán al idioma y la descripción que tú hayas definido cuando creaste por primera vez la plantilla.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="5c393e42940071dc747a07addf5cf900" id="tgt115" class="tgtSentence">Después, comprueba si quieres hacer algún cambio en las configuraciones siguientes:</caps:sentence>
                  </para>
                  <table>
                    <thead>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="7dc22b2c6a992f0232345df41303f5ea" id="tgt116" class="tgtSentence">Setting</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="5dc731e46ae38b87ff3e3e2eaf459db2" id="tgt117" class="tgtSentence">Más información</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </thead>
                    <tbody>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="4bb067e90d57996e2b477af7fa473936" id="tgt118" class="tgtSentence">expiración de contenido</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="82d6a807a65c4803c174f433bb2db8e3" id="tgt119" class="tgtSentence">Define una fecha o un número de días para esta plantilla cuando los archivos que están protegidos por dicha plantilla no deben abrirse.</caps:sentence>
                            <caps:sentence sentenceid="6409061e6ebfe76d5e7354be46ef1b3e" id="tgt120" class="tgtSentence"> Puedes especificar una fecha o un número de días a partir del momento en que se aplica la protección al archivo.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence sentenceid="8efd4981d6bf065e15184a32cceb0194" id="tgt121" class="tgtSentence">Cuando se especifica una fecha, entra en vigor a medianoche en su zona horaria actual.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="7f5b2837e334e11f35fe1af4b82f4f7a" id="tgt122" class="tgtSentence">acceso sin conexión</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="30c185b55198825827698b895ed9ed07" id="tgt123" class="tgtSentence">Usa esta configuración para equilibrar los requisitos de seguridad que tengas frente al requisito de que los usuarios deben poder abrir archivos protegidos cuando no disponen de conexión a Internet.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence sentenceid="4f68344d0d790068c64df6a2c3c32d51" id="tgt124" class="tgtSentence">Si especificas que el contenido no está disponible sin conexión a Internet o que el contenido está disponible solamente durante un número concreto de días, cuando se supere ese umbral, los usuarios deberán volver a autenticarse y se registrará su acceso.</caps:sentence>
                            <caps:sentence sentenceid="549e88118f42b0383a83f8e09b09a815" id="tgt125" class="tgtSentence"> Cuando esto sucede, si sus credenciales no se han almacenado en la memoria caché, se pedirá a los usuarios que inicien sesión antes de que puedan abrir el archivo.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence sentenceid="9640c29e75b468b51d309d835f668eba" id="tgt126" class="tgtSentence">Además de la reautenticación, también se vuelve a evaluar la directiva y la pertenencia al grupos de usuarios.</caps:sentence>
                            <caps:sentence sentenceid="f18e6ab07530612e88ef199319b16211" id="tgt127" class="tgtSentence"> De modo que los usuarios podrían experimentar diferentes resultados de acceso para el mismo archivo si se producen cambios en la directiva o la pertenencia al grupo desde la última vez que se accedió al archivo.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </tbody>
                  </table>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="d907a3a0d336bdf1da1b5356a634f764" id="tgt128" class="tgtSentence">Cuando esté seguro de que la plantilla está configurada correctamente para los usuarios, haga clic en <ui>PUBLICAR</ui> para que la plantilla esté visible para los usuarios y elija <ui>GUARDAR</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="7f74f91958c41f1022a129dbeb27be68" id="tgt129" class="tgtSentence">En el Portal clásico, haga clic en el botón para volver a la página <ui>PLANTILLAS</ui>, donde la plantilla tiene ahora el estado actualizado de <ui>Publicada</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence sentenceid="13fb24358d26f66139a82fe9ea408a4d" id="tgt130" class="tgtSentence">Para realizar cualquier cambio en tu plantilla, selecciónala y, a continuación, usa los pasos de inicio rápido otra vez.</caps:sentence>
                  <caps:sentence sentenceid="dfa8896c929ceb02c73612e5cb1cfafd" id="tgt131" class="tgtSentence"> O selecciona una de las opciones siguientes:</caps:sentence>
                </para>
                <list class="bullet">
                  <listItem>
                    <para>
                      <caps:sentence sentenceid="c5ddf11e47d9a50de8b90c3498866ba2" id="tgt132" class="tgtSentence">Para agregar más usuarios y grupos, y definir sus derechos: Haga clic en <ui>PERMISOS</ui> y elija <ui>AGREGAR</ui>.</caps:sentence>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <caps:sentence sentenceid="62163e81f1f74af25feac08dd43821f8" id="tgt133" class="tgtSentence">Para quitar los usuarios o grupos que has seleccionado anteriormente: Haga clic en<ui>PERMISOS</ui>, seleccione el usuario o grupo en la lista y elija <ui>ELIMINAR</ui>.</caps:sentence>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <caps:sentence sentenceid="c003cec8ba91e776d70375038afe6224" id="tgt134" class="tgtSentence">Para cambiar qué usuarios pueden ver las plantillas para seleccionarlas desde las aplicaciones: Haga clic en<ui>ÁMBITO</ui>, elija <ui>AGREGAR</ui>, <ui>ELIMINAR</ui> o <ui>COMPATIBILIDAD DE APLICACIÓN</ui>.</caps:sentence>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <caps:sentence sentenceid="7457a23ede24cb1bbefeee16c313cc5a" id="tgt135" class="tgtSentence">Para que la plantilla ya no sea visible para todos los usuarios: Haga clic en <ui>CONFIGURAR</ui>, elija <ui>ARCHIVO</ui> y haga clic en <ui>GUARDAR</ui>.</caps:sentence>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <caps:sentence sentenceid="3a4a9a8a32d08e7fc528fbf2c783efca" id="tgt136" class="tgtSentence">Para realizar otros cambios de configuración: Haga clic en <ui>CONFIGURAR</ui>, realice los cambios y elija <ui>GUARDAR</ui>.</caps:sentence>
                    </para>
                  </listItem>
                </list>
                <alert class="warning">
                  <para>
                    <caps:sentence sentenceid="3a8af685d7b33074c032eeaa3d1a6d73" id="tgt137" class="tgtSentence">Cuando realices cambios en una plantilla que has guardado antes, los clientes no verán dichos cambios en la plantilla hasta que se actualicen en sus equipos.</caps:sentence>
                    <caps:sentence sentenceid="54857a2224f5e6cc4546dbf8e03184a8" id="tgt138" class="tgtSentence"> Para obtener más información, consulte la sección <link xlink:href="1775d8d0-9a59-42c8-914f-ce285b71ac1c#BKMK_RefreshingTemplates">Refreshing templates for users</link> de este tema.</caps:sentence>
                  </para>
                </alert>
              </content>
            </conclusion>
          </procedure>
        </content>
      </section>
      <section address="BKMK_HowToCopyTemplates">
        <title>
          <caps:sentence sentenceid="3f8bbaecb1a8f4dcf696be3164155618" id="tgt139" class="tgtSentence">Cómo copiar una plantilla</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="8db6c5c5cf4ba15a1583dfc51c984664" id="tgt140" class="tgtSentence">Si desea crear una plantilla nueva que tenga una configuración muy similar a una plantilla existente, seleccione la plantilla original en la página <ui>PLANTILLAS</ui>, haga clic en <ui>COPIAR</ui>, especifique un nombre único y haga los cambios necesarios.</caps:sentence>
          </para>
          <alert class="important">
            <para>
              <caps:sentence sentenceid="bf8ada3ff34d0b234fb6fe9dd4deea7b" id="tgt141" class="tgtSentence">Al copiar una plantilla, se copia también el estado <ui>Publicada</ui> o <ui>Archivada</ui>.</caps:sentence>
              <caps:sentence sentenceid="609504e898a97a8bc6de37de4911e347" id="tgt142" class="tgtSentence"> De modo que si copia una plantilla publicada, se publicará su estado inmediato, a menos que lo cambie.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence sentenceid="30c1e465d67881c1dfa2f0d07371df3d" id="tgt143" class="tgtSentence">Puedes copiar plantillas personalizadas y plantillas predeterminadas.</caps:sentence>
            <caps:sentence sentenceid="df495fcfc4d653b69b6bc1c96eceb919" id="tgt144" class="tgtSentence"> Como práctica recomendada, copie una de las plantillas predeterminadas en lugar de crear una nueva plantilla personalizada si desea que la plantilla conceda derechos a todos los usuarios de su organización.</caps:sentence>
            <caps:sentence sentenceid="93c8be4297eb2456e6f3d038a3c29ff7" id="tgt145" class="tgtSentence"> Este método significa que no debe crear o seleccionar varios grupos para especificar todos los usuarios.</caps:sentence>
            <caps:sentence sentenceid="f873ccb553c29a81e163341331f7f4a0" id="tgt146" class="tgtSentence"> En este escenario, sin embargo, asegúrese de especificar un nombre y una descripción nuevos para la plantilla copiada para idiomas adicionales.</caps:sentence>
          </para>
        </content>
      </section>
      <section address="BKMK_HowToArchiveTemplates">
        <title>
          <caps:sentence sentenceid="7cd7b011ba418ef2fc3aacbff60453b1" id="tgt147" class="tgtSentence">Cómo quitar (archivar) plantillas</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="c427548f17ad6fcd62912e9312f6eb2d" id="tgt148" class="tgtSentence">Las plantillas predeterminadas no se pueden eliminar, pero se pueden archivar para que los usuarios no las vean.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="cd814fa7a194738bdf4a1c2a398f3d1f" id="tgt149" class="tgtSentence">De forma similar, si ha publicado una plantilla personalizada y ya no desea que los usuarios puedan verla, edite la plantilla y elija <ui>ARCHIVAR</ui>, <ui>GUARDAR</ui> en la página <ui>CONFIGURAR</ui>.</caps:sentence>
            <caps:sentence sentenceid="7e22988ac16b2ac22e740152cec15df8" id="tgt150" class="tgtSentence"> O bien seleccione la plantilla en la página <ui>PLANTILLAS</ui> y seleccione <ui>ARCHIVAR</ui>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="2333e0877da6d111b35146a49bb0d15c" id="tgt151" class="tgtSentence">Dado que no puede editar las plantillas predeterminadas, para archivar estas plantillas, debe utilizar la opción <ui>ARCHIVAR</ui> en la página <ui>PLANTILLAS</ui>.</caps:sentence>
            <caps:sentence sentenceid="095de9d4922ef02c6612f241edafe7f3" id="tgt152" class="tgtSentence"> No se puede archivar la opción de Outlook <ui>No reenviar</ui>.</caps:sentence>
          </para>
          <procedure>
            <title>
              <caps:sentence sentenceid="159812ea2091cd940d34c0ddc220ae66" id="tgt153" class="tgtSentence">Para quitar una plantilla predeterminada</caps:sentence>
            </title>
            <steps class="bullet">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="f5d5f8984eca9b3c515726db59c54d82" id="tgt154" class="tgtSentence">En la página <ui>PLANTILLAS</ui>, seleccione la plantilla predeterminada y haga clic en <ui>ARCHIVAR</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence sentenceid="57ccd81c2904bb586966d737689beb9b" id="tgt155" class="tgtSentence">El estado cambia de <ui>Publicada</ui> a <ui>Archivada</ui>.</caps:sentence>
                  <caps:sentence sentenceid="0881d2a469c2606a494369ff0808cbfe" id="tgt156" class="tgtSentence"> Si cambia de opinión, seleccione la plantilla y haga clic en <ui>PUBLICAR</ui>.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
        </content>
      </section>
      <section address="BKMK_RefreshingTemplates">
        <title>
          <caps:sentence sentenceid="c48c3b00f3f155bb904add68a1c26bb0" id="tgt157" class="tgtSentence">Actualización de plantillas para usuarios</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="6e1756339ea6cb4c65c14fad15e0c637" id="tgt158" class="tgtSentence">Cuando usas Azure RMS, se descargan de forma automática plantillas a los ordenadores cliente para que los usuarios puedan seleccionarlas desde sus aplicaciones.</caps:sentence>
            <caps:sentence sentenceid="e8743bb8b7923670d540a577df830bfa" id="tgt159" class="tgtSentence"> Sin embargo, es posible que tengas que tomar medidas adicionales si quieres efectuar cambios en las plantillas:</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ee608a6b49867dd26baac94eb541ee5d" id="tgt160" class="tgtSentence">Aplicación o servicio</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b138d94ddb65aac997edbe7e3be087bf" id="tgt161" class="tgtSentence">Cómo se actualizan las plantillas tras los cambios</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="49f2597b8557b0826ef4d33da1007862" id="tgt162" class="tgtSentence">Exchange Online</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3edd60ac826ab1b3791beb2aa264556a" id="tgt163" class="tgtSentence">Configuración manual precisa para actualizar plantillas.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="2adc135071bd8b27227ef641ef56b813" id="tgt164" class="tgtSentence">Para seguir los pasos de la configuración, expanda la sección siguiente, <link xlink:href="1775d8d0-9a59-42c8-914f-ce285b71ac1c#BKMK_ExchangeOnlineTemplatesUpdate">Exchange Online only: How to configure Exchange to download changed custom templates</link>.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7058a69b01e87f2a5e72edea8b01f865" id="tgt165" class="tgtSentence">Office 365</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4f382482a60a298b634f002ba34be85d" id="tgt166" class="tgtSentence">Actualización automática: no se requieren pasos adicionales.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c342613c15172dbe1564e09ea2af21ee" id="tgt167" class="tgtSentence">Office 2016 y Office 2013</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="4d753578c5274a31710d64aa0095c3cd" id="tgt168" class="tgtSentence">Aplicaciones de uso compartido de RMS para Windows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8472bfe05dc17995c1898e3525749da0" id="tgt169" class="tgtSentence">Actualización automática – programada: </caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="a630bb16e8f15d2f0a5ba223b0172547" id="tgt170" class="tgtSentence">Para estas versiones posteriores de Office: el intervalo de actualización predeterminado es cada 7 días.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="daecc3ac8089062ab999ef920e268247" id="tgt171" class="tgtSentence">Para la aplicación de uso compartido de RMS para Windows: a partir de la versión 1.0.1784.0, el intervalo de actualización predeterminado es cada día.</caps:sentence>
                        <caps:sentence sentenceid="91d17de05c3d88b2e7338813a12618ef" id="tgt172" class="tgtSentence"> Las versiones anteriores tienen un intervalo de actualización predeterminado de 7 días.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence sentenceid="08c5c5ac423ed6248db1ca28e1d0fe8f" id="tgt173" class="tgtSentence">Para que la actualización se lleve a cabo antes de lo programado, expanda la sección siguiente, <link xlink:href="#BKMK_Office2013ForceUpdate">Office 2016,  Office 2013, and RMS sharing application for Windows: How to force a refresh for a changed custom template</link>.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a905224547ab9aa4a77962c1320215d2" id="tgt174" class="tgtSentence">Office 2010</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8db28cd824d960239cfd07c38b45e16f" id="tgt175" class="tgtSentence">Se actualiza cuando los usuarios inician sesión.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="00927a31678bbd6771a850247f5f0b15" id="tgt176" class="tgtSentence">Para forzar una actualización, pide u obliga a los usuarios a cerrar sesión y volver a iniciar la sesión.</caps:sentence>
                    <caps:sentence sentenceid="010aa03dd267ad9ef96b16b273280d1c" id="tgt177" class="tgtSentence"> O bien, vea la sección siguiente: <link xlink:href="#BKMK_Office2010ForceUpdate">Office 2010 only: How to force a refresh for a changed custom template</link>.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <caps:sentence sentenceid="d7bc5ca85422d8caafb3a34fbfb623f7" id="tgt178" class="tgtSentence">Para los dispositivos móviles que usan la aplicación de uso compartido de RMS, se descargan automáticamente plantillas (y se actualizan si es necesario) sin que sea precisa una nueva configuración.</caps:sentence>
          </para>
        </content>
        <sections>
          <section address="BKMK_ExchangeOnlineTemplatesUpdate" expanded="false">
            <title>
              <caps:sentence sentenceid="94f89f36b2cc68e0cc6a66c791f078f9" id="tgt179" class="tgtSentence">Solamente Exchange Online: Cómo configurar Exchange para descargar las plantillas personalizadas que se han cambiado</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="282ac76506f0bd3d0e157fcbabaf1eef" id="tgt180" class="tgtSentence">Si ya has configurado Information Rights Management (IRM) para Exchange Online, no se descargarán plantillas personalizadas para usuarios hasta que realices los cambios siguientes mediante Windows PowerShell en Exchange Online.</caps:sentence>
              </para>
              <alert class="note">
                <para>
                  <caps:sentence sentenceid="b749843275b3b19c40f94b610ff3f4dc" id="tgt181" class="tgtSentence">Para obtener más información acerca de cómo usar Windows PowerShell en Exchange Online, consulte <externalLink><linkText>Usar PowerShell con Exchange Online</linkText><linkUri>https://technet.microsoft.com/library/jj200677(v=exchg.160).aspx</linkUri></externalLink>.</caps:sentence>
                </para>
              </alert>
              <para>
                <caps:sentence sentenceid="4fee9f22e6cba552f92c48419c91775a" id="tgt182" class="tgtSentence">Debes efectuar este procedimiento cada vez que cambies una plantilla.</caps:sentence>
              </para>
              <procedure>
                <title>
                  <caps:sentence sentenceid="3ecd6ba4d80d87fd2032e808faec13bd" id="tgt183" class="tgtSentence">Para actualizar plantillas para Exchange Online</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="21a47ac432e58e412f2c83dbcd821a9c" id="tgt184" class="tgtSentence">Conéctese al servicio mediante Windows PowerShell en Exchange Online:</caps:sentence>
                      </para>
                      <list class="ordered">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="1f823633b263d3789d0d60900d568a2b" id="tgt185" class="tgtSentence">Especifique el nombre de usuario y la contraseña de Office 365:</caps:sentence>
                          </para>
                          <code>$Cred = Get-Credential</code>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="9c51e8012468065678cc4e94f8ea8129" id="tgt186" class="tgtSentence">Conecte con el servicio Exchange Online mediante la ejecución de los dos comandos siguientes:</caps:sentence>
                          </para>
                          <code>$Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.outlook.com/powershell/ -Credential $Cred -Authentication Basic –AllowRedirection</code>
                          <code>Import-PSSession $Session</code>
                        </listItem>
                      </list>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="57719aa3521cc04d95861ed9b1115209" id="tgt187" class="tgtSentence">Usa el cmdlet <externalLink><linkText>Import-RMSTrustedPublishingDomain</linkText><linkUri>http://technet.microsoft.com/library/jj200724(v=exchg.160).aspx</linkUri></externalLink> para volver a importar tu Dominio de publicación de confianza (TPD) desde Azure RMS:</caps:sentence>
                      </para>
                      <code>Import-RMSTrustedPublishingDomain -Name "&lt;TPD name&gt;" -RefreshTemplates -RMSOnline</code>
                      <para>
                        <caps:sentence sentenceid="8a8a3a7bf3aed6bea0709b314ce72694" id="tgt188" class="tgtSentence">Por ejemplo, si su nombre TPD es <ui>RMS Online - 1</ui> (un nombre habitual en muchas organizaciones), escriba: <userInput>Import-RMSTrustedPublishingDomain -Name "RMS Online - 1" -RefreshTemplates -RMSOnline</userInput></caps:sentence>
                      </para>
                      <alert class="note">
                        <para>
                          <caps:sentence sentenceid="f7baf6bf6b52b57d3a74ee59089dd563" id="tgt189" class="tgtSentence">Para comprobar tu nombre de TPD, puedes usar el cmdlet <externalLink><linkText>Get-RMSTrustedPublishingDomain</linkText><linkUri>http://technet.microsoft.com/library/jj200707(v=exchg.160).aspx</linkUri></externalLink>.</caps:sentence>
                        </para>
                      </alert>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="9b3048c75d7a47f9e5e5ff30d8886c86" id="tgt190" class="tgtSentence">Para confirmar que se han importado correctamente las plantillas, espere unos minutos y, a continuación, ejecute el cmdlet <externalLink><linkText>Get-RMSTemplate</linkText><linkUri>http://technet.microsoft.com/library/dd297960(v=exchg.160).aspx</linkUri></externalLink> y, en Tipo, especifique Todas.</caps:sentence>
                        <caps:sentence sentenceid="4be0bb25039056347740ae85bcda324d" id="tgt191" class="tgtSentence"> Por ejemplo:</caps:sentence>
                      </para>
                      <code>Get-RMSTemplate -TrustedPublishingDomain "RMS Online - 1" -Type All
</code>
                      <alert class="tip">
                        <para>
                          <caps:sentence sentenceid="3bd6aa3512005cbedf92330596d6fa26" id="tgt192" class="tgtSentence">Es útil conservar una copia de la salida, con el fin de poder copiar fácilmente los nombres de plantilla o los GUID si posteriormente se archiva una plantilla.</caps:sentence>
                        </para>
                      </alert>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="8b40a426faf1c77d29748e822079490f" id="tgt193" class="tgtSentence">Por cada plantilla importada que desea que esté disponible en la aplicación web de Outlook, debe usar el cmdlet <externalLink><linkText>Set-RMSTemplate</linkText><linkUri>http://technet.microsoft.com/library/hh529923(v=exchg.160).aspx</linkUri></externalLink> y establecer Tipo en Distribuido:</caps:sentence>
                      </para>
                      <code>Set-RMSTemplate -Identity "&lt;name  or GUID of the template&gt;" -Type Distributed</code>
                      <para>
                        <caps:sentence sentenceid="64472e6edd900169927a8502fc76d9b8" id="tgt194" class="tgtSentence">Dado que Outlook Web Access almacena en caché la interfaz de usuario durante las 24 horas, es posible que los usuarios no puedan ver la plantilla nueva hasta un día después.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
              <para>
                <caps:sentence sentenceid="5daa701186c76fd097cbdd312b505dd3" id="tgt195" class="tgtSentence">Además, si archivas una plantilla (personalizada o predeterminada) y usas Exchange Online con Office 365, los usuarios continuarán viendo las plantillas archivadas si usan la aplicación web de Outlook o dispositivos móviles que usen el protocolo Exchange ActiveSync.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="e5a7fd0349b8debcd715b4e1d60a3090" id="tgt196" class="tgtSentence">Para que los usuarios no vean estas plantillas, conéctate al servicio mediante Windows PowerShell en Exchange Online y, a continuación, usa el cmdlet <externalLink><linkText>Set-RMSTemplate</linkText><linkUri>http://technet.microsoft.com/library/hh529923(v=exchg.160).aspx</linkUri></externalLink> y ejecuta este comando: </caps:sentence>
              </para>
              <code>Set-RMSTemplate -Identity "&lt;name or GUID of the template&gt;" -Type Archived</code>
            </content>
          </section>
          <section expanded="false" address="BKMK_Office2013ForceUpdate">
            <title>
              <caps:sentence sentenceid="24ff5268fb1b8da8cbaab403900d667a" id="tgt197" class="tgtSentence">Office 2016, Office 2013 y la aplicación RMS sharing para Windows: Cómo forzar una actualización de una plantilla personalizada que se ha cambiado</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="50b6ffb5719624496f54c542bcef93cd" id="tgt198" class="tgtSentence">Si modifica el Registro de los equipos que ejecutan Office 2016, Office 2013 o la aplicación Rights Management (RMS) sharing, puede cambiar la programación automática para que las plantillas cambiadas se actualicen en los equipos con más frecuencia que la indicada en sus valores predeterminados.</caps:sentence>
                <caps:sentence sentenceid="c9af07a21fcad7793ab37ad027ba8892" id="tgt199" class="tgtSentence"> También puede forzar una actualización inmediata eliminando los datos existentes en un valor del Registro.</caps:sentence>
              </para>
              <alert class="warning">
                <para>
                  <caps:sentence sentenceid="5181d6f94cb9ba09d2544143924b8d71" id="tgt200" class="tgtSentence">Si usas el Editor del Registro de forma incorrecta, es posible que ocasiones problemas serios que puedan hacer preciso que reinstales el sistema operativo.</caps:sentence>
                  <caps:sentence sentenceid="ec450b2ed94b11d7834d107ddddea1a6" id="tgt201" class="tgtSentence"> Microsoft no puede garantizar que seas capaz de resolver problemas ocasionados por el uso inapropiado del Editor del Registro.</caps:sentence>
                  <caps:sentence sentenceid="4ff25849eb1f853eb8b41052415a2af7" id="tgt202" class="tgtSentence"> Usa el Editor del Registro bajo tu propia responsabilidad.</caps:sentence>
                </para>
              </alert>
              <procedure>
                <title>
                  <caps:sentence sentenceid="aa0098439cd9daa075481a0528a78347" id="tgt203" class="tgtSentence">Para cambiar la programación automática</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="5d12c4fec638cbfa58babb96cccb3eb5" id="tgt204" class="tgtSentence">Con un editor del Registro, cree y establezca uno de los valores del Registro siguientes:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="0eb9681c48deb423d3e2d2b70d9b0ee4" id="tgt205" class="tgtSentence">Para establecer una frecuencia de actualización en días (mínimo de 1 día):  cree un nuevo valor del Registro denominado <ui>TemplateUpdateFrequency</ui> y defina un valor entero para los datos, que especifique la frecuencia en días para descargar los cambios en una plantilla descargada.</caps:sentence>
                            <caps:sentence sentenceid="f77ac7fe065b3338da90d9f8ef6f1ee5" id="tgt206" class="tgtSentence"> Use la tabla siguiente para localizar la ruta de acceso del Registro y crear este nuevo valor del Registro.</caps:sentence>
                          </para>
                          <table>
                            <thead>
                              <tr>
                                <TD>
                                  <para>
                                    <caps:sentence sentenceid="b75ba2542571d3ceaab9c5d83c92075c" id="tgt207" class="tgtSentence">Ruta de acceso del registro</caps:sentence>
                                  </para>
                                </TD>
                                <TD>
                                  <para>
                                    <caps:sentence sentenceid="599dcce2998a6b40b1e38e8c6006cb0a" id="tgt208" class="tgtSentence">Tipo</caps:sentence>
                                  </para>
                                </TD>
                                <TD>
                                  <para>
                                    <caps:sentence sentenceid="2063c1608d6e0baf80249c42e2be5804" id="tgt209" class="tgtSentence">Valor</caps:sentence>
                                  </para>
                                </TD>
                              </tr>
                            </thead>
                            <tbody>
                              <tr>
                                <TD>
                                  <para>
                                    <caps:sentence sentenceid="273fc666772881ae17cc4fe9a81b3112" id="tgt210" class="tgtSentence">HKEY_CURRENT_USER\Software\Classes\Local Settings\Software\Microsoft\MSIPC</caps:sentence>
                                  </para>
                                </TD>
                                <TD>
                                  <para>
                                    <caps:sentence sentenceid="218feb4305adffe7bdfa1642906f64b3" id="tgt211" class="tgtSentence">REG_DWORD</caps:sentence>
                                  </para>
                                </TD>
                                <TD>
                                  <para>
                                    <caps:sentence sentenceid="330310998e33eaae45d74865cb670695" id="tgt212" class="tgtSentence">TemplateUpdateFrequency</caps:sentence>
                                  </para>
                                </TD>
                              </tr>
                            </tbody>
                          </table>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="666dc016e658160c0756dec03435d4f7" id="tgt213" class="tgtSentence">Para establecer una frecuencia de actualización en segundos (mínimo de 1 segundo):  cree un nuevo valor del Registro denominado <ui>TemplateUpdateFrequencyInSeconds</ui> y defina un valor entero para los datos, que especifique la frecuencia en segundos para descargar los cambios en una plantilla descargada.</caps:sentence>
                            <caps:sentence sentenceid="f77ac7fe065b3338da90d9f8ef6f1ee5" id="tgt214" class="tgtSentence"> Use la tabla siguiente para localizar la ruta de acceso del Registro y crear este nuevo valor del Registro.</caps:sentence>
                          </para>
                          <table>
                            <thead>
                              <tr>
                                <TD>
                                  <para>
                                    <caps:sentence sentenceid="b75ba2542571d3ceaab9c5d83c92075c" id="tgt215" class="tgtSentence">Ruta de acceso del registro</caps:sentence>
                                  </para>
                                </TD>
                                <TD>
                                  <para>
                                    <caps:sentence sentenceid="599dcce2998a6b40b1e38e8c6006cb0a" id="tgt216" class="tgtSentence">Tipo</caps:sentence>
                                  </para>
                                </TD>
                                <TD>
                                  <para>
                                    <caps:sentence sentenceid="2063c1608d6e0baf80249c42e2be5804" id="tgt217" class="tgtSentence">Valor</caps:sentence>
                                  </para>
                                </TD>
                              </tr>
                            </thead>
                            <tbody>
                              <tr>
                                <TD>
                                  <para>
                                    <caps:sentence sentenceid="273fc666772881ae17cc4fe9a81b3112" id="tgt218" class="tgtSentence">HKEY_CURRENT_USER\Software\Classes\Local Settings\Software\Microsoft\MSIPC</caps:sentence>
                                  </para>
                                </TD>
                                <TD>
                                  <para>
                                    <caps:sentence sentenceid="218feb4305adffe7bdfa1642906f64b3" id="tgt219" class="tgtSentence">REG_DWORD</caps:sentence>
                                  </para>
                                </TD>
                                <TD>
                                  <para>
                                    <caps:sentence sentenceid="61eae0a6070a04ba24a987456484d968" id="tgt220" class="tgtSentence">TemplateUpdateFrequencyInSeconds</caps:sentence>
                                  </para>
                                </TD>
                              </tr>
                            </tbody>
                          </table>
                        </listItem>
                      </list>
                      <para>
                        <caps:sentence sentenceid="644c3e54e02861fce902d41eba85e565" id="tgt221" class="tgtSentence">Asegúrese de crear y establecer uno de estos valores del Registro, no ambos.</caps:sentence>
                        <caps:sentence sentenceid="da4e3a0fa3c7f9a16ab44be3640b15f7" id="tgt222" class="tgtSentence"> Si ambos están presentes, <system>TemplateUpdateFrequency</system> se omite.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="9d6eca84449af15fd9665335fbecfa2a" id="tgt223" class="tgtSentence">Si desea forzar una actualización inmediata de las plantillas, vaya al procedimiento siguiente.</caps:sentence>
                        <caps:sentence sentenceid="1912e182f0830d999a172ea4c4d6f74d" id="tgt224" class="tgtSentence"> En caso contrario, reinicie ahora las aplicaciones de Office y las instancias del Explorador de archivos.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
              <procedure>
                <title>
                  <caps:sentence sentenceid="4b0613ad8e2a0e7606654921772dba58" id="tgt225" class="tgtSentence">Para forzar una actualización inmediata</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="e80764f07f8f6da535730ff850e5990a" id="tgt226" class="tgtSentence">Con un editor del Registro, elimine los datos del valor <ui>LastUpdatedTime</ui>.</caps:sentence>
                        <caps:sentence sentenceid="e32ea5ab157e8e86580741fec5196600" id="tgt227" class="tgtSentence"> Por ejemplo, en los datos puede aparecer <ui>2015-04-20T15:52</ui>. Elimine 2015-04-20T15:52 para que no se muestre ningún dato.</caps:sentence>
                        <caps:sentence sentenceid="82502417f71389f9fbae9f233eb5f6ce" id="tgt228" class="tgtSentence"> Use la tabla siguiente para localizar la ruta de acceso del Registro y eliminar estos datos del valor del Registro.</caps:sentence>
                      </para>
                      <table>
                        <thead>
                          <tr>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="b75ba2542571d3ceaab9c5d83c92075c" id="tgt229" class="tgtSentence">Ruta de acceso del registro</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="599dcce2998a6b40b1e38e8c6006cb0a" id="tgt230" class="tgtSentence">Tipo</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="2063c1608d6e0baf80249c42e2be5804" id="tgt231" class="tgtSentence">Valor</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                        </thead>
                        <tbody>
                          <tr>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="3ecf8d04144f9c872f6a56bf1efcf1af" id="tgt232" class="tgtSentence">HKEY_CURRENT_USER\Software\Classes\Local Settings\Software\Microsoft\MSIPC\&lt;MicrosoftRMS_FQDN&gt;\Template</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="2b1bda4361069cdf7a4437824c22893c" id="tgt233" class="tgtSentence">REG_SZ</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="9f314df3b450e03872a2ad4b95509b11" id="tgt234" class="tgtSentence">LastUpdatedTime</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                        </tbody>
                      </table>
                      <alert class="tip">
                        <para>
                          <caps:sentence sentenceid="3cacbd764a14f3e778812254e3389651" id="tgt235" class="tgtSentence">En la ruta de acceso del Registro, <placeholder>&lt;MicrosoftRMS_FQDN&gt;</placeholder> hace referencia al FQDN de servicio de Microsoft RMS.</caps:sentence>
                          <caps:sentence sentenceid="f13fb0b6696bdeac83dc165ee15619e7" id="tgt236" class="tgtSentence"> Si desea comprobar este valor:</caps:sentence>
                        </para>
                        <list class="ordered">
                          <listItem>
                            <para>
                              <caps:sentence sentenceid="d93fe5ac9a49f4f86dc7b265338996f2" id="tgt237" class="tgtSentence">Ejecute el cmdlet <externalLink><linkText>Get-AadrmConfiguration</linkText><linkUri>https://msdn.microsoft.com/library/windowsazure/dn629410.aspx</linkUri></externalLink> para Azure RMS.</caps:sentence>
                              <caps:sentence sentenceid="01f98a3fb6bcba402290b37370e944e5" id="tgt238" class="tgtSentence"> Si no ha instalado todavía el módulo Windows PowerShell para Azure RMS, consulte <link xlink:href="0d665ed6-b1de-4d63-854a-bc57c1c49844">Installing Windows PowerShell for Azure Rights Management</link>.</caps:sentence>
                            </para>
                          </listItem>
                          <listItem>
                            <para>
                              <caps:sentence sentenceid="861a54c9e619aaf0b0bef400964efe11" id="tgt239" class="tgtSentence">En la salida, identifique el valor <ui>LicensingIntranetDistributionPointUrl</ui>.</caps:sentence>
                            </para>
                            <para>
                              <caps:sentence sentenceid="c7f7c8f690f0fc791d7b0b8b3a7c9a2e" id="tgt240" class="tgtSentence">Por ejemplo: <ui>LicensingIntranetDistributionPointUrl   : https://5c6bb73b-1038-4eec-863d-49bded473437.rms.na.aadrm.com/_wmcs/licensing</ui></caps:sentence>
                            </para>
                          </listItem>
                          <listItem>
                            <para>
                              <caps:sentence sentenceid="8f2b0edd7a56a8702be843aa4228a52e" id="tgt241" class="tgtSentence">En el valor, quite <ui>https://</ui> y <ui>/_wmcs/licensing</ui> de esta cadena.</caps:sentence>
                              <caps:sentence sentenceid="a159ab8a309a6e096eb4d68a4a478916" id="tgt242" class="tgtSentence"> El valor restante es el FQDN de servicio de Microsoft RMS.</caps:sentence>
                              <caps:sentence sentenceid="06d3e21ddb6464d0fdc93e59bc6bdf13" id="tgt243" class="tgtSentence"> En nuestro ejemplo, el FQDN de servicio de Microsoft RMS sería el valor siguiente:</caps:sentence>
                            </para>
                            <para>
                              <ui>
                                <caps:sentence sentenceid="ff0c56b714d3faf6016725fcbb3253d8" id="tgt244" class="tgtSentence">5c6bb73b-1038-4eec-863d-49bded473437.rms.na.aadrm.com</caps:sentence>
                              </ui>
                            </para>
                          </listItem>
                        </list>
                      </alert>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="0088a168c2b9c149ee8c9cf64a83a07c" id="tgt245" class="tgtSentence">Elimine la carpeta siguiente y todos los archivos que contenga: <system>%localappdata%\Microsoft\MSIPC\Templates</system></caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="860b6605ac7eb64e2b9bca20016ddd01" id="tgt246" class="tgtSentence">Reinicie las aplicaciones de Office y las instancias del Explorador de archivos.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
            </content>
          </section>
          <section expanded="false" address="BKMK_Office2010ForceUpdate">
            <title>
              <caps:sentence sentenceid="990825294442582abab81ef08227e516" id="tgt247" class="tgtSentence">Solamente para Office 2010: Cómo forzar una actualización de una plantilla personalizada que se ha cambiado</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="80ed44e32ece2342b2260d978665df53" id="tgt248" class="tgtSentence">Si modifica el Registro de los equipos que ejecutan Office 2010, puede establecer un valor para que las plantillas cambiadas se actualicen en los equipos sin esperar a que los usuarios cierren la sesión y vuelvan a iniciarla.</caps:sentence>
                <caps:sentence sentenceid="c9af07a21fcad7793ab37ad027ba8892" id="tgt249" class="tgtSentence"> También puede forzar una actualización inmediata eliminando los datos existentes en un valor del Registro.</caps:sentence>
              </para>
              <alert class="warning">
                <para>
                  <caps:sentence sentenceid="5181d6f94cb9ba09d2544143924b8d71" id="tgt250" class="tgtSentence">Si usas el Editor del Registro de forma incorrecta, es posible que ocasiones problemas serios que puedan hacer preciso que reinstales el sistema operativo.</caps:sentence>
                  <caps:sentence sentenceid="ec450b2ed94b11d7834d107ddddea1a6" id="tgt251" class="tgtSentence"> Microsoft no puede garantizar que seas capaz de resolver problemas ocasionados por el uso inapropiado del Editor del Registro.</caps:sentence>
                  <caps:sentence sentenceid="4ff25849eb1f853eb8b41052415a2af7" id="tgt252" class="tgtSentence"> Usa el Editor del Registro bajo tu propia responsabilidad.</caps:sentence>
                </para>
              </alert>
              <procedure>
                <title>
                  <caps:sentence sentenceid="84218dd0e1e8c69ed9cd9fdf7e0bae75" id="tgt253" class="tgtSentence">Para cambiar la frecuencia de actualización</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="91d018bf880aaac7e7527b0934e4c054" id="tgt254" class="tgtSentence">Con un editor del Registro, cree un nuevo valor del Registro denominado <ui>UpdateFrequency</ui> y defina un valor entero para los datos, que especifique la frecuencia en días para descargar los cambios en una plantilla descargada.</caps:sentence>
                        <caps:sentence sentenceid="f77ac7fe065b3338da90d9f8ef6f1ee5" id="tgt255" class="tgtSentence"> Use la tabla siguiente para localizar la ruta de acceso del Registro y crear este nuevo valor del Registro.</caps:sentence>
                      </para>
                      <table>
                        <thead>
                          <tr>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="b75ba2542571d3ceaab9c5d83c92075c" id="tgt256" class="tgtSentence">Ruta de acceso del registro</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="599dcce2998a6b40b1e38e8c6006cb0a" id="tgt257" class="tgtSentence">Tipo</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="2063c1608d6e0baf80249c42e2be5804" id="tgt258" class="tgtSentence">Valor</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                        </thead>
                        <tbody>
                          <tr>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="d5af49f6f597fcc8c1cc972723dabe80" id="tgt259" class="tgtSentence">HKEY_CURRENT_USER\Software\Microsoft\MSDRM\TemplateManagement</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="218feb4305adffe7bdfa1642906f64b3" id="tgt260" class="tgtSentence">REG_DWORD</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="1f4d2225db3bbe649e4cb0c8e62aa5f5" id="tgt261" class="tgtSentence">UpdateFrequency</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                        </tbody>
                      </table>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="9d6eca84449af15fd9665335fbecfa2a" id="tgt262" class="tgtSentence">Si desea forzar una actualización inmediata de las plantillas, vaya al procedimiento siguiente.</caps:sentence>
                        <caps:sentence sentenceid="f89a77f8955a4353b80dcfa3751898fd" id="tgt263" class="tgtSentence"> En caso contrario, reinicie ahora las aplicaciones de Office.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
              <procedure>
                <title>
                  <caps:sentence sentenceid="4b0613ad8e2a0e7606654921772dba58" id="tgt264" class="tgtSentence">Para forzar una actualización inmediata</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="e80764f07f8f6da535730ff850e5990a" id="tgt265" class="tgtSentence">Con un editor del Registro, elimine los datos del valor <ui>LastUpdatedTime</ui>.</caps:sentence>
                        <caps:sentence sentenceid="e32ea5ab157e8e86580741fec5196600" id="tgt266" class="tgtSentence"> Por ejemplo, en los datos puede aparecer <ui>2015-04-20T15:52</ui>. Elimine 2015-04-20T15:52 para que no se muestre ningún dato.</caps:sentence>
                        <caps:sentence sentenceid="82502417f71389f9fbae9f233eb5f6ce" id="tgt267" class="tgtSentence"> Use la tabla siguiente para localizar la ruta de acceso del Registro y eliminar estos datos del valor del Registro.</caps:sentence>
                      </para>
                      <table>
                        <thead>
                          <tr>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="b75ba2542571d3ceaab9c5d83c92075c" id="tgt268" class="tgtSentence">Ruta de acceso del registro</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="599dcce2998a6b40b1e38e8c6006cb0a" id="tgt269" class="tgtSentence">Tipo</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="2063c1608d6e0baf80249c42e2be5804" id="tgt270" class="tgtSentence">Valor</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                        </thead>
                        <tbody>
                          <tr>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="d5af49f6f597fcc8c1cc972723dabe80" id="tgt271" class="tgtSentence">HKEY_CURRENT_USER\Software\Microsoft\MSDRM\TemplateManagement</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="2b1bda4361069cdf7a4437824c22893c" id="tgt272" class="tgtSentence">REG_SZ</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="9f314df3b450e03872a2ad4b95509b11" id="tgt273" class="tgtSentence">lastUpdatedTime</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                        </tbody>
                      </table>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="0088a168c2b9c149ee8c9cf64a83a07c" id="tgt274" class="tgtSentence">Elimine la carpeta siguiente y todos los archivos que contenga: <system>%localappdata%\Microsoft\MSIPC\Templates</system></caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="f0aa5b34a492a74385d8c78c1e51297c" id="tgt275" class="tgtSentence">Reinicie las aplicaciones de Office.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
            </content>
          </section>
        </sections>
      </section>
      <section address="BKMK_PowerShellTemplates">
        <title>
          <caps:sentence sentenceid="aae4cdde6f11f49bf2e3b4137d246319" id="tgt276" class="tgtSentence">Referencia de Windows PowerShell</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="0c5804e0442b2ef43f1972af92e46744" id="tgt277" class="tgtSentence">Todo lo que puede hacer en el Portal de Azure clásico para crear y administrar plantillas puede hacerlo desde la línea de comandos con Windows PowerShell.</caps:sentence>
            <caps:sentence sentenceid="3e5c298c4aaa3f2018267c03f79d8b9f" id="tgt278" class="tgtSentence"> Además, puede exportar e importar plantillas, de manera que pueda copiar plantillas entre inquilinos o llevar a cabo ediciones en masa de propiedades complejas en plantillas, como descripciones y nombres multilingües.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="174c7775d52d796778fd6be5b71811cd" id="tgt279" class="tgtSentence">También puede utilizar la exportación e importación para restaurar y hacer una copia de seguridad de sus plantillas personalizadas. Como práctica recomendada, haga una copia de seguridad de sus plantillas personalizadas periódicamente, de modo que si realiza un cambio que no pretendía, pueda revertir fácilmente a una versión anterior.</caps:sentence>
          </para>
          <alert class="important">
            <para>
              <caps:sentence sentenceid="1920ad5d67304d11553b45bcd0c6bb5f" id="tgt280" class="tgtSentence">Para usar Windows PowerShell para crear y administrar plantillas de directiva de permisos de Azure RMS, debe tener al menos la versión 2.0.0.0 del <externalLink><linkText>módulo de Windows PowerShell para Azure RMS</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=257721</linkUri></externalLink>.</caps:sentence>
            </para>
            <para>
              <caps:sentence sentenceid="7109d3d4216b36bb3a2211346784d3da" id="tgt281" class="tgtSentence">Si ya instaló este módulo de Windows PowerShell, ejecute el comando siguiente en una ventana de PowerShell para comprobar el número de versión: <codeInline>(Get-Module aadrm -ListAvailable).Version</codeInline></caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence sentenceid="f5e8e4ee3591a128cc955b54bdcf1b35" id="tgt282" class="tgtSentence">Para obtener instrucciones de instalación, consulte <link xlink:href="0d665ed6-b1de-4d63-854a-bc57c1c49844">Installing Windows PowerShell for Azure Rights Management</link>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="455b359d21f8611208b32c0726b2ec0b" id="tgt283" class="tgtSentence">Los cmdlets que admite la creación y administración de plantillas:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <externalLink>
                  <linkText>
                    <caps:sentence sentenceid="fa5a498e6d4cd6853d058d8837968244" id="tgt284" class="tgtSentence">Add-AadrmTemplate</caps:sentence>
                  </linkText>
                  <linkUri>https://msdn.microsoft.com/library/azure/dn727075.aspx</linkUri>
                </externalLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <externalLink>
                  <linkText>
                    <caps:sentence sentenceid="413ca80acc1a27527c9990321a4da72f" id="tgt285" class="tgtSentence">Export-AadrmTemplate</caps:sentence>
                  </linkText>
                  <linkUri>https://msdn.microsoft.com/library/azure/dn727078.aspx</linkUri>
                </externalLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <externalLink>
                  <linkText>
                    <caps:sentence sentenceid="3823983d5e82063504923d463fe79524" id="tgt286" class="tgtSentence">Get-AadrmTemplate</caps:sentence>
                  </linkText>
                  <linkUri>https://msdn.microsoft.com/library/azure/dn727079.aspx</linkUri>
                </externalLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <externalLink>
                  <linkText>
                    <caps:sentence sentenceid="aad9ebe2ec0206d8a656a6f3e0bb9f29" id="tgt287" class="tgtSentence">Get-AadrmTemplateProperty</caps:sentence>
                  </linkText>
                  <linkUri>https://msdn.microsoft.com/library/azure/dn727081.aspx</linkUri>
                </externalLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <externalLink>
                  <linkText>
                    <caps:sentence sentenceid="ba53f5bacd4fc26570c5866cfffc92e2" id="tgt288" class="tgtSentence">Import-AadrmTemplate</caps:sentence>
                  </linkText>
                  <linkUri>https://msdn.microsoft.com/library/azure/dn727077.aspx</linkUri>
                </externalLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <externalLink>
                  <linkText>
                    <caps:sentence sentenceid="3680251f9142e74575241c1f235b86fa" id="tgt289" class="tgtSentence">New-AadrmRightsDefinition</caps:sentence>
                  </linkText>
                  <linkUri>https://msdn.microsoft.com/library/azure/dn727080.aspx</linkUri>
                </externalLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <externalLink>
                  <linkText>
                    <caps:sentence sentenceid="3d28229350cdb5aed345e5a7331e455d" id="tgt290" class="tgtSentence">Remove-AadrmTemplate</caps:sentence>
                  </linkText>
                  <linkUri>https://msdn.microsoft.com/library/azure/dn727082.aspx</linkUri>
                </externalLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <externalLink>
                  <linkText>
                    <caps:sentence sentenceid="19c66624055a6ff305e5486c981c49a0" id="tgt291" class="tgtSentence">Set-AadrmTemplateProperty</caps:sentence>
                  </linkText>
                  <linkUri>https://msdn.microsoft.com/library/azure/dn727076.aspx</linkUri>
                </externalLink>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="0a4f90ce90fc062c4fc00532513d86da" id="tgt292" class="tgtSentence">Pasos siguientes</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="8e2fc0c78b4051162cb73c3ed3e2195c" id="tgt293" class="tgtSentence">Después de configurar plantillas personalizadas para Azure Rights Management, consulte <link xlink:href="086600c2-c5d8-47ec-a4c0-c782e1797486">Azure Rights Management Deployment Roadmap</link> para comprobar si hay otros pasos de configuración que puedan ser necesarios antes de implementar <token>aad_rightsmanagement_1</token> en usuarios y administradores.</caps:sentence>
            <caps:sentence sentenceid="30338b30b2128fd6754c3f1a4dcb0cad" id="tgt294" class="tgtSentence"> Si no es necesario ningún otro paso de configuración, consulte <link xlink:href="18564e4a-9364-4ed2-8f17-89d24fc0d878">Using Azure Rights Management</link> para obtener instrucciones operativas para apoyar una implementación correcta en su organización.</caps:sentence>
          </para>
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
          <caps:sentence id="src1" class="srcSentence">After you have activated Azure Rights Management (Azure RMS), users are automatically able to use two default templates that make it easy for them to apply policies to sensitive files that restrict access to authorized users in your organization.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> These two templates have the following rights policy restrictions:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src3" class="srcSentence">Read-only viewing for the protected content</caps:sentence>
            </para>
            <list class="bullet">
              <listItem>
                <para>
                  <caps:sentence id="src4" class="srcSentence">Display name: <ui>&lt;organization name&gt; - Confidential View Only</ui></caps:sentence>
                </para>
              </listItem>
              <listItem>
                <para>
                  <caps:sentence id="src5" class="srcSentence">Specific permission: View Content</caps:sentence>
                </para>
              </listItem>
            </list>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src6" class="srcSentence">Read or Modify permissions for the protected content</caps:sentence>
            </para>
            <list class="bullet">
              <listItem>
                <para>
                  <caps:sentence id="src7" class="srcSentence">Display name: <ui>&lt;organization name&gt; - Confidential</ui></caps:sentence>
                </para>
              </listItem>
              <listItem>
                <para>
                  <caps:sentence id="src8" class="srcSentence">Specific permissions: View Content, Save File, Edit Content, View Assigned Rights, Allow Macros, Forward, Reply, Reply All</caps:sentence>
                </para>
              </listItem>
            </list>
          </listItem>
        </list>
        <para>
          <caps:sentence id="src9" class="srcSentence">In addition, the <externalLink><linkText>RMS sharing application</linkText><linkUri>http://technet.microsoft.com/library/dn339006.aspx</linkUri></externalLink> lets users define their own set of permissions.</caps:sentence>
          <caps:sentence id="src10" class="srcSentence"> And, for the Outlook client and Outlook Web Access, users can select the <ui>Do Not Forward</ui> option for email messages.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src11" class="srcSentence">For many organizations, the default templates might be sufficient.</caps:sentence>
          <caps:sentence id="src12" class="srcSentence"> But if you want to create your own custom rights policy templates, you can do so.</caps:sentence>
          <caps:sentence id="src13" class="srcSentence"> Reasons for creating a custom template include the following:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src14" class="srcSentence">You want a template to grant rights to a subset of users in the organization rather than all users.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src15" class="srcSentence">You want only a subset of users to be able to see and select a template (departmental template) from applications, rather than all users in the organization see and can select the template.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src16" class="srcSentence">You want to define a custom right for a template, such as View and Edit, but not Copy and Print.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src17" class="srcSentence">You want to configure additional options in a template that include an expiration date and whether the content can be accessed without an Internet connection.</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence id="src18" class="srcSentence">For users to be able to select a custom template that contains settings such as these, you must first create a custom template, configure it, and then publish it.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src19" class="srcSentence">Use the following sections to help you configure and use custom templates:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <link xlink:href="1775d8d0-9a59-42c8-914f-ce285b71ac1c#BKMK_HowToConfigureCustomTemplates">How to create, configure, and publish a custom template</link>
            </para>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="1775d8d0-9a59-42c8-914f-ce285b71ac1c#BKMK_HowToCopyTemplates">How to copy a template</link>
            </para>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="1775d8d0-9a59-42c8-914f-ce285b71ac1c#BKMK_HowToArchiveTemplates">How to remove (archive) templates</link>
            </para>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="1775d8d0-9a59-42c8-914f-ce285b71ac1c#BKMK_RefreshingTemplates">Refreshing templates for users</link>
            </para>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="1775d8d0-9a59-42c8-914f-ce285b71ac1c#BKMK_PowerShellTemplates">Windows PowerShell reference</link>
            </para>
          </listItem>
        </list>
      </introduction>
      <section address="BKMK_HowToConfigureCustomTemplates">
        <title>
          <caps:sentence id="src20" class="srcSentence">How to create, configure, and publish a custom template</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src21" class="srcSentence">You create and manage custom templates in the Azure classic portal.</caps:sentence>
            <caps:sentence id="src22" class="srcSentence"> You can do this directly from the Azure classic portal, or you can sign in to the Office 365 admin center, and choose the <ui>advanced features</ui> for Rights Management, which then redirects you to the Azure classic portal.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src23" class="srcSentence">Use the following procedures to create, configure, and publish custom templates for Rights Management.</caps:sentence>
          </para>
          <procedure>
            <title>
              <caps:sentence id="src24" class="srcSentence">To create a custom template</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src25" class="srcSentence">Depending on whether you sign in to the Office 365 admin center, or the Azure classic portal, do one of the following:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src26" class="srcSentence">From the <externalLink><linkText>Office 365 admin center</linkText><linkUri>https://portal.office.com/</linkUri></externalLink>:</caps:sentence>
                      </para>
                      <list class="ordered">
                        <listItem>
                          <para>
                            <caps:sentence id="src27" class="srcSentence">In the left pane, click <ui>service settings</ui>.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src28" class="srcSentence">From the <ui>service settings</ui> page, click <ui>rights management</ui>.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src29" class="srcSentence">In the <ui>Protect your information</ui> section, click <ui>Manage</ui>.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src30" class="srcSentence">In the <ui>rights management</ui> section, click <ui>advanced features</ui>.</caps:sentence>
                          </para>
                          <alert class="note">
                            <para>
                              <caps:sentence id="src31" class="srcSentence">If you haven’t activated Rights Management, first click <ui>activate</ui> and confirm your action.</caps:sentence>
                              <caps:sentence id="src32" class="srcSentence"> For more information, see <link xlink:href="f8707e01-b239-4d1a-a1ea-0d1cf9a8d214">Activating Azure Rights Management</link>.</caps:sentence>
                            </para>
                            <para>
                              <caps:sentence id="src33" class="srcSentence">If you haven’t clicked <ui>advanced features</ui> before, after Rights Management is activated, follow the on-screen instructions to get a free Azure subscription that’s required to access the Azure classic portal.</caps:sentence>
                            </para>
                          </alert>
                          <para>
                            <caps:sentence id="src34" class="srcSentence">Clicking <ui>advanced features</ui> loads the Azure classic portal, where you can manage <ui>RIGHTS MANAGEMENT</ui> for your organization's Azure Active Directory.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src35" class="srcSentence">From the <externalLink><linkText>Azure classic portal</linkText><linkUri>http://go.microsoft.com/fwlink/p/?LinkID=275081</linkUri></externalLink>:</caps:sentence>
                      </para>
                      <list class="ordered">
                        <listItem>
                          <para>
                            <caps:sentence id="src36" class="srcSentence">In the left pane, click <ui>ACTIVE DIRECTORY</ui>.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src37" class="srcSentence">From the <ui>active directory</ui> page, click <ui>RIGHTS MANAGEMENT</ui>.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src38" class="srcSentence">Select the directory to manage for Rights Management.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src39" class="srcSentence">If you have not already activated Rights Management, click <ui>ACTIVATE</ui> and confirm your action.</caps:sentence>
                          </para>
                          <alert class="note">
                            <para>
                              <caps:sentence id="src40" class="srcSentence">For more information, see <link xlink:href="f8707e01-b239-4d1a-a1ea-0d1cf9a8d214">Activating Azure Rights Management</link>.</caps:sentence>
                            </para>
                          </alert>
                        </listItem>
                      </list>
                    </listItem>
                  </list>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src41" class="srcSentence">Create a new template: </caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src42" class="srcSentence">In the Azure classic portal, from the <ui>Get started with Rights Management</ui> quick start page, click <ui>Create a new rights policy template</ui>.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src43" class="srcSentence">If you do not immediately see this page after following the instructions for Office 365, use the navigation instructions, above,  for the Azure classic portal.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src44" class="srcSentence">On the <ui>Add a new rights policy template</ui> page, choose a language in which you will type the template name and description that users will see (you can add more languages later).</caps:sentence>
                    <caps:sentence id="src45" class="srcSentence"> Then type a unique name and a description, and click the Complete button.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence id="src46" class="srcSentence">From the <ui>Get started with Rights Management</ui> quick start page, now click <ui>Manage your rights policy templates</ui>.</caps:sentence>
                  <caps:sentence id="src47" class="srcSentence"> You will see your newly created template added to the list of templates, with a status of <ui>Archived</ui>.</caps:sentence>
                  <caps:sentence id="src48" class="srcSentence"> At this stage, the template is created but not configured, and is not visible to users.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
          <procedure>
            <title>
              <caps:sentence id="src49" class="srcSentence">To configure and publish a custom template</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src50" class="srcSentence">Select your newly created template from the <ui>TEMPLATES</ui> page in the Azure classic portal.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src51" class="srcSentence">From the <ui>Your template has been added</ui> quick start page, click <ui>Get started</ui> from step 1, <ui>Configure rights for users and groups,</ui> then click <ui>GET STARTED NOW</ui> or <ui>ADD</ui>, and then select the users and groups who will have rights to use the content that is protected by the new template.</caps:sentence>
                  </para>
                  <alert class="note">
                    <para>
                      <caps:sentence id="src52" class="srcSentence">The users or groups that you select must have an email address.</caps:sentence>
                      <caps:sentence id="src53" class="srcSentence"> In a production environment, this will nearly always be the case but in a simple testing environment, you might need to add email addresses to user accounts or groups.</caps:sentence>
                    </para>
                  </alert>
                  <para>
                    <caps:sentence id="src54" class="srcSentence">As a best practice, use groups rather than users, which simplifies management of the templates.</caps:sentence>
                    <caps:sentence id="src55" class="srcSentence"> If you have Active Directory on-premises and are synchronizing to Azure AD, you can use mail-enabled groups that are either security groups or distribution groups.</caps:sentence>
                    <caps:sentence id="src56" class="srcSentence"> However, if you want to grant rights to all users in the organization, it will be more efficient to copy one of the default templates rather than specify multiple groups.</caps:sentence>
                    <caps:sentence id="src57" class="srcSentence"> For more information, see the <link xlink:href="1775d8d0-9a59-42c8-914f-ce285b71ac1c#BKMK_HowToCopyTemplates">How to copy a template</link> section in this topic.</caps:sentence>
                  </para>
                  <alert class="tip">
                    <para>
                      <caps:sentence id="src58" class="srcSentence">You can later add users from outside your organization to the template by using the <externalLink><linkText>Windows PowerShell module for Azure Rights Management</linkText><linkUri>https://technet.microsoft.com/library/jj585012.aspx</linkUri></externalLink> and using one of the following methods:</caps:sentence>
                    </para>
                    <list class="bullet">
                      <listItem>
                        <para>
                          <caps:sentence id="src59" class="srcSentence">
                            <embeddedLabel>Use a rights definition object to update a template</embeddedLabel>:    Specify the external email addresses and their rights in a rights definition object, which you then use to update your template.</caps:sentence>
                          <caps:sentence id="src60" class="srcSentence"> You specify the rights definition object by using the <externalLink><linkText>New-AadrmRightsDefinition</linkText><linkUri>https://msdn.microsoft.com/library/azure/dn727080.aspx</linkUri></externalLink> cmdlet to create a variable and then supply this variable to the  -RightsDefinition parameter with the <externalLink><linkText>Set-AadrmTemplateProperty</linkText><linkUri>https://msdn.microsoft.com/library/azure/dn727076.aspx</linkUri></externalLink> cmdlet to modify an existing template.</caps:sentence>
                          <caps:sentence id="src61" class="srcSentence"> However, if you're adding these users to an existing template, you will also need to define rights definition objects for the existing groups in the templates and not just the new, external users.</caps:sentence>
                        </para>
                      </listItem>
                      <listItem>
                        <para>
                          <caps:sentence id="src62" class="srcSentence">
                            <embeddedLabel>Export, edit, and import the updated template</embeddedLabel>:Use the <externalLink><linkText>Export-AadrmTemplate</linkText><linkUri>https://msdn.microsoft.com/library/azure/dn727078.aspx</linkUri></externalLink> cmdlet to export the template to a file that you can edit to add the external email addresses of these users and their rights to the existing groups and rights.</caps:sentence>
                          <caps:sentence id="src63" class="srcSentence"> Then use the <externalLink><linkText>Import-AadrmTemplate</linkText><linkUri>https://msdn.microsoft.com/library/azure/dn727077.aspx</linkUri></externalLink> cmdlet to import this change back into Azure RMS.</caps:sentence>
                        </para>
                      </listItem>
                    </list>
                  </alert>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src64" class="srcSentence">Click the Next button, and then assign one of the listed rights to your selected users and groups.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src65" class="srcSentence">Use the displayed description for more information about each right (and for custom rights).</caps:sentence>
                    <caps:sentence id="src66" class="srcSentence"> More detailed  information is also available in <link xlink:href="97ddde38-b91b-42a5-8eb4-3ce6ce15393d">Configuring Usage Rights for Azure Rights Management</link>.</caps:sentence>
                    <caps:sentence id="src67" class="srcSentence"> However, applications that support RMS might vary in how they implement these rights.</caps:sentence>
                    <caps:sentence id="src68" class="srcSentence"> Consult their documentation and do your own testing with the applications that users use to check the behavior before you deploy the template for users.</caps:sentence>
                    <caps:sentence id="src69" class="srcSentence"> To make this template visible to only administrators for this testing, make this template a departmental template (step 6).</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src70" class="srcSentence">If you selected <ui>Custom</ui>, click the Next button, and then select those custom rights.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src71" class="srcSentence">Although you can use any combination of the individual rights available, in some applications, some rights might have dependencies on other individual rights.</caps:sentence>
                    <caps:sentence id="src72" class="srcSentence"> When this is the case, the dependent rights are automatically selected for you.</caps:sentence>
                  </para>
                  <alert class="tip">
                    <para>
                      <caps:sentence id="src73" class="srcSentence">Consider adding the <ui>Copy and Extract Content</ui> right and grant this to selected administrators or personnel in other roles that have responsibilities for information recovery.</caps:sentence>
                      <caps:sentence id="src74" class="srcSentence"> Granting this right lets them remove protection if needed, from files and emails that will be protected by using this template.</caps:sentence>
                      <caps:sentence id="src75" class="srcSentence"> This ability to remove protection at the template level provides more fine-grained control than using the super user feature.</caps:sentence>
                    </para>
                  </alert>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src76" class="srcSentence">Click the Complete button.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src77" class="srcSentence">If you want the template to be visible to only a subset of users when they see a list of templates in applications: Click <ui>SCOPE</ui> to configure this as a departmental template, and click <ui>GET STARTED NOW</ui>.</caps:sentence>
                    <caps:sentence id="src78" class="srcSentence"> Otherwise, go to step 9.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src79" class="srcSentence">More information about departmental templates: By default, all users in your Azure directory see all the published templates and they can then select them from applications when they want to protect content.</caps:sentence>
                    <caps:sentence id="src80" class="srcSentence"> If you want specific users only to see some of the published templates, you must scope the templates to these users.</caps:sentence>
                    <caps:sentence id="src81" class="srcSentence"> Then, only these users will be able to select these templates.</caps:sentence>
                    <caps:sentence id="src82" class="srcSentence"> Other users that you do not specify will not see the templates and therefore, cannot select them.</caps:sentence>
                    <caps:sentence id="src83" class="srcSentence"> This technique can make choosing the correct template easier for users, especially when you create templates that are designed to be used by specific groups or departments.</caps:sentence>
                    <caps:sentence id="src84" class="srcSentence"> Users then see only the templates that are designed for them.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src85" class="srcSentence">For example, you’ve created a template for the Human Resources department that applies the Read-only permission to members of the Finance department.</caps:sentence>
                    <caps:sentence id="src86" class="srcSentence"> So that only members of the Human Resources department can apply this template when they use the Rights Management sharing application, you scope the template to the email-enabled group named HumanResources.</caps:sentence>
                    <caps:sentence id="src87" class="srcSentence"> Then, only members of this group see and can apply this template.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src88" class="srcSentence">On the <ui>TEMPLATE VISIBILITY</ui> page, select the users and groups who will be able to see and select the template from the RMS-enlightened applications.</caps:sentence>
                    <caps:sentence id="src89" class="srcSentence"> As before, as a best practice, use groups rather than users, and the groups or users you select must have an email address.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src90" class="srcSentence">Click the Next button, and decide whether you need to configure application compatibility for your departmental template.</caps:sentence>
                    <caps:sentence id="src91" class="srcSentence"> If you do, click <ui>APPLICATION COMPATIBILITY</ui>, select the check box, and click <ui>Complete</ui>.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src92" class="srcSentence">Why might you need to configure application compatibility?</caps:sentence>
                    <caps:sentence id="src93" class="srcSentence"> Not all applications can support departmental templates.</caps:sentence>
                    <caps:sentence id="src94" class="srcSentence"> To do so, the application must first authenticate with the RMS service before downloading the templates.</caps:sentence>
                    <caps:sentence id="src95" class="srcSentence"> If the authentication process does not occur, by default, none of the departmental templates are downloaded.</caps:sentence>
                    <caps:sentence id="src96" class="srcSentence"> You can override this behavior by specifying that all the departmental templates should download, by configuring application compatibility and selecting the <ui>Show this template to all users when the applications do not support user identity</ui> check box.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src97" class="srcSentence">For example, if you do not configure application compatibility for the departmental template in our Human Resources example, only users in the Human Resources department see the departmental template when they use the RMS sharing application, but no users see the departmental template when they use Outlook Web Access (OWA) from Exchange Server 2013 because Exchange OWA and Exchange ActiveSync do not currently support departmental templates.</caps:sentence>
                    <caps:sentence id="src98" class="srcSentence"> If you override this default behavior by configuring application compatibility, only users in the Human Resources department see the departmental template when they use the RMS sharing application, but all users see the departmental template when they use Outlook Web Access (OWA).</caps:sentence>
                    <caps:sentence id="src99" class="srcSentence"> If users use OWA or Exchange ActiveSync from Exchange Online, either all users will see the departmental templates or no users will see the department templates, based on the template status (archival or published) in Exchange Online.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src100" class="srcSentence">Office 2016 natively supports departmental templates, and so does Office 2013 with the latest  Office updates (<externalLink><linkText>KB 3054853</linkText><linkUri>https://support.microsoft.com/kb/3054853</linkUri></externalLink>).</caps:sentence>
                  </para>
                  <alert class="note">
                    <para>
                      <caps:sentence id="src101" class="srcSentence"> If you have applications that don’t yet natively support departmental templates, you can use a custom RMS template download script or other tools to deploy these templates to the local RMS client folder.</caps:sentence>
                      <caps:sentence id="src102" class="srcSentence"> Then, these applications will correctly display the departmental templates to only the users and groups that you selected for the template scope:</caps:sentence>
                    </para>
                    <list class="bullet">
                      <listItem>
                        <para>
                          <caps:sentence id="src103" class="srcSentence">For Office 2010, the client folder is <system>%localappdata%\Microsoft\DRM\Templates</system>.</caps:sentence>
                        </para>
                      </listItem>
                      <listItem>
                        <para>
                          <caps:sentence id="src104" class="srcSentence">From a client computer that has downloaded all the templates, you can copy and then paste the template files to other computers.</caps:sentence>
                        </para>
                      </listItem>
                    </list>
                    <para> </para>
                    <para>
                      <caps:sentence id="src105" class="srcSentence">You can <externalLink><linkText>download the custom RMS template script from the Microsoft Connect site</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=524506</linkUri></externalLink>.</caps:sentence>
                      <caps:sentence id="src106" class="srcSentence"> If you see an error when you click this link, you probably haven't registered on Microsoft Connect.</caps:sentence>
                      <caps:sentence id="src107" class="srcSentence">   To register:</caps:sentence>
                    </para>
                    <list class="ordered">
                      <listItem>
                        <para>
                          <caps:sentence id="src108" class="srcSentence">Go to the <externalLink><linkText>Microsoft Connect site</linkText><linkUri>http://www.connect.microsoft.com</linkUri></externalLink> and sign in with your Microsoft Account.</caps:sentence>
                        </para>
                      </listItem>
                      <listItem>
                        <para>
                          <caps:sentence id="src109" class="srcSentence">Click <ui>Directory</ui>, and select the <ui>View Connect products currently not accepting feedback</ui> category.</caps:sentence>
                        </para>
                      </listItem>
                      <listItem>
                        <para>
                          <caps:sentence id="src110" class="srcSentence">Search for <userInput>Rights Management Services</userInput>, and for the <ui>Microsoft RMS Enterprise Features</ui> program, click <ui>Join</ui>.</caps:sentence>
                        </para>
                      </listItem>
                    </list>
                  </alert>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src111" class="srcSentence">Click <ui>CONFIGURE</ui> and add additional languages that users use, together with the name and description of this template in that language.</caps:sentence>
                    <caps:sentence id="src112" class="srcSentence"> When you have multi-language users, it’s important to add each language that they use, and supply a name and description in that language.</caps:sentence>
                    <caps:sentence id="src113" class="srcSentence"> Users will then see the name and description of the template in the same language as their client operating system, which ensures they understand the policy applied to a document or email message.</caps:sentence>
                    <caps:sentence id="src114" class="srcSentence"> If there is no match with their client operating system, the name and description that they see falls back to the language and description that you defined when you first created the template.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src115" class="srcSentence">Then check whether you want to make any changes to the following settings:</caps:sentence>
                  </para>
                  <table>
                    <thead>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src116" class="srcSentence">Setting</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src117" class="srcSentence">More information</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </thead>
                    <tbody>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src118" class="srcSentence">content expiration</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src119" class="srcSentence">Define a date or number of days for this template when files that are protected by the template should not open.</caps:sentence>
                            <caps:sentence id="src120" class="srcSentence"> You can specify a date or specify a number of days starting from the time that the protection is applied to the file.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence id="src121" class="srcSentence">When you specify a date, it is effective midnight, in your current time zone.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src122" class="srcSentence">offline access</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src123" class="srcSentence">Use this setting to balance any security requirements that you have against the requirement that users must be able to open protected files when they don’t have an Internet connection.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence id="src124" class="srcSentence">If you specify that content is not available without an Internet connection or that content is only available for a specified number of days, when that threshold is reached, users must be re-authenticated and their access is logged.</caps:sentence>
                            <caps:sentence id="src125" class="srcSentence"> When this happens, if their credentials are not cached, users are prompted to sign in before they can open the file.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence id="src126" class="srcSentence">In addition to re-authentication, the policy and the user group membership is re-evaluated.</caps:sentence>
                            <caps:sentence id="src127" class="srcSentence"> This means that users could experience different access results for the same file if there are changes in the policy or group membership from when they last accessed the file.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </tbody>
                  </table>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src128" class="srcSentence">When you are confident that the template is configured appropriately for your users, click <ui>PUBLISH</ui> to make the template visible for users, and then click <ui>SAVE</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src129" class="srcSentence">Click the Back button in the classic portal to return to the <ui>TEMPLATES</ui> page, where your template now has an updated status of <ui>Published</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence id="src130" class="srcSentence">To make any changes to your template, select it, and then use the quick start steps again.</caps:sentence>
                  <caps:sentence id="src131" class="srcSentence"> Or, select one of the following options:</caps:sentence>
                </para>
                <list class="bullet">
                  <listItem>
                    <para>
                      <caps:sentence id="src132" class="srcSentence">To add more users and groups, and define the rights for those users and groups: Click <ui>RIGHTS</ui>, then click <ui>ADD</ui>.</caps:sentence>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <caps:sentence id="src133" class="srcSentence">To remove users or groups that you previously selected: Click <ui>RIGHTS</ui>, select the user or group from the list, and then click <ui>DELETE</ui>.</caps:sentence>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <caps:sentence id="src134" class="srcSentence">To change which users can see the templates to select them from applications: Click <ui>SCOPE</ui>, then click <ui>ADD</ui> or <ui>DELETE</ui>, or <ui>APPLICATION COMPATIBILITY</ui>.</caps:sentence>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <caps:sentence id="src135" class="srcSentence">To make the template no longer visible to all users: Click <ui>CONFIGURE</ui>, click <ui>ARCHIVE</ui>, and then click <ui>SAVE</ui>.</caps:sentence>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <caps:sentence id="src136" class="srcSentence">To make other configuration changes: Click <ui>CONFIGURE</ui>, make your changes, and then click <ui>SAVE</ui>.</caps:sentence>
                    </para>
                  </listItem>
                </list>
                <alert class="warning">
                  <para>
                    <caps:sentence id="src137" class="srcSentence">When you make changes to a template that was previously saved, clients will not see those changes to the template until templates are refreshed on their computers.</caps:sentence>
                    <caps:sentence id="src138" class="srcSentence"> For more information, see the <link xlink:href="1775d8d0-9a59-42c8-914f-ce285b71ac1c#BKMK_RefreshingTemplates">Refreshing templates for users</link> section in this topic.</caps:sentence>
                  </para>
                </alert>
              </content>
            </conclusion>
          </procedure>
        </content>
      </section>
      <section address="BKMK_HowToCopyTemplates">
        <title>
          <caps:sentence id="src139" class="srcSentence">How to copy a template</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src140" class="srcSentence">If you want to create a new template that has very similar settings to an existing template, select the original template on the <ui>TEMPLATES</ui> page, click <ui>COPY</ui>, specify a unique name, and make the changes that you need.</caps:sentence>
          </para>
          <alert class="important">
            <para>
              <caps:sentence id="src141" class="srcSentence">When you copy a template, the <ui>Published</ui> or <ui>Archived</ui> status is also copied.</caps:sentence>
              <caps:sentence id="src142" class="srcSentence"> So if you copy a published template, its immediate status will be published, unless you change it.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence id="src143" class="srcSentence">You can copy custom templates and the default templates.</caps:sentence>
            <caps:sentence id="src144" class="srcSentence"> As a best practice, copy one of the default templates instead of creating a new custom template if you want the template to grant rights to all users in your organization.</caps:sentence>
            <caps:sentence id="src145" class="srcSentence"> This method means that you don’t have to create or select multiple groups to specify all users.</caps:sentence>
            <caps:sentence id="src146" class="srcSentence"> In this scenario however, be sure to specify a new name and description for the copied template for additional languages.</caps:sentence>
          </para>
        </content>
      </section>
      <section address="BKMK_HowToArchiveTemplates">
        <title>
          <caps:sentence id="src147" class="srcSentence">How to remove (archive) templates</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src148" class="srcSentence">The default templates cannot be deleted, but they can be archived so that users do not see them.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src149" class="srcSentence">Similarly, if you have published a custom template and no longer want users to be able to see it, you can edit the template and choose <ui>ARCHIVE</ui> and <ui>SAVE</ui> from the <ui>CONFIGURE</ui> page.</caps:sentence>
            <caps:sentence id="src150" class="srcSentence"> Or, you can select it from the <ui>TEMPLATES</ui> page and select <ui>ARCHIVE</ui>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src151" class="srcSentence">Because you cannot edit the default templates, to archive these templates, you must use the <ui>ARCHIVE</ui> option from the <ui>TEMPLATES</ui> page.</caps:sentence>
            <caps:sentence id="src152" class="srcSentence"> You cannot archive the Outlook <ui>Do Not Forward</ui> option.</caps:sentence>
          </para>
          <procedure>
            <title>
              <caps:sentence id="src153" class="srcSentence">To remove a default template</caps:sentence>
            </title>
            <steps class="bullet">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src154" class="srcSentence">From the <ui>TEMPLATES</ui> page, select the default template, and click <ui>ARCHIVE</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence id="src155" class="srcSentence">The status changes from <ui>Published</ui> to <ui>Archived</ui>.</caps:sentence>
                  <caps:sentence id="src156" class="srcSentence"> If you change your mind, select the template and click <ui>PUBLISH</ui>.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
        </content>
      </section>
      <section address="BKMK_RefreshingTemplates">
        <title>
          <caps:sentence id="src157" class="srcSentence">Refreshing templates for users</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src158" class="srcSentence">When you use Azure RMS, templates are automatically downloaded to client computers so that users can select them from their applications.</caps:sentence>
            <caps:sentence id="src159" class="srcSentence"> However, you might need to take additional steps if you make changes to the templates:</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src160" class="srcSentence">Application or service</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src161" class="srcSentence">How templates are refreshed after changes</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src162" class="srcSentence">Exchange Online</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src163" class="srcSentence">Manual configuration required to refresh templates.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src164" class="srcSentence">For the configuration steps, expand the following section, <link xlink:href="1775d8d0-9a59-42c8-914f-ce285b71ac1c#BKMK_ExchangeOnlineTemplatesUpdate">Exchange Online only: How to configure Exchange to download changed custom templates</link>.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src165" class="srcSentence">Office 365</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src166" class="srcSentence">Automatically refreshed  – no additional steps required.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src167" class="srcSentence">Office 2016 and Office 2013</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src168" class="srcSentence">RMS sharing application for Windows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src169" class="srcSentence">Automatically refreshed – on a schedule: </caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src170" class="srcSentence">For these later versions of Office: The default refresh interval  is every 7 days.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src171" class="srcSentence">For the RMS sharing application for Windows: Starting with version 1.0.1784.0, the default refresh interval is every 1 day.</caps:sentence>
                        <caps:sentence id="src172" class="srcSentence"> Prior versions have a default refresh interval of every 7 days.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence id="src173" class="srcSentence">To force a refresh sooner than this schedule, expand the following section, <link xlink:href="#BKMK_Office2013ForceUpdate">Office 2016,  Office 2013, and RMS sharing application for Windows: How to force a refresh for a changed custom template</link>.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src174" class="srcSentence">Office 2010</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src175" class="srcSentence">Refreshed when users log on.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src176" class="srcSentence">To force a refresh, ask or force users to log off and log back on again.</caps:sentence>
                    <caps:sentence id="src177" class="srcSentence"> Or, see the following section, <link xlink:href="#BKMK_Office2010ForceUpdate">Office 2010 only: How to force a refresh for a changed custom template</link>.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <caps:sentence id="src178" class="srcSentence">For mobile devices that use the RMS sharing application, templates are automatically downloaded (and refreshed if necessary) without additional configuration required.</caps:sentence>
          </para>
        </content>
        <sections>
          <section address="BKMK_ExchangeOnlineTemplatesUpdate" expanded="false">
            <title>
              <caps:sentence id="src179" class="srcSentence">Exchange Online only: How to configure Exchange to download changed custom templates</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src180" class="srcSentence">If you have already configured Information Rights Management (IRM) for Exchange Online, custom templates will not download for users until you make the following changes by using Windows PowerShell in Exchange Online.</caps:sentence>
              </para>
              <alert class="note">
                <para>
                  <caps:sentence id="src181" class="srcSentence">For more information about how to use Windows PowerShell in Exchange Online, see <externalLink><linkText>Using PowerShell with Exchange Online</linkText><linkUri>https://technet.microsoft.com/library/jj200677(v=exchg.160).aspx</linkUri></externalLink>.</caps:sentence>
                </para>
              </alert>
              <para>
                <caps:sentence id="src182" class="srcSentence">You must do this procedure each time you change a template.</caps:sentence>
              </para>
              <procedure>
                <title>
                  <caps:sentence id="src183" class="srcSentence">To update templates for Exchange Online</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src184" class="srcSentence">Using Windows PowerShell in Exchange Online, connect to the service:</caps:sentence>
                      </para>
                      <list class="ordered">
                        <listItem>
                          <para>
                            <caps:sentence id="src185" class="srcSentence">Supply your Office 365 user name and password:</caps:sentence>
                          </para>
                          <code>$Cred = Get-Credential</code>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src186" class="srcSentence">Connect to the Exchange Online service by running the following two commands:</caps:sentence>
                          </para>
                          <code>$Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.outlook.com/powershell/ -Credential $Cred -Authentication Basic –AllowRedirection</code>
                          <code>Import-PSSession $Session</code>
                        </listItem>
                      </list>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src187" class="srcSentence">Use the <externalLink><linkText>Import-RMSTrustedPublishingDomain</linkText><linkUri>http://technet.microsoft.com/library/jj200724(v=exchg.160).aspx</linkUri></externalLink> cmdlet to re-import your trusted publishing domain (TPD) from Azure RMS:</caps:sentence>
                      </para>
                      <code>Import-RMSTrustedPublishingDomain -Name "&lt;TPD name&gt;" -RefreshTemplates -RMSOnline</code>
                      <para>
                        <caps:sentence id="src188" class="srcSentence">For example, if your TPD name is <ui>RMS Online - 1</ui> (a typical name for many organizations), enter: <userInput>Import-RMSTrustedPublishingDomain -Name "RMS Online - 1" -RefreshTemplates -RMSOnline</userInput></caps:sentence>
                      </para>
                      <alert class="note">
                        <para>
                          <caps:sentence id="src189" class="srcSentence">To verify your TPD name, you can use the <externalLink><linkText>Get-RMSTrustedPublishingDomain</linkText><linkUri>http://technet.microsoft.com/library/jj200707(v=exchg.160).aspx</linkUri></externalLink> cmdlet.</caps:sentence>
                        </para>
                      </alert>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src190" class="srcSentence">To confirm that the templates have imported successfully, wait a few minutes and then run the <externalLink><linkText>Get-RMSTemplate</linkText><linkUri>http://technet.microsoft.com/library/dd297960(v=exchg.160).aspx</linkUri></externalLink> cmdlet and set the Type to All.</caps:sentence>
                        <caps:sentence id="src191" class="srcSentence"> For example:</caps:sentence>
                      </para>
                      <code>Get-RMSTemplate -TrustedPublishingDomain "RMS Online - 1" -Type All
</code>
                      <alert class="tip">
                        <para>
                          <caps:sentence id="src192" class="srcSentence">It's useful to keep a copy of the output so that you can easily copy the template names or GUIDs if you later archive a template.</caps:sentence>
                        </para>
                      </alert>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src193" class="srcSentence">For each imported template that you want to be available in the Outlook Web App, you must use the <externalLink><linkText>Set-RMSTemplate</linkText><linkUri>http://technet.microsoft.com/library/hh529923(v=exchg.160).aspx</linkUri></externalLink> cmdlet and set the Type to Distributed:</caps:sentence>
                      </para>
                      <code>Set-RMSTemplate -Identity "&lt;name  or GUID of the template&gt;" -Type Distributed</code>
                      <para>
                        <caps:sentence id="src194" class="srcSentence">Because Outlook Web Access caches the UI for 24 hours, users might not see the new template for up to a day.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
              <para>
                <caps:sentence id="src195" class="srcSentence">In addition, if you archive a template (custom or default) and use Exchange Online with Office 365, users will continue to see the archived templates if they use the Outlook Web App or mobile devices that use the Exchange ActiveSync Protocol.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src196" class="srcSentence">So that users no longer see these templates, connect to the service by using Windows PowerShell in Exchange Online, and then use the <externalLink><linkText>Set-RMSTemplate</linkText><linkUri>http://technet.microsoft.com/library/hh529923(v=exchg.160).aspx</linkUri></externalLink> cmdlet by running the following command: </caps:sentence>
              </para>
              <code>Set-RMSTemplate -Identity "&lt;name or GUID of the template&gt;" -Type Archived</code>
            </content>
          </section>
          <section expanded="false" address="BKMK_Office2013ForceUpdate">
            <title>
              <caps:sentence id="src197" class="srcSentence">Office 2016,  Office 2013, and RMS sharing application for Windows: How to force a refresh for a changed custom template</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src198" class="srcSentence">By editing the registry on the computers running Office 2016, Office 2013, or the Rights Management (RMS) sharing application for Windows, you can change the automatic schedule so that changed templates are refreshed on computers more frequently than their default value.</caps:sentence>
                <caps:sentence id="src199" class="srcSentence"> You can also force an immediate refresh by deleting the existing data in a registry value.</caps:sentence>
              </para>
              <alert class="warning">
                <para>
                  <caps:sentence id="src200" class="srcSentence">If you use the Registry Editor incorrectly, you might cause serious problems that might require you to reinstall the operating system.</caps:sentence>
                  <caps:sentence id="src201" class="srcSentence"> Microsoft cannot guarantee that you can solve problems that result from using the Registry Editor incorrectly.</caps:sentence>
                  <caps:sentence id="src202" class="srcSentence"> Use the Registry Editor at your own risk.</caps:sentence>
                </para>
              </alert>
              <procedure>
                <title>
                  <caps:sentence id="src203" class="srcSentence">To change the automatic schedule</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src204" class="srcSentence">Using a registry editor, create and set one of the following registry values:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence id="src205" class="srcSentence">To set an update frequency in days (minimum of 1 day):  Create a new registry value named <ui>TemplateUpdateFrequency</ui> and define an integer value for the data, which specifies the frequency in days to download any changes to a downloaded template.</caps:sentence>
                            <caps:sentence id="src206" class="srcSentence"> Use the following table to locate the registry path to create this new registry value.</caps:sentence>
                          </para>
                          <table>
                            <thead>
                              <tr>
                                <TD>
                                  <para>
                                    <caps:sentence id="src207" class="srcSentence">Registry path</caps:sentence>
                                  </para>
                                </TD>
                                <TD>
                                  <para>
                                    <caps:sentence id="src208" class="srcSentence">Type</caps:sentence>
                                  </para>
                                </TD>
                                <TD>
                                  <para>
                                    <caps:sentence id="src209" class="srcSentence">Value</caps:sentence>
                                  </para>
                                </TD>
                              </tr>
                            </thead>
                            <tbody>
                              <tr>
                                <TD>
                                  <para>
                                    <caps:sentence id="src210" class="srcSentence">HKEY_CURRENT_USER\Software\Classes\Local Settings\Software\Microsoft\MSIPC</caps:sentence>
                                  </para>
                                </TD>
                                <TD>
                                  <para>
                                    <caps:sentence id="src211" class="srcSentence">REG_DWORD</caps:sentence>
                                  </para>
                                </TD>
                                <TD>
                                  <para>
                                    <caps:sentence id="src212" class="srcSentence">TemplateUpdateFrequency</caps:sentence>
                                  </para>
                                </TD>
                              </tr>
                            </tbody>
                          </table>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src213" class="srcSentence">To set an update frequency in seconds (minimum of 1 second):  Create a new registry value named <ui>TemplateUpdateFrequencyInSeconds</ui> and define an integer value for the data, which specifies the frequency in seconds to download any changes to a downloaded template.</caps:sentence>
                            <caps:sentence id="src214" class="srcSentence"> Use the following table to locate the registry path to create this new registry value.</caps:sentence>
                          </para>
                          <table>
                            <thead>
                              <tr>
                                <TD>
                                  <para>
                                    <caps:sentence id="src215" class="srcSentence">Registry path</caps:sentence>
                                  </para>
                                </TD>
                                <TD>
                                  <para>
                                    <caps:sentence id="src216" class="srcSentence">Type</caps:sentence>
                                  </para>
                                </TD>
                                <TD>
                                  <para>
                                    <caps:sentence id="src217" class="srcSentence">Value</caps:sentence>
                                  </para>
                                </TD>
                              </tr>
                            </thead>
                            <tbody>
                              <tr>
                                <TD>
                                  <para>
                                    <caps:sentence id="src218" class="srcSentence">HKEY_CURRENT_USER\Software\Classes\Local Settings\Software\Microsoft\MSIPC</caps:sentence>
                                  </para>
                                </TD>
                                <TD>
                                  <para>
                                    <caps:sentence id="src219" class="srcSentence">REG_DWORD</caps:sentence>
                                  </para>
                                </TD>
                                <TD>
                                  <para>
                                    <caps:sentence id="src220" class="srcSentence">TemplateUpdateFrequencyInSeconds</caps:sentence>
                                  </para>
                                </TD>
                              </tr>
                            </tbody>
                          </table>
                        </listItem>
                      </list>
                      <para>
                        <caps:sentence id="src221" class="srcSentence">Make sure that you create and set one of these registry values, not both.</caps:sentence>
                        <caps:sentence id="src222" class="srcSentence"> If both are present, <system>TemplateUpdateFrequency</system> is ignored.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src223" class="srcSentence">If you want to force an immediate refresh of the templates, go to the next procedure.</caps:sentence>
                        <caps:sentence id="src224" class="srcSentence"> Otherwise, restart your Office applications and instances of File Explorer now.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
              <procedure>
                <title>
                  <caps:sentence id="src225" class="srcSentence">To force an immediate refresh</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src226" class="srcSentence">Using a registry editor, delete the data for the <ui>LastUpdatedTime</ui> value.</caps:sentence>
                        <caps:sentence id="src227" class="srcSentence"> For example, the data might display <ui>2015-04-20T15:52</ui>; delete 2015-04-20T15:52 so that no data is displayed.</caps:sentence>
                        <caps:sentence id="src228" class="srcSentence"> Use the following table to locate the registry path to delete this registry value data.</caps:sentence>
                      </para>
                      <table>
                        <thead>
                          <tr>
                            <TD>
                              <para>
                                <caps:sentence id="src229" class="srcSentence">Registry path</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src230" class="srcSentence">Type</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src231" class="srcSentence">Value</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                        </thead>
                        <tbody>
                          <tr>
                            <TD>
                              <para>
                                <caps:sentence id="src232" class="srcSentence">HKEY_CURRENT_USER\Software\Classes\Local Settings\Software\Microsoft\MSIPC\&lt;MicrosoftRMS_FQDN&gt;\Template</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src233" class="srcSentence">REG_SZ</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src234" class="srcSentence">LastUpdatedTime</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                        </tbody>
                      </table>
                      <alert class="tip">
                        <para>
                          <caps:sentence id="src235" class="srcSentence">In the registry path, <placeholder>&lt;MicrosoftRMS_FQDN&gt;</placeholder> refers to your Microsoft RMS service FQDN.</caps:sentence>
                          <caps:sentence id="src236" class="srcSentence"> If you want to verify this value:</caps:sentence>
                        </para>
                        <list class="ordered">
                          <listItem>
                            <para>
                              <caps:sentence id="src237" class="srcSentence">Run the <externalLink><linkText>Get-AadrmConfiguration</linkText><linkUri>https://msdn.microsoft.com/library/windowsazure/dn629410.aspx</linkUri></externalLink> cmdlet for Azure RMS.</caps:sentence>
                              <caps:sentence id="src238" class="srcSentence"> If you haven’t already installed the Windows PowerShell module for Azure RMS, see <link xlink:href="0d665ed6-b1de-4d63-854a-bc57c1c49844">Installing Windows PowerShell for Azure Rights Management</link>.</caps:sentence>
                            </para>
                          </listItem>
                          <listItem>
                            <para>
                              <caps:sentence id="src239" class="srcSentence">From the output, identify the <ui>LicensingIntranetDistributionPointUrl</ui> value.</caps:sentence>
                            </para>
                            <para>
                              <caps:sentence id="src240" class="srcSentence">For example: <ui>LicensingIntranetDistributionPointUrl   : https://5c6bb73b-1038-4eec-863d-49bded473437.rms.na.aadrm.com/_wmcs/licensing</ui></caps:sentence>
                            </para>
                          </listItem>
                          <listItem>
                            <para>
                              <caps:sentence id="src241" class="srcSentence">From the value, remove <ui>https://</ui> and <ui>/_wmcs/licensing</ui> from this string.</caps:sentence>
                              <caps:sentence id="src242" class="srcSentence"> The remaining value is your Microsoft RMS service FQDN.</caps:sentence>
                              <caps:sentence id="src243" class="srcSentence"> In our example, the Microsoft RMS service FQDN would be the following value:</caps:sentence>
                            </para>
                            <para>
                              <ui>
                                <caps:sentence id="src244" class="srcSentence">5c6bb73b-1038-4eec-863d-49bded473437.rms.na.aadrm.com</caps:sentence>
                              </ui>
                            </para>
                          </listItem>
                        </list>
                      </alert>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src245" class="srcSentence">Delete the following folder and all files it contains: <system>%localappdata%\Microsoft\MSIPC\Templates</system></caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src246" class="srcSentence">Restart your Office applications and instances of File Explorer.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
            </content>
          </section>
          <section expanded="false" address="BKMK_Office2010ForceUpdate">
            <title>
              <caps:sentence id="src247" class="srcSentence">Office 2010 only: How to force a refresh for a changed custom template</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src248" class="srcSentence">By editing the registry on the computers running Office 2010, you can set a value so that changed templates are refreshed on computers without waiting for users to log off and back on.</caps:sentence>
                <caps:sentence id="src249" class="srcSentence"> You can also force an immediate refresh by deleting the existing data in a registry value.</caps:sentence>
              </para>
              <alert class="warning">
                <para>
                  <caps:sentence id="src250" class="srcSentence">If you use the Registry Editor incorrectly, you might cause serious problems that might require you to reinstall the operating system.</caps:sentence>
                  <caps:sentence id="src251" class="srcSentence"> Microsoft cannot guarantee that you can solve problems that result from using the Registry Editor incorrectly.</caps:sentence>
                  <caps:sentence id="src252" class="srcSentence"> Use the Registry Editor at your own risk.</caps:sentence>
                </para>
              </alert>
              <procedure>
                <title>
                  <caps:sentence id="src253" class="srcSentence">To change the update frequency</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src254" class="srcSentence">Using a registry editor, create a new registry value named <ui>UpdateFrequency</ui> and define an integer value for the data, which specifies the frequency in days to download any changes to a downloaded template.</caps:sentence>
                        <caps:sentence id="src255" class="srcSentence"> Use the following table to locate the registry path to create this new registry value.</caps:sentence>
                      </para>
                      <table>
                        <thead>
                          <tr>
                            <TD>
                              <para>
                                <caps:sentence id="src256" class="srcSentence">Registry path</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src257" class="srcSentence">Type</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src258" class="srcSentence">Value</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                        </thead>
                        <tbody>
                          <tr>
                            <TD>
                              <para>
                                <caps:sentence id="src259" class="srcSentence">HKEY_CURRENT_USER\Software\Microsoft\MSDRM\TemplateManagement</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src260" class="srcSentence">REG_DWORD</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src261" class="srcSentence">UpdateFrequency</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                        </tbody>
                      </table>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src262" class="srcSentence">If you want to force an immediate refresh of the templates, go to the next procedure.</caps:sentence>
                        <caps:sentence id="src263" class="srcSentence"> Otherwise, restart your Office applications now.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
              <procedure>
                <title>
                  <caps:sentence id="src264" class="srcSentence">To force an immediate refresh</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src265" class="srcSentence">Using a registry editor, delete the data for the <ui>LastUpdatedTime</ui> value.</caps:sentence>
                        <caps:sentence id="src266" class="srcSentence"> For example, the data might display <ui>2015-04-20T15:52</ui>; delete 2015-04-20T15:52 so that no data is displayed.</caps:sentence>
                        <caps:sentence id="src267" class="srcSentence"> Use the following table to locate the registry path to delete this registry value data.</caps:sentence>
                      </para>
                      <table>
                        <thead>
                          <tr>
                            <TD>
                              <para>
                                <caps:sentence id="src268" class="srcSentence">Registry path</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src269" class="srcSentence">Type</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src270" class="srcSentence">Value</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                        </thead>
                        <tbody>
                          <tr>
                            <TD>
                              <para>
                                <caps:sentence id="src271" class="srcSentence">HKEY_CURRENT_USER\Software\Microsoft\MSDRM\TemplateManagement</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src272" class="srcSentence">REG_SZ</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src273" class="srcSentence">lastUpdatedTime</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                        </tbody>
                      </table>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src274" class="srcSentence">Delete the following folder and all files it contains: <system>%localappdata%\Microsoft\MSIPC\Templates</system></caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src275" class="srcSentence">Restart your Office applications.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
            </content>
          </section>
        </sections>
      </section>
      <section address="BKMK_PowerShellTemplates">
        <title>
          <caps:sentence id="src276" class="srcSentence">Windows PowerShell reference</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src277" class="srcSentence">Everything that you can do in the Azure classic portal to create and manage templates, you can do from the command line, by using Windows PowerShell.</caps:sentence>
            <caps:sentence id="src278" class="srcSentence"> In addition, you can export and import templates, so that you can copy templates between tenants or perform bulk edits of complex properties in templates, such as multilingual names and descriptions.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src279" class="srcSentence">You can also use export and import to back up and restore your custom templates, As a best practice, regularly back up your custom templates, so that if you make a change that was not intended, you can easily revert to a previous version.</caps:sentence>
          </para>
          <alert class="important">
            <para>
              <caps:sentence id="src280" class="srcSentence">To use Windows PowerShell to create and manage Azure RMS rights policy templates, you must have at least version 2.0.0.0 of the <externalLink><linkText>Windows PowerShell module for Azure RMS</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=257721</linkUri></externalLink>.</caps:sentence>
            </para>
            <para>
              <caps:sentence id="src281" class="srcSentence">If you have previously installed this Windows PowerShell module, run the following command in a PowerShell window to check the version number: <codeInline>(Get-Module aadrm -ListAvailable).Version</codeInline></caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence id="src282" class="srcSentence">For installation instructions, see <link xlink:href="0d665ed6-b1de-4d63-854a-bc57c1c49844">Installing Windows PowerShell for Azure Rights Management</link>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src283" class="srcSentence">The cmdlets that support creating and managing templates:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <externalLink>
                  <linkText>
                    <caps:sentence id="src284" class="srcSentence">Add-AadrmTemplate</caps:sentence>
                  </linkText>
                  <linkUri>https://msdn.microsoft.com/library/azure/dn727075.aspx</linkUri>
                </externalLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <externalLink>
                  <linkText>
                    <caps:sentence id="src285" class="srcSentence">Export-AadrmTemplate</caps:sentence>
                  </linkText>
                  <linkUri>https://msdn.microsoft.com/library/azure/dn727078.aspx</linkUri>
                </externalLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <externalLink>
                  <linkText>
                    <caps:sentence id="src286" class="srcSentence">Get-AadrmTemplate</caps:sentence>
                  </linkText>
                  <linkUri>https://msdn.microsoft.com/library/azure/dn727079.aspx</linkUri>
                </externalLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <externalLink>
                  <linkText>
                    <caps:sentence id="src287" class="srcSentence">Get-AadrmTemplateProperty</caps:sentence>
                  </linkText>
                  <linkUri>https://msdn.microsoft.com/library/azure/dn727081.aspx</linkUri>
                </externalLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <externalLink>
                  <linkText>
                    <caps:sentence id="src288" class="srcSentence">Import-AadrmTemplate</caps:sentence>
                  </linkText>
                  <linkUri>https://msdn.microsoft.com/library/azure/dn727077.aspx</linkUri>
                </externalLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <externalLink>
                  <linkText>
                    <caps:sentence id="src289" class="srcSentence">New-AadrmRightsDefinition</caps:sentence>
                  </linkText>
                  <linkUri>https://msdn.microsoft.com/library/azure/dn727080.aspx</linkUri>
                </externalLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <externalLink>
                  <linkText>
                    <caps:sentence id="src290" class="srcSentence">Remove-AadrmTemplate</caps:sentence>
                  </linkText>
                  <linkUri>https://msdn.microsoft.com/library/azure/dn727082.aspx</linkUri>
                </externalLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <externalLink>
                  <linkText>
                    <caps:sentence id="src291" class="srcSentence">Set-AadrmTemplateProperty</caps:sentence>
                  </linkText>
                  <linkUri>https://msdn.microsoft.com/library/azure/dn727076.aspx</linkUri>
                </externalLink>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src292" class="srcSentence">Next steps</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src293" class="srcSentence">After you’ve configured custom templates for Azure Rights Management, use the <link xlink:href="086600c2-c5d8-47ec-a4c0-c782e1797486">Azure Rights Management Deployment Roadmap</link> to check whether there are other configuration steps that you might want to do before you roll out <token>aad_rightsmanagement_1</token> to users and administrators.</caps:sentence>
            <caps:sentence id="src294" class="srcSentence"> If there are no other configuration steps that you need to do, see <link xlink:href="18564e4a-9364-4ed2-8f17-89d24fc0d878">Using Azure Rights Management</link> for operational guidance to support a successful deployment for your organization.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="206a0bfe-0912-4e0e-aa15-484b000b264c">Configuring Azure Rights Management</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>