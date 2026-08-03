====================================
Guía de Despacho Electrónica
====================================

.. _localizations/ecuador/electronic-delivery-guide:

Una *Guía de Despacho Electrónica* en Ecuador es un documento legal que respalda el
transporte de bienes o mercancías de un lugar a otro dentro del territorio nacional. Es emitida
por el remitente de los bienes y tiene como objetivo registrar y justificar el movimiento de
productos para evitar problemas legales o fiscales. Es un requisito fiscal mandatado por el
*Servicio de Rentas Internas (SRI)*.

.. important::
   Asegúrese de :doc:`instalar </applications/general/apps_modules>` el módulo
   :guilabel:`Guía de Despacho Ecuadoriana` (`l10n_ec_edi_stock`).

.. _localizations/ecuador/transporter:

Transportista
-------------

Para crear un nuevo transportista, primero :doc:`cree un nuevo contacto
<../../applications/essentials/contacts>` y complete la información del contacto como
:guilabel:`Empresa`. Asegúrese de que los siguientes campos estén completos:

- :guilabel:`Número de Identificación`: Seleccione :guilabel:`RUC` y escriba el número de RUC
  del transportista.
- :guilabel:`Tipo de Contribuyente SRI`: Seleccione :guilabel:`Compañías - Personas Jurídicas`
  como la posición del socio en la pirámide de impuestos para automatizar el cálculo de
  retenciones de IVA.

.. image:: ecuador/l10n-ec-carrier-contact.png
   :alt: Configuración de un contacto de transportista.

.. _localizations/ecuador/certificate-file:

Archivo de Certificado para SRI
--------------------------------

Para cargar el archivo de certificado para SRI, vaya a
:menuselection:`Contabilidad --> Configuración --> Configuración`, desplácese hasta la sección
:guilabel:`Localización Ecuador` y haga clic en :icon:`oi-arrow-right`
:guilabel:`Certificados SRI` en la sección :guilabel:`Conexión SRI`. Luego, para crear un nuevo
certificado, haga clic en :guilabel:`Nuevo` y complete los siguientes campos:

- :guilabel:`Nombre`: El título del certificado.
- :guilabel:`Certificado`: Use el botón :guilabel:`Subir su archivo` para cargar el certificado
  SRI.
- :guilabel:`Contraseña del Certificado`: Incluya la contraseña para descifrar el archivo PKS
  si se requiere.

Una vez creado el certificado, haga clic en :guilabel:`Configuración` para volver a la
configuración y asegúrese de que el certificado esté seleccionado en el campo
:guilabel:`Archivo de Certificado para SRI` y que la casilla :guilabel:`Usar servidores de
producción` esté marcada.

.. _localizations/ecuador/warehouse-configuration:

Configuración del Almacén
--------------------------

Para configurar un almacén, primero :doc:`cree un nuevo almacén
<../../applications/inventory_and_mrp/inventory/warehouses_storage/inventory_management/warehouses>`.
Ingrese los siguientes datos para cada almacén que genere una guía de despacho electrónica:

- :guilabel:`Entidad de Emisión`: el número de entidad de emisión dado por el SRI
- :guilabel:`Punto de Emisión`: el número de punto de emisión dado por el SRI
- :guilabel:`Siguiente Número de Guía de Despacho`: el número de seguimiento de reenvío
  (editable después de la primera guardada del almacén).

.. _localizations/ecuador/generate-electronic-delivery:

Generar una Guía de Despacho Electrónica
-----------------------------------------

Una vez que se crea la :doc:`entrega
<../../applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration>` desde
el inventario durante el flujo de trabajo de ventas, asegúrese de que los siguientes campos
estén completos en la sección :guilabel:`Guía de Despacho` en la pestaña
:guilabel:`Información Adicional`:

- :guilabel:`Transportista`: Ingrese el :ref:`contacto <localizations/ecuador/transporter>`
  creado.
- :guilabel:`Número de Placa`: Ingrese el número de placa del vehículo.
- :guilabel:`Motivo de Transferencia`: Por defecto, se establece :guilabel:`Despacho de bienes`;
  modifique según sea necesario.
- :guilabel:`Fecha de Inicio`: Se establece automáticamente en la fecha de creación (editable).
- :guilabel:`Fecha de Fin`: Se establece automáticamente a 15 días después de la fecha de
  inicio (editable).

.. image:: ecuador/l10n-ec-delivery-guide-settings.png
   :alt: Configuración de la Guía de Despacho.

Haga clic en :guilabel:`Validar`, luego en :guilabel:`Generar Guía de Despacho`. Posteriormente,
la siguiente información estará disponible en la sección :guilabel:`Guía de Despacho`:

- :guilabel:`Fecha de Autorización`: fecha en que el gobierno autoriza el documento.
- :guilabel:`Número de Autorización`: número de autorización EDI (igual que la clave de acceso).
- :guilabel:`Estado de la Guía de Despacho`: estado de la guía de despacho.

.. image:: ecuador/l10n-ec-authorization-number.png
   :alt: Número de autorización.

Para recibir el XML y PDF, se puede enviar un correo electrónico al contacto utilizado en el
campo :guilabel:`Dirección de Entrega` - este es un paso opcional y manual; se debe hacer clic
en el botón :guilabel:`Enviar Correo Electrónico`.

.. image:: ecuador/l10n-ec-delivery-guide-pdf.png
   :alt: PDF de la Guía de Despacho.

.. seealso::
   - :doc:`07_documentos_venta`
   - :doc:`08_documentos_compra`
