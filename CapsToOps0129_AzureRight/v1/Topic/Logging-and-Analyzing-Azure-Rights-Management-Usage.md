---
title: Registro y an&#225;lisis del uso de Azure Rights Management
ms.custom: na
ms.reviewer: na
ms.service: rights-management
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a735f3f7-6eb2-4901-9084-8c3cd3a9087e
---
# Registro y an&#225;lisis del uso de Azure Rights Management
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="es-ES">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="22662a662dc8c6b7711e70d049524d3b" id="tgt1" class="tgtSentence">Use la información de este tema para comprender cómo puede usar el registro de uso con Azure Rights Management (Azure RMS).</caps:sentence>
          <caps:sentence sentenceid="7175e4cf114ae559272e83d5d77279ae" id="tgt2" class="tgtSentence"> El servicio Azure Rights Management permite registrar todas las solicitudes que realice para su organización, lo que incluye solicitudes de usuarios, acciones llevadas a cabo por administradores de Rights Management en su organización y acciones llevadas a cabo por operadores de Microsoft para admitir su implementación de Azure Rights Management.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="6e891353c2cf296b4e662ec87649e382" id="tgt3" class="tgtSentence">A continuación, puede usar estos registros de Azure Rights Management para admitir los siguientes escenarios empresariales:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="553ff180172154e8028ed6ff2d9351e3" id="tgt4" class="tgtSentence">Analizar enfoques empresariales.</caps:sentence>
            </para>
            <para>
              <caps:sentence sentenceid="5874d2c3cd1ecbbc4b200cbd0e8f4043" id="tgt5" class="tgtSentence">Azure Rights Management escribe los registros con el formato de registro extendido W3C en una cuenta de almacenamiento de Azure proporcionada por el usuario.</caps:sentence>
              <caps:sentence sentenceid="1ae65b531af18298f681545662cf3b6b" id="tgt6" class="tgtSentence"> Entonces puede dirigir estos registros al repositorio que elija (como una base de datos, un sistema de procesamiento analítico en línea (OLAP) o un sistema de asignar-reducir) para analizar la información y producir informes.</caps:sentence>
              <caps:sentence sentenceid="909a1e3fea32c0a37f22bfe00127820e" id="tgt7" class="tgtSentence"> Por ejemplo, podría notificar quién está accediendo a sus datos protegidos con RMS.</caps:sentence>
              <caps:sentence sentenceid="929430c45dc7213f067c3b017e1cdc68" id="tgt8" class="tgtSentence"> Puede determinar a qué datos protegidos con RMS está accediendo la gente y desde dónde y desde qué dispositivos.</caps:sentence>
              <caps:sentence sentenceid="e9b2481e2c3847564129dfa641ad70f0" id="tgt9" class="tgtSentence"> Puede averiguar si estas personas logran leer contenido protegido.</caps:sentence>
              <caps:sentence sentenceid="e2a448d437879096f82118ad9344911d" id="tgt10" class="tgtSentence"> También puede identificar qué personas han leído un documento importante que estaba protegido.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="9fd86164ea8ed3ef7fbef244c49b3381" id="tgt11" class="tgtSentence">Supervisar para controlar el abuso.</caps:sentence>
            </para>
            <para>
              <caps:sentence sentenceid="f19fdcf86275351596c6e312e0a9c1ff" id="tgt12" class="tgtSentence">La información del registro de Azure Rights Management está a su disposición casi en tiempo real, de manera que puede supervisar de manera continua el uso que se haga en su empresa de Azure Rights Management.</caps:sentence>
              <caps:sentence sentenceid="2ee220a94a479244df88f2e5f4ba5c74" id="tgt13" class="tgtSentence"> El 99,9% de los registros están disponibles en un plazo de 15 minutos de una acción iniciada por RMS.</caps:sentence>
            </para>
            <para>
              <caps:sentence sentenceid="9a5f200f4798df9885deb4eee9d0f982" id="tgt14" class="tgtSentence">Por ejemplo, puede que desee que se le alerte de si surge un aumento repentino de las personas que leen datos protegidos por RMS fuera de las hora laborales estándar, lo que podrían indica que un usuario malintencionado está recopilando información para venderla a competidores.</caps:sentence>
              <caps:sentence sentenceid="dd6dff482e6f2eb49b2ca9b46083cb1b" id="tgt15" class="tgtSentence"> O bien, si el mismo usuario aparentemente accede a los datos desde dos direcciones IP diferentes dentro de un breve intervalo de tiempo, lo que podría indicar que se ha puesto en peligro una cuenta de usuario.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="5592ef914ac95bf57f7c7ef51176a529" id="tgt16" class="tgtSentence">Realice un análisis forense.</caps:sentence>
            </para>
            <para>
              <caps:sentence sentenceid="ff0a5cf3b5e54c1a1e76257b6184a839" id="tgt17" class="tgtSentence">Si tiene una pérdida de información, es probable que se le pregunte quién accedió recientemente a documentos específicos y a qué información accedió la persona sospechosa.</caps:sentence>
              <caps:sentence sentenceid="331ee877d663f01887452f4ab492ab29" id="tgt18" class="tgtSentence"> Puede responder a este tipo de preguntas con Azure Rights Management y los registros, porque las personas que usan el contenido protegido siempre deben obtener una licencia de Azure Rights Management para abrir documentos e imágenes que estén protegidos con Azure Rights Management, incluso en el caso de que dichos archivos se muevan por correo electrónico o se copien en unidades USB u otras unidades de almacenamiento.</caps:sentence>
              <caps:sentence sentenceid="e3e1e90d1af46457c638e0f590981760" id="tgt19" class="tgtSentence"> Esto significa que puede usar los registros de Azure Rights Management como el origen fundamental de la información para realizar el análisis forense cuando protege sus datos con Azure Rights Management.</caps:sentence>
            </para>
          </listItem>
        </list>
        <alert class="note">
          <para>
            <caps:sentence sentenceid="3b779b1b840561a7ae3aec5a067825fb" id="tgt20" class="tgtSentence">Si solo está interesado en el registro de las tareas administrativas para Azure Rights Management y no desea realizar un seguimiento del modo en que los usuarios usan Rights Management, puede usar el cmdlet <externalLink><linkText>Get-AadrmAdminLog</linkText><linkUri>https://msdn.microsoft.com/library/azure/dn629430.aspx</linkUri></externalLink> de Windows PowerShell de Azure Rights Management.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="e61536dfc3e96c69b1a79f6db165135e" id="tgt21" class="tgtSentence">También puede usar el Portal de Azure clásico para ver informes de uso de alto nivel que incluyen <ui>Uso de RMS</ui>, <ui>Usuarios de RMS más activos</ui>, <ui>Uso de dispositivos RMS</ui> y <ui>Uso de aplicaciones con RMS habilitado</ui>.</caps:sentence>
            <caps:sentence sentenceid="348f2fd0dad974bab0e42292684ef73f" id="tgt22" class="tgtSentence"> Para poder acceder a estos informes desde el Portal de Azure clásico, haga clic en <ui>Active Directory</ui>, seleccione un directorio y ábralo y, luego, haga clic en <ui>INFORMES</ui>.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence sentenceid="e4c1bc6683cfc7bf9d0c4dea8adcef06" id="tgt23" class="tgtSentence">Use las secciones siguientes para obtener más información sobre el registro de uso de Azure Rights Management.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <link xlink:href="a735f3f7-6eb2-4901-9084-8c3cd3a9087e#BKMK_EnableRMSLogging">How to enable RMS logging</link>
            </para>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="a735f3f7-6eb2-4901-9084-8c3cd3a9087e#BKMK_AccesAndUseLogs">How to access and use your RMS logs</link>
            </para>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="a735f3f7-6eb2-4901-9084-8c3cd3a9087e#BKMK_ManageStorage">How to manage your RMS log storage</link>
            </para>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="a735f3f7-6eb2-4901-9084-8c3cd3a9087e#BKMK_Delegate">How to delegate access to your RMS logs</link>
            </para>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="a735f3f7-6eb2-4901-9084-8c3cd3a9087e#BKMK_Interpret">How to interpret your RMS logs</link>
            </para>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="a735f3f7-6eb2-4901-9084-8c3cd3a9087e#BKMK_PowerShell">Windows PowerShell reference</link>
            </para>
          </listItem>
        </list>
      </introduction>
      <section address="BKMK_EnableRMSLogging">
        <title>
          <caps:sentence sentenceid="1f3600c9cd6273f4cb0a7953a78b0671" id="tgt24" class="tgtSentence">Cómo habilitar el registro de uso de Azure Rights Management</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="540481a4317e26b1547221c197352dcb" id="tgt25" class="tgtSentence">El registro de uso de Azure Rights Management es opcional, por lo que, si desea usarlo, debe llevar a cabo pasos específicos.</caps:sentence>
            <caps:sentence sentenceid="d000f626454a3ae54c070e4cb78c28ca" id="tgt26" class="tgtSentence"> El uso del registro de uso de Azure Rights Management no implica ningún cambio en la manera en que Rights Management funciona. Además, el propio proceso es gratuito.</caps:sentence>
            <caps:sentence sentenceid="ba96e39b229c65dc703da109c8c8f53c" id="tgt27" class="tgtSentence"> Sin embargo, debe proporcionar una cuenta de almacenamiento de Azure para los registros y se le cobrará por este almacenamiento.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="98c944119b6bd280056311418ed87f7c" id="tgt28" class="tgtSentence">Antes de comenzar, asegúrese de que cumpla los siguientes requisitos previos para usar el registro de uso de Azure Rights Management:</caps:sentence>
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
                    <caps:sentence sentenceid="f0c8e0d48a5bfe3d60b027575599e81f" id="tgt31" class="tgtSentence">Una suscripción administrada por TI que incluye Azure Rights Management</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="dc69ef9a97237bcc33481df8946cd734" id="tgt32" class="tgtSentence">Debe tener una suscripción a Microsoft Azure Rights Management administrada por su organización.</caps:sentence>
                    <caps:sentence sentenceid="e1201fdcffa570cca1f19bfb89e25942" id="tgt33" class="tgtSentence"> Las organizaciones que usen RMS para usuarios individuales no pueden usar el registro de uso de Azure Rights Management.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="dd6acd3cb9b0e989bf09dc37a989ab01" id="tgt34" class="tgtSentence">Si su organización tiene usuarios que emplean RMS para usuarios, el registro de uso de Azure Rights Management ofrece una razón empresarial muy atractiva para convertir RMS para usuarios en una suscripción a Microsoft Azure Rights Management.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="7e241d2ca7e0d29557c5d3d02e7b2bd2" id="tgt35" class="tgtSentence">Para obtener más información sobre las suscripciones que incluyen Azure RMS, vea la sección <link xlink:href="dc78321d-d759-4653-8818-80da74b6cdeb#BKMK_SupportedSubscriptions">Cloud subscriptions that support Azure RMS</link> del tema <link xlink:href="dc78321d-d759-4653-8818-80da74b6cdeb">Requirements for Azure Rights Management</link>.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="d6313f0fbf5ca1ad5723ea38f88fa536" id="tgt36" class="tgtSentence">Para obtener más información sobre RMS para usuarios, consulte <link xlink:href="2efcb440-fefd-45e9-872b-f471573aadf2">RMS for Individuals and Azure Rights Management</link></caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e9a958e3a95884bc2b6a17370d017e53" id="tgt37" class="tgtSentence">la suscripción a Azure</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e9fab77a2f7f2ea27562640de4c54a0f" id="tgt38" class="tgtSentence">Debe tener una suscripción a Azure y almacenamiento suficiente en Azure para sus registros de Azure Rights Management.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="71bc936b1746b15dadaec1b9dfd40f54" id="tgt39" class="tgtSentence">Windows PowerShell para Azure Rights Management</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="98902f3607b0de9e10a56b5a34aeacc7" id="tgt40" class="tgtSentence">Si no lo ha hecho ya, descargue e instale el módulo de Windows PowerShell para Azure Rights Management.</caps:sentence>
                    <caps:sentence sentenceid="2eec5c1b5506ed7c67273cdabfba7db0" id="tgt41" class="tgtSentence"> Para configurar y administrar sus registros de uso de Azure Rights Management, tendrá que cmdlets de Windows PowerShell.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="78f46de00ad34ecb83811118c3a3100a" id="tgt42" class="tgtSentence">Para obtener más información, vea <link xlink:href="0d665ed6-b1de-4d63-854a-bc57c1c49844">Installing Windows PowerShell for Azure Rights Management</link>.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <caps:sentence sentenceid="87b36330723a87dd0317636c38a95df3" id="tgt43" class="tgtSentence">Use el siguiente procedimiento para habilitar el registro de uso de Azure Rights Management, que incluye los pasos para crear una cuenta de almacenamiento de Azure y, después, configure Azure para usar esta cuenta de almacenamiento para sus registros de Rights Management.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="57c6007bcbf6f438841837bbec56e945" id="tgt44" class="tgtSentence">Este procedimiento supone que dispone de una cuenta de Azure.</caps:sentence>
              <caps:sentence sentenceid="3e3fb8e67bccd8fc678be3c592b9b04e" id="tgt45" class="tgtSentence"> El registro de uso de Azure Rights Management admite cuentas individuales pero, como procedimiento recomendado, use cuentas profesionales o educativas.</caps:sentence>
              <caps:sentence sentenceid="30772583e317300ad595232f1f52dc4f" id="tgt46" class="tgtSentence"> Además, recomendamos que cree una cuenta de almacenamiento dedicado para sus registros de Rights Management.</caps:sentence>
              <caps:sentence sentenceid="93236b8c8811d2c6d96372a73fbb743d" id="tgt47" class="tgtSentence"> Debe compartir las claves de acceso de almacenamiento con Azure Rights Management y, potencialmente, con otras personas si también ellas van a usar los archivos de registro.</caps:sentence>
            </para>
            <para>
              <caps:sentence sentenceid="593a5b9526465570155b1e05e1795ce2" id="tgt48" class="tgtSentence">Para obtener más información sobre Almacenamiento de Azure, consulte la <externalLink><linkText>documentación de Azure para Almacenamiento</linkText><linkUri>http://azure.microsoft.com/documentation/services/storage/</linkUri></externalLink>.</caps:sentence>
            </para>
          </alert>
          <procedure>
            <title>
              <caps:sentence sentenceid="d8e22cce85bb6f234af129095f1a1980" id="tgt49" class="tgtSentence">Cómo crear una cuenta de almacenamiento y habilitar el registro de uso de Azure Rights Management</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="68ed02aa7205eb409ab30ce31e8b750a" id="tgt50" class="tgtSentence">Inicie sesión en el <externalLink><linkText>Portal de Azure</linkText><linkUri>https://portal.azure.com/</linkUri></externalLink>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="0ba6f5ad2fd43bd3a3052283674f3854" id="tgt51" class="tgtSentence">En el menú del concentrador, seleccione <ui>Nuevo</ui> -&gt; <ui>Datos y almacenamiento</ui> -&gt; <ui>Cuenta de almacenamiento</ui>.</caps:sentence>
                  </para>
                  <alert class="tip">
                    <para>
                      <caps:sentence sentenceid="d0ebb82309829aadc91cacaa2b9dbab5" id="tgt52" class="tgtSentence">Si no ve esta opción, compruebe que dispone de una suscripción de Azure además de la suscripción para Rights Management.</caps:sentence>
                    </para>
                  </alert>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="dadb86252078de0daa11945f3d261e32" id="tgt53" class="tgtSentence">Conserve el modelo de implementación predeterminado <ui>Clásico</ui> y haga clic en <ui>Crear</ui>.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="5eec891aaa904b49837c58de106218f4" id="tgt54" class="tgtSentence">Especifique el nombre de su cuenta de almacenamiento y, si es necesario, cambie las opciones seleccionadas de los campos <ui>Plan de tarifa</ui>, <ui>Grupo de recursos</ui> y <ui>Suscripción</ui> e indique si desea usar la opción <ui>Anclar al panel</ui>.</caps:sentence>
                    <caps:sentence sentenceid="c82aef6fc0a04ab522f7da142084ce66" id="tgt55" class="tgtSentence"> Después, haga clic en <ui>CREAR</ui>.</caps:sentence>
                    <caps:sentence sentenceid="2959b731a96aca72142dc43ca9d5a7fb" id="tgt56" class="tgtSentence"> Espere a que finalice la actividad <ui>Creando cuenta de almacenamiento</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="f01e288f25fc6f38c98005dddce0d2fe" id="tgt57" class="tgtSentence">Haga clic en la cuenta de almacenamiento recién creada y, después, en <ui>Configuración</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="9e8d363a79475c19866e5f0734a00115" id="tgt58" class="tgtSentence">En la hoja <ui>Configuración</ui>, haga clic en el icono <ui>Claves</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="7aa057045be66dddd2be095e3f7a6405" id="tgt59" class="tgtSentence">En la hoja <ui>Administrar claves</ui>, copie el valor de la <ui>CLAVE DE ACCESO PRINCIPAL</ui> y cierre la hoja.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="50748c32a69ae84138cf873027f9ca0e" id="tgt60" class="tgtSentence">Inicie Windows PowerShell con la opción <ui>Ejecutar como administrador</ui>.</caps:sentence>
                    <caps:sentence sentenceid="3aec01c4ed13e25ec854eb3bb237faaa" id="tgt61" class="tgtSentence"> Ejecute el comando <externalLink><linkText>Connect-AadrmService</linkText><linkUri>https://msdn.microsoft.com/library/azure/dn629415.aspx</linkUri></externalLink> para conectarse al servicio de Azure Rights Management:</caps:sentence>
                  </para>
                  <code>Connect-AadrmService</code>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="236eb2d0849650d2ae54c9f577741b48" id="tgt62" class="tgtSentence">Use el comando <externalLink><linkText>Set-AadrmUsageLogStorageAccount</linkText><linkUri>https://msdn.microsoft.com/library/azure/dn629426.aspx</linkUri></externalLink> para especificar dónde desea conservar sus registros de uso de Azure Rights Management. Para ello, sustituya <placeholder>&lt;Access_Key&gt;</placeholder> por la clave de acceso principal que ha copiado en el paso 6 y <placeholder>&lt;StorageAccount&gt;</placeholder> por el nombre de la cuenta de almacenamiento que ha creado en el paso 3:</caps:sentence>
                  </para>
                  <code>$accesskey = convertto-securestring -asplaintext -force –string <placeholder xmlns="">&lt;Access_Key&gt;</placeholder> Set-AadrmUsageLogStorageAccount -AccessKey $accesskey -StorageAccount <placeholder xmlns="">&lt;StorageAccount&gt;</placeholder></code>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="2268cc04e4ff547940f1beefe8323219" id="tgt63" class="tgtSentence">Use el comando <externalLink><linkText>Enable-AadrmUsageLogFeature</linkText><linkUri>https://msdn.microsoft.com/library/azure/dn629421.aspx</linkUri></externalLink> para habilitar el registro de uso de Azure Rights Management:</caps:sentence>
                  </para>
                  <code>Enable-AadrmUsageLogFeature</code>
                  <para>
                    <caps:sentence sentenceid="d9eced68736b4b3f239b5019dce23ae3" id="tgt64" class="tgtSentence">Debe ver el siguiente mensaje: <ui>La característica de registro de uso está habilitada para el servicio de Rights Management Service.</ui></caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence sentenceid="aab05520a5826f77f5de324537c86146" id="tgt65" class="tgtSentence">Ahora que el registro de uso está habilitado, Azure Rights Management puede empezar a registrar todas las acciones relativas a su organización y a guardar esta información en su cuenta de almacenamiento.</caps:sentence>
                  <caps:sentence sentenceid="3351fff94db1da9be25affb0176f1b36" id="tgt66" class="tgtSentence"> La información de registro no está disponible antes de este punto.</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="e4c26b2820e13a337f4cf8b8910cd3a4" id="tgt67" class="tgtSentence">Para obtener más información sobre cómo crear cuentas de almacenamiento, consulte la sección <externalLink><linkText>Crear una cuenta de almacenamiento</linkText><linkUri>https://azure.microsoft.com/documentation/articles/storage-create-storage-account/#create-a-storage-account</linkUri></externalLink> en <externalLink><linkText>Acerca de las cuentas de almacenamiento de Azure</linkText><linkUri>https://azure.microsoft.com/documentation/articles/storage-create-storage-account/</linkUri></externalLink>, en la documentación de Azure.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
        </content>
      </section>
      <section address="BKMK_AccesAndUseLogs">
        <title>
          <caps:sentence sentenceid="dc4a1a28217b1dd3982eaf83276f2c37" id="tgt68" class="tgtSentence">Cómo acceder a los registros de uso de Azure Rights Management y usarlos</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="dfaf479d19a1261f9ef0e74dbe9284d4" id="tgt69" class="tgtSentence">Azure Rights Management escribe registros en su cuenta de almacenamiento de Azure como una serie de blobs.</caps:sentence>
            <caps:sentence sentenceid="30febf2bb481a98bc09a1f40c034a5f0" id="tgt70" class="tgtSentence"> Cada blob contiene uno o más registros, en formato de registro extendido W3C.</caps:sentence>
            <caps:sentence sentenceid="786c43af7325b1745ee7fde27e09e6e5" id="tgt71" class="tgtSentence"> Los nombres de blob son números, en el orden en que se crearon.</caps:sentence>
            <caps:sentence sentenceid="3f42c28b2f7e182b9ebd51e6e9895efb" id="tgt72" class="tgtSentence"> La sección <link xlink:href="a735f3f7-6eb2-4901-9084-8c3cd3a9087e#BKMK_Interpret">How to interpret the RMS logs</link> que aparece más adelante en este documento contiene más información acerca del contenido del registro y su creación.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="8749a5358b98f2ba216c5cdd54e4d689" id="tgt73" class="tgtSentence">Puede que los registros tarden en aparecer en su cuenta de almacenamiento después de realizar alguna acción de Azure Rights Management.</caps:sentence>
            <caps:sentence sentenceid="1e79717caf4b582029f9085c915956a2" id="tgt74" class="tgtSentence"> La mayoría de los registros aparecen en 15 minutos.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="88df5d64348c0a53bb418f1351cb120c" id="tgt75" class="tgtSentence">La cuenta de almacenamiento que ha creado para sus registros de uso de Azure Rights Management es similar a un buzón de correo y admite la lectura directamente desde la cuenta de almacenamiento, pero no está optimizada para usarse de esta manera.</caps:sentence>
            <caps:sentence sentenceid="3fcc555aa2a34edfb985c904dff7721a" id="tgt76" class="tgtSentence"> En su lugar, para lograr un mejor rendimiento y para ayudar a reducir costos, recomendamos que descargue los registros en el almacenamiento local, como una carpeta local, una base de datos o un repositorio de asignar-reducir.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="349be16b36423dfe5e637b44011b6b29" id="tgt77" class="tgtSentence">Puede descargar sus registros de uso de dos maneras:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="256e81480aeaa9e5230637955d398bac" id="tgt78" class="tgtSentence">Use el cmdlet de Windows PowerShell <externalLink><linkText>Get-AadrmUsageLog</linkText><linkUri>https://msdn.microsoft.com/library/azure/dn629401.aspx</linkUri></externalLink>.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="5641ce03007faebba5d74be6c69fca13" id="tgt79" class="tgtSentence">Esta es la manera más sencilla de acceder a los registros de uso.</caps:sentence>
                <caps:sentence sentenceid="7f4c5f7410e06bde495fe746c2e2fef9" id="tgt80" class="tgtSentence"> Este cmdlet descarga registros en su equipo, descargando cada blob como un archivo en la ubicación que especifique.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="c0ce9501b5c6bb6bb9f5d50e85ccdf60" id="tgt81" class="tgtSentence">Utilice el <externalLink><linkText>SDK de Almacenamiento de Azure</linkText><linkUri>http://www.windowsazure.com/en-us/develop/net/</linkUri></externalLink> para escribir su propia aplicación personalizada para descargar los registros.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="ec6f9840011393a65343fdc6b933c95f" id="tgt82" class="tgtSentence">Una aplicación personalizada puede ofrecer mayor flexibilidad que el cmdlet Get-AadrmUsageLogs.</caps:sentence>
                <caps:sentence sentenceid="a07fcd56c121241df8fbee825c5ea8f1" id="tgt83" class="tgtSentence"> Por ejemplo, puede que desee delegar la descarga de los registros a alguien o a un proceso que no deba usar sus credenciales administrativas de Azure Rights Management.</caps:sentence>
                <caps:sentence sentenceid="0fe3a6aa9bc4eb3aa65567aac1b640fb" id="tgt84" class="tgtSentence"> O bien, puede que desee sondear los registros en tiempo real porque desea supervisar el uso incorrecto.</caps:sentence>
              </para>
            </listItem>
          </list>
          <procedure>
            <title>
              <caps:sentence sentenceid="cc3565295dee497953e3cd6b0d5a5fc5" id="tgt85" class="tgtSentence">Descargar sus registros de uso mediante PowerShell</caps:sentence>
            </title>
            <steps class="bullet">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="695ec94f1c08343c169b29242610d9b7" id="tgt86" class="tgtSentence">Inicie Windows PowerShell con la opción <ui>Ejecutar como administrador</ui> y ejecute <userInput>Get-AadrmUsageLog –Path &lt;location&gt;</userInput>.</caps:sentence>
                    <caps:sentence sentenceid="ea943b6df49a9006658062243b2ada13" id="tgt87" class="tgtSentence"> Por ejemplo, después de crear una carpeta denominada <system>logs</system> en la unidad E:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="d831938b24eb44a6b35c5f2d5ad9a308" id="tgt88" class="tgtSentence">Para descargar todos los registros disponibles en su carpeta E:\logs: <codeInline>Get-AadrmUsageLog -Path "e:\logs"</codeInline></caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="64d3dc8c2b27c92020fda1d91e6ed069" id="tgt89" class="tgtSentence">Para descargar un intervalo específico de blobs: <codeInline>Get-AadrmUsageLog –Path "e:\logs" –FromCounter 1024 –ToCounter 2047</codeInline></caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence sentenceid="13a14fd187043a220d91bbdd37ae6f5c" id="tgt90" class="tgtSentence">Cuando ejecuta estos cmdlets, Windows PowerShell muestra el nombre del último blob que se descargó.</caps:sentence>
                  <caps:sentence sentenceid="415ed2d3b4c9a23c6fda12610a4c09e7" id="tgt91" class="tgtSentence"> Puede asignar este nombre a una variable, lo que le permite ejecutar Get-AadrmUsageLog en un bucle o trabajo de programación, descargando solo los registros incrementales cada vez.</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="a1f6c7d21a6ee4379899b0d1aeea4222" id="tgt92" class="tgtSentence">Por ejemplo:  </caps:sentence>
                </para>
                <para>
                  <ui>
                    <caps:sentence sentenceid="3415067eec4beeceb4dbc9e82d924069" id="tgt93" class="tgtSentence">PS C:\&gt; $LastBlobName = Get-AadrmUsageLog –Path "e:\logs"</caps:sentence>
                  </ui>
                </para>
                <para>
                  <ui>
                    <caps:sentence sentenceid="5cce8dede893813f879b873962fb669f" id="tgt94" class="tgtSentence">1527</caps:sentence>
                  </ui>
                </para>
                <para>
                  <ui>
                    <caps:sentence sentenceid="2b424b192d1604c3cb776062e227ef00" id="tgt95" class="tgtSentence">PS C:\&gt; $LastBlobName</caps:sentence>
                  </ui>
                </para>
                <para>
                  <ui>
                    <caps:sentence sentenceid="5cce8dede893813f879b873962fb669f" id="tgt96" class="tgtSentence">1527</caps:sentence>
                  </ui>
                </para>
              </content>
            </conclusion>
          </procedure>
          <alert class="tip">
            <para>
              <caps:sentence sentenceid="fe2cd3cf4c5689e9c1be504e49125f83" id="tgt97" class="tgtSentence">Puede agrupar todos los archivos de registro descargados en un formato CSV mediante el uso del <externalLink><linkText>Analizador del registro de Microsoft</linkText><linkUri>http://www.microsoft.com/download/details.aspx?id=24659</linkUri></externalLink>, una herramienta para realizar conversiones entre diversos formatos de archivo conocidos.</caps:sentence>
              <caps:sentence sentenceid="718ae56ff7645b9dbed73d69a36d0aeb" id="tgt98" class="tgtSentence"> También puede usar esta herramienta para convertir datos al formato SYSLOG o importarlo a un base de datos.</caps:sentence>
              <caps:sentence sentenceid="ac77ffe3dc433d4da9abe432f5556beb" id="tgt99" class="tgtSentence"> Una vez que haya instalado la herramienta, ejecute <userInput>LogParser.exe /?</userInput> para obtener ayuda e información para usar esta herramienta.</caps:sentence>
              <caps:sentence sentenceid="3d2512f40fc44d3455edcc7273f602cc" id="tgt100" class="tgtSentence"> Por ejemplo, puede ejecutar el siguiente comando para importar toda la información en un formato de archivo .log: <userInput>logparser –i:w3c –o:csv “SELECT * INTO AllLogs.csv FROM *.log”</userInput>.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence sentenceid="40bb56c4a978f1782482e5748ef96f15" id="tgt101" class="tgtSentence">Puede suspender y reanudar el uso del registro de uso.</caps:sentence>
            <caps:sentence sentenceid="8359951e485e1e039ad71db1e4c358c5" id="tgt102" class="tgtSentence"> Cuando suspende el registro, Azure Rights Management conserva la información de su cuenta de almacenamiento, de manera que puede reanudar el registro con facilidad.</caps:sentence>
          </para>
          <procedure>
            <title>
              <caps:sentence sentenceid="6d175252b6d18419e7f44874c2d8868d" id="tgt103" class="tgtSentence">Suspender y reanudar el registro de uso</caps:sentence>
            </title>
            <steps class="bullet">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="16570773aca75ec14a6527f582e93948" id="tgt104" class="tgtSentence">Para suspender el registro, use el siguiente cmdlet: <externalLink><linkText>Disable-AadrmUsageLogFeature</linkText><linkUri>https://msdn.microsoft.com/library/azure/dn629404.aspx</linkUri></externalLink></caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="5b0127ffb8173302edec1845507821af" id="tgt105" class="tgtSentence">Para reanudar el registro, use el siguiente cmdlet: <externalLink><linkText>Enable-AadrmUsageLogFeature</linkText><linkUri>https://msdn.microsoft.com/library/azure/dn629421.aspx</linkUri></externalLink></caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="b98ec766be0c1df7ab3052ca4b5305d8" id="tgt106" class="tgtSentence">Para comprobar si el registro está habilitado o deshabilitado, use el siguiente cmdlet: <externalLink><linkText>Get-AadrmUsageLogFeature</linkText><linkUri>https://msdn.microsoft.com/library/azure/dn629425.aspx</linkUri></externalLink></caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="31f09fcf540867b0039f7e4b0ef82936" id="tgt107" class="tgtSentence">El valor <ui>True</ui> indica que el registro de uso está habilitado para Azure Rights Management, y el valor <ui>False</ui> indica que el registro de uso está deshabilitado.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
        </content>
      </section>
      <section address="BKMK_ManageStorage">
        <title>
          <caps:sentence sentenceid="9f112ac6900e27d6fc6cdab820ac9eb4" id="tgt108" class="tgtSentence">Cómo administrar el almacenamiento de registro de Azure Rights Management</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="960afa12e510934f332f9da245e8a906" id="tgt109" class="tgtSentence">Se le cobra por el espacio de almacenamiento que se usa para conservar sus registros de Azure Rights Management.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="e371c6c98c798ad7191255b54c6ff10a" id="tgt110" class="tgtSentence">Azure Rights Management no administra automáticamente los archivos del registro de uso.</caps:sentence>
            <caps:sentence sentenceid="d2efcec5b4bd584aa13ff611c2dc05b9" id="tgt111" class="tgtSentence"> Si no realiza ninguna acción, permanecerán en su cuenta de almacenamiento.</caps:sentence>
            <caps:sentence sentenceid="3031b7daa55495e350228c8c69bd59cf" id="tgt112" class="tgtSentence"> Sin embargo, para conservar el espacio y reducir los costes de almacenamiento, puede que desee eliminarlos tras su descarga.</caps:sentence>
            <caps:sentence sentenceid="ba91c05f3eaeb22e426d0083e542e62f" id="tgt113" class="tgtSentence"> O bien, puede elegir qué archivos desea eliminar.</caps:sentence>
            <caps:sentence sentenceid="cf073dcb1168338a9d109e5f62664a53" id="tgt114" class="tgtSentence"> Con una excepción, Azure Rights Management no usa estos archivos de registro, por lo que no hay restricciones acerca de cuándo puede eliminarlos.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="359275244501626faa4952c21a70a3fe" id="tgt115" class="tgtSentence">El archivo que no debe eliminar (ni modificar) es el que se llama <ui>metadata</ui> que se encuentra en el contenedor <ui>rms-metadata</ui>.</caps:sentence>
            <caps:sentence sentenceid="58a4cb03a4cb7778af0ce3c2f3ced5ac" id="tgt116" class="tgtSentence"> Azure Rights Management usa este blob para realizar un seguimiento del último número de blob que se use.</caps:sentence>
            <caps:sentence sentenceid="044ad7e892af7390100fedc4fbc90831" id="tgt117" class="tgtSentence"> Si se elimina este archivo, Azure Rights Management empieza un nuevo contenedor para los registros con un número de blob que empieza por 1. Todas las descargas futuras que usen el cmdlet Get-AadrmUsageLog usarán este nuevo contenedor para descargar archivos de registro.</caps:sentence>
            <caps:sentence sentenceid="3a3cc15659fc6b7fd326afb237f410d3" id="tgt118" class="tgtSentence"> Como resultado, se retienen los registros del contenedor original pero huérfanos.</caps:sentence>
            <caps:sentence sentenceid="a9f2543765cc1678acab822f227ea339" id="tgt119" class="tgtSentence"> La única manera de descargar estos registros huérfanos es usar el SDK de almacenamiento de Azure.</caps:sentence>
          </para>
          <alert class="tip">
            <para>
              <caps:sentence sentenceid="ba9329be7a6cb3e15721c9398f4a4b15" id="tgt120" class="tgtSentence">En lugar de administrar el almacenamiento del registro de Azure Rights Management el propio usuario, puede delegar esta función de administración en otra empresa compartiendo su nombre de cuenta de almacenamiento y la clave de acceso.</caps:sentence>
              <caps:sentence sentenceid="2e87169ffeac9e2cf802eece478a0ebd" id="tgt121" class="tgtSentence"> Para obtener más información, consulte la sección <link xlink:href="a735f3f7-6eb2-4901-9084-8c3cd3a9087e#BKMK_Delegate">How to delegate access to your RMS logs</link> que aparece más adelante en este tema.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence sentenceid="5868c659bd0e1da19037fdefcb434a9e" id="tgt122" class="tgtSentence">En algunas circunstancias, puede que desee regenerar sus claves de acceso de almacenamiento.</caps:sentence>
            <caps:sentence sentenceid="4be0bb25039056347740ae85bcda324d" id="tgt123" class="tgtSentence"> Por ejemplo:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="30f17a264c68cc899b95976c1e2ddef9" id="tgt124" class="tgtSentence">Cambia la empresa que administra sus registros de uso de Azure Rights Management.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="8be77f50e8f00a4e36c7231b8b84d0f7" id="tgt125" class="tgtSentence">Sospecha que se ha puesto en peligro la clave de acceso de almacenamiento.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="7c30654f7b0c28b28fb51871bb3d0055" id="tgt126" class="tgtSentence">Si le sucede esto, es cuando usa la clave de acceso secundaria (suponiendo que anteriormente estuviera usando la clave de acceso primaria) para garantizar la continuidad del servicio.</caps:sentence>
            <caps:sentence sentenceid="bda442ba2d89743385762b35632f6efb" id="tgt127" class="tgtSentence"> Cuando vuelva a generar la clave de acceso que no estuviera usando anteriormente, configurará Azure Rights Management para que use la nueva clave.</caps:sentence>
            <caps:sentence sentenceid="cb7a47952b8d0a380e54e52ea0230a60" id="tgt128" class="tgtSentence"> Use el siguiente procedimiento para volver a generar la clave de acceso secundaria y configurar Azure Rights Management para que la use:</caps:sentence>
          </para>
          <procedure>
            <title>
              <caps:sentence sentenceid="7238814bf3d7691da247d2b88d2fa075" id="tgt129" class="tgtSentence">Volver a generar la clave de acceso secundaria</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="cae37d648c86b6f47bc355b45824d076" id="tgt130" class="tgtSentence">Inicie sesión en el <externalLink><linkText>Portal de Azure</linkText><linkUri>https://portal.azure.com/</linkUri></externalLink>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="33ca12a16d67b46a984dab2889908af5" id="tgt131" class="tgtSentence">Haga clic en <ui>Todos los recursos</ui> y, para buscar su almacenamiento, escriba el nombre del almacenamiento en el cuadro de texto.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="adaf7620cb56764d5b1637570d51962f" id="tgt132" class="tgtSentence">Seleccione el almacenamiento y haga clic en <ui>Configuración</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="ca20a03e1cf92d31fc6bb5b517a3b4af" id="tgt133" class="tgtSentence">Haga clic en el icono <ui>Claves</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="76527b248f9eae623d0d81f2a9f84700" id="tgt134" class="tgtSentence">En la sección <ui>Administrar claves</ui>, haga clic en <ui>Regenerar clave secundaria</ui>, haga clic en Sí para confirmar que desea regenerar la clave de acceso secundaria y copie la nueva clave en el portapapeles.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="b5544643b73914a8e818bde967daba56" id="tgt135" class="tgtSentence">No cierre el Portal de Azure.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="87040541a28e235207f4587cc9395ab4" id="tgt136" class="tgtSentence">Inicie Windows PowerShell con la opción <ui>Ejecutar como administrador</ui> y use el cmdlet <externalLink><linkText>Set-AadrmUsageLogStorageAccount</linkText><linkUri>https://msdn.microsoft.com/library/azure/dn629426.aspx</linkUri></externalLink> para configurar Azure Rights Management para usar esta nueva clave de acceso. Para ello, sustituya <placeholder>&lt;StorageAccount&gt;</placeholder> por el nombre de la cuenta de almacenamiento y <placeholder>&lt;Access_Key&gt;</placeholder> por la clave de acceso secundaria regenerada que acaba de copiar:</caps:sentence>
                  </para>
                  <code>Set-AadrmUsageLogStorageAccount -StorageAccount <placeholder xmlns="">&lt;StorageAccount&gt;</placeholder>-AccessKey <placeholder xmlns="">&lt;Access_Key&gt;</placeholder></code>
                  <alert class="warning">
                    <para>
                      <caps:sentence sentenceid="231ffb09152ca251535417d8ce8f28ea" id="tgt137" class="tgtSentence">Aunque puede cambiar a otra cuenta de almacenamiento cuando ejecute este comando, esta acción deja huérfanos sus registros previos, con lo que ya no se podrá acceder a ellos con el cmdlet Set-AadrmUsageLogStorageAccount o con funciones y comandos de administración similares.</caps:sentence>
                    </para>
                  </alert>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="c741be5de58f47807ea603df6590204b" id="tgt138" class="tgtSentence">En el Portal de Azure, en la sección <ui>Administrar claves</ui>, regenere su clave de acceso principal.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence sentenceid="38c3448eb7c3aadba775791f7c5d6d6c" id="tgt139" class="tgtSentence">Para obtener más información sobre la manera de administrar las claves de acceso de almacenamiento, consulte la sección <externalLink><linkText>Administración de las claves de acceso de almacenamiento</linkText><linkUri>https://azure.microsoft.com/documentation/articles/storage-create-storage-account/#manage-your-storage-access-keys</linkUri></externalLink> en <externalLink><linkText>Acerca de las cuentas de almacenamiento de Azure</linkText><linkUri>https://azure.microsoft.com/documentation/articles/storage-create-storage-account/</linkUri></externalLink>, en la documentación de Azure.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
        </content>
      </section>
      <section address="BKMK_Delegate">
        <title address="BKMK_DelegateAccess">
          <caps:sentence sentenceid="d77e400fe7fa32738866fdfa1bed1d6c" id="tgt140" class="tgtSentence">Cómo delegar el acceso a los registros de uso de Azure Rights Management</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="f91bfa3fa851c57ca1cd1259b862f993" id="tgt141" class="tgtSentence">Puede delegar el acceso a sus registros de RMS compartiendo su clave de acceso y nombre de cuenta de almacenamiento.</caps:sentence>
            <caps:sentence sentenceid="9456f4df0aed5e6f524d1c70a5a490cf" id="tgt142" class="tgtSentence"> Puede que desee delegar el acceso a otro usuario administrativo, a un desarrollador de su propia organización o a un proveedor de software independiente (ISV).</caps:sentence>
            <caps:sentence sentenceid="04b90e7371044b923daac74ce8635f4a" id="tgt143" class="tgtSentence"> Dado que no tendrán sus credenciales de administrador de RMS, no pueden usar el cmdlet Get-AardrmUsageLog para descargar los registros de RMS.</caps:sentence>
            <caps:sentence sentenceid="0556092088db21a8d4e37f57bccb269a" id="tgt144" class="tgtSentence"> En su lugar, deben usar el SDK de almacenamiento de Windows para descargar los registros.</caps:sentence>
            <caps:sentence sentenceid="e8f76d769c2a47521ca6015932b6303d" id="tgt145" class="tgtSentence"> Como alternativa, puede escribir una aplicación para que lea los registros directamente desde el almacenamiento de almacenamiento de Azure.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="6238dcfa4b912f02d784b0f73aa40be9" id="tgt146" class="tgtSentence">Es seguro compartir su clave de acceso y su nombre de cuenta de almacenamiento de esta manera cuando la cuenta de almacenamiento está dedicada a sus registros de RMS.</caps:sentence>
            <caps:sentence sentenceid="5ff9e1e0e646a489073469aede84dbb7" id="tgt147" class="tgtSentence"> Incluso cuando otras personas tienen su clave de acceso, no pueden usarla para acceder a ninguna otra cuenta de almacenamiento o usar su cuenta de inquilino de RMS.</caps:sentence>
          </para>
        </content>
      </section>
      <section address="BKMK_Interpret">
        <title>
          <caps:sentence sentenceid="5c6bb80be89318ffebdcf10299a07402" id="tgt148" class="tgtSentence">Cómo interpretar los registros de uso de Azure Rights Management</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="59a66176b5102e4c4a74d1c34737270e" id="tgt149" class="tgtSentence">Use la siguiente información como ayuda para interpretar los registros de uso de Azure Rights Management.</caps:sentence>
          </para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence sentenceid="fd067266e2e21d97d5167abd3cc00b5b" id="tgt150" class="tgtSentence">El diseño de la cuenta de almacenamiento</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="040f720fa0870b0c7f70f0c3f108cbb0" id="tgt151" class="tgtSentence">La primera vez que Azure Rights Management escribe registros en la cuenta de almacenamiento, crea los siguientes dos contenedores:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="97697417872101f9d4fab09cd25cc446" id="tgt152" class="tgtSentence">
                      <ui>Rms-metadata</ui>: este contenedor está reservado para Azure Rights Management.</caps:sentence>
                    <caps:sentence sentenceid="e3b77c3d43dba43eb30eb4ffda250c6a" id="tgt153" class="tgtSentence"> No modifique ni elimine este contenedor.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="1cb029f0187e5f8dab66cc6641819d74" id="tgt154" class="tgtSentence">
                      <ui>Rms-logs-&lt;guid&gt;</ui>: en este contenedor Azure Rights Management crea y guarda los registros.</caps:sentence>
                    <caps:sentence sentenceid="75ec055df7b955189d8087a250f72f01" id="tgt155" class="tgtSentence"> Puede eliminar de manera segura los archivos de este contenedor si ya no desea la información de registro que pueden contener.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="9fa2ea972577b81dd318d304d045a3f4" id="tgt156" class="tgtSentence">Con el tiempo, Azure Rights Management puede crear contenedores <ui>Rms-logs-&lt;guid&gt;</ui> adicionales.</caps:sentence>
                <caps:sentence sentenceid="940119257e3614edaa74b13dad191a31" id="tgt157" class="tgtSentence"> Por ejemplo, si el contenedor <ui>Rms-metadata</ui> se daña o se elimina de manera accidental, Azure Rights Management restablece su contenido y crea un nuevo contenedor <ui>Rms-logs-&lt;guid&gt;</ui> para todos los registros futuros.</caps:sentence>
                <caps:sentence sentenceid="59d3c2a444df97b01c696fd9a69631ca" id="tgt158" class="tgtSentence"> Los registros antiguos del contenedor antiguo no se eliminan pero están huérfanos.</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="80430c9a4ac2534726d4e66923ec4edf" id="tgt159" class="tgtSentence">La secuencia de registro</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="11176a798c30453cb75c2be6609c6cbd" id="tgt160" class="tgtSentence">Azure Rights Management escribe los registros como una serie de blobs.</caps:sentence>
                <caps:sentence sentenceid="849f99dcee9c854baad8567459e0bb57" id="tgt161" class="tgtSentence"> Cada blob contiene uno o más registros, en formato de registro W3C extendido.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="4be416dbd6b1c6c9fdd6db68cd25891a" id="tgt162" class="tgtSentence">El nombre de cada blob es un número.</caps:sentence>
                <caps:sentence sentenceid="bab04283fb61bba2066b10e31cbc7125" id="tgt163" class="tgtSentence"> Dentro de cada contenedor de registro, el primer blob se denomina 000000001.</caps:sentence>
                <caps:sentence sentenceid="e295b69afd6e4e42d9c21c89e9431b2b" id="tgt164" class="tgtSentence"> Cada blob se denomina secuencialmente en el orden en que se creó.</caps:sentence>
                <caps:sentence sentenceid="da8bec5b9d6c692b080b65bf366fc392" id="tgt165" class="tgtSentence"> Cada blob contiene uno o más registros.</caps:sentence>
                <caps:sentence sentenceid="904e47a34f54f0bf428830e8401017f4" id="tgt166" class="tgtSentence"> Cada registro tiene una marca de tiempo UTC que indica el momento en el que la solicitud correspondiente recibió el servicio de Azure Rights Management.</caps:sentence>
              </para>
              <alert class="important">
                <para>
                  <caps:sentence sentenceid="5619bfc871913e3ecb396657c2eafd5e" id="tgt167" class="tgtSentence">El sistema de registro de Azure Rights Management se optimiza para proporcionarle registros con rapidez, en lugar de en estricto orden secuencial.</caps:sentence>
                  <caps:sentence sentenceid="f4c6881f9682fee7a503927d15db1337" id="tgt168" class="tgtSentence"> El orden de los blobs, así como el orden de los registros dentro de un blob, puede que esté fuera de la secuencia cronológica.</caps:sentence>
                  <caps:sentence sentenceid="d2c9c82195b2d281352be1db2bdd3b16" id="tgt169" class="tgtSentence"> El único motivo por el que se asignan nombres a los blobs de manera secuencial es para habilitarle su descarga efectiva de manera incremental.</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="99b9220c634dcc8a1ac47d3cf45fde4f" id="tgt170" class="tgtSentence">Dos ejemplos de resultados de secuencia de registro:</caps:sentence>
                </para>
                <list class="bullet">
                  <listItem>
                    <para>
                      <caps:sentence sentenceid="32d327dda5a57377d319815aac313094" id="tgt171" class="tgtSentence">Los registros del blob 000000004 se pueden superponer cronológicamente con los registros del blob 000000003.</caps:sentence>
                      <caps:sentence sentenceid="16adaee22ba7fb49c30415e9524f8809" id="tgt172" class="tgtSentence"> En casos extremos, todos los registros del blob 000000004 podrían haberse generados antes que todos los registros del blob 000000003.</caps:sentence>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <caps:sentence sentenceid="a1c47894a7d84af2504670c499f850ab" id="tgt173" class="tgtSentence">El segundo registro se podría haber generado antes que el primer registro pero se escribió en el almacenamiento en el orden inverso.</caps:sentence>
                    </para>
                  </listItem>
                </list>
              </alert>
              <para>
                <caps:sentence sentenceid="d20929dce36bf83c8f3f9ed07baadf7d" id="tgt174" class="tgtSentence">Antes de analizar sus registros de uso de Azure Rights Management, recomendamos que descargue e importe el registro en un repositorio donde pueda ordenar los registros en función de los registros basados en su marca de tiempo.</caps:sentence>
                <caps:sentence sentenceid="42d83b83c49ac75cb42e677d76dd606b" id="tgt175" class="tgtSentence"> Para obtener más información sobre cómo descargar los archivos, consulte la sección <link xlink:href="a735f3f7-6eb2-4901-9084-8c3cd3a9087e#BKMK_AccesAndUseLogs">How to access and use your RMS logs</link> de este tema.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="0d70986d8572ca17541727a8ad3ef988" id="tgt176" class="tgtSentence">Dado que los registros no son necesariamente cronológicos, sino que la mayoría de ellos se escriben a los 15 minutos de la solicitud, cuando identifique los registros que desea usando su marca de tiempo, agregue 15 minutos al tiempo en el que está interesado.</caps:sentence>
                <caps:sentence sentenceid="beb7275f545b4fbdf1374a5e606cadef" id="tgt177" class="tgtSentence"> A continuación, descargue estos registros.</caps:sentence>
                <caps:sentence sentenceid="1f5cfe1809f5fc07cd1f2b6b6ee41564" id="tgt178" class="tgtSentence"> Esta estrategia debe garantizar que obtiene casi todos los registros.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="a49c0edb5f6cfe662144b7446c8b5dc1" id="tgt179" class="tgtSentence">Otra cuestión que hay que recordar es que la marca de tiempo de cada registro corresponde a la hora local del servicio de Azure Rights Management que procesó la solicitud.</caps:sentence>
                <caps:sentence sentenceid="dfd9efa77e5d10a18367ea08d49e4ce7" id="tgt180" class="tgtSentence"> Dado que Azure Rights Management se ejecuta en varios servidores de varios centros de datos, a veces puede parecer que los registros estén fuera de secuencia, aunque estén ordenados por su marca de tiempo.</caps:sentence>
                <caps:sentence sentenceid="9f772490464a359c30951736522b13bb" id="tgt181" class="tgtSentence"> Sin embargo, la diferencia es mínima y generalmente se encuentra en un margen de un minuto.</caps:sentence>
                <caps:sentence sentenceid="2b14f022b1ea127f004c96605eabe8cd" id="tgt182" class="tgtSentence"> En la mayoría de los casos, este asunto no sería un problema para análisis de registros.</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="b716ed2ff4bbdc28ad05a88c1bd6ef67" id="tgt183" class="tgtSentence">El formato del blob</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="e1ef66cad9113ac795b0758e4bdcb469" id="tgt184" class="tgtSentence">Cada blob está en formato de registro extendido W3C.</caps:sentence>
                <caps:sentence sentenceid="b6a8e711017a3a12b539d70ad55cfb46" id="tgt185" class="tgtSentence"> Empieza por las siguientes dos líneas:</caps:sentence>
              </para>
              <para>
                <ui>
                  <caps:sentence sentenceid="5ad5720222f32901e83d695efdb60fdc" id="tgt186" class="tgtSentence">#Software: RMS</caps:sentence>
                </ui>
              </para>
              <para>
                <ui>
                  <caps:sentence sentenceid="192bc742f8b27706156989e005e0fd25" id="tgt187" class="tgtSentence">#Version: 1.1</caps:sentence>
                </ui>
              </para>
              <para>
                <caps:sentence sentenceid="7b95b0a04ea8dc37bef830c98394e714" id="tgt188" class="tgtSentence">La primera línea identifica que se trata de registros de Azure Rights Management.</caps:sentence>
                <caps:sentence sentenceid="db31192c1615db5368dcb3847d1bbc05" id="tgt189" class="tgtSentence"> La segunda línea identifica que el resto del blob sigue la especificación de la versión 1.1.</caps:sentence>
                <caps:sentence sentenceid="9140d350f4ea24befc6eab451f07b3c8" id="tgt190" class="tgtSentence"> Recomendamos que las aplicaciones que analicen estos registros comprueben estas dos líneas antes de continuar analizando el resto del blob.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="a6c667f34d05c92e449cb9aeeec93866" id="tgt191" class="tgtSentence">La tercera enumera una lista de nombres de campos separados por pestañas:</caps:sentence>
              </para>
              <para>
                <ui>
                  <caps:sentence sentenceid="5cd553c8da6146368f025e5057f98153" id="tgt192" class="tgtSentence">#Fields: date            time            row-id        request-type           user-id       result          correlation-id          content-id                owner-email           issuer                     template-id             file-name                  date-published      c-info         c-ip</caps:sentence>
                </ui>
              </para>
              <para>
                <caps:sentence sentenceid="4d30c7bd9fcb5e1bac3dcb04da02cd2c" id="tgt193" class="tgtSentence">Cada una de las líneas posteriores es un registro.</caps:sentence>
                <caps:sentence sentenceid="fa86655907b6c76ab4396fb8f95d07b0" id="tgt194" class="tgtSentence"> Los valores de los campos se encuentran en el mismo orden que la línea anterior y están separados por pestañas.</caps:sentence>
                <caps:sentence sentenceid="fa151854dac81720c6345842152915a9" id="tgt195" class="tgtSentence"> Use la siguiente tabla para interpretar los campos.</caps:sentence>
              </para>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="bfaad773361a781112fb325b433d54f7" id="tgt196" class="tgtSentence">Nombre de campo</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="75d51135c88c7a73f17807636b6af548" id="tgt197" class="tgtSentence">Tipo de datos W3C</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt198" class="tgtSentence">Descripción</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="6bad7e8404558aafa56e9b15195bba76" id="tgt199" class="tgtSentence">Valor de ejemplo</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="5fc732311905cb27e82d67f4f6511f7f" id="tgt200" class="tgtSentence">date</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="5fc732311905cb27e82d67f4f6511f7f" id="tgt201" class="tgtSentence">Fecha</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="290a4432650313b2fd9966ccbf5379a7" id="tgt202" class="tgtSentence">Fecha UTC cuando se realizó el servicio de la solicitud.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="c894aaf8f5afdd71b59ba77d58800659" id="tgt203" class="tgtSentence">El origen es el reloj local del servidor que realizó el servicio de la solicitud.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="c926349b55a58d87d7d5008c349fd1e9" id="tgt204" class="tgtSentence">2013-06-25</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="07cc694b9b3fc636710fa08b6922c42b" id="tgt205" class="tgtSentence">time</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="07cc694b9b3fc636710fa08b6922c42b" id="tgt206" class="tgtSentence">Hora</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="fb234cc46d733196ccc085ecb40a14b4" id="tgt207" class="tgtSentence">Hora UTC en formato de 24 hora cuando se realizó el servicio de la solicitud.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="c894aaf8f5afdd71b59ba77d58800659" id="tgt208" class="tgtSentence">El origen es el reloj local del servidor que realizó el servicio de la solicitud.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="f2e1a047ebad38fc058d3858ca0a1fa3" id="tgt209" class="tgtSentence">21:59:28</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="c913fc70fcd84001d9bffc79a03a2895" id="tgt210" class="tgtSentence">row-id</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="1cb251ec0d568de6a929b520c4aed8d1" id="tgt211" class="tgtSentence">Texto</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="edfc6e4c10780e0dcb1ce1bd46842611" id="tgt212" class="tgtSentence">GUID único para este registro.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="1750772217daf898de93596558b1cd3b" id="tgt213" class="tgtSentence">Este valor es útil cuando agrega registros o copia registros en otro formato.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="46ba6d7217f80efae3dd3bd6f906c673" id="tgt214" class="tgtSentence">1c3fe7a9-d9e0-4654-97b7-14fafa72ea63</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="e595e7b5d47e2070c3da3cd16bb822d2" id="tgt215" class="tgtSentence">request-type</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="b068931cc450442b63f5b3d276ea4297" id="tgt216" class="tgtSentence">Nombre</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a03c4131e5a4c3ad0034ede12f427c48" id="tgt217" class="tgtSentence">Nombre de la API de RMS que se solicitó.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="96378d61537db78d2fcef81d104db1b0" id="tgt218" class="tgtSentence">AcquireLicense</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="e35c1a36e525c2e4642c43b55246de30" id="tgt219" class="tgtSentence">user-id</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="b45cffe084dd3d20d928bee85e7b0f21" id="tgt220" class="tgtSentence">Cadena</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ffe3d27ecb9bc4c4507df43f95c61966" id="tgt221" class="tgtSentence">El usuario que realizó la solicitud.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="e908e1289e34b2049c4a49c6dbbb699f" id="tgt222" class="tgtSentence">El valor se incluye entre comillas únicas.</caps:sentence>
                        <caps:sentence sentenceid="f76e0ef479d78d5bdd80c58d7aed7dc2" id="tgt223" class="tgtSentence"> Algunos tipos de solicitudes son anónimos, en cuyo caso el valor es ”.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="df088d1c17ac7e56eb0c7d28294a0234" id="tgt224" class="tgtSentence">‘joe@contoso.com’</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="b4a88417b3d0170d754c647c30b7216a" id="tgt225" class="tgtSentence">result</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="b45cffe084dd3d20d928bee85e7b0f21" id="tgt226" class="tgtSentence">Cadena</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="3996930f607c6e99d8fb0f93244f7012" id="tgt227" class="tgtSentence">‘Success’ si se realizó el servicio de la solicitud correctamente.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="ce3099faf273786d788f3ed672b17d11" id="tgt228" class="tgtSentence">El tipo de error entre comillas si se produjo un error de la solicitud.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="1cca321971ced8592af906efc27b381e" id="tgt229" class="tgtSentence">‘Success’</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="d5a8a8adae9301f8dbe37316f7789236" id="tgt230" class="tgtSentence">correlation-id</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="1cb251ec0d568de6a929b520c4aed8d1" id="tgt231" class="tgtSentence">Texto</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="dfe31c18486351b9c432bebe29d6902d" id="tgt232" class="tgtSentence">GUID que es común entre el registro del cliente de RMS y el registro del servidor para una solicitud proporcionada.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="687dee56059627a65f0ff294bb224375" id="tgt233" class="tgtSentence">Este valor puede ser útil para ayudar a solucionar problemas del cliente.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="8a91284e061849269f1e225d9d07565d" id="tgt234" class="tgtSentence">cab52088-8925-4371-be34-4b71a3112356</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="c3ef8a4c2cedff1a4883a1317efb026a" id="tgt235" class="tgtSentence">content-id</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="1cb251ec0d568de6a929b520c4aed8d1" id="tgt236" class="tgtSentence">Texto</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="dd369f21803745039f8bff677781ad7d" id="tgt237" class="tgtSentence">GUID, entre llaves, que identifica el contenido protegido (por ejemplo, un documento).</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="651d7ca32856b7e986e7fb687acd4575" id="tgt238" class="tgtSentence">Este campo tiene un valor solo si request-type es AcquireLicense y está en blanco para todos los demás tipos de solicitudes.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="cc6d3e06881a333d8845146c650c7198" id="tgt239" class="tgtSentence">{bb4af47b-cfed-4719-831d-71b98191a4f2}</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="0969b13c79ef7c7fe184856700ef9f72" id="tgt240" class="tgtSentence">owner-email</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="b45cffe084dd3d20d928bee85e7b0f21" id="tgt241" class="tgtSentence">Cadena</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="6a53cc0ce1f0714291594191a937b7f7" id="tgt242" class="tgtSentence">Dirección de correo electrónico del propietario del documento.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="d5ec8a4bd7af1123c82fd7c591995a69" id="tgt243" class="tgtSentence">alice@contoso.com</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="3e6c2bc1e7f7e5e8c450394c747a8e9f" id="tgt244" class="tgtSentence">issuer</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="b45cffe084dd3d20d928bee85e7b0f21" id="tgt245" class="tgtSentence">Cadena</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="23464e55e6acca18a2e02c0281fe7d0c" id="tgt246" class="tgtSentence">Dirección de correo electrónico del emisor del documento.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="5ecfaa04435c6480d9683e1b522d3afc" id="tgt247" class="tgtSentence">alice@contoso.com (o) FederatedEmail.4c1f4d-93bf-00a95fa1e042@contoso.onmicrosoft.com'</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="175e9aa26a4ac89070acf9151c51da1b" id="tgt248" class="tgtSentence">Template-id</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="b45cffe084dd3d20d928bee85e7b0f21" id="tgt249" class="tgtSentence">Cadena</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="3faa3714d667d3ceb4b89663486c5cbc" id="tgt250" class="tgtSentence">Identificador de la plantilla que se usa para proteger el documento.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="018b4ce624d21e5282fd89091e995591" id="tgt251" class="tgtSentence">{6d9371a6-4e2d-4e97-9a38-202233fed26e}</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="9099dc152ffe017ba299615fe00d04f5" id="tgt252" class="tgtSentence">File-name</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="b45cffe084dd3d20d928bee85e7b0f21" id="tgt253" class="tgtSentence">Cadena</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="4c76f189c2d4d54886e515d53b4e2052" id="tgt254" class="tgtSentence">Nombre de archivo del documento que se ha protegido.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="37ca0fcfb823fc4504d9848d8a6e89e0" id="tgt255" class="tgtSentence">TopSecretDocument.docx</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="f30a14e3cc27bc057596d0db3f9eb998" id="tgt256" class="tgtSentence">Date-published</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="5fc732311905cb27e82d67f4f6511f7f" id="tgt257" class="tgtSentence">Fecha</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="682b196208f96dab1e3b9b70c5c6e248" id="tgt258" class="tgtSentence">Fecha en la que se ha protegido el documento.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a2ba20bd3ab052aab51563792a59f836" id="tgt259" class="tgtSentence">2015-10-15T21:37:00</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="5b6328163b6ef0eea4f1ec530019ad5b" id="tgt260" class="tgtSentence">c-info</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="b45cffe084dd3d20d928bee85e7b0f21" id="tgt261" class="tgtSentence">Cadena</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a5c61b3f394e463f7ee6a65e982a4766" id="tgt262" class="tgtSentence">Información acerca de la plataforma del cliente que está realizando la solicitud.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="c0659eccdf72b83cae1a422cfb8bdc0f" id="tgt263" class="tgtSentence">La cadena específica varía, en función de la aplicación (por ejemplo, el sistema operativo o el explorador).</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="0f2eb0df9729384f4580302df40cda2f" id="tgt264" class="tgtSentence">'MSIPC;version=1.0.623.47;AppName=WINWORD.EXE;AppVersion=15.0.4753.1000;AppArch=x86;OSName=Windows;OSVersion=6.1.7601;OSArch=amd64'</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="1cb4a97a2657ad9a1798614c8bef28e8" id="tgt265" class="tgtSentence">c-ip</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="884d9804999fc47a3c2694e49ad2536a" id="tgt266" class="tgtSentence">Address</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="de22b98c0f158684d0bbc9454badfeb2" id="tgt267" class="tgtSentence">Dirección IP del cliente que realiza la solicitud.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="4038d61bb6d2b9a837f87ab3c72c4c16" id="tgt268" class="tgtSentence">64.51.202.144</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
            <sections>
              <section>
                <title>
                  <caps:sentence sentenceid="3cb8dedc51daba8e4a2db1ce25397d8a" id="tgt269" class="tgtSentence">Excepciones para el campo user-id</caps:sentence>
                </title>
                <content>
                  <para>
                    <caps:sentence sentenceid="d8868e646ee8ab5943c7bec6fd05dc61" id="tgt270" class="tgtSentence">Aunque el campo user-id suele indicar el usuario que hay realizado la solicitud, hay dos excepciones en las que el valor no se asigna a un usuario real:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="a90451b935b3f17704f7d0ca1b0b0202" id="tgt271" class="tgtSentence">El valor <ui>'microsoftrmsonline@&lt;YourTenantID&gt;.rms.&lt;region&gt;.aadrm.com'</ui>.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="d386a4c6b3a6428c2b7e40ba69c34c03" id="tgt272" class="tgtSentence">Esto indica que un servicio de Office 365, como Exchange Online o Sharepoint Online, están realizando la solicitud.</caps:sentence>
                        <caps:sentence sentenceid="b2863e10426d2fbb18a1f9f49b76f298" id="tgt273" class="tgtSentence"> En la cadena, <placeholder>&lt;YourTenantID&gt;</placeholder> es el GUID de su inquilino y <placeholder>&lt;region&gt;</placeholder> es la región donde se registra el inquilino.</caps:sentence>
                        <caps:sentence sentenceid="bbe4d580dfb0dad052bf60cc71b5dd48" id="tgt274" class="tgtSentence"> Por ejemplo, <ui>na</ui> representa a Norteamérica, <ui>eu</ui> representa a Europa y <ui>ap</ui> representa a Asia.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="a5d54aa5eab26158b954d81318fdc046" id="tgt275" class="tgtSentence">Si está usando el conector RMS.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="ff8ccbcb09372ec9fdccd9cf5d9db36b" id="tgt276" class="tgtSentence">Las solicitudes de este conector se registran con el nombre de entidad de servicio que RMS genera automáticamente al instalar el conector RMS.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </content>
              </section>
              <section>
                <title>
                  <caps:sentence sentenceid="e5d03ec9c876cea77efaaaa6b8c32957" id="tgt277" class="tgtSentence">Tipos de solicitudes típicas</caps:sentence>
                </title>
                <content>
                  <para>
                    <caps:sentence sentenceid="696555a11237c723e42eb304ff698e39" id="tgt278" class="tgtSentence">Hay muchos tipos de solicitudes de Azure Rights Management, pero en la tabla siguiente se identifican algunos de los tipos que normalmente se usan más.</caps:sentence>
                  </para>
                  <table>
                    <thead>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="334cdaea3eadb364d4d70cdf2c1ba190" id="tgt279" class="tgtSentence">Tipo de solicitud</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt280" class="tgtSentence">Descripción</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </thead>
                    <tbody>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="96378d61537db78d2fcef81d104db1b0" id="tgt281" class="tgtSentence">AcquireLicense</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="fb39ef7d90067cd5a33d07376e4b78fe" id="tgt282" class="tgtSentence">Un cliente solicita desde un equipo basado en Windows una licencia para contenido protegido con RMS.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="63e3a6c5da909ad29bdda18879f82033" id="tgt283" class="tgtSentence">AcquirePreLicense</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="0b997288f6b3696891ca22bf8f1a04bd" id="tgt284" class="tgtSentence">Un cliente, en nombre del usuario, solicita una licencia para contenido protegido con RMS.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="0cd119a21477936392dd8833ff8a0cb0" id="tgt285" class="tgtSentence">AcquireTemplates</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="d21c8ab4a79fdb2819581cd41dac15d1" id="tgt286" class="tgtSentence">Se ha realizado una llamada para adquirir plantillas basadas en identificadores de plantilla. </caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="8b4ab876b775930408161069425da90c" id="tgt287" class="tgtSentence">AcquireTemplateInformation</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="48e43feafa7b101a45b17a2317e34488" id="tgt288" class="tgtSentence">Se ha realizado una llamada para obtener los identificadores de la plantilla del servicio.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="de8b5ce9105c2d038271d81244867b0e" id="tgt289" class="tgtSentence">AddTemplate</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="f00fb2ec9992581d7599908fc1b3aac7" id="tgt290" class="tgtSentence">Se realiza una llamada desde el Portal de Azure clásico para agregar una plantilla.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="925650923c3c094868130f694440ea20" id="tgt291" class="tgtSentence">BECreateEndUserLicenseV1</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="63acce0fedee037357eccf3a2e2158c4" id="tgt292" class="tgtSentence">Se realiza una llamada desde un dispositivo móvil para crear una licencia de usuario final.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="8897e225dceab3211ccaaea877f2fe54" id="tgt293" class="tgtSentence">BEGetAllTemplatesV1</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="9cbcbf5d61fe10fd9dcd1236efd6bb20" id="tgt294" class="tgtSentence">Se realiza una llamada desde un dispositivo móvil (back-end) para obtener todas las plantillas.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="b3fdd34850de16ddfa25719207b31b1c" id="tgt295" class="tgtSentence">Certify</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="401da8fd74102aafdde063d5b9c5f18f" id="tgt296" class="tgtSentence">El cliente está certificando el contenido para la protección.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="9a2d8ce3ffdcdf2123bddd94d79ef200" id="tgt297" class="tgtSentence">Decrypt</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="b79e84626a4a59644684284b3e47352a" id="tgt298" class="tgtSentence">El cliente está intentando descifrar el contenido protegido con RMS.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="b5d5255406e5df0b5d67f35cd19d9d90" id="tgt299" class="tgtSentence">DeleteTemplateById</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="7dd6302deff16b57ea00f080c80c4463" id="tgt300" class="tgtSentence">Se realiza una llamada desde el Portal de Azure clásico para eliminar una plantilla por identificador de plantilla.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="10b4933ca977180a3654cfaa8374e898" id="tgt301" class="tgtSentence">ExportTemplateById</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="91ab68a7a376ec114368344ed2f9f24c" id="tgt302" class="tgtSentence">Se realiza una llamada desde el Portal de Azure clásico para exportar una plantilla en función de un identificador de plantilla.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="957732255564a6c083ed77bbe2a48e55" id="tgt303" class="tgtSentence">FECreateEndUserLicenseV1</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="51c0c6ce7eb790bd55c39d3bbff5e9bd" id="tgt304" class="tgtSentence">Similar a la solicitud AcquireLicense pero desde dispositivos móviles.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="9fe26a3667ed1dc4b922544eff399527" id="tgt305" class="tgtSentence">FECreatePublishingLicenseV1</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="671360ade676ffa6abe865349bd4222a" id="tgt306" class="tgtSentence">Lo mismo que Certify y GetClientLicensorCert combinados, desde clientes móviles.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="be170906f7b85bf209878794503fb88c" id="tgt307" class="tgtSentence">FEGetAllTemplates</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="43d902653c9f38fa6598321b065fa1df" id="tgt308" class="tgtSentence">Se realiza una llamada desde un dispositivo móvil (front-end) para obtener las plantillas.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="bf96a4a7636509cbd02714a73edecddf" id="tgt309" class="tgtSentence">GetAllTemplates</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="5d117e62fc32890c49d4715d1126e7bc" id="tgt310" class="tgtSentence">Se realiza una llamada desde el Portal de Azure clásico para obtener todas las plantillas.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="9fb6765eeb3de2bbfaa48da6ac7e0bf5" id="tgt311" class="tgtSentence">GetClientLicensorCert</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="902a53f30cbf49cdf2627022aff6527f" id="tgt312" class="tgtSentence">El cliente está solicitando un certificado de publicación (que se utiliza posteriormente para proteger contenido) desde un equipo con Windows.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="4768e58106d46c69889899d955503a8a" id="tgt313" class="tgtSentence">GetConfiguration</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="96ca6781e326059494e6fcad6df6e618" id="tgt314" class="tgtSentence">Se llama a un cmdlet de Azure PowerShell para obtener la configuración del inquilino de Azure RMS.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="7475941ce4f57a82c2c16e9925a9c51a" id="tgt315" class="tgtSentence">GetConnectorAuthorizations</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="f01baea35f04cd2df044d27eaf78f450" id="tgt316" class="tgtSentence">Se realiza una llamada desde los conectores de RMS para obtener su configuración de la nube.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="7aead87288df2a51989244d9e87138d0" id="tgt317" class="tgtSentence">GetTenantFunctionalState </caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="e0847c988251dae1f4ad6b172ba0cbfd" id="tgt318" class="tgtSentence">El Portal de Azure clásico está comprobando si Azure RMS está activado.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="41a4dee8038bd0dff81e166a178c30ff" id="tgt319" class="tgtSentence">GetTemplateById</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="6bf9a128910b55589e4e9a162bbb73cf" id="tgt320" class="tgtSentence">Se realiza una llamada desde el Portal de Azure clásico para obtener una plantilla especificando un identificador de plantilla.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="10b4933ca977180a3654cfaa8374e898" id="tgt321" class="tgtSentence">ExportTemplateById</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="ef804f168a0cc9dccbe9e8db14a72f02" id="tgt322" class="tgtSentence">Se está realizando una llamada desde el Portal de Azure clásico para exportar una plantilla especificando un identificador de plantilla.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="334f66ab7bb1e6a257d5b4b798606d5f" id="tgt323" class="tgtSentence">FindServiceLocationsForUser</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="e63ebce2b3e3fe64f60d3175d6c756f5" id="tgt324" class="tgtSentence">Se realiza una llamada para consultar las direcciones URL, que se usan para llamar a Certify o AcquireLicense.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="24a443c03a3cec36d18a742fed7edeed" id="tgt325" class="tgtSentence">ImportTemplate</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="a3a925e8bdd3e270e5cfb0b2debd5411" id="tgt326" class="tgtSentence">Se realiza una llamada desde el Portal de Azure clásico para importar una plantilla.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="6dc5fa8f8186ca3219fd19e3dbdefecd" id="tgt327" class="tgtSentence">ServerCertify</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="7cecacb069ed0aded29d3e084396a308" id="tgt328" class="tgtSentence">Se realiza una llamada desde un cliente habilitado para RMS (como SharePoint) para certificar el servidor.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="6c632e47271c0bce1acf3e0ae085b5d8" id="tgt329" class="tgtSentence">SetUsageLogFeatureState</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="906f70ea4316763bdcc21a476bd64af4" id="tgt330" class="tgtSentence">Se realiza una llamada para habilitar el registro de uso.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="d7fa965c06a6254a5830dfb4a49e94f3" id="tgt331" class="tgtSentence">SetUsageLogStorageAccount </caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="780ca9388c7f1ceda013318b6e8fc891" id="tgt332" class="tgtSentence">Se realiza una llamada para especificar la ubicación de los registros de Azure RMS.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="4dfcdfef6c8e3bfaa444be440fb8f8cd" id="tgt333" class="tgtSentence">SignDigest</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="d79b10a3cd770c53259b85e8dd936666" id="tgt334" class="tgtSentence">Se realiza una llamada cuando se usa una clave con la intención de firmar.</caps:sentence>
                            <caps:sentence sentenceid="49fb4a3b71498837be6e2fe05df14cc7" id="tgt335" class="tgtSentence"> Suele llamarse una vez por cada elemento AcquireLicence (o FECreateEndUserLicenseV1), Certify y GetClientLicensorCert (o FECreatePublishingLicenseV1).</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="7ef2e38a51e898044929dcdf8b795ef6" id="tgt336" class="tgtSentence">UpdateTemplate</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="c92d05b92ffb57612e4720ccd6725229" id="tgt337" class="tgtSentence">Se realiza una llamada desde el Portal de Azure clásico para actualizar una plantilla existente.</caps:sentence>
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
      <section address="BKMK_PowerShell">
        <title>
          <caps:sentence sentenceid="c66e6fd3bb5af5f69c506be526e0dc22" id="tgt338" class="tgtSentence">Referencia de Windows PowerShell</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="73dbf3a08a2c5d59edca127ae1b6ef38" id="tgt339" class="tgtSentence">Use los siguientes cmdlets de Windows PowerShell como ayuda para configurar y usar el registro de uso de Azure Rights Management:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <externalLink>
                  <linkText>
                    <caps:sentence sentenceid="d0dc480c108ffb261a38cd1e05486b0a" id="tgt340" class="tgtSentence">Disable-AadrmUsageLogFeature</caps:sentence>
                  </linkText>
                  <linkUri>https://msdn.microsoft.com/library/azure/dn629404.aspx</linkUri>
                </externalLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <externalLink>
                  <linkText>
                    <caps:sentence sentenceid="f704ebefdaf11d1921d30b5ff10db15f" id="tgt341" class="tgtSentence">Enable-AadrmUsageLogFeature</caps:sentence>
                  </linkText>
                  <linkUri>https://msdn.microsoft.com/library/azure/dn629421.aspx</linkUri>
                </externalLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <externalLink>
                  <linkText>
                    <caps:sentence sentenceid="5a8eb9f853ac69882dfa45452cf339bb" id="tgt342" class="tgtSentence">Get-AadrmUsageLog</caps:sentence>
                  </linkText>
                  <linkUri>https://msdn.microsoft.com/library/azure/dn629401.aspx</linkUri>
                </externalLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <externalLink>
                  <linkText>
                    <caps:sentence sentenceid="4d76b38660f9d40beabed289b8475c97" id="tgt343" class="tgtSentence">Get-AadrmUsageLogFeature</caps:sentence>
                  </linkText>
                  <linkUri>https://msdn.microsoft.com/library/azure/dn629425.aspx</linkUri>
                </externalLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <externalLink>
                  <linkText>
                    <caps:sentence sentenceid="ac9424114a8cf868df88962200a8e66d" id="tgt344" class="tgtSentence">Get-AadrmUsageLogLastCounterValue</caps:sentence>
                  </linkText>
                  <linkUri>https://msdn.microsoft.com/library/azure/dn629423.aspx</linkUri>
                </externalLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <externalLink>
                  <linkText>
                    <caps:sentence sentenceid="5f42906261cc1ff100bce385571754cb" id="tgt345" class="tgtSentence">Get-AadrmUsageLogStorageAccount</caps:sentence>
                  </linkText>
                  <linkUri>https://msdn.microsoft.com/library/azure/dn629419.aspx</linkUri>
                </externalLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <externalLink>
                  <linkText>
                    <caps:sentence sentenceid="da1309c8f2b2998e31604fcd9fc38101" id="tgt346" class="tgtSentence">Set-AadrmUsageLogStorageAccount</caps:sentence>
                  </linkText>
                  <linkUri>https://msdn.microsoft.com/library/azure/dn629426.aspx</linkUri>
                </externalLink>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="e8b6acb467056e86fbf9c8f9d7f38a97" id="tgt347" class="tgtSentence">Para obtener más información sobre el uso de Windows PowerShell para Azure Rights Management, consulte <link xlink:href="a890e04a-4b70-41b5-8d5f-3c210a669faa">Administering Azure Rights Management by Using Windows PowerShell</link>.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="18564e4a-9364-4ed2-8f17-89d24fc0d878">Using rights management</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Use the information in this topic to help you understand how you can use usage logging with Azure Rights Management (Azure RMS).</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> The Azure Rights Management service can log every request that it makes for your organization, which includes requests from users, actions performed by Rights Management administrators in your organization, and actions performed by Microsoft operators to support your Azure Rights Management deployment.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src3" class="srcSentence">You can then use these Azure Rights Management logs to support the following business scenarios:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src4" class="srcSentence">Analyze for business insights.</caps:sentence>
            </para>
            <para>
              <caps:sentence id="src5" class="srcSentence">Azure Rights Management writes logs in W3C extended log format into an Azure storage account that you provide.</caps:sentence>
              <caps:sentence id="src6" class="srcSentence"> You can then direct these logs into a repository of your choice (such as a database, an online analytical processing (OLAP) system, or a map-reduce system) to analyze the information and produce reports.</caps:sentence>
              <caps:sentence id="src7" class="srcSentence"> As an example, you could identify who is accessing your RMS-protected data.</caps:sentence>
              <caps:sentence id="src8" class="srcSentence"> You can determine what RMS-protected data people are accessing, and from what devices and from where.</caps:sentence>
              <caps:sentence id="src9" class="srcSentence"> You can find out whether people can successfully read protected content.</caps:sentence>
              <caps:sentence id="src10" class="srcSentence"> You can also identify which people have read an important document that was protected.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src11" class="srcSentence">Monitor for abuse.</caps:sentence>
            </para>
            <para>
              <caps:sentence id="src12" class="srcSentence">Azure Rights Management logging information is available to you in near-real time, so that you can continuously monitor your company’s use of Rights Management .</caps:sentence>
              <caps:sentence id="src13" class="srcSentence"> 99.9% of logs are available within 15 minutes of an RMS-initiated action.</caps:sentence>
            </para>
            <para>
              <caps:sentence id="src14" class="srcSentence">For example, you might want to be alerted if there is a sudden increase of people reading RMS-protected data outside standard working hours, which could indicate that a malicious user is collecting information to sell to competitors.</caps:sentence>
              <caps:sentence id="src15" class="srcSentence"> Or, if the same user apparently accesses data from two different IP addresses within a short time frame, which could indicate that a user account has been compromised.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src16" class="srcSentence">Perform forensic analysis.</caps:sentence>
            </para>
            <para>
              <caps:sentence id="src17" class="srcSentence">If you have an information leak, you are likely to be asked who recently accessed specific documents and what information did a suspected person access recently.</caps:sentence>
              <caps:sentence id="src18" class="srcSentence"> You can answer these type of questions when you use Azure Rights Management and logging because people who use protected content must always get a Rights Management license to open documents and pictures that are protected by Azure Rights Management, even if these files are moved by email or copied to USB drives or other storage devices.</caps:sentence>
              <caps:sentence id="src19" class="srcSentence"> This means that you can use Azure Rights Management logs as a definitive source of information for forensic analysis when you protect your data by using Azure Rights Management.</caps:sentence>
            </para>
          </listItem>
        </list>
        <alert class="note">
          <para>
            <caps:sentence id="src20" class="srcSentence">If you are interested only in the logging of administrative tasks for Azure Rights Management, and do not want to track how users are using Rights Management, you can use the <externalLink><linkText>Get-AadrmAdminLog</linkText><linkUri>https://msdn.microsoft.com/library/azure/dn629430.aspx</linkUri></externalLink> Windows PowerShell cmdlet for Azure Rights Management.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src21" class="srcSentence">You can also use the Azure classic portal for high-level usage reports that include <ui>RMS usage</ui>, <ui>Most active RMS users</ui>, <ui>RMS device usage</ui>, and <ui>RMS enabled application usage</ui>.</caps:sentence>
            <caps:sentence id="src22" class="srcSentence"> To access these reports from the Azure classic portal, click <ui>Active Directory</ui>, select and open a directory, and then click <ui>REPORTS</ui>,</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence id="src23" class="srcSentence">Use the following sections for more information about Azure Rights Management usage logging.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <link xlink:href="a735f3f7-6eb2-4901-9084-8c3cd3a9087e#BKMK_EnableRMSLogging">How to enable RMS logging</link>
            </para>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="a735f3f7-6eb2-4901-9084-8c3cd3a9087e#BKMK_AccesAndUseLogs">How to access and use your RMS logs</link>
            </para>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="a735f3f7-6eb2-4901-9084-8c3cd3a9087e#BKMK_ManageStorage">How to manage your RMS log storage</link>
            </para>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="a735f3f7-6eb2-4901-9084-8c3cd3a9087e#BKMK_Delegate">How to delegate access to your RMS logs</link>
            </para>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="a735f3f7-6eb2-4901-9084-8c3cd3a9087e#BKMK_Interpret">How to interpret your RMS logs</link>
            </para>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="a735f3f7-6eb2-4901-9084-8c3cd3a9087e#BKMK_PowerShell">Windows PowerShell reference</link>
            </para>
          </listItem>
        </list>
      </introduction>
      <section address="BKMK_EnableRMSLogging">
        <title>
          <caps:sentence id="src24" class="srcSentence">How to enable Azure Rights Management usage logging</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src25" class="srcSentence">Azure Rights Management usage logging is optional, so if you want to use it, you must take specific steps.</caps:sentence>
            <caps:sentence id="src26" class="srcSentence"> When you use Azure Rights Management usage logging, there is no change in how  Rights Management works and the logging process itself is free.</caps:sentence>
            <caps:sentence id="src27" class="srcSentence"> However, you must provide an Azure storage account for the logs and you will be charged for this storage.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src28" class="srcSentence">Before you begin, make sure that you meet the following prerequisites to use Azure Rights Management usage logging:</caps:sentence>
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
                    <caps:sentence id="src31" class="srcSentence">An IT-managed subscription that includes Azure Rights Management</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src32" class="srcSentence">You must have a Microsoft Azure Rights Management subscription that is managed by your organization.</caps:sentence>
                    <caps:sentence id="src33" class="srcSentence"> Organizations that use RMS for individuals cannot use Azure Rights Management usage logging.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src34" class="srcSentence">If your organization has users who use RMS for individuals, Azure Rights Management usage logging provides a very compelling business reason to convert RMS for individuals into a Microsoft Azure Rights Management subscription.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src35" class="srcSentence">For more information about the subscriptions that include Azure RMS, see the <link xlink:href="dc78321d-d759-4653-8818-80da74b6cdeb#BKMK_SupportedSubscriptions">Cloud subscriptions that support Azure RMS</link> section in the <link xlink:href="dc78321d-d759-4653-8818-80da74b6cdeb">Requirements for Azure Rights Management</link> topic.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src36" class="srcSentence">For more information about RMS for individuals, see <link xlink:href="2efcb440-fefd-45e9-872b-f471573aadf2">RMS for Individuals and Azure Rights Management</link></caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src37" class="srcSentence">Azure subscription</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src38" class="srcSentence">You must have a subscription to Azure and sufficient storage on Azure for your Azure Rights Management logs.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src39" class="srcSentence">Windows PowerShell for Azure Rights Management</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src40" class="srcSentence">If you haven’t already done so, download and install the Windows PowerShell module for Azure Rights Management.</caps:sentence>
                    <caps:sentence id="src41" class="srcSentence"> You will use Windows PowerShell cmdlets to configure and manage your Azure Rights Management usage logs.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src42" class="srcSentence">For more information, see <link xlink:href="0d665ed6-b1de-4d63-854a-bc57c1c49844">Installing Windows PowerShell for Azure Rights Management</link>.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <caps:sentence id="src43" class="srcSentence">Use the following procedure to enable Azure Rights Management usage logging, which includes steps to create an Azure storage account and then configure Azure to use this storage account for your  Rights Management logs.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src44" class="srcSentence">This procedure assumes that you have an Azure account.</caps:sentence>
              <caps:sentence id="src45" class="srcSentence"> Azure Rights Management usage logging supports individual accounts but as a best practice, use work or school accounts.</caps:sentence>
              <caps:sentence id="src46" class="srcSentence"> In addition, we recommend that you create a dedicated storage account for your Rights Management logs.</caps:sentence>
              <caps:sentence id="src47" class="srcSentence"> You must share the storage access keys with Azure Rights Management, and potentially with other people if they will also use the log files.</caps:sentence>
            </para>
            <para>
              <caps:sentence id="src48" class="srcSentence">For more information about Azure storage, see the <externalLink><linkText>Azure documentation for Storage</linkText><linkUri>http://azure.microsoft.com/documentation/services/storage/</linkUri></externalLink>.</caps:sentence>
            </para>
          </alert>
          <procedure>
            <title>
              <caps:sentence id="src49" class="srcSentence">How to create your storage account and enable Azure Rights Management usage logging</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src50" class="srcSentence">Sign in to the <externalLink><linkText>Azure portal</linkText><linkUri>https://portal.azure.com/</linkUri></externalLink>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src51" class="srcSentence">On the Hub menu, select <ui>New</ui> -&gt; <ui>Data + Storage</ui> -&gt; <ui>Storage account</ui>.</caps:sentence>
                  </para>
                  <alert class="tip">
                    <para>
                      <caps:sentence id="src52" class="srcSentence">If you do not see this option, check that you have an Azure subscription in addition to your subscription for Rights Management.</caps:sentence>
                    </para>
                  </alert>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src53" class="srcSentence">Keep the default deployment model of <ui>Classic</ui>, and then click <ui>Create</ui>.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src54" class="srcSentence">Specify the name for your storage account, and if necessary, change the selected options for the <ui>Pricing tier</ui>, <ui>Resource Group</ui>, <ui>Subscription</ui>, and whether to <ui>Pin to dashboard</ui>.</caps:sentence>
                    <caps:sentence id="src55" class="srcSentence"> and then click <ui>CREATE</ui>.</caps:sentence>
                    <caps:sentence id="src56" class="srcSentence"> Wait for the <ui>Creating Storage Account</ui> activity to complete.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src57" class="srcSentence">Click the newly created storage account, and then click <ui>Settings</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src58" class="srcSentence">In the <ui>Settings</ui> blade, click the <ui>Keys</ui> icon.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src59" class="srcSentence">In the <ui>Manage keys</ui> blade, copy the value of the  <ui>PRIMARY ACCESS KEY</ui>  and close the blade.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src60" class="srcSentence">Start Windows PowerShell with the <ui>Run as administrator</ui> option.</caps:sentence>
                    <caps:sentence id="src61" class="srcSentence"> Run the <externalLink><linkText>Connect-AadrmService</linkText><linkUri>https://msdn.microsoft.com/library/azure/dn629415.aspx</linkUri></externalLink> command to connect to the Azure Rights Management service:</caps:sentence>
                  </para>
                  <code>Connect-AadrmService</code>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src62" class="srcSentence">Use the <externalLink><linkText>Set-AadrmUsageLogStorageAccount</linkText><linkUri>https://msdn.microsoft.com/library/azure/dn629426.aspx</linkUri></externalLink> command to specify where you want to keep your Azure Rights Management usage logs, replacing <placeholder>&lt;Access_Key&gt;</placeholder> with the primary access key that you copied in step 6 and <placeholder>&lt;StorageAccount&gt;</placeholder> with the name of the storage account that you created in step 3:</caps:sentence>
                  </para>
                  <code>$accesskey = convertto-securestring -asplaintext -force –string <placeholder xmlns="">&lt;Access_Key&gt;</placeholder> Set-AadrmUsageLogStorageAccount -AccessKey $accesskey -StorageAccount <placeholder xmlns="">&lt;StorageAccount&gt;</placeholder></code>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src63" class="srcSentence">Use the <externalLink><linkText>Enable-AadrmUsageLogFeature</linkText><linkUri>https://msdn.microsoft.com/library/azure/dn629421.aspx</linkUri></externalLink> command to enable Azure Rights Management usage logging:</caps:sentence>
                  </para>
                  <code>Enable-AadrmUsageLogFeature</code>
                  <para>
                    <caps:sentence id="src64" class="srcSentence">You should see the message: <ui>The usage log feature is enabled for the Rights management service.</ui></caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence id="src65" class="srcSentence">Now that usage logging is enabled, Azure Rights Management starts to log all actions for your organization and saves this information to your storage account.</caps:sentence>
                  <caps:sentence id="src66" class="srcSentence"> Logging information is not available before this point.</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src67" class="srcSentence">For more information about how to create storage accounts, see the  <externalLink><linkText>Create a storage account</linkText><linkUri>https://azure.microsoft.com/documentation/articles/storage-create-storage-account/#create-a-storage-account</linkUri></externalLink> section from the <externalLink><linkText>About Azure storage accounts</linkText><linkUri>https://azure.microsoft.com/documentation/articles/storage-create-storage-account/</linkUri></externalLink> in the Azure documentation.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
        </content>
      </section>
      <section address="BKMK_AccesAndUseLogs">
        <title>
          <caps:sentence id="src68" class="srcSentence">How to access and use your Azure Rights Management usage logs</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src69" class="srcSentence">Azure Rights Management writes logs to your Azure storage account as a series of blobs.</caps:sentence>
            <caps:sentence id="src70" class="srcSentence"> Each blob contains one or more log records, in W3C extended log format.</caps:sentence>
            <caps:sentence id="src71" class="srcSentence"> The blob names are numbers, in the order in which they were created.</caps:sentence>
            <caps:sentence id="src72" class="srcSentence"> The <link xlink:href="a735f3f7-6eb2-4901-9084-8c3cd3a9087e#BKMK_Interpret">How to interpret the RMS logs</link> section later in this document contains more information about the log contents and their creation.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src73" class="srcSentence">It can take a while for logs to appear in your storage account after an Azure Rights Management action.</caps:sentence>
            <caps:sentence id="src74" class="srcSentence"> Most logs appear within 15 minutes.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src75" class="srcSentence">The storage account that you created for your Azure Rights Management usage logs is like a mailbox and supports reading directly from the storage account, but it is not optimized to be used in this way.</caps:sentence>
            <caps:sentence id="src76" class="srcSentence"> Instead, for best performance and to help reduce costs, we recommend that you download the logs to local storage, such as a local folder, a database, or a map-reduce repository.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src77" class="srcSentence">You can download your usage logs in two ways:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src78" class="srcSentence">Use the Windows PowerShell cmdlet <externalLink><linkText>Get-AadrmUsageLog</linkText><linkUri>https://msdn.microsoft.com/library/azure/dn629401.aspx</linkUri></externalLink>.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src79" class="srcSentence">This is the simplest way to access your usage logs.</caps:sentence>
                <caps:sentence id="src80" class="srcSentence"> This cmdlet downloads logs to your computer, downloading each blob as a file to a location that you specify.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src81" class="srcSentence">Use the <externalLink><linkText>Azure Storage SDK</linkText><linkUri>http://www.windowsazure.com/en-us/develop/net/</linkUri></externalLink> to write your own custom application to download the logs.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src82" class="srcSentence">A custom application can provide more flexibility than the Get-AadrmUsageLogs cmdlet.</caps:sentence>
                <caps:sentence id="src83" class="srcSentence"> For example, you might want to delegate the download of logs to somebody or a process that must not use your Azure Rights Management administrative credentials.</caps:sentence>
                <caps:sentence id="src84" class="srcSentence"> Or, you might want to poll the logs in real time because you want to monitor for misuse.</caps:sentence>
              </para>
            </listItem>
          </list>
          <procedure>
            <title>
              <caps:sentence id="src85" class="srcSentence">To download your usage logs by using PowerShell</caps:sentence>
            </title>
            <steps class="bullet">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src86" class="srcSentence">Start Windows PowerShell with the <ui>Run as administrator</ui> option and run <userInput>Get-AadrmUsageLog –Path &lt;location&gt;</userInput>.</caps:sentence>
                    <caps:sentence id="src87" class="srcSentence"> For example, after creating a folder named <system>logs</system> on your E drive:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src88" class="srcSentence">To download all available logs to your E:\logs folder: <codeInline>Get-AadrmUsageLog -Path "e:\logs"</codeInline></caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src89" class="srcSentence">To download a specific range of blobs: <codeInline>Get-AadrmUsageLog –Path "e:\logs" –FromCounter 1024 –ToCounter 2047</codeInline></caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence id="src90" class="srcSentence">When you run these cmdlets, Windows PowerShell displays the name of the last blob that was downloaded.</caps:sentence>
                  <caps:sentence id="src91" class="srcSentence"> You can assign this name to a variable, which lets you run Get-AadrmUsageLog in a loop or a schedule job, downloading only the incremental logs each time.</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src92" class="srcSentence">For example:  </caps:sentence>
                </para>
                <para>
                  <ui>
                    <caps:sentence id="src93" class="srcSentence">PS C:\&gt; $LastBlobName = Get-AadrmUsageLog –Path "e:\logs"</caps:sentence>
                  </ui>
                </para>
                <para>
                  <ui>
                    <caps:sentence id="src94" class="srcSentence">1527</caps:sentence>
                  </ui>
                </para>
                <para>
                  <ui>
                    <caps:sentence id="src95" class="srcSentence">PS C:\&gt; $LastBlobName</caps:sentence>
                  </ui>
                </para>
                <para>
                  <ui>
                    <caps:sentence id="src96" class="srcSentence">1527</caps:sentence>
                  </ui>
                </para>
              </content>
            </conclusion>
          </procedure>
          <alert class="tip">
            <para>
              <caps:sentence id="src97" class="srcSentence">You can aggregate all your downloaded log files into a CSV format by using <externalLink><linkText>Microsoft’s Log Parser</linkText><linkUri>http://www.microsoft.com/download/details.aspx?id=24659</linkUri></externalLink>, which is a tool to convert between various well-known log formats.</caps:sentence>
              <caps:sentence id="src98" class="srcSentence"> You can also use this tool to convert data to SYSLOG format, or import it into a database.</caps:sentence>
              <caps:sentence id="src99" class="srcSentence"> After you have installed the tool, run <userInput>LogParser.exe /?</userInput> for help and information to use this tool.</caps:sentence>
              <caps:sentence id="src100" class="srcSentence"> For example, you might run the following command to import all information into a .log file format: <userInput>logparser –i:w3c –o:csv “SELECT * INTO AllLogs.csv FROM *.log”</userInput>.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence id="src101" class="srcSentence">You can suspend and resume usage logging.</caps:sentence>
            <caps:sentence id="src102" class="srcSentence"> When you suspend logging, Azure Rights Management retains your storage account information, so that you can easily resume logging again.</caps:sentence>
          </para>
          <procedure>
            <title>
              <caps:sentence id="src103" class="srcSentence">To suspend and resume usage logging</caps:sentence>
            </title>
            <steps class="bullet">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src104" class="srcSentence">To suspend logging, use the following cmdlet: <externalLink><linkText>Disable-AadrmUsageLogFeature</linkText><linkUri>https://msdn.microsoft.com/library/azure/dn629404.aspx</linkUri></externalLink></caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src105" class="srcSentence">To resume logging, use the following cmdlet: <externalLink><linkText>Enable-AadrmUsageLogFeature</linkText><linkUri>https://msdn.microsoft.com/library/azure/dn629421.aspx</linkUri></externalLink></caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src106" class="srcSentence">To check whether logging is enabled or disabled, use the following cmdlet: <externalLink><linkText>Get-AadrmUsageLogFeature</linkText><linkUri>https://msdn.microsoft.com/library/azure/dn629425.aspx</linkUri></externalLink></caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src107" class="srcSentence">A value of <ui>True</ui> means that usage logging is enabled for Azure Rights Management and a value of <ui>False</ui> means that usage logging is disabled.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
        </content>
      </section>
      <section address="BKMK_ManageStorage">
        <title>
          <caps:sentence id="src108" class="srcSentence">How to manage your Azure Rights Management log storage</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src109" class="srcSentence">You are charged for the storage space that is used to keep your Azure Rights Management logs.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src110" class="srcSentence">Azure Rights Management does no automatic management of your usage log files.</caps:sentence>
            <caps:sentence id="src111" class="srcSentence"> If you take no action, they will remain in your storage account.</caps:sentence>
            <caps:sentence id="src112" class="srcSentence"> However, to conserve space and reduce storage costs, you might want to delete them after you have downloaded them.</caps:sentence>
            <caps:sentence id="src113" class="srcSentence"> Or you can choose which files to delete.</caps:sentence>
            <caps:sentence id="src114" class="srcSentence"> With one exception, Azure Rights Management does not use these log files, so there are no restrictions about when you can delete them.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src115" class="srcSentence">The file that you must not delete (or modify) is named <ui>metadata</ui> that is in the <ui>rms-metadata</ui> container.</caps:sentence>
            <caps:sentence id="src116" class="srcSentence"> Azure Rights Management uses this blob to keep track of the last blob number that it used.</caps:sentence>
            <caps:sentence id="src117" class="srcSentence"> If this file is deleted, Azure Rights Management starts a new container for logs, with a blob number that starts from 1, and all future downloads that use the Get-AadrmUsageLog cmdlet use this new container to download log files.</caps:sentence>
            <caps:sentence id="src118" class="srcSentence"> As a result, any logs in the original container are retained, but orphaned.</caps:sentence>
            <caps:sentence id="src119" class="srcSentence"> The only way to download these orphaned logs is to use the Azure storage SDK.</caps:sentence>
          </para>
          <alert class="tip">
            <para>
              <caps:sentence id="src120" class="srcSentence">Instead of managing your Azure Rights Management log storage yourself, you can delegate this management function to another company by sharing your storage account name and access key.</caps:sentence>
              <caps:sentence id="src121" class="srcSentence"> For more information, see the <link xlink:href="a735f3f7-6eb2-4901-9084-8c3cd3a9087e#BKMK_Delegate">How to delegate access to your RMS logs</link> section later in this topic.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence id="src122" class="srcSentence">In some circumstances, you might want to regenerate your storage access keys.</caps:sentence>
            <caps:sentence id="src123" class="srcSentence"> For example:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src124" class="srcSentence">You change the company that manages your Azure Rights Management usage logs.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src125" class="srcSentence">You suspect that your storage access key is compromised.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src126" class="srcSentence">If this happens to you, this is when you use the secondary access key (on the assumption that you were previously using the primary access key) to ensure service continuity.</caps:sentence>
            <caps:sentence id="src127" class="srcSentence"> When you regenerate the access key that you were not previously using, you then configure Azure Rights Management to use the new key.</caps:sentence>
            <caps:sentence id="src128" class="srcSentence"> Use the following procedure to regenerate the secondary access key and configure Azure Rights Management to use it:</caps:sentence>
          </para>
          <procedure>
            <title>
              <caps:sentence id="src129" class="srcSentence">To regenerate the secondary access key</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src130" class="srcSentence">Sign in to the <externalLink><linkText>Azure  portal</linkText><linkUri>https://portal.azure.com/</linkUri></externalLink>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src131" class="srcSentence">Click <ui>All Resources</ui>, and search for your storage by typing the storage name in the text box..</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src132" class="srcSentence">Select your storage, and click <ui>Settings</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src133" class="srcSentence">Click the <ui>Keys</ui> icon.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src134" class="srcSentence">In the <ui>Manage  keys</ui> section, click <ui>Regenerate secondary key</ui> click Yes to confirm that you want to regenerate secondary access key, and copy the new secondary access key to the clipboard.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src135" class="srcSentence">Do not close the Azure portal.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src136" class="srcSentence">Start Windows PowerShell with the <ui>Run as administrator</ui> option and use the <externalLink><linkText>Set-AadrmUsageLogStorageAccount</linkText><linkUri>https://msdn.microsoft.com/library/azure/dn629426.aspx</linkUri></externalLink> cmdlet to configure Azure Rights Management to use this new access key, replacing <placeholder>&lt;StorageAccount&gt;</placeholder> with the name of your storage account and <placeholder>&lt;Access_Key&gt;</placeholder> with the regenerated secondary access key that you just copied:</caps:sentence>
                  </para>
                  <code>Set-AadrmUsageLogStorageAccount -StorageAccount <placeholder xmlns="">&lt;StorageAccount&gt;</placeholder>-AccessKey <placeholder xmlns="">&lt;Access_Key&gt;</placeholder></code>
                  <alert class="warning">
                    <para>
                      <caps:sentence id="src137" class="srcSentence">Although you can switch to another storage account when you run this command, this action orphans your previous logs and they will no longer be accessible to the Set-AadrmUsageLogStorageAccount cmdlet or similar management commands and functions.</caps:sentence>
                    </para>
                  </alert>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src138" class="srcSentence">Back in the Azure portal, <ui>Manage  Keys</ui> section, regenerate your primary access key.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence id="src139" class="srcSentence">For more information about how to manage your storage access keys, see the  <externalLink><linkText>Manage your storage access keys</linkText><linkUri>https://azure.microsoft.com/documentation/articles/storage-create-storage-account/#manage-your-storage-access-keys</linkUri></externalLink> section from the <externalLink><linkText>About Azure storage accounts</linkText><linkUri>https://azure.microsoft.com/documentation/articles/storage-create-storage-account/</linkUri></externalLink> in the Azure documentation.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
        </content>
      </section>
      <section address="BKMK_Delegate">
        <title address="BKMK_DelegateAccess">
          <caps:sentence id="src140" class="srcSentence">How to delegate access to your Azure Rights Management usage logs</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src141" class="srcSentence">You can delegate access to your RMS logs by sharing your storage account name and access key.</caps:sentence>
            <caps:sentence id="src142" class="srcSentence"> You might want to delegate access to another administrative user, to a developer within your own organization, or to an independent software vendor (ISV).</caps:sentence>
            <caps:sentence id="src143" class="srcSentence"> Because they will not have your RMS administrator credentials, they cannot use the Get-AardrmUsageLog cmdlet to download the RMS logs.</caps:sentence>
            <caps:sentence id="src144" class="srcSentence"> Instead, they must use the Windows Storage SDK to download the logs.</caps:sentence>
            <caps:sentence id="src145" class="srcSentence"> Alternatively, they can write an application to read the logs directly from Azure Storage.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src146" class="srcSentence">It is safe to share your storage account name and access key in this way when the storage account is dedicated to your RMS logs.</caps:sentence>
            <caps:sentence id="src147" class="srcSentence"> Even though other people have your access key, they cannot use this to access any other storage account or use your RMS tenant account.</caps:sentence>
          </para>
        </content>
      </section>
      <section address="BKMK_Interpret">
        <title>
          <caps:sentence id="src148" class="srcSentence">How to interpret your Azure Rights Management usage  logs</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src149" class="srcSentence">Use the following information to help you interpret the Azure Rights Management usage  logs.</caps:sentence>
          </para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence id="src150" class="srcSentence">The storage account layout</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src151" class="srcSentence">The first time Azure Rights Management writes logs to your storage account, it creates the following two containers:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src152" class="srcSentence">
                      <ui>Rms-metadata</ui>: This container is reserved for Azure Rights Management .</caps:sentence>
                    <caps:sentence id="src153" class="srcSentence"> Do not modify or delete this container.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src154" class="srcSentence">
                      <ui>Rms-logs-&lt;guid&gt;</ui>: This container is where Azure Rights Management creates and saves the logs.</caps:sentence>
                    <caps:sentence id="src155" class="srcSentence"> You can safely delete any files in this container if you no longer want the logging information that they contain.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src156" class="srcSentence">Over time, Azure Rights Management might create additional <ui>Rms-logs-&lt;guid&gt;</ui> containers.</caps:sentence>
                <caps:sentence id="src157" class="srcSentence"> For example, if the <ui>Rms-metadata</ui> container becomes corrupted or it is accidentally deleted, Azure Rights Management resets its contents and creates a new <ui>Rms-logs-&lt;guid&gt;</ui> container for all future logs.</caps:sentence>
                <caps:sentence id="src158" class="srcSentence"> The old logs in the old container are not deleted but are orphaned.</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src159" class="srcSentence">The log sequence</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src160" class="srcSentence">Azure Rights Management writes the logs as a series of blobs.</caps:sentence>
                <caps:sentence id="src161" class="srcSentence"> Each blob contains one or more log records, in extended W3C log format.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src162" class="srcSentence">The name of each blob is a number.</caps:sentence>
                <caps:sentence id="src163" class="srcSentence"> Within each log container the first blob is named 000000001.</caps:sentence>
                <caps:sentence id="src164" class="srcSentence"> Each blob is named sequentially in the order in which it was created.</caps:sentence>
                <caps:sentence id="src165" class="srcSentence"> Each blob contains one or more log records.</caps:sentence>
                <caps:sentence id="src166" class="srcSentence"> Each log record has a UTC time stamp that indicates when the corresponding request was served by Azure Rights Management.</caps:sentence>
              </para>
              <alert class="important">
                <para>
                  <caps:sentence id="src167" class="srcSentence">The Azure Rights Management logging system is optimized to provide you with logs quickly, rather than in strict sequential order.</caps:sentence>
                  <caps:sentence id="src168" class="srcSentence"> The order of the blobs, as well as the order of log records within a blob, might be out of chronological sequence.</caps:sentence>
                  <caps:sentence id="src169" class="srcSentence"> The only reason the blobs are named sequentially is to enable you to efficiently download them incrementally.</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src170" class="srcSentence">Two examples of potential log sequence results:</caps:sentence>
                </para>
                <list class="bullet">
                  <listItem>
                    <para>
                      <caps:sentence id="src171" class="srcSentence">The log records in blob 000000004 might overlap chronologically with the log records in blob 000000003.</caps:sentence>
                      <caps:sentence id="src172" class="srcSentence"> In an extreme case, all log records in blob 000000004 might have been generated before all log records in blob 000000003.</caps:sentence>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <caps:sentence id="src173" class="srcSentence">The second log record in a blob might have been generated before the first log record, but was written to storage in reverse order.</caps:sentence>
                    </para>
                  </listItem>
                </list>
              </alert>
              <para>
                <caps:sentence id="src174" class="srcSentence">Before you analyze your Azure Rights Management usage logs, we recommend that you download and import the log into a repository where you can sort the logs based on their timestamp.</caps:sentence>
                <caps:sentence id="src175" class="srcSentence"> For more information about to download the logs, see the <link xlink:href="a735f3f7-6eb2-4901-9084-8c3cd3a9087e#BKMK_AccesAndUseLogs">How to access and use your RMS logs</link> section in this topic.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src176" class="srcSentence">Because the logs are not necessarily chronological but the majority of them are written within 15 minutes of the request, when you identify the logs that you want by using their timestamp , add 15 minutes to the time that you are interested in.</caps:sentence>
                <caps:sentence id="src177" class="srcSentence"> Then download these logs.</caps:sentence>
                <caps:sentence id="src178" class="srcSentence"> This strategy should ensure that you get almost all logs.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src179" class="srcSentence">One other thing to remember is that the timestamp on each log record is the local time of the Azure Rights Management service that processed the request.</caps:sentence>
                <caps:sentence id="src180" class="srcSentence"> Because Azure Rights Management runs on multiple servers across multiple data center, sometimes the logs might seem to be out of sequence, even when they are sorted by their timestamp.</caps:sentence>
                <caps:sentence id="src181" class="srcSentence"> However, the different is small and usually within a minute.</caps:sentence>
                <caps:sentence id="src182" class="srcSentence"> In most cases, this is not an issue that would be a problem for log analysis.</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src183" class="srcSentence">The blob format</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src184" class="srcSentence">Each blob is in W3C extended log format.</caps:sentence>
                <caps:sentence id="src185" class="srcSentence"> It starts with the following two lines:</caps:sentence>
              </para>
              <para>
                <ui>
                  <caps:sentence id="src186" class="srcSentence">#Software: RMS</caps:sentence>
                </ui>
              </para>
              <para>
                <ui>
                  <caps:sentence id="src187" class="srcSentence">#Version: 1.1</caps:sentence>
                </ui>
              </para>
              <para>
                <caps:sentence id="src188" class="srcSentence">The first line identifies that these are Azure Rights Management logs.</caps:sentence>
                <caps:sentence id="src189" class="srcSentence"> The second line identifies that the rest of the blob follows the version 1.1 specification.</caps:sentence>
                <caps:sentence id="src190" class="srcSentence"> We recommend that any applications that parse these logs verify these two lines before continuing to parse the rest of the blob.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src191" class="srcSentence">The third line enumerates a list of field names that are separated by tabs:</caps:sentence>
              </para>
              <para>
                <ui>
                  <caps:sentence id="src192" class="srcSentence">#Fields: date            time            row-id        request-type           user-id       result          correlation-id          content-id                owner-email           issuer                     template-id             file-name                  date-published      c-info         c-ip</caps:sentence>
                </ui>
              </para>
              <para>
                <caps:sentence id="src193" class="srcSentence">Each of the subsequent lines is a log record.</caps:sentence>
                <caps:sentence id="src194" class="srcSentence"> The values of the fields are in the same order as the preceding line, and are separated by tabs.</caps:sentence>
                <caps:sentence id="src195" class="srcSentence"> Use the following table to interpret the fields.</caps:sentence>
              </para>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src196" class="srcSentence">Field name</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src197" class="srcSentence">W3C data type</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src198" class="srcSentence">Description</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src199" class="srcSentence">Example value</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src200" class="srcSentence">date</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src201" class="srcSentence">Date</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src202" class="srcSentence">UTC date when the request was served.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src203" class="srcSentence">The source is the local clock on the server that served the request.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src204" class="srcSentence">2013-06-25</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src205" class="srcSentence">time</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src206" class="srcSentence">Time</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src207" class="srcSentence">UTC time in 24-hour format when the request was served.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src208" class="srcSentence">The source is the local clock on the server that served the request.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src209" class="srcSentence">21:59:28</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src210" class="srcSentence">row-id</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src211" class="srcSentence">Text</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src212" class="srcSentence">Unique GUID for this log record.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src213" class="srcSentence">This value is useful when you aggregate logs or copy logs into another format.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src214" class="srcSentence">1c3fe7a9-d9e0-4654-97b7-14fafa72ea63</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src215" class="srcSentence">request-type</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src216" class="srcSentence">Name</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src217" class="srcSentence">Name of the RMS API that was requested.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src218" class="srcSentence">AcquireLicense</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src219" class="srcSentence">user-id</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src220" class="srcSentence">String</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src221" class="srcSentence">The user who made the request.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src222" class="srcSentence">The value is enclosed in single quotation marks.</caps:sentence>
                        <caps:sentence id="src223" class="srcSentence"> Some request types are anonymous, in which case the value is ”.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src224" class="srcSentence">‘joe@contoso.com’</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src225" class="srcSentence">result</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src226" class="srcSentence">String</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src227" class="srcSentence">‘Success’ if the request was served successful.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src228" class="srcSentence">The error type in single quotation marks if the request failed.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src229" class="srcSentence">‘Success’</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src230" class="srcSentence">correlation-id</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src231" class="srcSentence">Text</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src232" class="srcSentence">GUID that is common between the RMS client log and server log for a given request.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src233" class="srcSentence">This value can be useful to help troubleshooting client issues.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src234" class="srcSentence">cab52088-8925-4371-be34-4b71a3112356</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src235" class="srcSentence">content-id</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src236" class="srcSentence">Text</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src237" class="srcSentence">GUID, enclosed in curly braces that identifies the protected content (for example, a document).</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src238" class="srcSentence">This field has a value only if request-type is AcquireLicense and is blank for all other request types.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src239" class="srcSentence">{bb4af47b-cfed-4719-831d-71b98191a4f2}</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src240" class="srcSentence">owner-email</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src241" class="srcSentence">String</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src242" class="srcSentence">Email address of the owner of the document.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src243" class="srcSentence">alice@contoso.com</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src244" class="srcSentence">issuer</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src245" class="srcSentence">String</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src246" class="srcSentence">Email address of the document issuer.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src247" class="srcSentence">alice@contoso.com (or) FederatedEmail.4c1f4d-93bf-00a95fa1e042@contoso.onmicrosoft.com'</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src248" class="srcSentence">Template-id</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src249" class="srcSentence">String</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src250" class="srcSentence">ID of the template used to protect the document.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src251" class="srcSentence">{6d9371a6-4e2d-4e97-9a38-202233fed26e}</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src252" class="srcSentence">File-name</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src253" class="srcSentence">String</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src254" class="srcSentence">File name of the document that was protected.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src255" class="srcSentence">TopSecretDocument.docx</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src256" class="srcSentence">Date-published</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src257" class="srcSentence">Date</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src258" class="srcSentence">Date when the document was protected.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src259" class="srcSentence">2015-10-15T21:37:00</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src260" class="srcSentence">c-info</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src261" class="srcSentence">String</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src262" class="srcSentence">Information about the client platform that is making the request.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src263" class="srcSentence">The specific string varies, depending on the application (for example, the operating system or the browser).</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src264" class="srcSentence">'MSIPC;version=1.0.623.47;AppName=WINWORD.EXE;AppVersion=15.0.4753.1000;AppArch=x86;OSName=Windows;OSVersion=6.1.7601;OSArch=amd64'</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src265" class="srcSentence">c-ip</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src266" class="srcSentence">Address</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src267" class="srcSentence">IP address of the client that makes the request.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src268" class="srcSentence">64.51.202.144</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
            <sections>
              <section>
                <title>
                  <caps:sentence id="src269" class="srcSentence">Exceptions for the user-id field</caps:sentence>
                </title>
                <content>
                  <para>
                    <caps:sentence id="src270" class="srcSentence">Although the user-id field usually indicates the user who made the request, there are two exceptions where the value does not map to a real user:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src271" class="srcSentence">The value <ui>'microsoftrmsonline@&lt;YourTenantID&gt;.rms.&lt;region&gt;.aadrm.com'</ui>.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src272" class="srcSentence">This indicates an Office 365 service, such as Exchange Online or Sharepoint Online, is making the request.</caps:sentence>
                        <caps:sentence id="src273" class="srcSentence"> In the string, <placeholder>&lt;YourTenantID&gt;</placeholder> is the GUID for your tenant and <placeholder>&lt;region&gt;</placeholder> is the region where your tenant is registered.</caps:sentence>
                        <caps:sentence id="src274" class="srcSentence"> For example, <ui>na</ui> represents North America, <ui>eu</ui> represents Europe, and <ui>ap</ui> represents Asia.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src275" class="srcSentence">If you are using the RMS connector.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src276" class="srcSentence">Requests from this connector are logged with the service principal name that RMS automatically generates when you install the RMS connector.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </content>
              </section>
              <section>
                <title>
                  <caps:sentence id="src277" class="srcSentence">Typical request types</caps:sentence>
                </title>
                <content>
                  <para>
                    <caps:sentence id="src278" class="srcSentence">There are many request types for Azure Rights Management but the following table identifies some of the most typically used request types.</caps:sentence>
                  </para>
                  <table>
                    <thead>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src279" class="srcSentence">Request type</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src280" class="srcSentence">Description</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </thead>
                    <tbody>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src281" class="srcSentence">AcquireLicense</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src282" class="srcSentence">A client from a Windows based machine is requesting a license for RMS-protected content.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src283" class="srcSentence">AcquirePreLicense</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src284" class="srcSentence">A client, on behalf of the user, is requesting for a license for RMS-protected content.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src285" class="srcSentence">AcquireTemplates</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src286" class="srcSentence">A call was made to acquires templates based on template IDs </caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src287" class="srcSentence">AcquireTemplateInformation</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src288" class="srcSentence">A call was made to get the IDs of the template from the service.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src289" class="srcSentence">AddTemplate</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src290" class="srcSentence">A call is  made from the Azure classic portal to add a template.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src291" class="srcSentence">BECreateEndUserLicenseV1</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src292" class="srcSentence">A call is  made from a mobile device to create an end-user license.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src293" class="srcSentence">BEGetAllTemplatesV1</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src294" class="srcSentence">A call is  made from a mobile device (back-end) to get all the templates.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src295" class="srcSentence">Certify</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src296" class="srcSentence">The client is certifying the content for protection.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src297" class="srcSentence">Decrypt</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src298" class="srcSentence">The client is attempting to decrypt the RMS-protected content.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src299" class="srcSentence">DeleteTemplateById</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src300" class="srcSentence">A call is  made from the Azure classic portal, to delete a template by template  ID.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src301" class="srcSentence">ExportTemplateById</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src302" class="srcSentence">A call is  made from the Azure classic portal to export a template based on a template ID.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src303" class="srcSentence">FECreateEndUserLicenseV1</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src304" class="srcSentence">Similar to the AcquireLicense request but from mobile devices.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src305" class="srcSentence">FECreatePublishingLicenseV1</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src306" class="srcSentence">The same as Certify and GetClientLicensorCert combined, from mobile clients.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src307" class="srcSentence">FEGetAllTemplates</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src308" class="srcSentence">A call is  made, from a mobile device (front-end) to get the templates.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src309" class="srcSentence">GetAllTemplates</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src310" class="srcSentence">A call is  made from the Azure classic portal, to get all the templates.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src311" class="srcSentence">GetClientLicensorCert</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src312" class="srcSentence">The client is requesting a publishing certificate (that is later used to protect content) from a Windows-based computer.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src313" class="srcSentence">GetConfiguration</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src314" class="srcSentence">An Azure PowerShell cmdlet is called to get the configuration of the Azure RMS tenant.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src315" class="srcSentence">GetConnectorAuthorizations</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src316" class="srcSentence">A call  is made from the RMS connectors to get their configuration from the cloud.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src317" class="srcSentence">GetTenantFunctionalState </caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src318" class="srcSentence">The Azure classic portal is checking whether Azure RMS is activated.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src319" class="srcSentence">GetTemplateById</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src320" class="srcSentence">A call is  made from the Azure classic portal to get a template by specifying a template ID.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src321" class="srcSentence">ExportTemplateById</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src322" class="srcSentence">A call is being made from the Azure classic portal to export a template by specifying a template ID.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src323" class="srcSentence">FindServiceLocationsForUser</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src324" class="srcSentence">A call is made to query for URLs, which is used to call Certify or AcquireLicense.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src325" class="srcSentence">ImportTemplate</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src326" class="srcSentence">A call is  made from the Azure classic portal to import a template.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src327" class="srcSentence">ServerCertify</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src328" class="srcSentence">A call is  made from an RMS-enabled client (such as SharePoint) to certify the server.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src329" class="srcSentence">SetUsageLogFeatureState</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src330" class="srcSentence">A call is  made to enable usage logging.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src331" class="srcSentence">SetUsageLogStorageAccount </caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src332" class="srcSentence">A call is  made to specify the location of the Azure RMS logs.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src333" class="srcSentence">SignDigest</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src334" class="srcSentence">A call is made when a key is used for signing purposes.</caps:sentence>
                            <caps:sentence id="src335" class="srcSentence"> This is called typically once per AcquireLicence (or FECreateEndUserLicenseV1), Certify, and GetClientLicensorCert (or FECreatePublishingLicenseV1).</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src336" class="srcSentence">UpdateTemplate</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src337" class="srcSentence">A call is  made from the Azure classic portal to update an existing template.</caps:sentence>
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
      <section address="BKMK_PowerShell">
        <title>
          <caps:sentence id="src338" class="srcSentence">Windows PowerShell reference</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src339" class="srcSentence">Use the following Windows PowerShell cmdlets to help you configure and use Azure Rights Management usage logging:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <externalLink>
                  <linkText>
                    <caps:sentence id="src340" class="srcSentence">Disable-AadrmUsageLogFeature</caps:sentence>
                  </linkText>
                  <linkUri>https://msdn.microsoft.com/library/azure/dn629404.aspx</linkUri>
                </externalLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <externalLink>
                  <linkText>
                    <caps:sentence id="src341" class="srcSentence">Enable-AadrmUsageLogFeature</caps:sentence>
                  </linkText>
                  <linkUri>https://msdn.microsoft.com/library/azure/dn629421.aspx</linkUri>
                </externalLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <externalLink>
                  <linkText>
                    <caps:sentence id="src342" class="srcSentence">Get-AadrmUsageLog</caps:sentence>
                  </linkText>
                  <linkUri>https://msdn.microsoft.com/library/azure/dn629401.aspx</linkUri>
                </externalLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <externalLink>
                  <linkText>
                    <caps:sentence id="src343" class="srcSentence">Get-AadrmUsageLogFeature</caps:sentence>
                  </linkText>
                  <linkUri>https://msdn.microsoft.com/library/azure/dn629425.aspx</linkUri>
                </externalLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <externalLink>
                  <linkText>
                    <caps:sentence id="src344" class="srcSentence">Get-AadrmUsageLogLastCounterValue</caps:sentence>
                  </linkText>
                  <linkUri>https://msdn.microsoft.com/library/azure/dn629423.aspx</linkUri>
                </externalLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <externalLink>
                  <linkText>
                    <caps:sentence id="src345" class="srcSentence">Get-AadrmUsageLogStorageAccount</caps:sentence>
                  </linkText>
                  <linkUri>https://msdn.microsoft.com/library/azure/dn629419.aspx</linkUri>
                </externalLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <externalLink>
                  <linkText>
                    <caps:sentence id="src346" class="srcSentence">Set-AadrmUsageLogStorageAccount</caps:sentence>
                  </linkText>
                  <linkUri>https://msdn.microsoft.com/library/azure/dn629426.aspx</linkUri>
                </externalLink>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src347" class="srcSentence">For more information about using Windows PowerShell for Azure Rights Management, see <link xlink:href="a890e04a-4b70-41b5-8d5f-3c210a669faa">Administering Azure Rights Management by Using Windows PowerShell</link>.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="18564e4a-9364-4ed2-8f17-89d24fc0d878">Using rights management</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>