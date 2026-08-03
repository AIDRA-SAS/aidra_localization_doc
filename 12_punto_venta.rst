==============================================
Facturación Electrónica en Punto de Venta
==============================================

.. _localizations/ecuador/point-of-sale:

Asegúrese de que el *Módulo Ecuadoriano para Punto de Venta* (`l10n_ec_edi_pos`) esté
:ref:`instalado <localizations/ecuador/module-installation>` para habilitar las siguientes
características y configuraciones:

- Elegir el método de pago SRI en la configuración de cada método de pago.
- Ingresar manualmente el tipo y número de identificación del cliente al crear un nuevo contacto
  en el *Punto de Venta*.
- Generar automáticamente una factura electrónica válida para Ecuador al finalizar el proceso de
  pago.

.. _localizations/ecuador/payment-method-configuration:

Configuración del Método de Pago
--------------------------------

Para :doc:`crear un método de pago para un punto de venta
<../../applications/sales/point_of_sale/payment_methods>`, vaya a
:menuselection:`Punto de Venta --> Configuración --> Métodos de Pago`. Luego, establezca el
:guilabel:`Método de Pago SRI` en el formulario del método de pago.

.. _localizations/ecuador/invoicing-flow:

Flujos de Facturación
---------------------

.. _localizations/ecuador/identification-type-number:

Tipo y Número de Identificación
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

El cajero del Punto de Venta puede :ref:`crear un nuevo contacto para un cliente
<pos/use/customers>` que solicite una factura desde el registro del Punto de Venta.

El *Módulo Ecuadoriano para Punto de Venta* agrega dos nuevos campos al formulario de creación
de contactos: :guilabel:`Tipo de Identificación` y :guilabel:`RUC/Cédula`.

.. note::
   Como la longitud del número de identificación varía dependiendo del tipo de identificación,
   Odoo verifica automáticamente el campo :guilabel:`RUC/Cédula` al guardar el formulario del
   contacto. Para verificar manualmente que la longitud sea correcta, sepa que los tipos
   :guilabel:`RUC` y :guilabel:`Cédula` requieren 13 y 10 dígitos, respectivamente.

.. _localizations/ecuador/anonymous-end-consumer:

Factura Electrónica: Consumidor Final Anónimo
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Cuando los clientes no solicitan una factura electrónica por su compra, Odoo establece
automáticamente al cliente como :guilabel:`Consumidor Final` y genera una factura electrónica de
todos modos.

.. note::
   Si el cliente solicita una nota de crédito debido a una devolución de este tipo de compra, la
   nota de crédito debe realizarse con la información de contacto real del cliente. Las notas de
   crédito no pueden crearse para *Consumidor Final* y pueden gestionarse
   :ref:`directamente desde el registro del Punto de Venta <pos/use/refund>`.

.. _localizations/ecuador/specific-customer:

Factura Electrónica: Cliente Específico
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Si un cliente solicita una factura por su compra, es posible seleccionar o crear un contacto con
su información fiscal. Esto asegura que la factura se genere con los datos precisos del cliente.

.. note::
   Si el cliente solicita una nota de crédito debido a una devolución de este tipo de compra, el
   proceso de nota de crédito y devolución puede gestionarse
   :ref:`directamente desde el registro del Punto de Venta <pos/use/refund>`.

.. seealso::
   - :doc:`11_ecommerce`
   - :doc:`07_documentos_venta`
