# TallerPro

Sistema web demostrativo para talleres mecánicos, lavaderos y centros de detailing. Está realizado con HTML5, CSS3, Bootstrap, Bootstrap Icons, JavaScript y archivos JSON.

## Cómo ejecutar

1. Descomprime la carpeta.
2. Abre `index.html` con Chrome, Edge o Firefox.
3. Inicia sesión con una de las cuentas de `CREDENCIALES.txt`.

El sistema funciona al abrir `index.html` directamente. Cuando el navegador no permite leer JSON desde `file://`, `app.js` usa una copia de respaldo de los mismos datos. Si se sirve por HTTP, intenta leer primero los archivos de la carpeta `data/`.

## Dependencias

- Bootstrap 5.1.1 incluido localmente en `vendor/bootstrap/`.
- Bootstrap Icons incluido localmente en `vendor/bootstrap-icons/`.
- No requiere Node.js, npm, base de datos ni compilación.
- La foto decorativa del taller se carga desde Unsplash. Si no hay Internet, se mantiene el fondo degradado y el sistema sigue siendo funcional.

## Módulos incluidos

- Inicio de sesión y control visual por roles.
- Dashboard operativo.
- Citas.
- Clientes.
- Vehículos y ficha técnica.
- Órdenes de trabajo y flujo de estados.
- Mecánica, lavado y detailing.
- Repuestos, proveedores y alertas de stock mínimo.
- Historial por vehículo.
- Facturación/pagos de demostración.
- Equipo y carga de trabajo.
- Reportes operativos.
- Portal de cliente.
- Persistencia local mediante `localStorage`.
- Diseño responsive para escritorio, tablet y móvil.

## Funciones de demostración

Se pueden crear clientes, vehículos, citas, órdenes, repuestos y pagos; actualizar stock; cambiar el estado de citas; avanzar órdenes de trabajo; visualizar el detalle de una orden; consultar el historial y usar búsqueda/filtros en tablas. Los cambios se conservan en el navegador mediante `localStorage`.

Para volver a los datos originales, elimina del almacenamiento local del sitio las claves `tallerpro_state` y `tallerpro_session` o limpia los datos del sitio en el navegador.

## Estructura

```text
TallerPro/
├── index.html
├── README.md
├── CREDENCIALES.txt
├── assets/
│   ├── css/styles.css
│   ├── js/app.js
│   └── img/logo-mark.svg
├── data/
│   ├── appointments.json
│   ├── clients.json
│   ├── history.json
│   ├── inventory.json
│   ├── invoices.json
│   ├── orders.json
│   ├── users.json
│   └── vehicles.json
└── vendor/
    ├── bootstrap/
    └── bootstrap-icons/
```

## Alcance técnico

Este proyecto es un prototipo funcional front-end. No incluye API ni base de datos real. Por eso las credenciales y la información de ejemplo son visibles en los archivos del proyecto. Para producción se debe sustituir la capa de datos por una API, almacenar contraseñas con hash, implementar autenticación real, permisos del lado servidor, auditoría, respaldos y base de datos.
