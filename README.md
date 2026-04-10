# Nexus app — APK

Esta carpeta contiene **`app-release.apk`**, el instalador Android de **Nexus**. La app nativa solo envuelve la **misma aplicación web** (ERP en el navegador) dentro de un WebView; no es otra producto distinto.

---

## Resumen de la aplicación web (Nexus)

**Nexus** es un **ERP multiempresa** (SaaS): cada empresa tiene sus propios datos, usuarios y límites según su **plan** (Starter, Pro, Enterprise). La interfaz está en **español, inglés y catalán**.

### Autenticación y empresa

- Registro de empresa y administrador, inicio de sesión y perfil.
- Datos fiscales y configuración de la empresa (moneda, NIF/CIF, dirección, etc.).
- **Roles:** administrador de empresa, usuario estándar y **gestoría** (acceso muy limitado, orientado a facturas).

### Gestión comercial y stock

- **Clientes:** alta, edición y consulta (CRM ligero); enlace con facturas.
- **Productos y categorías:** catálogo con precios, IVA, stock y stock mínimo (alertas).
- **Facturas:** numeración, fechas, líneas con producto o concepto manual, estados (pendiente, pagada, cancelada), totales e IVA.
- **Exportaciones:** libro de ingresos en CSV/Excel/PDF por periodo, PDF por factura, paquetes ZIP de PDFs para gestoría.

### Cobros y logística

- **Pagos** asociados a facturas (importe, método, fecha).
- **Envíos** ligados a facturas: transportista, seguimiento, estados y fechas.

### Organización

- **Calendario y recordatorios** con avisos por correo (si el servidor tiene correo configurado).
- **Tareas** tipo tablero (pendiente, en progreso, revisión, completado) con comentarios.

### Análisis y administración

- **Panel principal (dashboard):** resúmenes, gráficos de facturación, avisos de stock bajo, actividad reciente.
- **Analytics:** ingresos por periodo, facturas por estado, productos con stock bajo (según plan).
- **Usuarios de la empresa** (planes que lo permitan).
- **Planes:** consulta del plan actual, límites de uso y solicitud de mejora de plan.

### Plataforma

- **Administración global** (`/platform-admin`) para operadores de plataforma: empresas, planes y usuarios, según emails autorizados en el backend.

---

## Información legal (web pública)

La política de privacidad y el resto de textos legales están en el **mismo dominio** donde está desplegado el frontend (Vercel u otro). Sustituye el host por el tuyo:

- **Privacidad:** `https://TU-DOMINIO/legal/privacidad`
- **Términos:** `https://TU-DOMINIO/legal/terminos`
- **Aviso legal:** `https://TU-DOMINIO/legal/aviso-legal`

En Google Play Console suele pedirse la URL de **privacidad**; usa la primera.

---

## Instalación del APK en el móvil

Copia `app-release.apk` al dispositivo, ábrelo y acepta instalar desde orígenes externos si Android lo solicita. No pasa por Google Play.

**Identificador del paquete:** `com.colabstudio.nexus`.
