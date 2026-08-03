====================
Documentos de Compra
====================

.. _localizations/ecuador/purchase-documents:

.. _localizations/ecuador/vendor-bill:

Factura de Proveedor
--------------------

Las :doc:`facturas de proveedor <../applications/finance/accounting/vendor_bills>`, documentos
no electrónicos creados desde órdenes de compra o manualmente, requieren un
:ref:`diario de facturas de proveedor <localizations/ecuador/vendor-bills-journal>` específico.

.. _localizations/ecuador/vendor-bills-journal:

Diario de Facturas de Proveedor
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Use la siguiente configuración para establecer el diario de facturas de proveedor:

- Seleccione :guilabel:`Compra` como :guilabel:`Tipo`.
- **No** marque la casilla :guilabel:`Liquidaciones de Compra`.
- Agregue una :guilabel:`Cuenta de Gastos Predeterminada`.

Para configurar una factura de proveedor, asegúrese también de completar los siguientes campos
específicos de Ecuador:

- :guilabel:`Tipo de Documento`: Ingrese este tipo de documento: `(01) Factura`.
- :guilabel:`Número de Documento`: Ingrese el número del documento.
- :guilabel:`Método de Pago (SRI)`: Seleccione cómo pagar la factura de proveedor.

.. important::
   Al crear la retención de compra, verifique que las bases (montos base) sean correctos. Si el
   monto del impuesto en la :guilabel:`Factura de Proveedor` necesita editarse, haga clic en
   :guilabel:`Editar`. O, desde la pestaña :guilabel:`Apuntes Contables`, haga clic en
   :guilabel:`Editar` y establezca el ajuste como desee.

.. _localizations/ecuador/purchase-liquidation:

Liquidación de Compra
---------------------

Las *liquidaciones de compra* son documentos electrónicos que se envían al SRI una vez validados.
Las empresas las emiten cuando realizan una compra, pero el proveedor no proporciona una factura
debido a una o más de las siguientes razones:

- No residentes de Ecuador que prestaron servicios.
- Empresas extranjeras que prestaron servicios sin residencia ni instalación en Ecuador.
- Compra de bienes o servicios de personas naturales no registradas con RUC, que no pueden
  emitir recibos de venta o facturas de clientes.
- Reembolso por compra de bienes o servicios que debe otorgarse a empleados en relación de
  dependencia (empleado a tiempo completo).
- Miembros de órganos colegiados han prestado servicios en el ejercicio de su función.

En estos casos, se debe crear un :ref:`diario de liquidación de compra
<localizations/ecuador/purchase-liquidation-journal>`.

.. _localizations/ecuador/purchase-liquidation-journal:

Crear un Diario de Liquidación de Compra
*****************************************

Para crear un diario de *liquidaciones de compra*, ingrese la siguiente información:

- :guilabel:`Nombre del Diario`: Ingrese este formato:
  `[Entidad de Emisión]-[Punto de Emisión] [Tipo de Documento]`,
  por ejemplo, `001-001 Liquidaciones de Compra`.
- :guilabel:`Tipo`: Se refiere al tipo de diario. Seleccione :guilabel:`Compra`.

Una vez seleccionado el :guilabel:`Tipo`, complete los siguientes campos:

- :guilabel:`Liquidaciones de Compra`: Marque esta casilla para habilitar liquidaciones de
  compra.
- :guilabel:`¿Usar Documentos?`: Active esta opción si se usa facturación legal (facturas,
  notas de débito/crédito), ya que esta es la configuración estándar. Si no, seleccione la
  opción para registrar asientos contables no relacionados con documentos de facturación legal,
  como recibos, pagos de impuestos o asientos de diario.
- :guilabel:`Entidad de Emisión`: Ingrese el número de la instalación.
- :guilabel:`Punto de Emisión`: Ingrese el punto de impresión.
- :guilabel:`Dirección de Emisión`: Ingrese la dirección de la instalación.
- :guilabel:`Código Corto`: Ingrese un código único de 5 dígitos para la secuencia de asientos
  contables (por ejemplo, `PT001`).

Finalmente, en la pestaña :guilabel:`Configuración Avanzada`, marque la casilla de
:guilabel:`Facturación Electrónica` para habilitar el envío de facturas XML/EDI.

.. _localizations/ecuador/purchase-liquidation-creation:

Crear una Liquidación de Compra
*******************************

Las liquidaciones de compra, creadas desde *órdenes de compra* o manualmente desde *facturas de
proveedor*, deben contener los siguientes datos:

- :guilabel:`Proveedor`: Ingrese la información del proveedor.
- :guilabel:`Diario`: Seleccione el diario de :guilabel:`Liquidación de Compra` con el punto de
  impresión correcto.
- :guilabel:`Tipo de Documento`: Ingrese este tipo de documento:
  `(03) Liquidación de Compra`.
- :guilabel:`Número de Documento`: Ingrese el número de documento (secuencia). Esto solo debe
  ingresarse una vez, y la secuencia se asignará automáticamente a los documentos siguientes.
- :guilabel:`Método de Pago (SRI)`: Seleccione cómo pagar la factura.
- :guilabel:`Productos`: Especifique el producto con los impuestos correctos.

Luego, valide la :guilabel:`Liquidación de Compra`.

.. _localizations/ecuador/purchase-withholding:

Retención de Compra
-------------------

Las *retenciones de compra* son documentos electrónicos que se envían al SRI una vez validados.
Solo pueden registrarse desde una factura validada (contabilizada).

En la factura, haga clic en :guilabel:`Agregar Retención` y complete los siguientes campos en la
ventana :guilabel:`Retención`:

- :guilabel:`Número de Documento`: Ingrese el número de documento (secuencia). Esto solo debe
  ingresarse una vez, y la secuencia se asignará automáticamente para los documentos siguientes.
- :guilabel:`Líneas de Retención`: Los impuestos aparecen automáticamente según la
  configuración de productos y proveedores. Revise si los impuestos y el soporte fiscal son
  correctos. Si no, edite y seleccione los impuestos y el soporte fiscal correctos.

Luego, valide la :guilabel:`Retención`.

.. note::
   Los tipos de soporte fiscal deben configurarse en la :guilabel:`Factura de Proveedor`. Para
   hacerlo, vaya al impuesto aplicado en la :guilabel:`Factura de Proveedor` y cambie el
   :guilabel:`Soporte Fiscal` allí.

Un impuesto de retención puede dividirse en dos o más líneas, dependiendo de si se aplican dos o
más porcentajes de retención.

.. example::
   Odoo sugiere una retención de IVA del 30% con soporte fiscal 01. Se puede agregar una
   retención de IVA del 70% en una nueva línea con el mismo soporte fiscal. Odoo lo permite si
   el total de la base coincide con el total de la :guilabel:`Factura de Proveedor`.

.. seealso::
   - :doc:`07_documentos_venta`
   - :doc:`09_reembolso_gastos`
