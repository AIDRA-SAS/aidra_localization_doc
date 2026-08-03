===================================
Configuración General de la Localización
===================================

.. _localizations/ecuador/specifics:

El paquete de localización ecuatoriana garantiza el cumplimiento de las regulaciones fiscales y
contables ecuatorianas. Incluye herramientas para gestionar impuestos, posiciones fiscales,
reportes y un plan de cuentas predefinido adaptado a los estándares de Ecuador.

El paquete de localización ecuatoriana proporciona las siguientes características clave para
garantizar el cumplimiento de las regulaciones fiscales y contables locales:

- :doc:`../applications/finance/accounting/get_started/chart_of_accounts`: una estructura
  predefinida alineada con los últimos estándares de la *Superintendencia de Compañías* de
  Ecuador, organizada en múltiples categorías y totalmente compatible con la contabilidad NIIF
- :ref:`Productos <localizations/ecuador/products>`
- :ref:`Impuestos <localizations/ecuador/taxes>`: tasas de impuestos preconfiguradas, incluyendo
  IVA estándar, tasa cero y exentas
- :doc:`../applications/finance/accounting/taxes/fiscal_positions`: ajustes automáticos de
  impuestos según el estado de registro del cliente o proveedor
- :ref:`Tipos de documento <localizations/ecuador/document types>`: clasificación de
  transacciones como *facturas de clientes* y *facturas de proveedores* utilizando tipos de
  documentos definidos por el gobierno establecidos por el SRI (autoridad tributaria de Ecuador)
- :ref:`Empresa y contactos <localizations/ecuador/company-contact>`
- :ref:`Documentos electrónicos <localizations/ecuador/electronic-documents>`
- :ref:`Retención de IVA <localizations/ecuador/vat-withholding>`
- :ref:`Puntos de impresión <localizations/ecuador/printer-points>`
- :ref:`Retenciones <localizations/ecuador/withholding>`
- :ref:`Reportes <localizations/ecuador/reporting>`

.. _localizations/ecuador/products:

Productos
---------

Si los productos tienen algún :doc:`impuesto de retención <../applications/finance/accounting/taxes/retention>`,
deben configurarse en el formulario del producto. Para hacerlo, vaya a
:menuselection:`Contabilidad --> Proveedores --> Productos`. En la pestaña
:guilabel:`Información General`, especifique tanto :guilabel:`Impuestos de Compra` como
:guilabel:`Retención de Ganancias`.

.. _localizations/ecuador/taxes:

Impuestos
---------

Para gestionar impuestos, navegue a :menuselection:`Contabilidad --> Configuración --> Impuestos`.
Dependiendo del tipo de impuesto, las siguientes opciones pueden ser necesarias para una
configuración adicional:

- :guilabel:`Nombre del Impuesto`: Sigue un formato específico dependiendo del tipo de impuesto:

  - | **Para IVA (Impuesto al Valor Agregado)**:
    | `IVA [porcentaje] (104, [código de formulario] [código de soporte fiscal] [nombre corto del soporte fiscal])`
    | Ejemplo: `IVA 12% (104, RUC [código de soporte fiscal] IVA)`
  - | **Para códigos de retención del Impuesto a la Renta**:
    | `Código ATS [porcentaje de retención] [nombre de retención]`
    | Ejemplo: `Código ATS 10% Retención a la Fuente`

- :guilabel:`Soporte Fiscal`: Configure solo para el impuesto de IVA. Esta opción se utiliza
  para registrar retenciones de compra.
- :guilabel:`Código ATS`: Configure solo para códigos de retención del impuesto a la renta, ya
  que es necesario para registrar una retención.

En la pestaña :guilabel:`Definición`:

- :guilabel:`Cuadrículas de Impuestos`: Configure el código de un formulario 104 si es un
  impuesto de IVA, y el código de un formulario 103 si es un código de retención del impuesto
  a la renta.

.. seealso::
   :doc:`Configuración de impuestos <../applications/finance/accounting/taxes>`

.. _localizations/ecuador/document types:

Tipos de Documentos
-------------------

Para acceder o configurar los tipos de documentos, vaya a
:menuselection:`Contabilidad --> Configuración --> Tipos de Documentos`. Cada tipo de documento
puede tener una secuencia única por diario donde se asigna. Como parte de la localización, el
tipo de documento incluye el país donde es aplicable; además, los datos se crean automáticamente
cuando se instala el módulo de localización. La información requerida para los tipos de
documentos está incluida por defecto y no necesita ser modificada.

.. _localizations/ecuador/company-contact:

Empresa y Contactos
-------------------

.. seealso::
   :doc:`Configurar un contacto de empresa o individuo <../../applications/essentials/contacts>`

Los siguientes campos deben completarse para fines de localización en el formulario del contacto:

- :guilabel:`Nombre`: Ingrese el nombre de la empresa o individuo.
- :guilabel:`Dirección`: El subcampo :guilabel:`Calle` es obligatorio para confirmar facturas
  electrónicas.
- :guilabel:`Número de Identificación`: Para una empresa, ingrese el :guilabel:`RUC`. Para
  individuos, ingrese el número de :guilabel:`Cédula` o :guilabel:`Pasaporte`.
- :guilabel:`Tipo de Contribuyente SRI`: Seleccione el tipo de contribuyente SRI del contacto.
- :guilabel:`Teléfono`: Ingrese el número de teléfono de la empresa o individuo.
- :guilabel:`Correo Electrónico`: Ingrese el correo electrónico de la empresa o individuo. Este
  correo se utiliza para enviar documentos electrónicos, como facturas.

.. note::
   El :guilabel:`Tipo de Contribuyente SRI` indicado en el formulario del contacto determina
   qué :ref:`retenciones de IVA y de ganancias <localizations/ecuador/vat-withholding>` se
   aplican cuando se usa este contacto en una factura de proveedor.

.. seealso::
   - :doc:`04_documentos_electronicos_retenciones`
   - :doc:`05_puntos_impresion_retenciones`
