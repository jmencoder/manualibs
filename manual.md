<!-- TAG: Portada, General, Version -->
<!-- AUDIENCE: Todos -->
<!-- LEVEL: Basico -->
<!-- SEARCH: version manual fecha autor plataforma integral business solutions -->
# Manual de Usuario - IBS Facturas QB (Punto de Venta)

---

<!-- TAG: Versiones, Historial, Cambios, Control -->
<!-- AUDIENCE: Administrador, Tecnico -->
<!-- LEVEL: Basico -->
<!-- SEARCH: control versiones historial cambios documento actualizacion -->
## 1. Control de Versiones

| Versión | Fecha | Autor | Cambios realizados |
|---------|-------|-------|-------------------|
| 1.0 | 22/11/2026 | Equipo IBS | Documento inicial creado basado en la estructura base. |
| 1.1 | 22/11/2026 | Equipo IBS | Inclusión de metadatos HTML, rutas de imágenes embebidas y detalles de integración. |

---

<!-- TAG: Indice, Tabla de contenidos, Navegacion -->
<!-- AUDIENCE: Todos -->
<!-- LEVEL: Basico -->
<!-- SEARCH: indice tabla contenidos navegacion secciones manual -->
## 2. Índice / Tabla de Contenidos

1. [Control de Versiones](#1-control-de-versiones)
2. [Índice / Tabla de Contenidos](#2-índice--tabla-de-contenidos)
3. [Introducción](#3-introducción)
4. [Requisitos del Sistema](#4-requisitos-del-sistema)
5. [Primeros Pasos](#5-primeros-pasos)
6. [Descripción General de la Interfaz](#6-descripción-general-de-la-interfaz)
7. [Módulo de Facturación (Punto de Venta)](#7-módulo-de-facturación-punto-de-venta)
8. [Gestión de Clientes](#8-gestión-de-clientes)
9. [Gestión de Items / Productos](#9-gestión-de-items--productos)
10. [Autorizaciones (CAI)](#10-autorizaciones-cai)
11. [Términos de Pago](#11-términos-de-pago)
12. [Reportes](#12-reportes)
13. [Configuración y Parámetros](#13-configuración-y-parámetros)
14. [Glosario](#14-glosario)
15. [Soporte y Contacto](#15-soporte-y-contacto)

---

<!-- TAG: Introduccion, Proposito, Alcance, Objetivo -->
<!-- AUDIENCE: Todos -->
<!-- LEVEL: Basico -->
<!-- SEARCH: que es aplicacion proposito alcance publico objetivo convenciones -->
## 3. Introducción

<!-- TAG: Definicion, Funcionalidad, QuickBooks, Facturacion electronica -->
<!-- AUDIENCE: Todos -->
<!-- LEVEL: Basico -->
<!-- SEARCH: que es la aplicacion para que sirve quickbooks QB QBO facturacion electronica -->
### ¿Qué es la aplicación y para qué sirve?
**IBS | Facturas QB** es un sistema de automatización y punto de venta (POS) desarrollado sobre WordPress, diseñado para integrarse de forma nativa con **QuickBooks Desktop (QB)** y **QuickBooks Online (QBO)**. Permite la emisión de facturas electrónicas cumpliendo con la normativa fiscal de Honduras (CAI), gestión de inventario, control de series, procesamiento de pagos (incluyendo integración con BAC XpressPago) y sincronización bidireccional de datos contables.

<!-- TAG: Publico objetivo, Roles, Perfiles -->
<!-- AUDIENCE: Administrador, Recursos Humanos -->
<!-- LEVEL: Basico -->
<!-- SEARCH: publico objetivo roles perfiles cajero administrador contador -->
### Público objetivo
- **Técnico:** Personal de TI encargado de la instalación, configuración de red y mantenimiento del conector de QuickBooks.
- **Administrador:** Gerentes o supervisores que configuran parámetros, usuarios, formatos de impresión y revisan reportes.
- **Usuario Final:** Cajeros, vendedores y personal de facturación que operan el punto de venta a diario.

<!-- TAG: Alcance, Modulos, Cobertura -->
<!-- AUDIENCE: Administrador, Usuario Final -->
<!-- LEVEL: Basico -->
<!-- SEARCH: alcance del manual modulos cubiertos point of sales devoluciones guias -->
### Alcance del manual
Este documento cubre la operación del módulo principal **Facturas (Point of Sales)**, incluyendo la creación de documentos, gestión de catálogos (clientes e items), manejo de autorizaciones fiscales (CAI), aplicación de pagos y sincronización con QuickBooks.

<!-- TAG: Convenciones, Simbolos, Formato -->
<!-- AUDIENCE: Todos -->
<!-- LEVEL: Basico -->
<!-- SEARCH: convenciones usadas simbolos formato negrita codigo advertencia consejo -->
### Convenciones usadas
| Símbolo / Formato | Significado |
|-------------------|-------------|
| **Negrita** | Nombres de botones, menús, campos o acciones a realizar. |
| `Código` | Nombres técnicos de campos, rutas de archivo o valores del sistema. |
| 📷 | Indica una captura de pantalla embebida para referencia visual. |
| ⚠️ | Advertencia o punto crítico a considerar para evitar errores. |
| 💡 | Consejo o recomendación práctica para optimizar el flujo de trabajo. |

---

<!-- TAG: Requisitos, Hardware, Software, Instalacion -->
<!-- AUDIENCE: Tecnico, Administrador -->
<!-- LEVEL: Basico -->
<!-- SEARCH: requisitos sistema windows quickbooks .net framework navegador chrome -->
## 4. Requisitos del Sistema

<!-- TAG: Hardware, Especificaciones, Equipos -->
<!-- AUDIENCE: Tecnico, Administrador -->
<!-- LEVEL: Basico -->
<!-- SEARCH: requisitos hardware procesador ram almacenamiento disco red lan -->
### 4.1 Requisitos de Hardware
- **Procesador:** Intel Core i5 o superior (recomendado para el equipo que ejecute el conector de QuickBooks Desktop).
- **Memoria RAM:** Mínimo 8 GB (16 GB recomendados para entornos multiusuario).
- **Almacenamiento:** 50 GB de espacio libre en disco SSD para la base de datos local y caché de la aplicación.
- **Red:** Conexión de red local (LAN) estable y acceso a Internet de banda ancha para sincronización con QBO.

<!-- TAG: Software, Sistemas operativos, Navegadores, Dependencias -->
<!-- AUDIENCE: Tecnico, Administrador -->
<!-- LEVEL: Basico -->
<!-- SEARCH: requisitos software windows 10 11 mac linux chrome firefox edge safari .net framework -->
### 4.2 Requisitos de Software
- **Sistema Operativo:** Windows 10 / 11 (64 bits) para el servidor o estación de trabajo con QuickBooks Desktop. macOS o Linux son compatibles solo para el acceso vía navegador web (modo QBO).
- **Navegadores Web Compatibles:** Google Chrome (última versión, recomendado), Mozilla Firefox, Microsoft Edge, Safari.
- **QuickBooks:** QuickBooks Desktop (versión 2020 o superior) o QuickBooks Online (QBO).
- **.NET Framework:** Versión 4.7.2 o superior (requerido exclusivamente para el funcionamiento del conector de sincronización local de QuickBooks Desktop).
- **JavaScript y Cookies:** Deben estar habilitados en el navegador web.

<!-- TAG: Instalacion, Configuracion inicial, Pasos -->
<!-- AUDIENCE: Tecnico, Administrador -->
<!-- LEVEL: Intermedio -->
<!-- SEARCH: instalacion configuracion inicial quickbooks multi-user conector ibs permisos wordpress -->
### 4.3 Instalación y Configuración Inicial
1. Instalar QuickBooks Desktop en modo "Multi-User" o configurar el acceso a QBO.
2. Instalar el **Conector IBS para QuickBooks** en la máquina host (requiere permisos de administrador y .NET Framework).
3. Acceder a la URL web de la aplicación (ej. `https://apps.integralbsolutions.com/`).
4. El administrador del sistema debe asignar los permisos de módulo (ej. `point-of-sales`, `guides-app`, `apartados-app`) desde el perfil de usuario en WordPress.

---

<!-- TAG: Primeros pasos, Acceso, Login -->
<!-- AUDIENCE: Usuario Final, Cajero -->
<!-- LEVEL: Basico -->
<!-- SEARCH: acceso aplicacion login usuario contraseña seleccion empresa iniciar sesion -->
## 5. Primeros Pasos

<!-- TAG: Acceso, Autenticacion, Login -->
<!-- AUDIENCE: Usuario Final, Cajero -->
<!-- LEVEL: Basico -->
<!-- SEARCH: como entrar a la aplicacion url usuario contraseña iniciar sesion -->
### 5.1 Acceso a la aplicación
1. Abra su navegador web compatible.
2. Ingrese la URL proporcionada por su administrador.
3. Ingrese su **usuario** y **contraseña**.
4. Seleccione la **Empresa** activa desde el modal de selección.
5. Haga clic en **Iniciar Sesión**.

<!-- TAG: Interfaz, Recorrido, Pantalla principal -->
<!-- AUDIENCE: Usuario Final, Cajero -->
<!-- LEVEL: Basico -->
<!-- SEARCH: recorrido interfaz pantalla principal header sidebar area trabajo barra inferior -->
### 5.2 Recorrido por la interfaz
📷 **Interfaz Principal del Módulo de Facturas**  
![Interfaz Principal de Facturas](https://integralbizsolutions.com/manual/img/factura-interfaz-principal.png)

La pantalla se divide en:
- **Barra Superior (Header):** Logo, título del módulo, fecha, y accesos rápidos (Búsqueda, Configuración, Sincronización, Notificaciones, Perfil).
- **Barra Lateral (Sidebar):** Navegación entre módulos (Facturas, Devoluciones, Guías, Órdenes de Compra, Apartados, Inventario).
- **Área de Trabajo Central:** Datos del cliente, tabla de items (productos/servicios) y totales.
- **Barra Inferior:** Acciones rápidas, información del CAI activo, bodega seleccionada y formato de impresión.

<!-- TAG: Cierre sesion, Bloqueo, Seguridad -->
<!-- AUDIENCE: Usuario Final, Cajero -->
<!-- LEVEL: Basico -->
<!-- SEARCH: cerrar sesion bloquear pantalla seguridad perfil usuario -->
### 5.3 Cierre de sesión
Haga clic en el **icono de perfil** (esquina superior derecha) y seleccione **Cerrar Sesión**. Use **Bloquear Pantalla** si se ausenta temporalmente de su estación de trabajo.

---

<!-- TAG: Interfaz, Descripcion general, Componentes -->
<!-- AUDIENCE: Usuario Final, Cajero -->
<!-- LEVEL: Basico -->
<!-- SEARCH: descripcion general interfaz componentes barra navegacion atajos teclado -->
## 6. Descripción General de la Interfaz

<!-- TAG: Navegacion, Menu principal, Iconos -->
<!-- AUDIENCE: Usuario Final, Cajero -->
<!-- LEVEL: Basico -->
<!-- SEARCH: barra navegacion menu principal iconos funciones busqueda configuracion sincronizacion reportes -->
### 6.1 Barra de navegación / menú principal
| Icono | Función |
|-------|---------|
| ☰ | Abre/cierra el menú lateral de navegación. |
| 🔍 | Búsqueda global de documentos, clientes o items. |
| ⚙️ | Abre el modal de **Parámetros y Configuración**. |
| 🔄 | Ejecuta la **Sincronización** manual con QuickBooks. |
| 📊 | Acceso directo al módulo de **Reportes**. |
| 👤 | Menú de perfil de usuario (Cambiar contraseña, Bloquear, Cerrar sesión). |

<!-- TAG: Atajos, Teclado, Productividad -->
<!-- AUDIENCE: Usuario Final, Cajero -->
<!-- LEVEL: Intermedio -->
<!-- SEARCH: atajos teclado F2 F3 F4 F5 F9 Esc rapidez facturacion -->
### 6.2 Atajos de teclado
| Atajo | Acción |
|-------|--------|
| `F2` | Abrir modal de búsqueda y selección de Clientes. |
| `F3` | Abrir modal de búsqueda y selección de Items/Productos. |
| `F4` | Abrir modal de Términos de Pago. |
| `F5` | Guardar la factura actual. |
| `F9` | Imprimir el documento activo. |
| `Esc` | Cerrar el modal o ventana emergente activa. |

---

<!-- TAG: Facturacion, Punto de Venta, POS, Crear factura -->
<!-- AUDIENCE: Usuario Final, Cajero -->
<!-- LEVEL: Intermedio -->
<!-- SEARCH: modulo facturacion punto de venta crear nueva factura pasos -->
## 7. Módulo de Facturación (Punto de Venta)

<!-- TAG: Crear factura, Pasos, Proceso -->
<!-- AUDIENCE: Usuario Final, Cajero -->
<!-- LEVEL: Basico -->
<!-- SEARCH: como crear una nueva factura numero correlativo cliente items totales aplicar pago -->
### 7.1 Crear una nueva factura
1. Desde el menú, seleccione **Facturas**. El sistema asignará un número correlativo basado en el CAI vigente (ej. `000-016-01-00015001`).
2. Seleccione el **Cliente** (ver sección 8).
3. Agregue los **Items** a la tabla de detalle (ver sección 9).
4. Verifique el **Panel de Totales** (descuentos, exenciones, ISV 15%).
5. Haga clic en **Aplicar** para procesar el pago.

<!-- TAG: Tabla items, Lineas factura, Detalle -->
<!-- AUDIENCE: Usuario Final, Cajero -->
<!-- LEVEL: Basico -->
<!-- SEARCH: tabla items lineas factura descripcion bodega cantidad precio descuento total -->
### 7.2 Tabla de items (líneas de factura)
📷 **Detalle de la Tabla de Items**  
![Tabla de Items en Factura](https://integralbizsolutions.com/manual/img/factura-tabla-items.png)

Columnas principales:
- **Descripción:** Nombre del producto/servicio y su etiqueta fiscal (Gravado, Exento, Exonerado).
- **Bodega:** Sucursal o almacén de despacho (ej. `01 SUCURSAL PRINCIPAL`).
- **Cant.:** Cantidad a facturar.
- **Precio:** Precio unitario (el sistema calcula automáticamente el precio sin impuesto si el item está configurado como "Impuesto Incluido" en QBO).
- **Descuento:** Rebaja aplicada a la línea específica.
- **Total:** Importe final de la línea.

---

<!-- TAG: Clientes, Gestion, Listado -->
<!-- AUDIENCE: Usuario Final, Cajero, Administrador -->
<!-- LEVEL: Basico -->
<!-- SEARCH: gestion clientes listado modal busqueda filtrar -->
## 8. Gestión de Clientes

<!-- TAG: Listado clientes, Modal, Busqueda -->
<!-- AUDIENCE: Usuario Final, Cajero -->
<!-- LEVEL: Basico -->
<!-- SEARCH: abrir listado clientes F2 modal busqueda filtrar contenido RTN identidad -->
### 8.1 Abrir el listado de clientes
Haga clic en el campo del cliente o presione `F2` para abrir el modal.

📷 **Modal de Listado de Clientes**  
![Modal Listado de Clientes](https://integralbizsolutions.com/manual/img/modal-listado-clientes.png)

<!-- TAG: Acciones clientes, Editar, Favorito, Agregar -->
<!-- AUDIENCE: Usuario Final, Cajero, Administrador -->
<!-- LEVEL: Basico -->
<!-- SEARCH: acciones clientes editar datos fiscales marcar favorito agregar nuevo cliente sincronizacion QBO -->
### 8.2 Acciones disponibles
- **Filtrar Contenido:** Busque por nombre, RTN o número de identidad.
- **Editar:** Modifica los datos fiscales del cliente seleccionado.
- **⭐ (Favorito):** Marca el cliente para acceso rápido en futuras facturas.
- **Agregar:** Crea un nuevo cliente. Si usa QBO, el cliente se sincronizará automáticamente con QuickBooks Online al guardar.

---

<!-- TAG: Items, Productos, Inventario, Catalogo -->
<!-- AUDIENCE: Usuario Final, Cajero, Administrador -->
<!-- LEVEL: Intermedio -->
<!-- SEARCH: gestion items productos catalogo listado modal -->
## 9. Gestión de Items / Productos

<!-- TAG: Listado items, Modal, Busqueda -->
<!-- AUDIENCE: Usuario Final, Cajero -->
<!-- LEVEL: Basico -->
<!-- SEARCH: abrir listado items F3 modal busqueda filtros existencias tipo -->
### 9.1 Abrir el listado de items
Haga clic en el icono ➕ de una línea vacía o presione `F3`.

📷 **Modal de Listado de Items**  
![Modal Listado de Items](https://integralbizsolutions.com/manual/img/modal-listado-items.png)

<!-- TAG: Filtros items, Visualizacion, Etiquetas fiscales -->
<!-- AUDIENCE: Usuario Final, Cajero, Administrador -->
<!-- LEVEL: Intermedio -->
<!-- SEARCH: filtros items mostrar con existencias tipo inventario servicios bodega etiquetas fiscales gravado exento exonerado -->
### 9.2 Filtros y visualización
- **Mostrar con existencias:** Interruptor para ocultar productos con stock en cero.
- **Tipo de filtro:** Inventario, Servicios o Todo.
- **Bodega:** Seleccione la sucursal para ver la existencia real en ese almacén.
- **Etiquetas fiscales:** Los items muestran badges de color indicando si son `Gravado` (ISV 15%), `Exento` o `Exonerado`.

---

<!-- TAG: CAI, Autorizacion, Fiscal, SAR, Honduras -->
<!-- AUDIENCE: Administrador, Contador -->
<!-- LEVEL: Intermedio -->
<!-- SEARCH: autorizaciones CAI codigo autorizacion impresion fiscal SAR Honduras -->
## 10. Autorizaciones (CAI)

<!-- TAG: Definicion CAI, Concepto fiscal -->
<!-- AUDIENCE: Administrador, Contador, Usuario Final -->
<!-- LEVEL: Basico -->
<!-- SEARCH: que es el CAI codigo autorizacion impresion rango numerico plazo SAR -->
### 10.1 ¿Qué es el CAI?
El **Código de Autorización de Impresión (CAI)** es el rango numérico y plazo autorizado por la SAR (Honduras) para la emisión legal de facturas.

<!-- TAG: Consultar CAI, Modal autorizaciones -->
<!-- AUDIENCE: Administrador, Contador -->
<!-- LEVEL: Basico -->
<!-- SEARCH: consultar autorizaciones CAI modal gestion barra inferior -->
### 10.2 Consultar autorizaciones
Haga clic en el texto del CAI en la barra inferior para abrir el modal de gestion.

📷 **Modal de Autorizaciones CAI**  
![Modal Autorizaciones CAI](https://integralbizsolutions.com/manual/img/modal-autorizaciones-cai.png)

<!-- TAG: Estados CAI, Vigencia, Alertas -->
<!-- AUDIENCE: Administrador, Contador -->
<!-- LEVEL: Intermedio -->
<!-- SEARCH: estados CAI activo tienda TGU vencido rango disponible alerta agotamiento -->
### 10.3 Estados del CAI
- **Activo (Azul):** Rango vigente y en uso.
- **Tienda TGU (Amarillo):** CAI asignado específicamente a una sucursal o tienda física.
- **Vencido (Rosa):** El plazo o el rango numérico ha expirado. ⚠️ *Contacte a su administrador para cargar un nuevo CAI antes de que el activo se agote.*

---

<!-- TAG: Pagos, Terminos de pago, Cobro -->
<!-- AUDIENCE: Usuario Final, Cajero -->
<!-- LEVEL: Intermedio -->
<!-- SEARCH: terminos de pago procesar pago modal F4 -->
## 11. Términos de Pago

<!-- TAG: Procesar pago, Modal pago -->
<!-- AUDIENCE: Usuario Final, Cajero -->
<!-- LEVEL: Basico -->
<!-- SEARCH: como procesar un pago boton aplicar F4 modal terminos de pago -->
### 11.1 Procesar el pago
Haga clic en **Aplicar** o presione `F4` para abrir el modal de pago.

📷 **Modal de Términos de Pago**  
![Modal Términos de Pago](https://integralbizsolutions.com/manual/img/modal-terminos-pago.png)

<!-- TAG: Metodos de pago, Efectivo, Tarjeta, Transferencia, Credito -->
<!-- AUDIENCE: Usuario Final, Cajero -->
<!-- LEVEL: Basico -->
<!-- SEARCH: metodos de pago disponibles efectivo tarjeta credito debito transferencia deposito BAC XpressPago credito cuenta por cobrar -->
### 11.2 Métodos de pago disponibles
- **Efectivo:** Ingrese el monto recibido. El sistema calcula automáticamente el **Cambio** (vuelto). Use los botones de denominación rápida (500, 200, 100, 50, 20, 10, 5, 1, 0.25) para agilizar el cobro.
- **Tarjeta de Crédito / Débito:** Registre el último de 4 dígitos y la entidad bancaria.
- **Transferencia / Depósito:** Registre el número de referencia bancaria.
- **BAC XpressPago:** Si la empresa tiene dispositivos POS integrados, el sistema permitirá procesar el pago directamente enviando la orden al pinpad (requiere configuración previa en Parámetros).
- **Crédito:** La factura se guarda como "Cuenta por Cobrar" en QuickBooks.

<!-- TAG: Opciones pago, Correo, Descuento -->
<!-- AUDIENCE: Usuario Final, Cajero -->
<!-- LEVEL: Basico -->
<!-- SEARCH: opciones adicionales pago enviar por correo PDF aplicar descuento recibo -->
### 11.3 Opciones adicionales
- **Enviar por correo:** Marca esta casilla para enviar el PDF de la factura al email registrado del cliente automáticamente.

---

<!-- TAG: Reportes, Estadisticas, Exportacion -->
<!-- AUDIENCE: Administrador, Contador -->
<!-- LEVEL: Intermedio -->
<!-- SEARCH: modulo reportes estadisticas ventas exportar -->
## 12. Reportes

<!-- TAG: Tipos de reportes, Listados, Detalles -->
<!-- AUDIENCE: Administrador, Contador -->
<!-- LEVEL: Intermedio -->
<!-- SEARCH: tipos de reportes disponibles listado facturas detalles factura ventas por vendedor cliente producto -->
### 12.1 Reportes disponibles
Acceda mediante el icono 📊 en la barra superior. Los reportes disponibles incluyen:
- **Listado de Facturas:** Filtrado por fecha, vendedor o estado de sincronización.
- **Detalles de Factura:** Desglose línea por línea de los documentos emitidos.
- **Ventas por Vendedor / Cliente / Producto:** Análisis de rendimiento comercial.

<!-- TAG: Exportar reportes, Formatos, PDF, Excel -->
<!-- AUDIENCE: Administrador, Contador -->
<!-- LEVEL: Basico -->
<!-- SEARCH: exportar reportes formatos disponibles Excel CSV PDF impresion directa -->
### 12.2 Exportación de reportes
Todos los reportes pueden exportarse a **Excel (CSV)** o **PDF** para su análisis externo o archivo físico.

---

<!-- TAG: Configuracion, Parametros, Ajustes -->
<!-- AUDIENCE: Administrador, Tecnico -->
<!-- LEVEL: Avanzado -->
<!-- SEARCH: configuracion parametros ajustes del sistema modal -->
## 13. Configuración y Parámetros

<!-- TAG: Acceso configuracion, Modal parametros -->
<!-- AUDIENCE: Administrador, Tecnico -->
<!-- LEVEL: Basico -->
<!-- SEARCH: como acceder a la configuracion icono engranaje modal parametros -->
### 13.1 Acceso
Haga clic en el icono ⚙️ en la barra superior.

📷 **Modal de Parámetros y Configuración**  
![Modal Parámetros Configuración](https://integralbizsolutions.com/manual/img/modal-parametros-configuracion.png)

<!-- TAG: Parametros clave, Bodega, Formato, Serie -->
<!-- AUDIENCE: Administrador, Tecnico -->
<!-- LEVEL: Intermedio -->
<!-- SEARCH: parametros clave empresa activa bodega sucursal formato impresion numeros de serie acumulados separados -->
### 13.2 Parámetros clave
- **Empresa activa / Bodega:** Verifica que la sucursal asignada sea la correcta para el descuento de inventario.
- **Formato de impresión:** Seleccione la plantilla (ej. `ticket_technos.php`, `factura_carta.php`).
- **Números de Serie:** Configure si el sistema debe "Acumular" o "Separar" los números de serie en la impresión.

<!-- TAG: Sincronizacion, QuickBooks, Conexion, Solucion problemas -->
<!-- AUDIENCE: Administrador, Tecnico -->
<!-- LEVEL: Avanzado -->
<!-- SEARCH: sincronizacion quickbooks QB QBO activar desactivar solucion problemas conexion conector .net framework -->
### 13.3 Sincronización y Solución de problemas
Active o desactive la sincronización automática de Clientes, Artículos, Facturas, Notas de Crédito y Existencias.

⚠️ **Alerta de Conexión QuickBooks**  
![Alerta Conexion QuickBooks](https://integralbizsolutions.com/manual/img/alerta-conexion-quickbooks.png)  
Si aparece el mensaje *"QuickBooks Online está impidiendo tu conexión al archivo contable"* o similar en modo Desktop:
1. Verifique que QuickBooks Desktop esté abierto en la máquina host.
2. Confirme que el archivo de la compañía (.QBW) esté abierto.
3. Asegúrese de que el **Conector IBS** esté ejecutándose en la bandeja del sistema de Windows.
4. Verifique que el .NET Framework esté actualizado.

---

<!-- TAG: Glosario, Definiciones, Terminos -->
<!-- AUDIENCE: Todos -->
<!-- LEVEL: Basico -->
<!-- SEARCH: glosario definiciones terminos tecnicos fiscales -->
## 14. Glosario

<!-- TAG: Terminos fiscales, CAI, ISV, RTN -->
<!-- AUDIENCE: Todos -->
<!-- LEVEL: Basico -->
<!-- SEARCH: definicion CAI ISV RTN SAR Honduras -->
### 14.1 Términos Fiscales
| Término | Definición |
|---------|-----------|
| **CAI** | Código de Autorización de Impresión. Requisito fiscal de Honduras. |
| **ISV** | Impuesto sobre Ventas (15% en Honduras). |
| **RTN** | Registro Tributario Nacional. |

<!-- TAG: Terminos tecnicos, QB, QBO, SKU, TxnID -->
<!-- AUDIENCE: Tecnico, Administrador -->
<!-- LEVEL: Intermedio -->
<!-- SEARCH: definicion QB QBO SKU TxnID Conector IBS BAC XpressPago -->
### 14.2 Términos Técnicos y del Sistema
| Término | Definición |
|---------|-----------|
| **QB / QBO** | QuickBooks Desktop / QuickBooks Online. |
| **SKU** | Código único de identificación de un producto (Stock Keeping Unit). |
| **TxnID** | Identificador único de transacción generado por QuickBooks. |
| **BAC XpressPago** | Pasarela de pago integrada para procesamiento con tarjetas en punto de venta. |
| **Conector IBS** | Aplicación de escritorio (.NET) que puentea la aplicación web con QuickBooks Desktop. |

---

<!-- TAG: Soporte, Contacto, Ayuda, Recomendaciones -->
<!-- AUDIENCE: Todos -->
<!-- LEVEL: Basico -->
<!-- SEARCH: soporte tecnico contacto ayuda recomendaciones practicas integral business solutions -->
## 15. Soporte y Contacto

<!-- TAG: Recomendaciones practicas, Mejores practicas -->
<!-- AUDIENCE: Usuario Final, Administrador -->
<!-- LEVEL: Basico -->
<!-- SEARCH: recomendaciones practicas mejores practicas sincronizar final dia verificar CAI conector activo -->
### 15.1 Recomendaciones prácticas
1. **Sincronice al final del día:** Use el botón 🔄 para asegurar que todas las facturas del día estén en QuickBooks antes de cerrar.
2. **Verifique el CAI:** Revise periódicamente el rango disponible para evitar interrupciones en la facturación.
3. **No minimice el conector:** En modo QB Desktop, el conector debe permanecer activo en la barra de tareas de Windows.

<!-- TAG: Datos de contacto, Soporte tecnico -->
<!-- AUDIENCE: Todos -->
<!-- LEVEL: Basico -->
<!-- SEARCH: datos contacto soporte tecnico correo horario portal web integral business solutions -->
### 15.2 Contacto de Soporte Técnico
- **Empresa:** Integral Business Solutions (IBS)
- **Portal Web:** `https://apps.integralbsolutions.com/`
- **Horario de atención:** Lunes a Viernes, 8:00 AM - 6:00 PM
- **Correo de soporte:** soporte@integralbizsolutions.com

---
*© 2026 Integral Business Solutions. Todos los derechos reservados. Documento confidencial para uso interno y de clientes autorizados.*
