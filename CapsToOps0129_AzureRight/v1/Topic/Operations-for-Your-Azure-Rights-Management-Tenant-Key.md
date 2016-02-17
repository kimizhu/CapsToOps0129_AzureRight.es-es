---
title: Operaciones para su clave de inquilino de Administraci&#243;n de permisos de Azure
ms.custom: na
ms.reviewer: na
ms.service: rights-management
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1284d0ee-0a72-45ba-a64c-3dcb25846c3d
---
# Operaciones para su clave de inquilino de Administraci&#243;n de permisos de Azure
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="es-ES">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="cbcc8caf8d0ce4b7178d67e6d9ef567c" id="tgt1" class="tgtSentence">En función de la topología de la clave de inquilino (administrada por Microsoft o por el cliente), tiene diferentes niveles de control y responsabilidad para su clave de inquilino de Microsoft Azure Rights Management (Azure RMS) una vez implementada.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="f89f002101e04d5aa5fbc726e795849c" id="tgt2" class="tgtSentence">Cuando administra su propia clave de inquilino, esto a menudo se denomina aportar tu propia clave (BYOK).</caps:sentence>
          <caps:sentence sentenceid="6408c7e2d30f5bb5920b02f75e85f6e5" id="tgt3" class="tgtSentence"> Para obtener más información acerca de este escenario y acerca de cómo elegir entre las dos topologías clave, vea <link xlink:href="f0d33c5f-a6a6-44a1-bdec-5be1bc8e1e14">Planning and operations for your Azure Rights Management tenant key</link>.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="4552cefa5647b5f7fce757a85eb5eef5" id="tgt4" class="tgtSentence">La tabla siguiente identifica qué operaciones puede realizar en función de la topología que eligió para su clave de inquilino de Azure RMS.</caps:sentence>
        </para>
        <table>
          <thead>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="64205b19f2f155e93788d18c2d3858a6" id="tgt5" class="tgtSentence">Operación del ciclo de vida</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="06ba91f4fac5274dd76b108d3883fc68" id="tgt6" class="tgtSentence">Administrada por Microsoft (predeterminada)</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="bb42b180ba57d0d33beaafa4ec1de882" id="tgt7" class="tgtSentence">Administrada por el cliente (BYOK)</caps:sentence>
                </para>
              </TD>
            </tr>
          </thead>
          <tbody>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="aa4c20163fd7bc47f8e25375406ec6fb" id="tgt8" class="tgtSentence">Revocar su clave de inquilino</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="9f4373a0a79fcadfd300334b48d24a1d" id="tgt9" class="tgtSentence">No automática</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="9f4373a0a79fcadfd300334b48d24a1d" id="tgt10" class="tgtSentence">No automática</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="18d8dd06fcb6d67508b252024996e60a" id="tgt11" class="tgtSentence">Vuelva a introducir su clave de inquilino</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt12" class="tgtSentence">Sí</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt13" class="tgtSentence">Sí</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="4a337e29bf1a6444a43307272bcd878b" id="tgt14" class="tgtSentence">Realizar una copia de seguridad y recuperar la clave de inquilino</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt15" class="tgtSentence">No</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt16" class="tgtSentence">Sí</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="414ca16dc978d6351ef4f8d9618f4305" id="tgt17" class="tgtSentence">Exportar su clave de inquilino</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt18" class="tgtSentence">Sí</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt19" class="tgtSentence">No</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="3f2932f1c2da2de325245973e9e22c43" id="tgt20" class="tgtSentence">Responder a una infracción</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt21" class="tgtSentence">Sí</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt22" class="tgtSentence">Sí</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
        <para></para>
        <para>
          <caps:sentence sentenceid="31028de612149e3531f42f42ef29950f" id="tgt23" class="tgtSentence">Una vez que identifique qué topología implementó, use una de las siguientes secciones para más información sobre estas operaciones de su clave de inquilino de Azure RMS.</caps:sentence>
        </para>
      </introduction>
      <section address="BKMK_MSManagedOperations" expanded="false">
        <title>
          <caps:sentence sentenceid="bba3714be85f0735bef7f47656e0a7c8" id="tgt24" class="tgtSentence">Administradas por Microsoft: Operaciones de ciclo de vida de clave de inquilino</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="5eda74d98b7b7754421ce6f9de9a005b" id="tgt25" class="tgtSentence">Si Microsoft administra su clave de inquilino para Azure Rights Management (la predeterminada), use las siguientes secciones para obtener más información acerca de las operaciones del ciclo de vida que son relevantes para esta topología:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <link xlink:href="1284d0ee-0a72-45ba-a64c-3dcb25846c3d#BKMK_MSRevoke">Revoke your tenant key</link>
              </para>
            </listItem>
            <listItem>
              <para>
                <link xlink:href="1284d0ee-0a72-45ba-a64c-3dcb25846c3d#BKMK_MSRekey">Re-key your tenant key</link>
              </para>
            </listItem>
            <listItem>
              <para>
                <link xlink:href="1284d0ee-0a72-45ba-a64c-3dcb25846c3d#BKMK_MSBackup">Backup and recover your tenant key</link>
              </para>
            </listItem>
            <listItem>
              <para>
                <link xlink:href="1284d0ee-0a72-45ba-a64c-3dcb25846c3d#BKMK_MSExport">Export your tenant key</link>
              </para>
            </listItem>
            <listItem>
              <para>
                <link xlink:href="1284d0ee-0a72-45ba-a64c-3dcb25846c3d#BKMK_MSBreach">Respond to a breach</link>
              </para>
            </listItem>
          </list>
        </content>
        <sections>
          <section address="BKMK_MSRevoke">
            <title>
              <caps:sentence sentenceid="aa4c20163fd7bc47f8e25375406ec6fb" id="tgt26" class="tgtSentence">Revocar su clave de inquilino</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="51ad9fa33fa0e5526f1b572db9b58555" id="tgt27" class="tgtSentence">Cuando anule la suscripción de Azure RMS, Azure RMS dejará de usar su clave de inquilino y no será necesario que realice ninguna acción.</caps:sentence>
              </para>
            </content>
          </section>
          <section address="BKMK_MSRekey">
            <title>
              <caps:sentence sentenceid="18d8dd06fcb6d67508b252024996e60a" id="tgt28" class="tgtSentence">Vuelva a introducir su clave de inquilino</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="172f1b92d10968bd6108624e6eaf8a87" id="tgt29" class="tgtSentence">La acción de volver a introducir la clave también se le conoce como revertir su clave.</caps:sentence>
                <caps:sentence sentenceid="6676dd086981e1475a9e2e7007a4afdf" id="tgt30" class="tgtSentence"> No vuelva a introducir su clave de inquilino a menos que sea necesario.</caps:sentence>
                <caps:sentence sentenceid="114ce94135e58c76796a4a8584f1c483" id="tgt31" class="tgtSentence"> Otros clientes, como Office 2010, no se diseñaron para tratar cambios de clave correctamente.</caps:sentence>
                <caps:sentence sentenceid="e05317ff9fc0f8fe964b59bda0f4966b" id="tgt32" class="tgtSentence"> En este escenario, debe desactivar el estado de RMS en los equipos usando la directiva de grupo o un mecanismo equivalente.</caps:sentence>
                <caps:sentence sentenceid="aad27323870acdd57722e7204dc87da1" id="tgt33" class="tgtSentence"> Sin embargo, hay algunos eventos legítimos que pueden forzarle a volver a introducir la clave de inquilino.</caps:sentence>
                <caps:sentence sentenceid="4be0bb25039056347740ae85bcda324d" id="tgt34" class="tgtSentence"> Por ejemplo:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="81fc3599278a2edec8716956b688bb3c" id="tgt35" class="tgtSentence">La compañía se ha dividido en una o dos compañías.</caps:sentence>
                    <caps:sentence sentenceid="5972e4fcbc41e24e350371167af6e329" id="tgt36" class="tgtSentence"> Cuando vuelve a introducir la clave de inquilino, la nueva compañía no tendrá acceso al nuevo contenido que publiquen sus empleados.</caps:sentence>
                    <caps:sentence sentenceid="05f9a203a3f674c35611e78ca1d334a1" id="tgt37" class="tgtSentence"> Pueden acceder al antiguo contenido si tienen una copia de la antigua clave de inquilino.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="9f85433af9f207a9822583cb0710dad0" id="tgt38" class="tgtSentence">Cree que la copia maestra de su clave de inquilino (la copia en su posesión) se ha puesto en peligro.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="fcd71101385703a65e8cae293464c309" id="tgt39" class="tgtSentence">Puede volver a introducir su clave de inquilino llamando a los servicios de soporte al cliente de Microsoft (CSS) y demostrando que es el administrador inquilino.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="42a289bd93ef8c9c17ef727906942098" id="tgt40" class="tgtSentence">Cuando vuelve a introducir su clave de inquilino, el nuevo contenido está protegido usando la nueva clave de inquilino.</caps:sentence>
                <caps:sentence sentenceid="ac56e5c690310b1f2d2aa676f6d9f6dd" id="tgt41" class="tgtSentence"> Esto sucede en fases, por lo que para un período de tiempo, algún contenido nuevo continuará siendo protegido por la antigua clave de inquilino.</caps:sentence>
                <caps:sentence sentenceid="701e070f476d4665bbea1f943be1a2a4" id="tgt42" class="tgtSentence"> El contenido protegido anteriormente permanece protegido para su antigua clave de inquilino.</caps:sentence>
                <caps:sentence sentenceid="faf9dcf6ae4b540bbe9403dfe04d7d2a" id="tgt43" class="tgtSentence"> Para admitir este escenario, Azure RMS retiene su clave de inquilino antigua para que pueda emitir licencias para contenido antiguo.</caps:sentence>
              </para>
            </content>
          </section>
          <section address="BKMK_MSBackup">
            <title>
              <caps:sentence sentenceid="4a337e29bf1a6444a43307272bcd878b" id="tgt44" class="tgtSentence">Realizar una copia de seguridad y recuperar la clave de inquilino</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="fdaa7904d4938afa5c959fd899d3b0af" id="tgt45" class="tgtSentence">Microsoft es responsable de realizar la copia de seguridad de su clave de inquilino y no se requiere que realice ninguna acción.</caps:sentence>
              </para>
            </content>
          </section>
          <section address="BKMK_MSExport">
            <title>
              <caps:sentence sentenceid="414ca16dc978d6351ef4f8d9618f4305" id="tgt46" class="tgtSentence">Exportar su clave de inquilino</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="9e48b17d467d6074b0b40b6a8f491035" id="tgt47" class="tgtSentence">Puede exportar su configuración de Azure RMS y su clave de inquilino siguiendo las instrucciones de estos tres pasos:</caps:sentence>
              </para>
              <procedure>
                <title>
                  <caps:sentence sentenceid="b01b7117b551aca4180a0dfaa6ffa802" id="tgt48" class="tgtSentence">Paso 1: Iniciar exportación</caps:sentence>
                </title>
                <steps class="bullet">
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="b2bf8bfdfc2ea6de2e040fca21783d3e" id="tgt49" class="tgtSentence">Para ello, póngase en contacto con el Soporte de servicio al cliente (CSS) de Microsoft.</caps:sentence>
                        <caps:sentence sentenceid="1550d4bbd9b60ddc7847d3b6be92bf8c" id="tgt50" class="tgtSentence"> Debe probar que es un administrador para su inquilino de Azure RMS.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
              <procedure>
                <title>
                  <caps:sentence sentenceid="2babb1aacf6d2a0ec56db83bc59df6fd" id="tgt51" class="tgtSentence">Paso 2: Esperar comprobación</caps:sentence>
                </title>
                <steps class="bullet">
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="359709353c7f75b098cdedb37e37b0c1" id="tgt52" class="tgtSentence">Microsoft verifica que la solicitud para liberar su clave de inquilino de RMS es legítima.</caps:sentence>
                        <caps:sentence sentenceid="dbd365b3ae0c038527f24d554d509aea" id="tgt53" class="tgtSentence"> Este proceso puede tardar hasta 3 semanas.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
              <procedure>
                <title>
                  <caps:sentence sentenceid="070f8c24880e095e78b79b7e5b742477" id="tgt54" class="tgtSentence">Paso 3: Recibir instrucciones de clave de CSS</caps:sentence>
                </title>
                <steps class="bullet">
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="1cc4742c56e44afa7a2254acd995749f" id="tgt55" class="tgtSentence">Los Servicios de soporte al cliente de Microsoft (CSS) le enviarán su configuración de Azure RMS y clave de inquilino como cifrada en un archivo protegido con contraseña que tiene una extensión de nombre de archivo .tpd.</caps:sentence>
                        <caps:sentence sentenceid="e609c5e2d0cb994d92c560d87e1943f2" id="tgt56" class="tgtSentence"> Para ello, CSS le envía (como la persona que inició el informe) una herramienta por correo electrónico.</caps:sentence>
                        <caps:sentence sentenceid="da2f3a31cd2360d30b7e249bb7d444d1" id="tgt57" class="tgtSentence"> Debe ejecutar la herramienta desde un símbolo del sistema de la siguiente manera:</caps:sentence>
                      </para>
                      <code>AadrmTpd.exe -createkey
