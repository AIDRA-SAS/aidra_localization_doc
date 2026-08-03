==========
eCommerce
==========

.. _localizations/ecuador/ecommerce:

El :ref:`módulo de Reporte ATS <localizations/ecuador/ats>` habilita lo siguiente:

- Elegir el *Método de Pago SRI* para la configuración de cada método de pago.
- Los clientes pueden ingresar manualmente su tipo y número de identificación durante el proceso
  de pago del eCommerce.
- Generar automáticamente una factura electrónica válida para Ecuador al finalizar el proceso de
  pago.

.. seealso::
   :doc:`Documentación de eCommerce <../../applications/websites/ecommerce>`

.. _localizations/ecuador/online-payments:

Pagos en Línea
--------------

Para habilitar pagos en línea, agregue los :doc:`proveedores de pago <../applications/finance/payment_providers>`
relevantes y configure los :ref:`métodos de pago <payment_providers/payment_methods>` necesarios.
Es obligatorio establecer el :guilabel:`Método de Pago SRI` para cada método.

.. note::
   Agregar el :guilabel:`Método de Pago SRI` es necesario para generar correctamente la factura
   electrónica a partir de una venta de eCommerce. Seleccione un **método de pago** para acceder
   a su menú de configuración y campo.

.. _localizations/ecuador/automatic-invoice:

Factura Automática
------------------

Las :ref:`facturas <ecommerce/handling/invoices>` pueden generarse después del proceso de pago.

.. tip::
   La plantilla de correo electrónico de la factura puede modificarse desde el campo
   :guilabel:`Plantilla de Correo de Factura` bajo la opción :guilabel:`Factura Automática`.

.. important::
   El diario de ventas utilizado para facturar es el primero en la secuencia de prioridad en el
   menú :guilabel:`Diario`.

.. _localizations/ecuador/ecommerce-workflow:

Tipo y Número de Identificación
--------------------------------

Durante el proceso de pago, el cliente que realiza una compra tendrá la opción de indicar su
tipo y número de identificación. Esta información es requerida para generar la factura
electrónica después de que el pago se complete correctamente.

.. note::
   Se realiza una verificación para asegurar que el campo :guilabel:`Número de Identificación`
   esté completado y tenga el número correcto de dígitos. Para identificación de RUC, se
   requieren 13 dígitos, y para Cédula, se requieren 9 dígitos.

Al finalizar el proceso de pago, se genera una factura confirmada, lista para ser enviada
manual o asincrónicamente al SRI.

.. seealso::
   - :doc:`06_reportes`
   - :doc:`12_punto_venta`
