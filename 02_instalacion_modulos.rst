========================
Instalación de Módulos
========================

.. _localizations/ecuador/module-installation:

:doc:`Instale </applications/general/apps_modules>` los siguientes módulos para obtener todas las
características de la localización ecuatoriana:

.. list-table::
   :header-rows: 1
   :widths: 25 25 50

   * - Nombre
     - Nombre técnico
     - Descripción
   * - :guilabel:`Ecuadorian - Accounting`
     - `l10n_ec`
     - El :doc:`paquete de localización fiscal <../applications/finance/fiscal_localizations>` por
       defecto agrega características contables para la localización ecuatoriana, que representan
       la configuración mínima requerida para que una empresa opere en Ecuador según las directrices
       del :abbr:`SRI (Servicio de Rentas Internas)`. La instalación del módulo carga
       automáticamente: un plan de cuentas, impuestos, tipos de documentos y tipos de soporte
       fiscal. Además, la generación de formularios 103 y 104 es automática.
   * - :guilabel:`Ecuadorian Accounting EDI`
     - `l10n_ec_edi`
     - Incluye todos los requisitos técnicos y funcionales para generar y validar
       :doc:`Documentos Electrónicos <../applications/finance/accounting/customer_invoices/electronic_invoicing>` basados en la documentación técnica publicada por el SRI. Los documentos autorizados son: Facturas, Notas de Crédito, Notas de Débito, Retenciones y Liquidaciones de Compra.
   * - :guilabel:`Ecuadorian Accounting Reports`
     - `l10n_ec_reports`
     - Incluye todos los requisitos técnicos y funcionales para generar los formularios 103 y 104.
   * - :guilabel:`Ecuador - ATS Report`
     - `l10n_ec_reports_ats`
     - Incluye todos los requisitos técnicos y funcionales para generar el archivo XML del reporte
       ATS listo para ser cargado en el *DIMM Formularios*.
   * - :guilabel:`Ecuadorian Website`
     - `l10n_ec_website_sale`
     - Incluye todos los requisitos técnicos y funcionales para generar facturas electrónicas
       automáticas a partir de una venta en el sitio web.
   * - :guilabel:`Ecuadorian Point of Sale`
     - `l10n_ec_edi_pos`
     - Incluye todos los requisitos técnicos y funcionales para generar facturas electrónicas
       automáticas a partir de una venta en el Punto de Venta.
   * - :guilabel:`Ecuadorian Delivery Guide`
     - `l10n_ec_edi_stock`
     - Incluye todos los requisitos técnicos y funcionales para generar
       :ref:`guías de despacho electrónicas <localizations/ecuador/electronic-delivery-guide>`.

.. note::
   En algunos casos, como al actualizar a una versión con módulos adicionales, esos módulos pueden
   no instalarse automáticamente. Cualquier módulo faltante puede
   :doc:`instalarse manualmente </applications/general/apps_modules>`.

.. seealso::
   :doc:`/applications/hr/payroll/payroll_localizations` se documentan por separado.

.. seealso::
   - :doc:`01_introduccion_glosario`
   - :doc:`03_configuracion_general`
