==========
Reportes
==========

.. _localizations/ecuador/reporting:

Las empresas ecuatorianas presentan reportes fiscales al SRI, y Odoo soporta dos principales:
**reportes 103** y **104**.

Para obtener estos reportes, vaya a :menuselection:`Contabilidad --> Reportes --> Declaración de
Impuestos`. Haga clic en el ícono :icon:`fa-book` :guilabel:`Reporte:` y seleccione `103 (EC)` o
`104 (EC)`.

.. _localizations/ecuador/report-103:

Reporte 103
~~~~~~~~~~~

Este reporte detalla las retenciones del impuesto a la renta en un período dado y puede
declararse mensual o semestralmente. Incluye información sobre la base, los montos del impuesto
y los códigos de impuestos, y puede utilizarse para la declaración ante el SRI.

.. _localizations/ecuador/report-104:

Reporte 104
~~~~~~~~~~~

Este reporte detalla el IVA y la retención de IVA en un período dado y puede generarse mensual o
semestralmente. Incluye información sobre la base, los montos del impuesto y los códigos de
impuestos, y puede utilizarse para la declaración ante el SRI.

.. _localizations/ecuador/ats:

Reporte ATS
~~~~~~~~~~~

Para habilitar la descarga del reporte :abbr:`ATS (Anexo Transaccional Simplificado)` en formato
XML, :doc:`instale </applications/general/apps_modules>` el módulo *ATS Report*
(`l10n_ec_reports_ats`).

.. note::
   El módulo *ATS Report* ecuatoriano depende de la instalación previa de la aplicación
   *Contabilidad* y del *Módulo EDI Ecuadoriano*.

.. _localizations/ecuador/ats-configuration:

Configuración del ATS
*********************

Para emitir documentos electrónicos, asegúrese de que la empresa esté configurada como se
explica en la sección de :ref:`factura electrónica <localizations/ecuador/company-contact>`. En
el :abbr:`ATS (Anexo Transaccional Simplificado)`, se incluye cada documento generado en Odoo,
como :ref:`facturas <localizations/ecuador/customer-invoice>`, :ref:`facturas de proveedor
<localizations/ecuador/vendor-bill>`, :ref:`retenciones de ventas
<localizations/ecuador/customer-withholdings>` y :ref:`retenciones de compras
<localizations/ecuador/purchase-withholding>`, :ref:`notas de crédito
<localizations/ecuador/credit-notes>`, y :ref:`notas de débito
<localizations/ecuador/debit-notes>`.

.. _localizations/ecuador/ats-vendor-bills:

Facturas de Proveedor
^^^^^^^^^^^^^^^^^^^^^

Al generar una :ref:`factura de proveedor <localizations/ecuador/vendor-bill>`, registre el
número de autorización de la factura del proveedor. Para hacerlo, vaya a
:menuselection:`Contabilidad --> Proveedores --> Facturas` y seleccione la factura. Luego,
ingrese el número de la factura del proveedor en el campo :guilabel:`Número de Autorización`.

.. _localizations/ecuador/ats-credit-debit-notes:

Notas de Crédito y Débito
^^^^^^^^^^^^^^^^^^^^^^^^^

Al crear una :ref:`nota de crédito <localizations/ecuador/credit-notes>` o :ref:`nota de débito
<localizations/ecuador/debit-notes>` manualmente o a través de una importación, vincúlela a la
factura de venta que modifica.

.. note::
   Se requiere cierta información en los documentos antes de descargar el archivo
   :abbr:`ATS (Anexo Transaccional Simplificado)`. Por ejemplo, agregue el *Número de
   Autorización* y el *Método de Pago SRI* a los documentos cuando sea necesario.

.. _localizations/ecuador/ats-xml-generation:

Generación de XML
*****************

Para generar el reporte :abbr:`ATS (Anexo Transaccional Simplificado)`, vaya a
:menuselection:`Contabilidad --> Reportes --> Declaración de Impuestos`. Elija un período para
el reporte :abbr:`ATS (Anexo Transaccional Simplificado)` deseado, luego haga clic en
:guilabel:`ATS`. Luego, cargue el archivo XML descargado en *DIMM Formularios*.

.. note::
   Al descargar el reporte :abbr:`ATS (Anexo Transaccional Simplificado)`, Odoo genera una
   ventana emergente de advertencia alertando al usuario si un documento tiene datos faltantes o
   incorrectos. Sin embargo, el archivo XML aún puede descargarse.

.. seealso::
   - :doc:`04_documentos_electronicos_retenciones`
   - :doc:`07_documentos_venta`
   - :doc:`08_documentos_compra`
