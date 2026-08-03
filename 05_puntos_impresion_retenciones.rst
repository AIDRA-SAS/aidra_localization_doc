=============================================
Puntos de Impresión y Diario de Retenciones
=============================================

.. _localizations/ecuador/printer-points:

Puntos de Impresión
-------------------

Los *puntos de impresión* necesitan configurarse para cada tipo de documento electrónico
utilizado, como facturas de clientes, notas de crédito y notas de débito.

Para configurar puntos de impresión, navegue a :menuselection:`Contabilidad --> Configuración -->
Diarios`. Para cada documento electrónico, haga clic en :guilabel:`Nuevo` e ingrese la siguiente
información en el formulario del diario:

- :guilabel:`Nombre del Diario`: Ingrese en este formato:
  `[Entidad de Emisión]-[Punto de Emisión] [Tipo de Documento]`,
  por ejemplo, `001-001 Documentos de Venta`.
- :guilabel:`Tipo`: Se refiere al tipo de diario; seleccione :guilabel:`Ventas`.

Una vez seleccionado el :guilabel:`Tipo`, complete los siguientes campos:

- :guilabel:`¿Usar Documentos?`: Active esta opción si se usa facturación legal (facturas,
  notas de débito/crédito), ya que esta es la configuración estándar. Si no, seleccione la
  opción para registrar asientos contables no relacionados con documentos de facturación legal,
  como recibos, pagos de impuestos o asientos de diario.
- :guilabel:`Entidad de Emisión`: Ingrese el número de la instalación.
- :guilabel:`Punto de Emisión`: Ingrese el punto de impresión.
- :guilabel:`Dirección de Emisión`: Ingrese la dirección de la instalación.

En la pestaña :guilabel:`Asientos Contables`, bajo la sección :guilabel:`Información Contable`,
complete los siguientes campos:

- :guilabel:`Cuenta de Ingresos Predeterminada`: Ingrese la cuenta de ingresos predeterminada.
- :guilabel:`Secuencia Dedicada de Nota de Crédito`: Active esta opción si las *notas de
  crédito* deben generarse desde este punto de impresión (es decir, el diario).
- :guilabel:`Secuencia Dedicada de Nota de Débito`: Active esta opción si las *notas de débito*
  deben generarse desde este punto de impresión (es decir, el diario).
- :guilabel:`Código Corto`: Ingrese un código único de 5 dígitos para la secuencia de asientos
  contables (por ejemplo, VT001).

Las facturas de clientes, notas de crédito y notas de débito deben usar el mismo diario que el
:guilabel:`Punto de Emisión`, mientras que la :guilabel:`Entidad de Emisión` debe ser única por
diario.

Finalmente, en la pestaña :guilabel:`Configuración Avanzada`, marque la casilla de
:guilabel:`Facturación Electrónica` para habilitar el envío de facturas XML/EDI.

.. seealso::
   :doc:`../applications/finance/accounting/customer_invoices/electronic_invoicing`

.. _localizations/ecuador/withholding:

Diario de Retenciones
---------------------

Para definir un *diario de retenciones*, vaya a
:menuselection:`Contabilidad --> Configuración --> Diarios`. Para cada diario de retenciones,
haga clic en :guilabel:`Nuevo` e ingrese la siguiente información:

- :guilabel:`Nombre del Diario`: Ingrese este formato:
  `[Entidad de Emisión]-[Punto de Emisión] [Tipo de Documento]`,
  por ejemplo, `001-001 Retención`.
- :guilabel:`Tipo`: Se refiere al tipo de diario. Seleccione :guilabel:`Misceláneos`.
- :guilabel:`Tipo de Retención`: Seleccione :guilabel:`Retención de Compra`.

Una vez seleccionado el :guilabel:`Tipo` y el :guilabel:`Tipo de Retención`, complete los
siguientes campos:

- :guilabel:`Entidad de Emisión`: Ingrese el número de la instalación.
- :guilabel:`Punto de Emisión`: Ingrese el punto de impresión.
- :guilabel:`Dirección de Emisión`: Ingrese la dirección de la instalación.

En la pestaña :guilabel:`Asientos Contables`, bajo la sección :guilabel:`Información Contable`,
complete los siguientes campos:

- :guilabel:`Cuenta Predeterminada`: Configure la cuenta de ingresos predeterminada.
- :guilabel:`Código Corto`: Ingrese un código único de 5 dígitos para la secuencia de asientos
  contables (por ejemplo, `WT001`).

Finalmente, en la pestaña :guilabel:`Configuración Avanzada`, marque la casilla de
:guilabel:`Facturación Electrónica` para habilitar el envío de facturas XML/EDI.

.. seealso::
   - :doc:`04_documentos_electronicos_retenciones`
   - :doc:`06_reportes`