</code>
                      <para>
                        <caps:sentence sentenceid="a959423eef95d02f37ae46aacc851d85" id="tgt58" class="tgtSentence">Esto genera un plan de claves RSA y guarda las mitades públicas y privadas como archivos en la carpeta actual.</caps:sentence>
                        <caps:sentence sentenceid="407e8379b5443b7c0092c35c8bab7f29" id="tgt59" class="tgtSentence"> Por ejemplo: <system>PublicKey-FA29D0FE-5049-4C8E-931B-96C6152B0441.txt</system> y <system>PrivateKey-FA29D0FE-5049-4C8E-931B-96C6152B0441.txt</system>.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="e4e3b8462ecf9264aabc723b46444126" id="tgt60" class="tgtSentence">Responda al correo electrónico de CSS, adjuntando el archivo cuyo nombre comienza por <system>PublicKey</system>.</caps:sentence>
                        <caps:sentence sentenceid="851337d522aa2f71b834aeb8de0b9cfc" id="tgt61" class="tgtSentence"> CSS le enviará un archivo TPD como archivo .xml que está cifrado con su clave de RSA.</caps:sentence>
                        <caps:sentence sentenceid="aed99d622e664750aa0bbe50dd33f2d6" id="tgt62" class="tgtSentence"> Copie este archivo en la misma carpeta en la que ejecutó la herramienta AadrmTpd originalmente y ejecute la herramienta de nuevo, con el archivo que comienza por <system>PrivateKey</system> y el archivo de CSS.</caps:sentence>
                        <caps:sentence sentenceid="4be0bb25039056347740ae85bcda324d" id="tgt63" class="tgtSentence"> Por ejemplo:</caps:sentence>
                      </para>
                      <code>AadrmTpd.exe -key PrivateKey-FA29D0FE-5049-4C8E-931B-96C6152B0441.txt -target TPD-77172C7B-8E21-48B7-9854-7A4CEAC474D0.xml</code>
                      <para>
                        <caps:sentence sentenceid="4ead342f059560f8f64e808fb4d16908" id="tgt64" class="tgtSentence">El resultado de este comando deben ser dos archivos: Uno contiene la contraseña de texto simple para el TPD protegido con contraseña y el otro es el propio TPD protegido con contraseña.</caps:sentence>
                        <caps:sentence sentenceid="f3cc40b8589af5c98fee8f7b852afb86" id="tgt65" class="tgtSentence"> Para fines de referencias cruzadas, ambos deben tener el mismo GUID que los archivos de clave pública y privada cuando ejecutó el comando AadrmTpd.exe -createkey:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="1202b95c83abb4df3da4d6fbe7b70431" id="tgt66" class="tgtSentence">Password-FA29D0FE-5049-4C8E-931B-96C6152B0441.txt</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="dab191cbdbe540f1330d93831603e035" id="tgt67" class="tgtSentence">ExportedTPD-FA29D0FE-5049-4C8E-931B-96C6152B0441.xml</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                      <para>
                        <caps:sentence sentenceid="164dd608106e90cd820e3b6e49952b2b" id="tgt68" class="tgtSentence">Realice una copia de seguridad de estos archivos y guárdelos de manera segura para poder continuar descifrando el contenido protegido con esta clave de inquilino.</caps:sentence>
                        <caps:sentence sentenceid="6fd87fe01ca64dce718357fced99d15a" id="tgt69" class="tgtSentence"> Además, si está migrando a AD RMS, puede importar este archivo TPD (el archivo que empieza por <system>ExportedTDP</system>) a su servidor de AD RMS.</caps:sentence>
                      </para>
                      <para></para>
                    </content>
                  </step>
                </steps>
              </procedure>
              <procedure>
                <title>
                  <caps:sentence sentenceid="aa375bacd6a018e913e7d759894c0fdf" id="tgt70" class="tgtSentence">Paso 4: En curso: Proteger su clave de inquilino</caps:sentence>
                </title>
                <steps class="bullet">
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="9bb3800cb9b1479985d70efee7b7e2a7" id="tgt71" class="tgtSentence">Cuando haya recibido su clave de inquilino, manténgala a buen recaudo, ya que si alguien consigue acceso a ella, podrá descifrar todos los documentos que se hayan protegido con esa clave.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="ce96e12f5ff6bb291706c6eaf8e8a6db" id="tgt72" class="tgtSentence">Si el motivo por el que desea exportar la clave de inquilino es porque no quiere usar más Azure RMS, como procedimiento recomendado, desactive en este momento su inquilino de RMS.</caps:sentence>
                        <caps:sentence sentenceid="23987e8baf86d136decc01dc5a6b6a29" id="tgt73" class="tgtSentence"> No se demore en hacerlo después de recibir su clave de inquilino, ya que esta precaución le ayudará a minimizar las consecuencias si alguien que no debería tener su clave de inquilino consigue acceso a ella.</caps:sentence>
                        <caps:sentence sentenceid="dba73f72c649c5a7c9a7b7f3cb9b69ff" id="tgt74" class="tgtSentence"> Para obtener instrucciones, vea <link xlink:href="0b1c2064-0d01-45ae-a541-cebd7fd762ad">Deactivating Azure Rights Management</link>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
            </content>
          </section>
          <section address="BKMK_MSBreach">
            <title>
              <caps:sentence sentenceid="3f2932f1c2da2de325245973e9e22c43" id="tgt75" class="tgtSentence">Responder a una infracción</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="4cd239b664a4167b7d102db547a24b80" id="tgt76" class="tgtSentence">Ningún sistema de seguridad, por seguro que sea, está completo sin un proceso de respuesta a infracción.</caps:sentence>
                <caps:sentence sentenceid="8d8bbab9d90717bbf8ca29bb7fb6dbd5" id="tgt77" class="tgtSentence"> Puede que se haya robado o puesto en peligro su clave de inquilino.</caps:sentence>
                <caps:sentence sentenceid="4f2c5a978992f461c57320309e378d0e" id="tgt78" class="tgtSentence"> Aunque esté bien protegido, se pueden encontrar vulnerabilidades en la tecnología HSM de la generación actual o algoritmos y longitudes de clave actuales.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="8f668f1a7fddcb16b7ed72d9e50994db" id="tgt79" class="tgtSentence">Microsoft tiene un equipo dedicado a responder a incidentes de seguridad en sus productos y servicios.</caps:sentence>
                <caps:sentence sentenceid="42c0a6d9fbdf68720a054b54307ebd7a" id="tgt80" class="tgtSentence"> Tan pronto como aparece un informe fiable de un incidente, este equipo se pone a investigar el alcance, la causa del origen del mismo y cómo mitigarlo.</caps:sentence>
                <caps:sentence sentenceid="7bd9536d07fecf6db896afc70efa5a8b" id="tgt81" class="tgtSentence"> Si este incidente afecta a sus activos, Microsoft notificará a sus administradores de inquilino de Azure RMS por correo electrónico usando la dirección que ha suministrado cuando realizó la suscripción.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="a13dc86a26eb4f4ac693d06e2f6e384e" id="tgt82" class="tgtSentence">Si tiene una infracción, la mejor acción que usted o Microsoft puede llevar a cabo dependerá del alcance de la infracción. Microsoft trabajará con usted en este proceso.</caps:sentence>
                <caps:sentence sentenceid="dbc7955c70882dd29232588299631d40" id="tgt83" class="tgtSentence"> La tabla siguiente muestra algunas situaciones típicas y la respuesta probable, aunque la respuesta exacta dependerá de toda la información que se revele durante la investigación.</caps:sentence>
              </para>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ed6166e25bfb68cb89daea1cea0982df" id="tgt84" class="tgtSentence">Descripción del incidente</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="e1f4b3dc96ff0ea7f7ff1445dba2797a" id="tgt85" class="tgtSentence">Respuesta probable</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="c1be903d713f5f3ab027ec39d8c2c06c" id="tgt86" class="tgtSentence">Se ha filtrado su clave de inquilino.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="67a65c974f1c6ef351c200a2afa52929" id="tgt87" class="tgtSentence">Vuelva a introducir su clave de inquilino.</caps:sentence>
                        <caps:sentence sentenceid="3950a377ccc2e153a1563c0d5971a0cb" id="tgt88" class="tgtSentence"> Vea la sección <link xlink:href="1284d0ee-0a72-45ba-a64c-3dcb25846c3d#BKMK_MSRekey">Re-key your tenant key</link> de este tema.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="2689986d254dea6ef9d3a858c483e523" id="tgt89" class="tgtSentence">Un individuo no autorizado o malware han tenido derechos de uso de su clave de inquilino, pero la clave en sí no se ha filtrado.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="4c9b679497e5ccb2ad1b96e0fae5a05c" id="tgt90" class="tgtSentence">La nueva introducción de la clave de inquilino no resulta útil aquí y requiere el análisis de la causa principal.</caps:sentence>
                        <caps:sentence sentenceid="34944e70393f71b303e1f0db6df96e95" id="tgt91" class="tgtSentence"> Si un error de software o de proceso ha sido el responsable de que un individuo no autorizado obtuviera acceso, dicha situación se debe resolver.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ac5475941f4804bc47c8f0bfc0087f3c" id="tgt92" class="tgtSentence">Vulnerabilidad descubierta en el algoritmo de RSA, o longitud de clave, o ataques por fuerza bruta se hacen factibles computacionalmente.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="c514a781ce2692f216a608e5ee175469" id="tgt93" class="tgtSentence">Microsoft debe actualizar Azure RMS para que admita nuevos algoritmos y longitudes de clave más largas que sean resistentes, e indica a todos los clientes que renueven sus claves de inquilino.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
        </sections>
      </section>
      <section address="BKMK_BYOKManagedOperations" expanded="false">
        <title>
          <caps:sentence sentenceid="f36b617a7a594895b0ae2de42b90984c" id="tgt94" class="tgtSentence">Administrada por el cliente: Operaciones de ciclo de vida de clave de inquilino</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="47a43e96255ec4130ed100391e71892e" id="tgt95" class="tgtSentence">Si administra su clave de inquilino para Azure Rights Management (el escenario Aportar tu propia clave, o BYOK), use las siguientes secciones para obtener más información acerca de las operaciones del ciclo de vida que son relevantes para esta topología:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <link xlink:href="1284d0ee-0a72-45ba-a64c-3dcb25846c3d#BKMK_BYOKRevoke">Revoke your tenant key</link>
              </para>
            </listItem>
            <listItem>
              <para>
                <link xlink:href="1284d0ee-0a72-45ba-a64c-3dcb25846c3d#BKMK_BYOKRekey">Re-key your tenant key</link>
              </para>
            </listItem>
            <listItem>
              <para>
                <link xlink:href="1284d0ee-0a72-45ba-a64c-3dcb25846c3d#BKMK_BYOKBackup">Backup and recover your tenant key</link>
              </para>
            </listItem>
            <listItem>
              <para>
                <link xlink:href="1284d0ee-0a72-45ba-a64c-3dcb25846c3d#BKMK_BYOKExport">Export your tenant key</link>
              </para>
            </listItem>
            <listItem>
              <para>
                <link xlink:href="1284d0ee-0a72-45ba-a64c-3dcb25846c3d#BKMK_BYOKBreach">Respond to a breach</link>
              </para>
            </listItem>
          </list>
        </content>
        <sections>
          <section address="BKMK_BYOKRevoke">
            <title>
              <caps:sentence sentenceid="aa4c20163fd7bc47f8e25375406ec6fb" id="tgt96" class="tgtSentence">Revocar su clave de inquilino</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="51ad9fa33fa0e5526f1b572db9b58555" id="tgt97" class="tgtSentence">Cuando anule la suscripción de Azure RMS, Azure RMS dejará de usar su clave de inquilino y no será necesario que realice ninguna acción.</caps:sentence>
              </para>
            </content>
          </section>
          <section address="BKMK_BYOKRekey">
            <title>
              <caps:sentence sentenceid="18d8dd06fcb6d67508b252024996e60a" id="tgt98" class="tgtSentence">Vuelva a introducir su clave de inquilino</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="172f1b92d10968bd6108624e6eaf8a87" id="tgt99" class="tgtSentence">La acción de volver a introducir la clave también se le conoce como revertir su clave.</caps:sentence>
                <caps:sentence sentenceid="6676dd086981e1475a9e2e7007a4afdf" id="tgt100" class="tgtSentence"> No vuelva a introducir su clave de inquilino a menos que sea necesario.</caps:sentence>
                <caps:sentence sentenceid="114ce94135e58c76796a4a8584f1c483" id="tgt101" class="tgtSentence"> Otros clientes, como Office 2010, no se diseñaron para tratar cambios de clave correctamente.</caps:sentence>
                <caps:sentence sentenceid="e05317ff9fc0f8fe964b59bda0f4966b" id="tgt102" class="tgtSentence"> En este escenario, debe desactivar el estado de RMS en los equipos usando la directiva de grupo o un mecanismo equivalente.</caps:sentence>
                <caps:sentence sentenceid="aad27323870acdd57722e7204dc87da1" id="tgt103" class="tgtSentence"> Sin embargo, hay algunos eventos legítimos que pueden forzarle a volver a introducir la clave de inquilino.</caps:sentence>
                <caps:sentence sentenceid="4be0bb25039056347740ae85bcda324d" id="tgt104" class="tgtSentence"> Por ejemplo:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="81fc3599278a2edec8716956b688bb3c" id="tgt105" class="tgtSentence">La compañía se ha dividido en una o dos compañías.</caps:sentence>
                    <caps:sentence sentenceid="5972e4fcbc41e24e350371167af6e329" id="tgt106" class="tgtSentence"> Cuando vuelve a introducir la clave de inquilino, la nueva compañía no tendrá acceso al nuevo contenido que publiquen sus empleados.</caps:sentence>
                    <caps:sentence sentenceid="05f9a203a3f674c35611e78ca1d334a1" id="tgt107" class="tgtSentence"> Pueden acceder al antiguo contenido si tienen una copia de la antigua clave de inquilino.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="9f85433af9f207a9822583cb0710dad0" id="tgt108" class="tgtSentence">Cree que la copia maestra de su clave de inquilino (la copia en su posesión) se ha puesto en peligro.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="42a289bd93ef8c9c17ef727906942098" id="tgt109" class="tgtSentence">Cuando vuelve a introducir su clave de inquilino, el nuevo contenido está protegido usando la nueva clave de inquilino.</caps:sentence>
                <caps:sentence sentenceid="ac56e5c690310b1f2d2aa676f6d9f6dd" id="tgt110" class="tgtSentence"> Esto sucede en fases, por lo que para un período de tiempo, algún contenido nuevo continuará siendo protegido por la antigua clave de inquilino.</caps:sentence>
                <caps:sentence sentenceid="701e070f476d4665bbea1f943be1a2a4" id="tgt111" class="tgtSentence"> El contenido protegido anteriormente permanece protegido para su antigua clave de inquilino.</caps:sentence>
                <caps:sentence sentenceid="faf9dcf6ae4b540bbe9403dfe04d7d2a" id="tgt112" class="tgtSentence"> Para admitir este escenario, Azure RMS retiene su clave de inquilino antigua para que pueda emitir licencias para contenido antiguo.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="92fdd864f7b85a2fc6883ea772743c8c" id="tgt113" class="tgtSentence">Para volver a introducir su clave de inquilino, genere y cree una nueva clave en Internet o en persona, mediante los procedimientos de la sección <link xlink:href="f0d33c5f-a6a6-44a1-bdec-5be1bc8e1e14#BKMK_ImplementBYOK">Implementing bring your own key (BYOK)</link> del tema <link xlink:href="f0d33c5f-a6a6-44a1-bdec-5be1bc8e1e14">Planning and operations for your Azure Rights Management tenant key</link>.</caps:sentence>
              </para>
            </content>
          </section>
          <section address="BKMK_BYOKBackup">
            <title>
              <caps:sentence sentenceid="4a337e29bf1a6444a43307272bcd878b" id="tgt114" class="tgtSentence">Realizar una copia de seguridad y recuperar la clave de inquilino</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="a77d5672e49501c0d12b88205ba2288f" id="tgt115" class="tgtSentence">Es responsable de realizar copias de seguridad de su clave de inquilino.</caps:sentence>
                <caps:sentence sentenceid="025ef00c2abe476c12f13e4eb9c4a41b" id="tgt116" class="tgtSentence"> Si ha generado su clave de inquilino en un HSM de Thales, para realizar una copia de seguridad de la clave acortada, el archivo de Word y las tarjetas de administrador.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="039a7b4642a7d624f17ca489a49316b1" id="tgt117" class="tgtSentence">Si ha transferido su clave siguiendo los procedimientos de la sección <link xlink:href="f0d33c5f-a6a6-44a1-bdec-5be1bc8e1e14#BKMK_ImplementBYOK">Implementing bring your own key (BYOK)</link> del tema <link xlink:href="f0d33c5f-a6a6-44a1-bdec-5be1bc8e1e14">Planning and operations for your Azure Rights Management tenant key</link>, Azure RMS continuará con el archivo de clave acortado, para proteger frente a los errores de cualquier nodo de Azure RMS.</caps:sentence>
                <caps:sentence sentenceid="4447c6f07cf47e71f64833146dc979ca" id="tgt118" class="tgtSentence"> Sin embargo, no considere esto una copia de seguridad completa.</caps:sentence>
                <caps:sentence sentenceid="d31bb34dc77053e8dd4f979f6d3572ff" id="tgt119" class="tgtSentence"> Por ejemplo, si alguna vez necesita una copia de texto simple de su clave para usarla fuera de un HSM de Thales, Azure RMS no podrá recuperarla para usted porque solo tiene una copia no recuperable.</caps:sentence>
              </para>
            </content>
          </section>
          <section address="BKMK_BYOKExport">
            <title>
              <caps:sentence sentenceid="414ca16dc978d6351ef4f8d9618f4305" id="tgt120" class="tgtSentence">Exportar su clave de inquilino</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="2d85dfccf3e0a4b6e965163b56728f90" id="tgt121" class="tgtSentence">Si usa BYOK, no puede exportar su clave de inquilino desde Azure RMS.</caps:sentence>
                <caps:sentence sentenceid="7cc6443f3dcfe68e72fb16ad25e61293" id="tgt122" class="tgtSentence"> La copia en Azure RMS es irrecuperable.</caps:sentence>
                <caps:sentence sentenceid="8d274ab900621abfa9a7323118ecd2e0" id="tgt123" class="tgtSentence"> Si desea eliminar esta clave para que no se pueda volver a usar, póngase en contacto con los servicios de atención al cliente y soporte técnico de Microsoft (CSS).</caps:sentence>
              </para>
            </content>
          </section>
          <section address="BKMK_BYOKBreach">
            <title>
              <caps:sentence sentenceid="3f2932f1c2da2de325245973e9e22c43" id="tgt124" class="tgtSentence">Responder a una infracción</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="4cd239b664a4167b7d102db547a24b80" id="tgt125" class="tgtSentence">Ningún sistema de seguridad, por seguro que sea, está completo sin un proceso de respuesta a infracción.</caps:sentence>
                <caps:sentence sentenceid="8d8bbab9d90717bbf8ca29bb7fb6dbd5" id="tgt126" class="tgtSentence"> Puede que se haya robado o puesto en peligro su clave de inquilino.</caps:sentence>
                <caps:sentence sentenceid="4f2c5a978992f461c57320309e378d0e" id="tgt127" class="tgtSentence"> Aunque esté bien protegido, se pueden encontrar vulnerabilidades en la tecnología HSM de la generación actual o algoritmos y longitudes de clave actuales.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="8f668f1a7fddcb16b7ed72d9e50994db" id="tgt128" class="tgtSentence">Microsoft tiene un equipo dedicado a responder a incidentes de seguridad en sus productos y servicios.</caps:sentence>
                <caps:sentence sentenceid="42c0a6d9fbdf68720a054b54307ebd7a" id="tgt129" class="tgtSentence"> Tan pronto como aparece un informe fiable de un incidente, este equipo se pone a investigar el alcance, la causa del origen del mismo y cómo mitigarlo.</caps:sentence>
                <caps:sentence sentenceid="7bd9536d07fecf6db896afc70efa5a8b" id="tgt130" class="tgtSentence"> Si este incidente afecta a sus activos, Microsoft notificará a sus administradores de inquilino de Azure RMS por correo electrónico usando la dirección que ha suministrado cuando realizó la suscripción.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="f8852b8fc9f57ad41436fc5a52ca72cd" id="tgt131" class="tgtSentence">Si tiene una infracción, la mejor acción que usted o Microsoft puede llevar a cabo dependerá del alcance de la infracción; Microsoft trabajará con usted en este proceso.</caps:sentence>
                <caps:sentence sentenceid="dbc7955c70882dd29232588299631d40" id="tgt132" class="tgtSentence"> La tabla siguiente muestra algunas situaciones típicas y la respuesta probable, aunque la respuesta exacta dependerá de toda la información que se revele durante la investigación.</caps:sentence>
              </para>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ed6166e25bfb68cb89daea1cea0982df" id="tgt133" class="tgtSentence">Descripción del incidente</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="e1f4b3dc96ff0ea7f7ff1445dba2797a" id="tgt134" class="tgtSentence">Respuesta probable</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="c1be903d713f5f3ab027ec39d8c2c06c" id="tgt135" class="tgtSentence">Se ha filtrado su clave de inquilino.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="67a65c974f1c6ef351c200a2afa52929" id="tgt136" class="tgtSentence">Vuelva a introducir su clave de inquilino.</caps:sentence>
                        <caps:sentence sentenceid="3950a377ccc2e153a1563c0d5971a0cb" id="tgt137" class="tgtSentence"> Vea la sección <link xlink:href="1284d0ee-0a72-45ba-a64c-3dcb25846c3d#BKMK_BYOKRekey">Re-key your tenant key</link> de este tema.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="2689986d254dea6ef9d3a858c483e523" id="tgt138" class="tgtSentence">Un individuo no autorizado o malware han tenido derechos de uso de su clave de inquilino, pero la clave en sí no se ha filtrado.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="4c9b679497e5ccb2ad1b96e0fae5a05c" id="tgt139" class="tgtSentence">La nueva introducción de la clave de inquilino no resulta útil aquí y requiere el análisis de la causa principal.</caps:sentence>
                        <caps:sentence sentenceid="34944e70393f71b303e1f0db6df96e95" id="tgt140" class="tgtSentence"> Si un error de software o de proceso ha sido el responsable de que un individuo no autorizado obtuviera acceso, dicha situación se debe resolver.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="416c0ac137c9dd0b7c010e4c60210393" id="tgt141" class="tgtSentence">Vulnerabilidad descubierta en la tecnología HSM de generación actual.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ee0faf9ad70dc391486b1e63c3352a6d" id="tgt142" class="tgtSentence">Microsoft debe actualizar los HSM.</caps:sentence>
                        <caps:sentence sentenceid="8dfdfdb3ec4b6120c288e7cd830f184d" id="tgt143" class="tgtSentence"> Si no hay motivos para creer que la vulnerabilidad afectó a las claves, Microsoft indicará a todos los clientes que renueven sus claves de inquilino.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ac5475941f4804bc47c8f0bfc0087f3c" id="tgt144" class="tgtSentence">Vulnerabilidad descubierta en el algoritmo de RSA, o longitud de clave, o ataques por fuerza bruta se hacen factibles computacionalmente.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="c514a781ce2692f216a608e5ee175469" id="tgt145" class="tgtSentence">Microsoft debe actualizar Azure RMS para que admita nuevos algoritmos y longitudes de clave más largas que sean resistentes, e indica a todos los clientes que renueven sus claves de inquilino.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
        </sections>
      </section>
      <relatedTopics>
        <link xlink:href="18564e4a-9364-4ed2-8f17-89d24fc0d878">Using Azure Rights Management</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Depending on your tenant key topology (Microsoft-managed or customer-managed), you have different levels of control and responsibility for your Microsoft Azure Rights Management (Azure RMS) tenant key after it is implemented.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src2" class="srcSentence">When you manage your own tenant key, this is often referred to as bring your own key (BYOK).</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> For more information about this scenario and how to choose between the two tenant key topologies, see <link xlink:href="f0d33c5f-a6a6-44a1-bdec-5be1bc8e1e14">Planning and operations for your Azure Rights Management tenant key</link>.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src4" class="srcSentence">The following table identifies which operations you can do, depending on the topology that you’ve chosen for your Azure RMS tenant key.</caps:sentence>
        </para>
        <table>
          <thead>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src5" class="srcSentence">Lifecycle operation</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src6" class="srcSentence">Microsoft-managed (default)</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src7" class="srcSentence">Customer-managed (BYOK)</caps:sentence>
                </para>
              </TD>
            </tr>
          </thead>
          <tbody>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src8" class="srcSentence">Revoke your tenant key</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src9" class="srcSentence">No (automatic)</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src10" class="srcSentence">No (automatic)</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src11" class="srcSentence">Re-key your tenant key</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src12" class="srcSentence">Yes</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src13" class="srcSentence">Yes</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src14" class="srcSentence">Backup and recover your tenant key</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src15" class="srcSentence">No</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src16" class="srcSentence">Yes</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src17" class="srcSentence">Export your tenant key</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src18" class="srcSentence">Yes</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src19" class="srcSentence">No</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src20" class="srcSentence">Respond to a breach</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src21" class="srcSentence">Yes</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src22" class="srcSentence">Yes</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
        <para></para>
        <para>
          <caps:sentence id="src23" class="srcSentence">After you have identified which topology you have implemented, use one of the following sections for more information about these operations for your Azure RMS tenant key.</caps:sentence>
        </para>
      </introduction>
      <section address="BKMK_MSManagedOperations" expanded="false">
        <title>
          <caps:sentence id="src24" class="srcSentence">Microsoft-managed: Tenant key lifecycle operations</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src25" class="srcSentence">If Microsoft manages your tenant key for Azure Rights Management (the default), use the following sections for more information about the lifecycle operations that are relevant to this topology:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <link xlink:href="1284d0ee-0a72-45ba-a64c-3dcb25846c3d#BKMK_MSRevoke">Revoke your tenant key</link>
              </para>
            </listItem>
            <listItem>
              <para>
                <link xlink:href="1284d0ee-0a72-45ba-a64c-3dcb25846c3d#BKMK_MSRekey">Re-key your tenant key</link>
              </para>
            </listItem>
            <listItem>
              <para>
                <link xlink:href="1284d0ee-0a72-45ba-a64c-3dcb25846c3d#BKMK_MSBackup">Backup and recover your tenant key</link>
              </para>
            </listItem>
            <listItem>
              <para>
                <link xlink:href="1284d0ee-0a72-45ba-a64c-3dcb25846c3d#BKMK_MSExport">Export your tenant key</link>
              </para>
            </listItem>
            <listItem>
              <para>
                <link xlink:href="1284d0ee-0a72-45ba-a64c-3dcb25846c3d#BKMK_MSBreach">Respond to a breach</link>
              </para>
            </listItem>
          </list>
        </content>
        <sections>
          <section address="BKMK_MSRevoke">
            <title>
              <caps:sentence id="src26" class="srcSentence">Revoke your tenant key</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src27" class="srcSentence">When you unsubscribe from Azure RMS, Azure RMS stops using your tenant key and no action is needed from you.</caps:sentence>
              </para>
            </content>
          </section>
          <section address="BKMK_MSRekey">
            <title>
              <caps:sentence id="src28" class="srcSentence">Re-key your tenant key</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src29" class="srcSentence">Re-keying is also known as rolling your key.</caps:sentence>
                <caps:sentence id="src30" class="srcSentence"> Do not re-key your tenant key unless it’s really necessary.</caps:sentence>
                <caps:sentence id="src31" class="srcSentence"> Older clients, such as Office 2010, were not designed to handle key changes gracefully.</caps:sentence>
                <caps:sentence id="src32" class="srcSentence"> In this scenario, you must clear the RMS state on computers by using Group Policy or an equivalent mechanism.</caps:sentence>
                <caps:sentence id="src33" class="srcSentence"> However, there are some legitimate events that may force you to re-key your tenant key.</caps:sentence>
                <caps:sentence id="src34" class="srcSentence"> For example:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src35" class="srcSentence">Your company has split into two or more companies.</caps:sentence>
                    <caps:sentence id="src36" class="srcSentence"> When you re-key your tenant key, the new company will not have access to new content that your employees publish.</caps:sentence>
                    <caps:sentence id="src37" class="srcSentence"> They can access the old content if they have a copy of the old tenant key.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src38" class="srcSentence">You believe the master copy of your tenant key (the copy in your possession) was compromised.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src39" class="srcSentence">You can re-key your tenant key by calling Microsoft Customer Support Services (CSS) and proving that you are the tenant administrator.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src40" class="srcSentence">When you re-key your tenant key, new content is protected by using the new tenant key.</caps:sentence>
                <caps:sentence id="src41" class="srcSentence"> This happens in a phased manner, so for a period of time, some new content will continue to be protected with the old tenant key.</caps:sentence>
                <caps:sentence id="src42" class="srcSentence"> Previously protected content stays protected to your old tenant key.</caps:sentence>
                <caps:sentence id="src43" class="srcSentence"> To support this scenario, Azure RMS retains your old tenant key so that it can issue licenses for old content.</caps:sentence>
              </para>
            </content>
          </section>
          <section address="BKMK_MSBackup">
            <title>
              <caps:sentence id="src44" class="srcSentence">Backup and recover your tenant key</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src45" class="srcSentence">Microsoft is responsible for backing up your tenant key and no action is required from you.</caps:sentence>
              </para>
            </content>
          </section>
          <section address="BKMK_MSExport">
            <title>
              <caps:sentence id="src46" class="srcSentence">Export your tenant key</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src47" class="srcSentence">You can export your Azure RMS configuration and tenant key by following the instructions in these three steps:</caps:sentence>
              </para>
              <procedure>
                <title>
                  <caps:sentence id="src48" class="srcSentence">Step 1: Initiate export</caps:sentence>
                </title>
                <steps class="bullet">
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src49" class="srcSentence">To do this, contact Microsoft Customer Service Support (CSS).</caps:sentence>
                        <caps:sentence id="src50" class="srcSentence"> You must prove you are an administrator for your Azure RMS tenant.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
              <procedure>
                <title>
                  <caps:sentence id="src51" class="srcSentence">Step 2: Wait for verification</caps:sentence>
                </title>
                <steps class="bullet">
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src52" class="srcSentence">Microsoft verifies that your request to release your RMS tenant key is legitimate.</caps:sentence>
                        <caps:sentence id="src53" class="srcSentence"> This process can take up to 3 weeks.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
              <procedure>
                <title>
                  <caps:sentence id="src54" class="srcSentence">Step 3: Receive key instructions from CSS</caps:sentence>
                </title>
                <steps class="bullet">
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src55" class="srcSentence">Microsoft Customer Support Services (CSS) will send you your Azure RMS configuration and tenant key as encrypted in a password-protected file that has a .tpd file name extension.</caps:sentence>
                        <caps:sentence id="src56" class="srcSentence"> To do this, CSS first sends you (as the person who initiated the export) a tool by email.</caps:sentence>
                        <caps:sentence id="src57" class="srcSentence"> You must run the tool from a command prompt as follows:</caps:sentence>
                      </para>
                      <code>AadrmTpd.exe -createkey
