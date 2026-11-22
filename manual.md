
---

<!-- TAG: Pagos, Terminos de pago, Cobro -->
<!-- AUDIENCE: Usuario Final, Cajero -->
<!-- LEVEL: Intermedio -->
<!-- SEARCH: terminos de pago procesar pago modal F4 -->
## 11. Términos de Pago

<!-- TAG: Modal pago, Metodos, Efectivo, Tarjeta -->
<!-- AUDIENCE: Usuario Final, Cajero -->
<!-- LEVEL: Basico -->
<!-- SEARCH: modal terminos de pago contado tarjeta credito transferencia deposito efectivo -->
### 11.1 Modal de Términos de Pago

📷 **Modal de Términos de Pago**  
![Modal Términos de Pago](https://integralbizsolutions.com/manual/img/modal-terminos-pago.png)

Para abrir el modal de pagos:
- Haga clic en el botón **Aplicar** en la barra inferior
- O haga clic directamente en el ícono de pago

**Tipo de pago:**
- **Contado:** Pago completo al momento
- **Crédito:** Pago posterior (genera Cuenta por Cobrar en QuickBooks)

**Métodos de pago disponibles:**
- **Tarjeta de Crédito**
- **Transferencia**
- **Depósito**
- **Certificado de Regalo**
- **Cheque**
- **Efectivo**

<!-- TAG: Pago efectivo, Denominaciones, Cambio -->
<!-- AUDIENCE: Usuario Final, Cajero -->
<!-- LEVEL: Basico -->
<!-- SEARCH: pago efectivo cantidad recibida denominaciones rapidas cambio vuelto -->
### 11.2 Pago en Efectivo

**Campo de Cantidad Recibida:**
- Ingrese el monto recibido en el campo de texto
- Botón **Revertir** para limpiar el campo

**Botones de denominaciones rápidas:**
- Billetes: `500`, `200`, `100`, `50`, `20`
- Monedas: `10`, `1`, `2`, `5`

Al hacer clic en una denominación, se suma al monto recibido automáticamente.

<!-- TAG: Resumen pago, Total, Recibido, Restante, Cambio -->
<!-- AUDIENCE: Usuario Final, Cajero -->
<!-- LEVEL: Basico -->
<!-- SEARCH: resumen pago total pagar total recibido total restante cambio -->
### 11.3 Resumen del Pago

El modal muestra el siguiente resumen:

| Concepto | Descripción |
|----------|-------------|
| **Total a pagar** | Monto total de la factura (ej. `12,392.10`) |
| **Tarjeta de Crédito** | Monto pagado con tarjeta |
| **Transferencia** | Monto pagado por transferencia |
| **Deposito** | Monto pagado por depósito |
| **Certificado de Regalo** | Monto pagado con certificado |
| **Cheque** | Monto pagado con cheque |
| **Efectivo** | Monto pagado en efectivo |
| **Total Recibido** | Suma de todos los pagos registrados |
| **Total Restante** | Saldo pendiente por pagar (en rosa si hay saldo) |
| **Cambio** | Vuelto al cliente (si pagó en efectivo de más) |

<!-- TAG: Opciones pago, Correo, Descuento -->
<!-- AUDIENCE: Usuario Final, Cajero -->
<!-- LEVEL: Basico -->
<!-- SEARCH: opciones pago enviar correo PDF aplicar descuento recibo -->
### 11.4 Opciones adicionales

- **Enviar por correo:** Casilla para enviar el PDF de la factura al email del cliente
- **Aplicar descuento al recibo:** Enlace para aplicar descuento adicional

**Botones de acción:**
- **Aplicar:** Confirma el pago, guarda la factura y la envía a impresión/QuickBooks
- **Cerrar:** Cancela la operación sin guardar

<!-- TAG: Integracion BAC, XpressPago, Tarjeta -->
<!-- AUDIENCE: Usuario Final, Cajero, Administrador -->
<!-- LEVEL: Intermedio -->
<!-- SEARCH: integracion BAC XpressPago tarjeta pinpad transacciones approved payments -->
### 11.5 Integración con BAC XpressPago

Si la empresa tiene dispositivos POS integrados:
- El sistema permite procesar pagos con tarjeta directamente
- Las transacciones se almacenan en `transaccionesBAC`
- Los pagos aprobados se registran en `approvedPayments`
- Requiere configuración previa en Parámetros

---

<!-- TAG: Tipos documento, Factura, Devolucion, Guia -->
<!-- AUDIENCE: Administrador, Usuario Final -->
<!-- LEVEL: Intermedio -->
<!-- SEARCH: tipos documentos disponibles factura devolucion guia orden compra cotizacion -->
## 12. Tipos de Documentos Disponibles

<!-- TAG: Facturas, SalesReceipt, Invoice -->
<!-- AUDIENCE: Usuario Final, Cajero -->
<!-- LEVEL: Basico -->
<!-- SEARCH: facturas SalesReceipt Invoice contado credito -->
### 12.1 Facturas (Point of Sales)

- **SalesReceipt:** Factura de contado (pago inmediato)
- **Invoice:** Factura a crédito (pago posterior, genera Cuenta por Cobrar)

El tipo se determina según el método de pago seleccionado:
- Pago completo = `SalesReceipt`
- Pago parcial o crédito = `Invoice`

<!-- TAG: Devoluciones, CreditMemo -->
<!-- AUDIENCE: Usuario Final, Cajero -->
<!-- LEVEL: Intermedio -->
<!-- SEARCH: devoluciones CreditMemo nota credito retorno -->
### 12.2 Devoluciones

- **CreditMemo:** Nota de crédito o devolución
- Módulo: `devoluciones-app`
- Permite devolver items facturados previamente
- Se vincula con la factura original mediante `Invoice` (TxnID)

<!-- TAG: Guias, Guide -->
<!-- AUDIENCE: Usuario Final, Administrador -->
<!-- LEVEL: Intermedio -->
<!-- SEARCH: guias despacho Guide transporte mercaderia -->
### 12.3 Guías de Despacho

- **Guide:** Guía de transporte de mercadería
- Módulo: `guides-app`
- Requerida para transporte de mercadería según normativa

<!-- TAG: Ordenes Compra, PurchaseOrder -->
<!-- AUDIENCE: Administrador, Compras -->
<!-- LEVEL: Intermedio -->
<!-- SEARCH: ordenes compra PurchaseOrder proveedores adquisiciones -->
### 12.4 Órdenes de Compra

- **PurchaseOrder:** Orden de compra a proveedores
- Módulo: `purchase-orders-app`
- Genera compromiso de compra antes de recibir mercadería

<!-- TAG: Cotizaciones, Estimate -->
<!-- AUDIENCE: Usuario Final, Vendedor -->
<!-- LEVEL: Intermedio -->
<!-- SEARCH: cotizaciones Estimate presupuestos proformas -->
### 12.5 Cotizaciones

- **Estimate:** Cotización o presupuesto
- Módulo: `quotation-app` o `proformas-app`
- Puede convertirse en factura posteriormente (`converted`)

<!-- TAG: Ordenes Venta, SalesOrder -->
<!-- AUDIENCE: Usuario Final, Vendedor -->
<!-- LEVEL: Intermedio -->
<!-- SEARCH: ordenes venta SalesOrder pedidos reservas -->
### 12.6 Órdenes de Venta

- **SalesOrder:** Orden de venta o pedido
- Módulo: `sales-order-app`
- Reserva mercadería antes de la facturación

<!-- TAG: Apartados -->
<!-- AUDIENCE: Usuario Final, Cajero -->
<!-- LEVEL: Intermedio -->
<!-- SEARCH: apartados reservas pagos parciales -->
### 12.7 Apartados

- Módulo: `apartados-app`
- Permite apartar mercadería con pagos parciales
- Similar a SalesOrder pero con flujo de pagos

<!-- TAG: Inventario, Salidas, Entradas -->
<!-- AUDIENCE: Administrador, Bodega -->
<!-- LEVEL: Intermedio -->
<!-- SEARCH: inventario salidas entradas InventoryIssues ajustes stock -->
### 12.8 Gestión de Inventario

- **InventoryIssues:** Salidas de inventario (ajustes, mermas, etc.)
- Módulo: `item-issues-app`
- **Bill:** Registro de gastos/costos
- Módulo: `bill-app`
- **inv-request:** Solicitudes de inventario entre bodegas
- Módulo: `inv-request-app`
- **Check:** Conteos de inventario
- Módulo: `check-app`

---

<!-- TAG: Configuracion, Parametros, Ajustes -->
<!-- AUDIENCE: Administrador, Tecnico -->
<!-- LEVEL: Avanzado -->
<!-- SEARCH: configuracion parametros ajustes del sistema modal -->
## 13. Configuración y Parámetros

<!-- TAG: Acceso configuracion, Modal parametros -->
<!-- AUDIENCE: Administrador, Tecnico -->
<!-- LEVEL: Basico -->
<!-- SEARCH: como acceder a la configuracion modal settings js-modal-settings -->
### 13.1 Acceso a la configuración

La configuración se realiza mediante:
- Modal de settings (`js-modal-settings`)
- Meta datos de usuario en WordPress
- Opciones globales en `get_value_setting()`

<!-- TAG: Parametros clave, Bodega, Formato, Serie -->
<!-- AUDIENCE: Administrador, Tecnico -->
<!-- LEVEL: Intermedio -->
<!-- SEARCH: parametros clave empresa bodega sucursal formato impresion numeros serie -->
### 13.2 Parámetros principales

**Configuración de empresa y bodega:**
- `current_company` - Empresa activa
- `select_site` - Bodega/sitio seleccionado
- `all_sites` - Listado de bodegas disponibles

**Configuración de formato de impresión:**
- `formato_activo` - Formato asignado al usuario
- `documento-meta-box-text` - Nombre del formato (ej. `carta_technos`, `ticket_technos`)
- Ruta de formatos: `wp-content/themes/pdf/Formatos/COMPID/[formato].php`

**Configuración de series:**
- `serials_setting` - Control de series (0 o 1)
  - `0` - No requiere series
  - `1` - Requiere series (cantidad no editable)

**Configuración de cuentas de depósito:**
- `cash-deposit-account` - Cuenta para depósitos en efectivo
- `credit-deposit-account` - Cuenta para depósitos con tarjeta

**Configuración de redondeo:**
- Parámetros de redondeo de precios y totales
- Función `roundUp(number, decimals)` para redondeo hacia arriba

<!-- TAG: Configuracion usuario, Tema, Modulos -->
<!-- AUDIENCE: Administrador, Tecnico -->
<!-- LEVEL: Intermedio -->
<!-- SEARCH: configuracion usuario tema modulo permisos current_theme_user modulos_comprados -->
### 13.3 Configuración de usuario

**Tema/módulo asignado:**
- `current_theme_user` - Módulo activo del usuario (ej. `point-of-sales`)

**Permisos de módulos:**
- `modulos_comprados` - Lista de módulos disponibles para el usuario

**Configuración de versión:**
- `app_version_date` - Fecha de última actualización de la aplicación
- Modal de actualización: `modal-app-version-update`

<!-- TAG: Configuracion documento, Redondeo, Descuentos -->
<!-- AUDIENCE: Administrador, Cajero -->
<!-- LEVEL: Intermedio -->
<!-- SEARCH: configuracion documento redondeo descuentos totales decimales -->
### 13.4 Configuración de documentos

**Redondeo de valores:**
- El sistema permite redondear precios y totales
- Configuración mediante parámetros de redondeo

**Descuentos:**
- **A nivel de línea:** Descuento por item en la tabla de facturación
- **A nivel de documento:** Descuento general en `Descuento Doc.`
- Función `CalcularDescuentosApp()` para calcular descuentos
- Función `PrepararDescuentoDoc()` para aplicar descuento porcentual

**Totales:**
- Función `TotalizarDocumento()` - Calcula totales exactos
- Función `TotalizarDocumentoExactos()` - Calcula totales con precisión
- Función `ClearTotals()` - Limpia todos los totales
- Formateo decimal mediante `RemoveDecimals()`, `RemoveComma()`, `RefreshNumberFormat()`

**Impuestos:**
- Cálculo automático de ISV 15%
- Separación de importes gravados, exentos y exonerados
- `ExentosTotales` - Suma de items exentos (`tax_type="EXE"`)
- `GravadosTotales` - Suma de items gravados

---

<!-- TAG: Sincronizacion, QuickBooks, QB, QBO -->
<!-- AUDIENCE: Administrador, Tecnico -->
<!-- LEVEL: Avanzado -->
<!-- SEARCH: sincronizacion QuickBooks QB QBO TxnID ListID sincronizada pendiente -->
## 14. Sincronización con QuickBooks

<!-- TAG: Modos operacion, QB Desktop, QBO Online -->
<!-- AUDIENCE: Administrador, Tecnico -->
<!-- LEVEL: Intermedio -->
<!-- SEARCH: modos operacion QuickBooks Desktop QB Online QBO OnlineOrDesktop -->
### 14.1 Modos de operación

La aplicación opera en dos modos según la configuración:

**QuickBooks Desktop (QB):**
- Variable: `OnlineOrDesktop="QB"`
- Requiere conector local instalado
- Sincronización mediante archivo de compañía (.QBW)
- Identificadores: `ListID`, `TxnID`
- Nombres: `FullName`, `SalesDesc`

**QuickBooks Online (QBO):**
- Variable: `OnlineOrDesktop="QBO"`
- Sincronización vía API en la nube
- Identificadores: `Id`
- Nombres: `FullyQualifiedName`, `Description`
- Departamentos: `locationqbo`, `Department`

<!-- TAG: Estados sincronizacion, Pendiente, Sincronizado -->
<!-- AUDIENCE: Administrador, Cajero -->
<!-- LEVEL: Basico -->
<!-- SEARCH: estados sincronizacion pendiente sincronizado badge icono sync -->
### 14.2 Estados de sincronización

**En el listado de documentos:**
- **Sincronizado:** Sin indicador especial
- **Pendiente de sincronizar:** Badge amarillo con ícono 🔄 (`far fa-sync`)
- Texto: "Pendiente de sincronizar"

**Campos de control:**
- `sincronizada` - Estado de sincronización
- `sincroStatus` - Estado detallado de sincronización
- `TxnID` - Identificador de transacción en QuickBooks (vacío si no sincronizado)

<!-- TAG: Acciones sincronizacion, Forzar, Manual -->
<!-- AUDIENCE: Administrador, Cajero -->
<!-- LEVEL: Intermedio -->
<!-- SEARCH: acciones sincronizacion forzar sincronizar manual automatico -->
### 14.3 Acciones de sincronización

**Botones de sincronización:**
- **Forzar Sincronización:** Disponible en modo QB (`data-action="sync"`)
- **Sincronizar:** Disponible en modo QBO (`data-action="sync"`)

**Enlace a QuickBooks Online:**
- Botón `open-quickbooks-transaction-button`
- Abre la transacción directamente en QBO
- URL: `https://qbo.intuit.com/app/journal`
- Requiere `TxnID` y `type` del documento

<!-- TAG: Endpoints, API, Guardado -->
<!-- AUDIENCE: Tecnico, Administrador -->
<!-- LEVEL: Avanzado -->
<!-- SEARCH: endpoints API guardado SavePrintedDocument UpdatePrintedDocument ActualizarExistencias -->
### 14.4 Endpoints de sincronización

Según el código, los principales endpoints son:

- `SavePrintedDocument` - Guarda documento nuevo en QuickBooks
- `UpdatePrintedDocument` - Actualiza documento existente
- `ActualizarExistencias` - Actualiza stock de productos
- `CheckUsedSeries` - Valida series únicas
- `SaveDocumentLogging` - Guarda logging de acciones
- `RemoveFile` - Elimina archivos temporales
- `ExecuteProcess` - Ejecuta procesos en servidor

**Proceso de guardado:**
1. Se prepara el documento en `baseToPrint`
2. Se envía al endpoint correspondiente
3. Se valida respuesta (`saved.isValid`)
4. Si hay errores, se muestran en toast (`saved.errors`)
5. Si es exitoso, se registra en logging (`RecordDocumentLogging`)

<!-- TAG: Errores sincronizacion, Validacion -->
<!-- AUDIENCE: Administrador, Tecnico -->
<!-- LEVEL: Intermedio -->
<!-- SEARCH: errores sincronizacion validacion isValid errors toast mensajes -->
### 14.5 Manejo de errores

**Validación de respuesta:**
- `saved.isValid` - Booleano que indica si el guardado fue exitoso
- `saved.errors` - Array de errores (si los hay)
- `saved.response` - Respuesta del servidor

**Mensajes de error:**
- Se muestran mediante `tostao.ShowToast()`
- Tipo: `error`, `warning`, `success`, `info`
- Posición: `toast-top-center`, `toast-top-left`

**Ejemplos de mensajes:**
- Éxito: "Factura sincronizada exitosamente!"
- Error: "No hemos conseguido registrar el Bill"
- Errores múltiples: Se concatenan con `<br>`

---

<!-- TAG: Historial, Documentos, Reportes -->
<!-- AUDIENCE: Administrador, Contador -->
<!-- LEVEL: Intermedio -->
<!-- SEARCH: historial documentos reportes listado detalles ventas -->
## 15. Historial de Documentos

<!-- TAG: Modal historial, Listado documentos -->
<!-- AUDIENCE: Administrador, Contador -->
<!-- LEVEL: Intermedio -->
<!-- SEARCH: modal historial documentos listado filtros tipo estado fecha -->
### 15.1 Modal de Historial de Documentos

📷 **Modal de Historial de Documentos** (referencia del código)

Para acceder al historial:
- El modal se identifica como `modal-history-docs`
- Muestra listado de documentos con DataTables

**Columnas del listado:**
- **Num** - Número correlativo
- **Identifier** - Identificador completo del documento
- **Document** - Número de documento
- **Status** - Estado (toPrint, printed, saved, paused)
- **Customer** - Cliente
- **Date** - Fecha del documento
- **Type** - Tipo de documento (SalesReceipt, Invoice, CreditMemo, etc.)
- **Ref** - Referencia
- **Color** - Color/etiqueta
- **Tag** - Etiqueta adicional
- **Balance** - Saldo pendiente
- **Carbon** - Fecha de creación formateada
- **Devolution** - Identificador de devolución (si aplica)
- **Sync** - Estado de sincronización
- **Action** - Acciones disponibles
- **Converted** - Indica si fue convertido (ej. cotización a factura)
- **CurrencySymbol** - Símbolo de moneda
- **CurrencyRate** - Tipo de cambio
- **IsVoid** - Indica si está anulado
- **TxnID** - ID de transacción en QuickBooks

<!-- TAG: Filtros historial, Tipo, Estado -->
<!-- AUDIENCE: Administrador, Contador -->
<!-- LEVEL: Intermedio -->
<!-- SEARCH: filtros historial tipo documento estado todos SalesReceipt Invoice CreditMemo -->
### 15.2 Filtros del historial

**Filtro por tipo de documento:**
- `point-of-sales`: `WHERE type="SalesReceipt" OR type="Invoice"`
- `devoluciones-app`: `WHERE type="CreditMemo"`
- `guides-app`: `WHERE type="Guide"`
- `purchase-orders-app`: `WHERE type="PurchaseOrder"`
- `quotation-app`: `WHERE type="Estimate"`
- `sales-order-app`: `WHERE type="SalesOrder"`
- `debitos-app`: `WHERE type="Invoice"`

**Filtro por estado:**
- Todos los estados
- Estados específicos (toPrint, printed, saved, paused)
- Búsqueda por tags

**Filtro "all":**
- Muestra todos los documentos del tipo correspondiente al módulo activo

<!-- TAG: Documentos convertidos, Cotizacion a Factura -->
<!-- AUDIENCE: Usuario Final, Cajero -->
<!-- LEVEL: Intermedio -->
<!-- SEARCH: documentos convertidos cotizacion factura proforma orden venta -->
### 15.3 Documentos convertidos

El sistema permite convertir documentos:
- **Estimate → Invoice/SalesReceipt:** Cotización a factura
- **SalesOrder → Invoice/SalesReceipt:** Orden de venta a factura
- **Proforma → Factura:** Proforma a factura

**Indicadores visuales:**
- Badge "convertida" en documentos convertidos
- Botón `open-quickbooks-transaction-button` para ver en QBO

<!-- TAG: Documentos reservados, Correlativos -->
<!-- AUDIENCE: Administrador, Cajero -->
<!-- LEVEL: Intermedio -->
<!-- SEARCH: documentos reservados correlativos isReserved documentToNumber reservadosImpresos -->
### 15.4 Documentos reservados

El sistema permite reservar números de documento:
- `isReserved` - Flag de documento reservado
- `documentToNumber` - Número específico asignado
- `reservadosImpresos` - Array de números ya impresos

**Lógica de asignación:**

```javascript
if (reservadosImpresos.includes(docNumber.toString())) {
  while (reservadosImpresos.includes(docNumber.toString())) {
    docNumber += 1;
  }
}
```

<!-- TAG: Logging, Auditoria, Acciones -->
<!-- AUDIENCE: Administrador, Contador -->
<!-- LEVEL: Intermedio -->
<!-- SEARCH: logging auditoria acciones usuario fecha hora documento RecordDocumentLogging -->
### 15.5 Logging de acciones

El sistema registra acciones importantes mediante `RecordDocumentLogging()`:

**Información registrada:**
- `identifier` - Identificador del documento
- `time` - Momento de la acción
- `invoice` - Array de acciones realizadas
- `user` - ID de usuario (`aria-user`)
- `name` - Nombre de usuario (`aria-user-name`)
- `createdAt` - Fecha/hora formateada
- `momento` - Timestamp en milisegundos

**Ejemplo de acción registrada:**

```
"Imprimió y registró la factura 000-016-01-00015009"
```


**Endpoint:** `SaveDocumentLogging`

---

<!-- TAG: Glosario, Definiciones, Terminos -->
<!-- AUDIENCE: Todos -->
<!-- LEVEL: Basico -->
<!-- SEARCH: glosario definiciones terminos tecnicos fiscales -->
## 16. Glosario

<!-- TAG: Terminos fiscales, CAI, ISV, RTN -->
<!-- AUDIENCE: Todos -->
<!-- LEVEL: Basico -->
<!-- SEARCH: definicion CAI ISV RTN SAR Honduras -->
### 16.1 Términos Fiscales

| Término | Definición |
|---------|-----------|
| **CAI** | Código de Autorización de Impresión. Requisito fiscal de Honduras para emisión de facturas. |
| **ISV** | Impuesto sobre Ventas (15% en Honduras). |
| **RTN** | Registro Tributario Nacional. Identificador fiscal de empresas en Honduras. |
| **SAR** | Servicio de Administración de Rentas. Autoridad fiscal de Honduras. |
| **Gravado** | Item sobre el cual se aplica ISV. |
| **Exento** | Item que no paga ISV por ley (`tax_type="EXE"`). |
| **Exonerado** | Item que no paga ISV por exoneración específica del cliente. |

<!-- TAG: Terminos tecnicos, QB, QBO, SKU, TxnID -->
<!-- AUDIENCE: Tecnico, Administrador -->
<!-- LEVEL: Intermedio -->
<!-- SEARCH: definicion QB QBO SKU TxnID ListID FullName SalesReceipt Invoice -->
### 16.2 Términos Técnicos

| Término | Definición |
|---------|-----------|
| **QB** | QuickBooks Desktop (versión de escritorio). |
| **QBO** | QuickBooks Online (versión en la nube). |
| **TxnID** | Identificador único de transacción en QuickBooks. |
| **ListID** | Identificador único de item/cliente en QuickBooks Desktop. |
| **Id** | Identificador único en QuickBooks Online. |
| **FullName** | Nombre completo del item/cliente en QB. |
| **FullyQualifiedName** | Nombre completo en QBO. |
| **SalesDesc** | Descripción de venta del item. |
| **SalesReceipt** | Factura de contado en QuickBooks. |
| **Invoice** | Factura a crédito en QuickBooks. |
| **CreditMemo** | Nota de crédito o devolución. |
| **PurchaseOrder** | Orden de compra. |
| **Estimate** | Cotización o presupuesto. |
| **SalesOrder** | Orden de venta. |
| **Guide** | Guía de despacho. |
| **InventoryIssues** | Salida de inventario. |
| **Bill** | Registro de gasto/costo. |
| **SKU** | Código único de identificación de producto. |
| **POS** | Point of Sale (Punto de Venta). |

<!-- TAG: Terminos aplicacion, Modulos, Variables -->
<!-- AUDIENCE: Tecnico, Administrador -->
<!-- LEVEL: Intermedio -->
<!-- SEARCH: definicion modulos variables current_theme_user OnlineOrDesktop baseToPrint -->
### 16.3 Términos de la Aplicación

| Término | Definición |
|---------|-----------|
| **current_theme_user** | Módulo activo del usuario (ej. `point-of-sales`). |
| **OnlineOrDesktop** | Modo de operación: `QB` o `QBO`. |
| **baseToPrint** | Objeto con datos del documento a imprimir/guardar. |
| **productos_facturados** | Array de items en la factura actual. |
| **copia_items_facturados** | Copia temporal de items para documentos pausados. |
| **series_registradas** | Array de números de serie registrados. |
| **current_client** | Cliente seleccionado actualmente. |
| **current_seller** | Vendedor asignado al documento. |
| **select_site** | Bodega/sitio seleccionado. |
| **current_auto** | CAI activo con rangos autorizados. |
| **transaccionesBAC** | Transacciones de BAC XpressPago. |
| **approvedPayments** | Pagos aprobados con tarjeta. |
| **logging_actions** | Objeto de logging de acciones del usuario. |
| **columnasTablas** | Configuración de índices de columnas en tablas. |
| **modulos_comprados** | Lista de módulos disponibles para el usuario. |
| **formato_activo** | Formato de impresión asignado al usuario. |
| **serials_setting** | Configuración de control de series (0 o 1). |
| **cash-deposit-account** | Cuenta para depósitos en efectivo. |
| **credit-deposit-account** | Cuenta para depósitos con tarjeta. |

---

<!-- TAG: Soporte, Contacto, Ayuda -->
<!-- AUDIENCE: Todos -->
<!-- LEVEL: Basico -->
<!-- SEARCH: soporte tecnico contacto ayuda recomendaciones practicas -->
## 17. Soporte

<!-- TAG: Recomendaciones practicas, Mejores practicas -->
<!-- AUDIENCE: Usuario Final, Administrador -->
<!-- LEVEL: Basico -->
<!-- SEARCH: recomendaciones practicas mejores practicas sincronizar final dia verificar CAI -->
### 17.1 Recomendaciones prácticas

1. **Verifique el CAI activo** antes de iniciar operaciones del día
2. **Sincronice con QuickBooks** al final de cada jornada usando el botón de sincronización
3. **Revise documentos pendientes de sincronización** (badge amarillo con ícono 🔄)
4. **Valide límites de crédito** antes de facturar a clientes con crédito
5. **Verifique series y lotes** antes de imprimir documentos
6. **Mantenga actualizada la aplicación** (modal de actualización cuando haya nueva versión)
7. **No comparta sus credenciales** de acceso de WordPress
8. **Cierre sesión** al terminar su jornada

<!-- TAG: Problemas comunes, Soluciones -->
<!-- AUDIENCE: Usuario Final, Administrador -->
<!-- LEVEL: Intermedio -->
<!-- SEARCH: problemas comunes soluciones errores sincronizacion formato impresion -->
### 17.2 Problemas comunes

**Error: "No se ha encontrado, el formato definido"**
- Causa: No hay formato de impresión configurado para el usuario
- Solución: Configurar `formato_activo` en el perfil de usuario

**Error: "No hemos conseguido registrar el Bill"**
- Causa: Error de sincronización con QuickBooks
- Solución: Verificar conexión con QuickBooks y revisar `saved.errors`

**Documento pendiente de sincronizar**
- Causa: Falla en la comunicación con QuickBooks
- Solución: Usar botón "Forzar Sincronización" o "Sincronizar"

**CAI vencido o agotado**
- Causa: El rango o fecha del CAI ha expirado
- Solución: Contactar al administrador para cargar nuevo CAI

**Serie ya utilizada**
- Causa: El número de serie ya existe en el sistema
- Solución: Verificar mediante `CheckUsedSeries` y usar serie diferente

**Lote vencido**
- Causa: El item tiene un lote con fecha de expiración pasada
- Solución: Seleccionar item con lote vigente o actualizar lote

<!-- TAG: Contacto soporte, Integral Business Solutions -->
<!-- AUDIENCE: Todos -->
<!-- LEVEL: Basico -->
<!-- SEARCH: contacto soporte tecnico Integral Business Solutions IBS -->
### 17.3 Contacto de soporte

**Empresa:** Integral Business Solutions (IBS)  
**Sitio web:** `https://apps.integralbsolutions.com/`  
**Aplicación:** `https://app.integralbizsolutions.com/`

Para soporte técnico:
- Contacte al administrador de su empresa
- Revise los mensajes de error en los toast notifications
- Verifique el estado de sincronización con QuickBooks
- Consulte el logging de acciones para auditoría

---

*© 2026 Integral Business Solutions. Todos los derechos reservados.*  
*Documento generado el 22 de noviembre de 2026*  
*Versión 1.0 - Basado en documentación técnica y capturas de pantalla*
