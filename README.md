🛒 Desarrollo y Despliegue de E-commerce: Especias Michelle

Caso de Estudio: Migración de entorno local a producción, integración de pasarelas de pago y hardening de seguridad.

Este repositorio documenta el proceso técnico y los desafíos superados durante el desarrollo y puesta en marcha de una tienda online real para el sector de alimentación. El objetivo fue crear una plataforma robusta, segura y automatizada sobre WordPress/WooCommerce.

🔗 Ver proyecto en vivo: www.especiasmichelle.com

🚀 Desafíos Técnicos y Soluciones

Este proyecto fue más allá de la instalación de un CMS; implicó gestión de servidores, seguridad y lógica de negocio personalizada.

1. Infraestructura y Despliegue

Migración Crítica: Realicé el despliegue desde un entorno de desarrollo local a un servidor VPS/Hosting (Hostinger).

Gestión de DNS: Configuración de registros A y CNAME, además de registros SPF y DKIM para garantizar la entregabilidad de los correos transaccionales (evitando la carpeta de SPAM).

Base de Datos: Actualización masiva de URLs serializadas en la base de datos para corregir enlaces rotos post-migración.

2. Integración de Pagos (Stripe)

Implementación de la pasarela de pagos Stripe mediante API.

Configuración manual de Webhooks para asegurar la sincronización de estados de pago (evitando pedidos "pendientes de pago" cuando el cargo fue exitoso).

Lógica de envíos condicionales basada en zonas geográficas y subtotal del carrito.

3. Seguridad (Hardening)

SSL/HTTPS: Forzado de redirecciones seguras a nivel de servidor.

Protección contra Fuerza Bruta: Implementación de límites de intentos de login y ofuscación de rutas de administración.

RBAC: Configuración estricta de roles y permisos de usuario.

4. Troubleshooting (Resolución de Problemas)

Conflicto de Caché: Diagnóstico y solución de problemas con LiteSpeed Cache que impedían la actualización del carrito en tiempo real.

Integración de API Social: Resolución de errores de conexión con la API Graph de Instagram tras el cambio de dominio, implementando una solución de tokens de acceso persistentes.

🛠 Stack Tecnológico

CMS: WordPress + WooCommerce

Frontend: Elementor Pro, CSS3 personalizado

Pagos: Stripe API

Servidor: LiteSpeed / Hostinger

Herramientas: FileZilla (FTP), phpMyAdmin

📸 Capturas del Proyecto

A continuación se muestran algunas vistas clave de la implementación:

Home & Branding

Página de Producto





Carrito & Checkout

Pasarela Stripe





Desarrollado y desplegado por Daniel Meléndez.