</code>
                      <para>
                        <caps:sentence id="src58" class="srcSentence">This generates an RSA key pair and saves the public and private halves as files in the current folder.</caps:sentence>
                        <caps:sentence id="src59" class="srcSentence"> For example: <system>PublicKey-FA29D0FE-5049-4C8E-931B-96C6152B0441.txt</system> and <system>PrivateKey-FA29D0FE-5049-4C8E-931B-96C6152B0441.txt</system>.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src60" class="srcSentence">Respond to the email from CSS, attaching the file that has a name that starts with <system>PublicKey</system>.</caps:sentence>
                        <caps:sentence id="src61" class="srcSentence"> CSS will next send you a TPD file as an .xml file that is encrypted with your RSA key.</caps:sentence>
                        <caps:sentence id="src62" class="srcSentence"> Copy this file to the same folder as you ran the AadrmTpd tool originally, and run the tool again, using your file that starts with <system>PrivateKey</system> and the file from CSS.</caps:sentence>
                        <caps:sentence id="src63" class="srcSentence"> For example:</caps:sentence>
                      </para>
                      <code>AadrmTpd.exe -key PrivateKey-FA29D0FE-5049-4C8E-931B-96C6152B0441.txt -target TPD-77172C7B-8E21-48B7-9854-7A4CEAC474D0.xml</code>
                      <para>
                        <caps:sentence id="src64" class="srcSentence">The output of this command should be two files: One contains the plaintext password for the password-protected TPD, and the other is the password-protected TPD itself.</caps:sentence>
                        <caps:sentence id="src65" class="srcSentence"> For cross-referencing purposes, both should have the same GUID as the public and private key files from when you ran the AadrmTpd.exe -createkey command:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence id="src66" class="srcSentence">Password-FA29D0FE-5049-4C8E-931B-96C6152B0441.txt</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src67" class="srcSentence">ExportedTPD-FA29D0FE-5049-4C8E-931B-96C6152B0441.xml</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                      <para>
                        <caps:sentence id="src68" class="srcSentence">Backup these files and store them safely to ensure that you can continue to decrypt content that is protected with this tenant key.</caps:sentence>
                        <caps:sentence id="src69" class="srcSentence"> In addition, if you are migrating to AD RMS, you can import this TPD file (the file that starts with <system>ExportedTDP</system>) to your AD RMS server.</caps:sentence>
                      </para>
                      <para></para>
                    </content>
                  </step>
                </steps>
              </procedure>
              <procedure>
                <title>
                  <caps:sentence id="src70" class="srcSentence">Step 4: Ongoing: Protect your tenant key</caps:sentence>
                </title>
                <steps class="bullet">
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src71" class="srcSentence">After you receive your tenant key, keep it well-guarded, because if somebody gets access to it, they can decrypt all documents that are protected by using that key.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src72" class="srcSentence">If the reason for exporting your tenant key is because you no longer want to use Azure RMS, as a best practice, now deactivate your RMS tenant.</caps:sentence>
                        <caps:sentence id="src73" class="srcSentence"> Do not delay doing this after you receive your tenant key because this precaution will help to minimize the consequences if your tenant key is accessed by somebody who should not have it.</caps:sentence>
                        <caps:sentence id="src74" class="srcSentence"> For instructions, see <link xlink:href="0b1c2064-0d01-45ae-a541-cebd7fd762ad">Deactivating Azure Rights Management</link>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
            </content>
          </section>
          <section address="BKMK_MSBreach">
            <title>
              <caps:sentence id="src75" class="srcSentence">Respond to a breach</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src76" class="srcSentence">No security system, no matter how strong, is complete without a breach response process.</caps:sentence>
                <caps:sentence id="src77" class="srcSentence"> Your tenant key might be compromised or stolen.</caps:sentence>
                <caps:sentence id="src78" class="srcSentence"> Even when it’s well protected well, vulnerabilities might be found in current generation HSM technology or current key lengths and algorithms.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src79" class="srcSentence">Microsoft has a dedicated team to respond to security incidents in its products and services.</caps:sentence>
                <caps:sentence id="src80" class="srcSentence"> As soon as there is a credible report of an incident, this team engages to investigate the scope, root cause, and mitigations.</caps:sentence>
                <caps:sentence id="src81" class="srcSentence"> If this incident affects your assets, then Microsoft will notify your Azure RMS tenant administrators by email by using the address that you supplied when you subscribed.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src82" class="srcSentence">If you have a breach, the best action that you or Microsoft can take depends on the scope of the breach; Microsoft will work with you through this process.</caps:sentence>
                <caps:sentence id="src83" class="srcSentence"> The following table shows some typical situations and the likely response, although the exact response will depend on all the information that is revealed during the investigation.</caps:sentence>
              </para>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src84" class="srcSentence">Incident description</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src85" class="srcSentence">Likely response</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src86" class="srcSentence">Your tenant key is leaked.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src87" class="srcSentence">Re-key your tenant key.</caps:sentence>
                        <caps:sentence id="src88" class="srcSentence"> See the <link xlink:href="1284d0ee-0a72-45ba-a64c-3dcb25846c3d#BKMK_MSRekey">Re-key your tenant key</link> section in this topic.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src89" class="srcSentence">An unauthorized individual or malware got rights to use your tenant key but the key itself did not leak.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src90" class="srcSentence">Re-keying your tenant key does not help here and requires root-cause analysis.</caps:sentence>
                        <caps:sentence id="src91" class="srcSentence"> If a process or software bug was responsible for the unauthorized individual to get access, that situation must be resolved.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src92" class="srcSentence">Vulnerability discovered in the RSA algorithm, or key length, or brute-force attacks become computationally feasible.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src93" class="srcSentence">Microsoft must update the Azure RMS to support new algorithms and longer key lengths that are resilient, and instruct all customers to renew their tenant keys.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
        </sections>
      </section>
      <section address="BKMK_BYOKManagedOperations" expanded="false">
        <title>
          <caps:sentence id="src94" class="srcSentence">Customer-managed: Tenant key lifecycle operations</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src95" class="srcSentence">If you manage your tenant key for Azure Rights Management (the bring your own key, or BYOK, scenario), use the following sections for more information about the lifecycle operations that are relevant to this topology:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <link xlink:href="1284d0ee-0a72-45ba-a64c-3dcb25846c3d#BKMK_BYOKRevoke">Revoke your tenant key</link>
              </para>
            </listItem>
            <listItem>
              <para>
                <link xlink:href="1284d0ee-0a72-45ba-a64c-3dcb25846c3d#BKMK_BYOKRekey">Re-key your tenant key</link>
              </para>
            </listItem>
            <listItem>
              <para>
                <link xlink:href="1284d0ee-0a72-45ba-a64c-3dcb25846c3d#BKMK_BYOKBackup">Backup and recover your tenant key</link>
              </para>
            </listItem>
            <listItem>
              <para>
                <link xlink:href="1284d0ee-0a72-45ba-a64c-3dcb25846c3d#BKMK_BYOKExport">Export your tenant key</link>
              </para>
            </listItem>
            <listItem>
              <para>
                <link xlink:href="1284d0ee-0a72-45ba-a64c-3dcb25846c3d#BKMK_BYOKBreach">Respond to a breach</link>
              </para>
            </listItem>
          </list>
        </content>
        <sections>
          <section address="BKMK_BYOKRevoke">
            <title>
              <caps:sentence id="src96" class="srcSentence">Revoke your tenant key</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src97" class="srcSentence">When you unsubscribe from Azure RMS, Azure RMS stops using your tenant key and no action is needed from you.</caps:sentence>
              </para>
            </content>
          </section>
          <section address="BKMK_BYOKRekey">
            <title>
              <caps:sentence id="src98" class="srcSentence">Re-key your tenant key</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src99" class="srcSentence">Re-keying is also known as rolling your key.</caps:sentence>
                <caps:sentence id="src100" class="srcSentence"> Do not re-key your tenant key unless it’s really necessary.</caps:sentence>
                <caps:sentence id="src101" class="srcSentence"> Older clients, such as Office 2010, were not designed to handle key changes gracefully.</caps:sentence>
                <caps:sentence id="src102" class="srcSentence"> In this scenario, you must clear the RMS state on computers by using Group Policy or an equivalent mechanism.</caps:sentence>
                <caps:sentence id="src103" class="srcSentence"> However, there are some legitimate events that may force you to re-key your tenant key.</caps:sentence>
                <caps:sentence id="src104" class="srcSentence"> For example:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src105" class="srcSentence">Your company has split into two or more companies.</caps:sentence>
                    <caps:sentence id="src106" class="srcSentence"> When you re-key your tenant key, the new company will not have access to new content that your employees publish.</caps:sentence>
                    <caps:sentence id="src107" class="srcSentence"> They can access the old content if they have a copy of the old tenant key.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src108" class="srcSentence">You believe the master copy of your tenant key (the copy in your possession) was compromised.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src109" class="srcSentence">When you re-key your tenant key, new content is protected by using the new tenant key.</caps:sentence>
                <caps:sentence id="src110" class="srcSentence"> This happens in a phased manner, so for a period of time, some new content will continue to be protected with the old tenant key.</caps:sentence>
                <caps:sentence id="src111" class="srcSentence"> Previously protected content stays protected to your old tenant key.</caps:sentence>
                <caps:sentence id="src112" class="srcSentence"> To support this scenario, Azure RMS retains your old tenant key so that it can issue licenses for old content.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src113" class="srcSentence">To re-key your tenant key, generate and create a new key over the Internet or in person, by using the procedures in the <link xlink:href="f0d33c5f-a6a6-44a1-bdec-5be1bc8e1e14#BKMK_ImplementBYOK">Implementing bring your own key (BYOK)</link> section from the <link xlink:href="f0d33c5f-a6a6-44a1-bdec-5be1bc8e1e14">Planning and operations for your Azure Rights Management tenant key</link> topic.</caps:sentence>
              </para>
            </content>
          </section>
          <section address="BKMK_BYOKBackup">
            <title>
              <caps:sentence id="src114" class="srcSentence">Backup and recover your tenant key</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src115" class="srcSentence">You are responsible for backing up your tenant key.</caps:sentence>
                <caps:sentence id="src116" class="srcSentence"> If you generated your tenant key in a Thales HSM, to back up the key, just back up the Tokenized Key file, the World file, and the Administrator Cards.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src117" class="srcSentence">If you transferred your key by following the procedures in the <link xlink:href="f0d33c5f-a6a6-44a1-bdec-5be1bc8e1e14#BKMK_ImplementBYOK">Implementing bring your own key (BYOK)</link> section from the <link xlink:href="f0d33c5f-a6a6-44a1-bdec-5be1bc8e1e14">Planning and operations for your Azure Rights Management tenant key</link> topic, Azure RMS will persist the Tokenized Key File, to protect against failure of any Azure RMS nodes.</caps:sentence>
                <caps:sentence id="src118" class="srcSentence"> However, do not consider this to be a full backup.</caps:sentence>
                <caps:sentence id="src119" class="srcSentence"> For example, if you ever need a plaintext copy of your key to use outside a Thales HSM, Azure RMS will not be able to retrieve it for you because it only has a non-recoverable copy.</caps:sentence>
              </para>
            </content>
          </section>
          <section address="BKMK_BYOKExport">
            <title>
              <caps:sentence id="src120" class="srcSentence">Export your tenant key</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src121" class="srcSentence">If you use BYOK, you cannot export your tenant key from Azure RMS.</caps:sentence>
                <caps:sentence id="src122" class="srcSentence"> The copy in Azure RMS is non-recoverable.</caps:sentence>
                <caps:sentence id="src123" class="srcSentence"> If you want to delete this key so it can no longer be used, contact Microsoft Customer Service Support (CSS).</caps:sentence>
              </para>
            </content>
          </section>
          <section address="BKMK_BYOKBreach">
            <title>
              <caps:sentence id="src124" class="srcSentence">Respond to a breach</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src125" class="srcSentence">No security system, no matter how strong, is complete without a breach response process.</caps:sentence>
                <caps:sentence id="src126" class="srcSentence"> Your tenant key might be compromised or stolen.</caps:sentence>
                <caps:sentence id="src127" class="srcSentence"> Even when it’s well protected well, vulnerabilities might be found in current generation HSM technology or current key lengths and algorithms.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src128" class="srcSentence">Microsoft has a dedicated team to respond to security incidents in its products and services.</caps:sentence>
                <caps:sentence id="src129" class="srcSentence"> As soon as there is a credible report of an incident, this team engages to investigate the scope, root cause, and mitigations.</caps:sentence>
                <caps:sentence id="src130" class="srcSentence"> If this incident affects your assets, then Microsoft will notify your Azure RMS tenant administrators by email by using the address that you supplied when you subscribed.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src131" class="srcSentence">If you have a breach, the best action that you or Microsoft can take  depends on the scope of the breach; Microsoft will work with you through this process.</caps:sentence>
                <caps:sentence id="src132" class="srcSentence"> The following table shows some typical situations and the likely response, although the exact response will depend on all the information that is revealed during the investigation.</caps:sentence>
              </para>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src133" class="srcSentence">Incident description</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src134" class="srcSentence">Likely response</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src135" class="srcSentence">Your tenant key is leaked.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src136" class="srcSentence">Re-key your tenant key.</caps:sentence>
                        <caps:sentence id="src137" class="srcSentence"> See the <link xlink:href="1284d0ee-0a72-45ba-a64c-3dcb25846c3d#BKMK_BYOKRekey">Re-key your tenant key</link> section in this topic.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src138" class="srcSentence">An unauthorized individual or malware got rights to use your tenant key but the key itself did not leak.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src139" class="srcSentence">Re-keying your tenant key does not help here and requires root-cause analysis.</caps:sentence>
                        <caps:sentence id="src140" class="srcSentence"> If a process or software bug was responsible for the unauthorized individual to get access, that situation must be resolved.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src141" class="srcSentence">Vulnerability discovered in the current-generation HSM technology.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src142" class="srcSentence">Microsoft must update the HSMs.</caps:sentence>
                        <caps:sentence id="src143" class="srcSentence"> If there is reason to believe that the vulnerability exposed keys, then Microsoft will instruct all customers to renew their tenant keys.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src144" class="srcSentence">Vulnerability discovered in the RSA algorithm, or key length, or brute-force attacks become computationally feasible.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src145" class="srcSentence">Microsoft must update the Azure RMS to support new algorithms and longer key lengths that are resilient, and instruct all customers to renew their tenant keys.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
        </sections>
      </section>
      <relatedTopics>
        <link xlink:href="18564e4a-9364-4ed2-8f17-89d24fc0d878">Using Azure Rights Management</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>