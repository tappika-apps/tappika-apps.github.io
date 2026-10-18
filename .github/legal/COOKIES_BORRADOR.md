# Información sobre cookies y tecnologías externas — táppika

**BORRADOR INTERNO, PENDIENTE DE VERIFICACIÓN EN NAVEGADOR Y DE TITULAR LEGAL.** Fecha de revisión de fuente: 18/10/2026.

## Responsable
[IDENTIFICAR TITULAR LEGAL Y ENLAZAR AVISO LEGAL]. Contacto: info.tappika@gmail.com.

## Estado técnico observado
El sitio auditado es una web informativa estática con demostraciones visuales y enlaces de contacto. Su propio JavaScript no contiene llamadas a `document.cookie`, `localStorage` o `sessionStorage`, no incorpora en el código un gestor analítico, píxeles publicitarios ni scripts de publicidad, y no envía formularios a un servidor propio.

Sin embargo, se cargan recursos externos de **Google Fonts** para la familia Manrope, y el alojamiento corre sobre GitHub Pages. Estos proveedores pueden recibir datos técnicos al atender peticiones HTTP; la existencia efectiva de cookies o cabeceras de terceros debe contrastarse con una prueba de red real en navegador antes de publicar afirmaciones definitivas.

Enlaces de navegación a **WhatsApp** abren un servicio externo solo cuando la persona decide utilizarlo; las políticas de cookies de WhatsApp corresponden a ese proveedor.

## Consentimiento
Mientras se verifique que el sitio no utiliza cookies o identificadores no exentos, **no se necesita un banner de aceptación de cookies inventado o ornamental**. Si se habilitan analíticas, píxeles de seguimiento, vídeos incorporados u otras tecnologías no exentas, habrá que obtener el consentimiento previo cuando sea exigible, con opciones de aceptar y rechazar equivalentes, y actualizar este documento.

## Gestión en el navegador
Se pueden bloquear o borrar cookies desde la configuración del navegador. Esta opción puede afectar servicios externos a los que se acceda voluntariamente.

## Revisión
Fecha de última revisión: [CONFIRMAR AL PUBLICAR]. Estos datos se actualizarán si cambian proveedor, scripts o tecnologías.

## Referencias
- Guía de cookies AEPD: https://www.aepd.es/guias/guia-cookies.pdf
- Google Fonts privacidad: https://fonts.googleblog.com/2022/11/your-privacy-and-google-fonts.html
- GitHub privacidad: https://docs.github.com/es/site-policy/privacy-policies/github-general-privacy-statement

## Antes de publicar
- [ ] Abrir la web con perfil limpio en Chromium escritorio y móvil, comprobar cookies, localStorage y todas las peticiones de terceros.
- [ ] Si existe alguna cookie no exenta, identificar titular, finalidad, duración y habilitar consentimiento previo o eliminarla.
- [ ] Si solo existen cookies exceptuadas/no existen, no crear banner; incorporar enlace discreto a la política.
- [ ] Verificar que los textos coinciden exactamente con el código final acordado con Claude.
