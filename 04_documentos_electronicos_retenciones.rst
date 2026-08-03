==============================================
Documentos Electrónicos y Retención de IVA
==============================================

.. _localizations/ecuador/electronic-documents:

Documentos Electrónicos
-----------------------

Para cargar la información de los documentos electrónicos, vaya a
:menuselection:`Contabilidad --> Configuración --> Configuración` y desplácese hasta la sección
:guilabel:`Localización Ecuador`.

Configure la siguiente información, comenzando con la sección :guilabel:`Facturación Electrónica`:

- :guilabel:`Nombre Legal de la Empresa`
- :guilabel:`Régimen`: Seleccione si la empresa está en el :guilabel:`Régimen Regular (sin
  mensajes adicionales en el RIDE)` o está calificada como :guilabel:`Régimen RIMPE`.
- :guilabel:`Número de Contribuyente Especial`: Si la empresa está calificada como
  contribuyente especial, complete este campo con el número de contribuyente correspondiente.
- :guilabel:`Obligada a Llevar Contabilidad`: Active esta opción si es necesario.

Sección :guilabel:`Retenciones`:

- :guilabel:`Bienes Consumibles`: Ingrese el código del impuesto de retención predeterminado
  que se utiliza al comprar bienes.
- :guilabel:`Servicios`: Ingrese el código del impuesto de retención predeterminado que se
  utiliza al comprar servicios.
- :guilabel:`Tarjeta de Crédito`: Ingrese el código del impuesto de retención predeterminado
  que se utiliza al comprar con tarjetas de crédito.
- :guilabel:`Número de Agente de Retención`: Ingrese el número de resolución de agente de
  retención de la empresa, si aplica.

Sección :guilabel:`Conexión SRI`:

- :guilabel:`Archivo de Certificado para SRI`: Seleccione el :guilabel:`Certificado SRI` de la
  empresa. Haga clic en :icon:`oi-arrow-right` :guilabel:`Certificados SRI` para cargar uno,
  si es necesario.
- :guilabel:`Usar servidores de producción`: Active esta opción si los documentos electrónicos
  se utilizan en el entorno de producción; déjela deshabilitada si se utiliza el entorno de
  pruebas.

Sección :guilabel:`Cuentas de Retención`:

- :guilabel:`Cuenta Base de Impuesto de Ventas`: Ingrese la cuenta base de impuesto de ventas
  de la empresa.
- :guilabel:`Cuenta Base de Impuesto de Compras`: Ingrese la cuenta de compra de impuesto base
  de ventas de la empresa.

.. important::
   Al usar el entorno de pruebas, los datos EDI se envían a servidores de prueba.

.. note::
   - Los valores ingresados en los campos de retención de :guilabel:`Bienes Consumibles` y
     :guilabel:`Servicios` se utilizan como valores predeterminados para ventas nacionales
     **solo cuando** no hay retenciones configuradas en el *Tipo de Contribuyente SRI*.
   - El valor de retención de :guilabel:`Tarjeta de Crédito` ingresado se aplica siempre que se
     utilize un método de pago SRI con tarjeta de crédito o débito.

.. _localizations/ecuador/vat-withholding:

Retención de IVA
----------------

.. note::
   Esta configuración aplica solo si el SRI reconoce a la empresa como agente de retención. Si
   no lo es, omita este paso.

Para configurar una retención de IVA, vaya a
:menuselection:`Contabilidad --> Configuración --> Tipo de Contribuyente SRI`. Luego, configure
el :guilabel:`Nombre` del tipo de contribuyente, la :guilabel:`Retención de IVA de Bienes` y la
:guilabel:`Retención de IVA de Servicios`.

.. tip::
   Si el :guilabel:`Tipo de Contribuyente` es :guilabel:`Rimpe`, configure el porcentaje de
   :guilabel:`Retención de Ganancias`.

.. seealso::
   - :doc:`05_puntos_impresion_retenciones`
   - :doc:`07_documentos_venta`
