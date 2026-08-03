======================
Reembolso de Gastos
======================

.. _localizations/ecuador/expense-reimbursement:

Los reembolsos de gastos aplican a los siguientes casos:

- :guilabel:`Individual`: reembolso a un empleado por gastos varios (por ejemplo,
  liquidaciones de compra)
- :guilabel:`Persona Jurídica`: reembolso por gastos incurridos, como gastos de representación
  (por ejemplo, contratar un abogado)

Para habilitar el reembolso de gastos, asegúrese de que se haya creado un
:ref:`diario de liquidación de compra <localizations/ecuador/purchase-liquidation>` para un
individuo o un :ref:`diario de facturas de proveedor
<localizations/ecuador/vendor-bill>` para una persona jurídica.

.. note::
   En el diario de facturas de proveedor, asegúrese de que las siguientes configuraciones
   necesarias estén establecidas para una persona jurídica:

   - Seleccione :guilabel:`Compra` como :guilabel:`Tipo`.
   - **No** marque la casilla :guilabel:`Liquidaciones de Compra`.
   - Agregue una :guilabel:`Cuenta de Gastos Predeterminada`.

Luego, para crear un reembolso, :ref:`cree una factura de proveedor
<localizations/ecuador/vendor-bill>` usando el diario de *liquidación de compra* o *facturas de
proveedor*. En la factura de proveedor, configure los siguientes campos:

- :guilabel:`Proveedor`: Este campo debe ser un empleado.
- :guilabel:`Tipo de Documento`: Verifique que este campo esté completado correctamente desde
  el diario.
- :guilabel:`Método de Pago (SRI)`: Seleccione un método de pago.
- :guilabel:`Pestaña Líneas de Reembolso`: Haga clic en :guilabel:`Auto-completar Líneas de
  Factura` para completar automáticamente las líneas de la factura o agregue los gastos línea
  por línea, y proporcione los siguientes detalles para cada gasto:

  - :guilabel:`Socio o número de autorización`
  - :guilabel:`Fecha`
  - :guilabel:`Tipo de Documento`
  - :guilabel:`Número de Documento`
  - :guilabel:`Base Imponible`
  - :guilabel:`Impuesto`

Luego, haga clic en :guilabel:`Confirmar Factura de Proveedor` y :guilabel:`Procesar Ahora`. El
XML y el número de autorización para la liquidación de compra se registran, y la retención de
compra creada desde esta factura de proveedor incluye la información del reembolso.

.. image:: ecuador/l10n-ec-individual-flow.png
   :alt: Reembolso de Gastos.

.. seealso::
   - :doc:`08_documentos_compra`
   - :doc:`07_documentos_venta`
