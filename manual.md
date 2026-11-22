<!-- TAG: Requisitos, Hardware, Software, Instalacion -->
<!-- AUDIENCE: Tecnico, Administrador -->
<!-- LEVEL: Basico -->
<!-- SEARCH: requisitos sistema windows quickbooks .net framework -->

# Manual de Usuario - IBS Facturas QB (Punto de Venta)

---

## 1. Portada

**Nombre de la aplicación:** IBS | Facturas QB (Point of Sales)  
**Logotipo:**  
![Logotipo Integral Business Solutions](https://integralbizsolutions.com/manual/img/logo-ibs.png)  
**Título:** Manual de Usuario  
**Versión del documento:** 1.1  
**Versión de la app:** 2.0  
**Fecha de elaboración/actualización:** 22 de noviembre de 2026  
**Autor o área responsable:** Departamento de Desarrollo e Implementación - Integral Business Solutions  
**Plataforma:** Aplicación Web (WordPress) integrada con QuickBooks Desktop (QB) y QuickBooks Online (QBO).

---

## 2. Control de Versiones

| Versión | Fecha | Autor | Cambios realizados |
|---------|-------|-------|-------------------|
| 1.0 | 22/11/2026 | Equipo IBS | Documento inicial creado basado en la estructura base. |
| 1.1 | 22/11/2026 | Equipo IBS | Inclusión de metadatos HTML, rutas de imágenes embebidas y detalles de integración con QuickBooks y BAC XpressPago. |

---

## 3. Índice / Tabla de Contenidos

1. [Portada](#1-portada)
2. [Control de Versiones](#2-control-de-versiones)
3. [Índice / Tabla de Contenidos](#3-índice--tabla-de-contenidos)
4. [Introducción](#4-introducción)
5. [Requisitos del Sistema](#5-requisitos-del-sistema)
6. [Primeros Pasos](#6-primeros-pasos)
7. [Descripción General de la Interfaz](#7-descripción-general-de-la-interfaz)
8. [Módulo de Facturación (Punto de Venta)](#8-módulo-de-facturación-punto-de-venta)
9. [Gestión de Clientes](#9-gestión-de-clientes)
10. [Gestión de Items / Productos](#10-gestión-de-items--productos)
11. [Autorizaciones (CAI)](#11-autorizaciones-cai)
12. [Términos de Pago](#12-términos-de-pago)
13. [Reportes](#13-reportes)
14. [Configuración y Parámetros](#14-configuración-y-parámetros)
15. [Glosario](#15-glosario)
16. [Soporte y Contacto](#16-soporte-y-contacto)

---

## 4. Introducción

### ¿Qué es la aplicación y para qué sirve?
**IBS | Facturas QB** es un sistema de automatización y punto de venta (POS) desarrollado sobre WordPress, diseñado para integrarse de forma nativa con **QuickBooks Desktop (QB)** y **QuickBooks Online (QBO)**. Permite la emisión de facturas electrónicas cumpliendo con la normativa fiscal de Honduras (CAI), gestión de inventario, control de series, procesamiento de pagos (incluyendo integración con BAC XpressPago) y sincronización bidireccional de datos contables.

### Público objetivo
- **Técnico:** Personal de TI encargado de la instalación, configuración de red y mantenimiento del conector de QuickBooks.
- **Administrador:** Gerentes o supervisores que configuran parámetros, usuarios, formatos de impresión y revisan reportes.
- **Usuario Final:** Cajeros, vendedores y personal de facturación que operan el punto de venta a diario.

### Alcance del manual
Este documento cubre la operación del módulo principal **Facturas (Point of Sales)**, incluyendo la creación de documentos, gestión de catálogos (clientes e items), manejo de autorizaciones fiscales (CAI), aplicación de pagos y sincronización con QuickBooks.

### Convenciones usadas
| Símbolo / Formato | Significado |
|-------------------|-------------|
| **Negrita** | Nombres de botones, menús, campos o acciones a realizar. |
| `Código` | Nombres técnicos de campos, rutas de archivo o valores del sistema. |
| 📷 | Indica una captura de pantalla embebida para referencia visual. |
| ⚠️ | Advertencia o punto crítico a considerar para evitar errores. |
| 💡 | Consejo o recomendación práctica para optimizar el flujo de trabajo. |

---

## 5. Requisitos del Sistema

### 5.1 Requisitos de Hardware
- **Procesador:** Intel Core i5 o superior (recomendado para el equipo que ejecute el conector de QuickBooks Desktop).
- **Memoria RAM:** Mínimo 8 GB (16 GB recomendados para entornos multiusuario).
- **Almacenamiento:** 50 GB de espacio libre en disco SSD para la base de datos local y caché de la aplicación.
- **Red:** Conexión de red local (LAN) estable y acceso a Internet de banda ancha para sincronización con QBO.

### 5.2 Requisitos de Software
- **Sistema Operativo:** Windows 10 / 11 (64 bits) para el servidor o estación de trabajo con QuickBooks Desktop. macOS o Linux son compatibles solo para el acceso vía navegador web (modo QBO).
- **Navegadores Web Compatibles:** Google Chrome (última versión, recomendado), Mozilla Firefox, Microsoft Edge, Safari.
- **QuickBooks:** QuickBooks Desktop (versión 2020 o superior) o QuickBooks Online (QBO).
- **.NET Framework:** Versión 4.7.2 o superior (requerido exclusivamente para el funcionamiento del conector de sincronización local de QuickBooks Desktop).
- **JavaScript y Cookies:** Deben estar habilitados en el navegador web.

### 5.3 Instalación y Configuración Inicial
1. Instalar QuickBooks Desktop en modo "Multi-User" o configurar el acceso a QBO.
2. Instalar el **Conector IBS para QuickBooks** en la máquina host (requiere permisos de administrador y .NET Framework).
3. Acceder a la URL web de la aplicación (ej. `https://apps.integralbsolutions.com/`).
4. El administrador del sistema debe asignar los permisos de módulo (ej. `point-of-sales`, `guides-app`, `apartados-app`) desde el perfil de usuario en WordPress.

---

## 6. Primeros Pasos

### 6.1 Acceso a la aplicación
1. Abra su navegador web compatible.
2. Ingrese la URL proporcionada por su administrador.
3. Ingrese su **usuario** y **contraseña**.
4. Seleccione la **Empresa** activa desde el modal de selección.
5. Haga clic en **Iniciar Sesión**.

### 6.2 Recorrido por la interfaz
📷 **Interfaz Principal del Módulo de Facturas**  
![Interfaz Principal de Facturas](https://integralbizsolutions.com/manual/img/factura-interfaz-principal.png)

La pantalla se divide en:
- **Barra Superior (Header):** Logo, título del módulo, fecha, y accesos rápidos (Búsqueda, Configuración, Sincronización, Notificaciones, Perfil).
- **Barra Lateral (Sidebar):** Navegación entre módulos (Facturas, Devoluciones, Guías, Órdenes de Compra, Apartados, Inventario).
- **Área de Trabajo Central:** Datos del cliente, tabla de items (productos/servicios) y totales.
- **Barra Inferior:** Acciones rápidas, información del CAI activo, bodega seleccionada y formato de impresión.

### 6.3 Cierre de sesión
Haga clic en el **icono de perfil** (esquina superior derecha) y seleccione **Cerrar Sesión**. Use **Bloquear Pantalla** si se ausenta temporalmente de su estación de trabajo.

---

## 7. Descripción General de la Interfaz

### 7.1 Barra de navegación / menú principal
| Icono | Función |
|-------|---------|
| ☰ | Abre/cierra el menú lateral de navegación. |
| 🔍 | Búsqueda global de documentos, clientes o items. |
| ⚙️ | Abre el modal de **Parámetros y Configuración**. |
| 🔄 | Ejecuta la **Sincronización** manual con QuickBooks. |
| 📊 | Acceso directo al módulo de **Reportes**. |
| 👤 | Menú de perfil de usuario (Cambiar contraseña, Bloquear, Cerrar sesión). |

### 7.2 Atajos de teclado
| Atajo | Acción |
|-------|--------|
| `F2` | Abrir modal de búsqueda y selección de Clientes. |
| `F3` | Abrir modal de búsqueda y selección de Items/Productos. |
| `F4` | Abrir modal de Términos de Pago. |
| `F5` | Guardar la factura actual. |
| `F9` | Imprimir el documento activo. |
| `Esc` | Cerrar el modal o ventana emergente activa. |

---

## 8. Módulo de Facturación (Punto de Venta)

### 8.1 Crear una nueva factura
1. Desde el menú, seleccione **Facturas**. El sistema asignará un número correlativo basado en el CAI vigente (ej. `000-016-01-00015001`).
2. Seleccione el **Cliente** (ver sección 9).
3. Agregue los **Items** a la tabla de detalle (ver sección 10).
4. Verifique el **Panel de Totales** (descuentos, exenciones, ISV 15%).
5. Haga clic en **Aplicar** para procesar el pago.

### 8.2 Tabla de items (líneas de factura)
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

## 9. Gestión de Clientes

### 9.1 Abrir el listado de clientes
Haga clic en el campo del cliente o presione `F2` para abrir el modal.

📷 **Modal de Listado de Clientes**  
![Modal Listado de Clientes](https://integralbizsolutions.com/manual/img/modal-listado-clientes.png)

### 9.2 Acciones disponibles
- **Filtrar Contenido:** Busque por nombre, RTN o número de identidad.
- **Editar:** Modifica los datos fiscales del cliente seleccionado.
- **⭐ (Favorito):** Marca el cliente para acceso rápido en futuras facturas.
- **Agregar:** Crea un nuevo cliente. Si usa QBO, el cliente se sincronizará automáticamente con QuickBooks Online al guardar.

---

## 10. Gestión de Items / Productos

### 10.1 Abrir el listado de items
Haga clic en el icono ➕ de una línea vacía o presione `F3`.

📷 **Modal de Listado de Items**  
![Modal Listado de Items](https://integralbizsolutions.com/manual/img/modal-listado-items.png)

### 10.2 Filtros y visualización
- **Mostrar con existencias:** Interruptor para ocultar productos con stock en cero.
- **Tipo de filtro:** Inventario, Servicios o Todo.
- **Bodega:** Seleccione la sucursal para ver la existencia real en ese almacén.
- **Etiquetas fiscales:** Los items muestran badges de color indicando si son `Gravado` (ISV 15%), `Exento` o `Exonerado`.

---

## 11. Autorizaciones (CAI)

### 11.1 ¿Qué es el CAI?
El **Código de Autorización de Impresión (CAI)** es el rango numérico y plazo autorizado por la SAR (Honduras) para la emisión legal de facturas.

### 11.2 Consultar autorizaciones
Haga clic en el texto del CAI en la barra inferior para abrir el modal de gestion.

📷 **Modal de Autorizaciones CAI**  
![Modal Autorizaciones CAI](https://integralbizsolutions.com/manual/img/modal-autorizaciones-cai.png)

### 11.3 Estados del CAI
- **Activo (Azul):** Rango vigente y en uso.
- **Tienda TGU (Amarillo):** CAI asignado específicamente a una sucursal o tienda física.
- **Vencido (Rosa):** El plazo o el rango numérico ha expirado. ⚠️ *Contacte a su administrador para cargar un nuevo CAI antes de que el activo se agote.*

---

## 12. Términos de Pago

### 12.1 Procesar el pago
Haga clic en **Aplicar** o presione `F4` para abrir el modal de pago.

📷 **Modal de Términos de Pago**  
![Modal Términos de Pago](https://integralbizsolutions.com/manual/img/modal-terminos-pago.png)

### 12.2 Métodos de pago disponibles
- **Efectivo:** Ingrese el monto recibido. El sistema calcula automáticamente el **Cambio** (vuelto). Use los botones de denominación rápida (500, 200, 100, 50, 20, 10, 5, 1, 0.25) para agilizar el cobro.
- **Tarjeta de Crédito / Débito:** Registre el último de 4 dígitos y la entidad bancaria.
- **Transferencia / Depósito:** Registre el número de referencia bancaria.
- **BAC XpressPago:** Si la empresa tiene dispositivos POS integrados, el sistema permitirá procesar el pago directamente enviando la orden al pinpad (requiere configuración previa en Parámetros).
- **Crédito:** La factura se guarda como "Cuenta por Cobrar" en QuickBooks.

### 12.3 Opciones adicionales
- **Enviar por correo:** Marca esta casilla para enviar el PDF de la factura al email registrado del cliente automáticamente.

---

## 13. Reportes

Acceda mediante el icono 📊 en la barra superior. Los reportes disponibles incluyen:
- **Listado de Facturas:** Filtrado por fecha, vendedor o estado de sincronización.
- **Detalles de Factura:** Desglose línea por línea de los documentos emitidos.
- **Ventas por Vendedor / Cliente / Producto:** Análisis de rendimiento comercial.
- **Exportación:** Todos los reportes pueden exportarse a **Excel (CSV)** o **PDF**.

---

## 14. Configuración y Parámetros

### 14.1 Acceso
Haga clic en el icono ⚙️ en la barra superior.

📷 **Modal de Parámetros y Configuración**  
![Modal Parámetros Configuración](https://integralbizsolutions.com/manual/img/modal-parametros-configuracion.png)

### 14.2 Parámetros clave
- **Empresa activa / Bodega:** Verifica que la sucursal asignada sea la correcta para el descuento de inventario.
- **Formato de impresión:** Seleccione la plantilla (ej. `ticket_technos.php`, `factura_carta.php`).
- **Números de Serie:** Configure si el sistema debe "Acumular" o "Separar" los números de serie en la impresión.
- **Sincronización:** Active o desactive la sincronización automática de Clientes, Artículos, Facturas, Notas de Crédito y Existencias.

### 14.3 Solución de problemas de conexión
⚠️ **Alerta de Conexión QuickBooks**  
![Alerta Conexion QuickBooks](https://integralbizsolutions.com/manual/img/alerta-conexion-quickbooks.png)  
Si aparece el mensaje *"QuickBooks Online está impidiendo tu conexión al archivo contable"* o similar en modo Desktop:
1. Verifique que QuickBooks Desktop esté abierto en la máquina host.
2. Confirme que el archivo de la compañía (.QBW) esté abierto.
3. Asegúrese de que el **Conector IBS** esté ejecutándose en la bandeja del sistema de Windows.
4. Verifique que el .NET Framework esté actualizado.

---

## 15. Glosario

| Término | Definición |
|---------|-----------|
| **CAI** | Código de Autorización de Impresión. Requisito fiscal de Honduras. |
| **ISV** | Impuesto sobre Ventas (15% en Honduras). |
| **RTN** | Registro Tributario Nacional. |
| **QB / QBO** | QuickBooks Desktop / QuickBooks Online. |
| **SKU** | Código único de identificación de un producto (Stock Keeping Unit). |
| **TxnID** | Identificador único de transacción generado por QuickBooks. |
| **BAC XpressPago** | Pasarela de pago integrada para procesamiento con tarjetas en punto de venta. |
| **Conector IBS** | Aplicación de escritorio (.NET) que puentea la aplicación web con QuickBooks Desktop. |

---

## 16. Soporte y Contacto

### Recomendaciones prácticas
1. **Sincronice al final del día:** Use el botón 🔄 para asegurar que todas las facturas del día estén en QuickBooks antes de cerrar.
2. **Verifique el CAI:** Revise periódicamente el rango disponible para evitar interrupciones en la facturación.
3. **No minimice el conector:** En modo QB Desktop, el conector debe permanecer activo en la barra de tareas de Windows.

### Contacto de Soporte Técnico
- **Empresa:** Integral Business Solutions (IBS)
- **Portal Web:** `https://apps.integralbsolutions.com/`
- **Horario de atención:** Lunes a Viernes, 8:00 AM - 6:00 PM
- **Correo de soporte:** soporte@integralbizsolutions.com

---
*© 2026 Integral Business Solutions. Todos los derechos reservados. Documento confidencial para uso interno y de clientes autorizados.*
