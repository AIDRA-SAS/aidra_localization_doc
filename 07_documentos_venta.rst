===================
Documentos de Venta
===================

.. _localizations/ecuador/sales-documents:

.. _localizations/ecuador/customer-invoice:

Factura de Cliente
------------------

Las facturas de cliente, documentos electrónicos
:doc:`creados desde órdenes de venta o manualmente
<../applications/finance/accounting/customer_invoices/overview>`, deben contener los siguientes
datos y, una vez validados, se envían al SRI:

- :guilabel:`Diario`: Seleccione la opción que coincida con el punto de impresión de la factura
  de cliente.
- :guilabel:`Tipo de Documento`: Escriba el tipo de documento en este formato:
  `(01) Factura`.
- :guilabel:`Método de Pago (SRI)`: Seleccione cómo se pagará la factura.

.. _localizations/ecuador/credit-notes:

Nota de Crédito de Cliente
--------------------------

Las :doc:`notas de crédito de cliente <../applications/finance/accounting/customer_invoices/credit_notes>`
son documentos electrónicos que se envían al SRI una vez validados. Las :ref:`notas de crédito
<accounting/credit_notes/issue-credit-note>` solo pueden registrarse desde una factura validada
(contabilizada).

Mantenga el :guilabel:`Tipo de Documento` en :guilabel:`(04) Nota de Crédito` en la ventana de
:guilabel:`Nota de Crédito`.

El proceso para completar una nota de crédito es el mismo que el de completar una
:ref:`factura <accounting/invoice/creation>`.

.. note::
   Al crear la primera nota de crédito, seleccione :guilabel:`Revertir` y asigne el primer
   número de nota de crédito o, por defecto, Odoo asigna `NotCr 001-001-000000001` como el
   primer número de nota de crédito.

.. _localizations/ecuador/debit-notes:

Nota de Débito de Cliente
-------------------------

Las :ref:`notas de débito de cliente <accounting/credit_notes/issue-debit-note>` son documentos
electrónicos que se envían al SRI una vez validados. Solo pueden registrarse desde una factura
validada (contabilizada).

En :guilabel:`Usar Diario Específico` de la ventana :guilabel:`Crear Nota de Débito`,
seleccione el punto de impresión para la nota de crédito o déjelo vacío para usar el mismo
diario que la factura original.

.. _localizations/ecuador/customer-withholdings:

Retención de Cliente
--------------------

Las :guilabel:`retenciones de cliente` son documentos no electrónicos emitidos por el cliente
para aplicar una retención a una venta. Solo pueden registrarse desde una factura validada
(contabilizada).

En la factura, haga clic en :guilabel:`Agregar Retención` y complete la siguiente información en
la ventana :guilabel:`Retención de Cliente`:

- :guilabel:`Número de Documento`: Ingrese el número de retención.
- :guilabel:`Líneas de Retención`: Seleccione los impuestos que el cliente está reteniendo.

Antes de validar la retención, revise que los montos de cada impuesto sean iguales a los del
documento original.

.. seealso::
   - :doc:`08_documentos_compra`
   - :doc:`06_reportes`
