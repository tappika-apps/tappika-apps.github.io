# Dominio propio de táppika — guía operativa y requisitos de publicación

Estado: **SIN COMPRAR / SIN CONFIGURAR / DISPONIBILIDAD NO VERIFICADA**. Documento interno 18/10/2026. Nombre visible de marca siempre `táppika`; nombres técnicos DNS sin tilde.

## Dominio propuesto
- Principal para actividad local española: `tappika.es`, **si la consulta de disponibilidad en un registrador autorizado permite comprarlo**.
- Defensa opcional: `tappika.com` si está disponible, cabe en presupuesto y la estrategia lo justifica.
- Estos nombres son propuestas técnicas, **no pruebas de disponibilidad ni de derechos de marca**.
- No comprar dominios `táppika.*` con IDN hasta valorar necesidad y compatibilidad; dominio ASCII `tappika.es` es simple para memorizar.

## Registro paso a paso, ejemplo con DonDominio
1. Abrir https://www.dondominio.com/ en sesión de navegación propia.
2. Introducir exactamente `tappika.es` en el buscador y pulsar «Buscar dominios».
3. Si figura **«Añadir al carrito»**, el proveedor muestra registro disponible en ese momento; añadir. Si aparece «Transferir» o no disponible, **no pagar por una transferencia** que no pertenezca al titular.
4. Continuar sin alojamiento web de pago. Para gestionar la zona DNS, comprobar que queda incluido el servicio gratuito **Redirección y Parking**; la web ya usa GitHub Pages. No contratar creador de webs, hosting adicional, SSL de pago ni correo opcional por error.
5. Entrar en «Configurar» dentro del carrito y rellenar **Titular** con el nombre/razón social legal del registrante real, dirección válida y datos requeridos. El nombre público `táppika` no sustituye a la identidad jurídica. Verificar condiciones de transferencia y titularidad.
6. Utilizar cuenta administrativa exclusiva de táppika (preferencia por `info.tappika@gmail.com`), establecer contraseña robusta y 2FA si el registrador lo permite. No compartir credenciales ni datos de pago en ChatGPT.
7. Antes de aceptar condiciones/pagar, comprobar precio del **primer año**, **renovación anual**, IVA, servicios añadidos, modalidad de renovación y que el proveedor muestra el dominio correcto. Activar renovación automática si se considera conveniente y mantener un método de pago válido.
8. Pagar directamente al registrador. Guardar factura y correo de confirmación. Verificar en el panel «Mis dominios» que `tappika.es` aparece bajo el titular elegido y que la zona DNS está administrable.
9. Comunicar únicamente **el nombre exacto de dominio comprado**; no usuario, contraseña, códigos de acceso, NIF ni tarjeta.

Fuente pasos de carrito: https://www.dondominio.com/es/help/2/como-puedo-registrar-dominio/
Fuente gestión DNS: https://www.dondominio.com/es/help/296/que-puedo-hacer-desde-panel-gestion-mi-dominio/

## Configuración posterior, solo cuando el dominio esté realmente comprado
**Orden de seguridad:** añadir dominio propio en GitHub Pages y/o verificar titularidad antes de apuntar DNS, para evitar riesgos de toma de subdominio.

En repo `tappika-apps/tappika-apps.github.io`, rama `main`, en Settings → Pages → Custom domain guardar `tappika.es`. GitHub puede crear el archivo `CNAME`. Dado que la conexión actual no expone la configuración de Pages por API, si procede se podrá insertar un `CNAME` en el repositorio con la identidad exacta **después de la compra**, además de comprobar el panel real.

En la **Zona DNS** del registrador, si se elige el dominio raíz:
- Tipo `A`, host `@`, valor `185.199.108.153`.
- Tipo `A`, host `@`, valor `185.199.109.153`.
- Tipo `A`, host `@`, valor `185.199.110.153`.
- Tipo `A`, host `@`, valor `185.199.111.153`.
- Tipo `CNAME`, host `www`, destino `tappika-apps.github.io` (sin `https://`, sin `/tappika-apps.github.io` ni nombre de repo repetido).
- Quitar registros preexistentes que **conflicten** con @ o www antes de crear los nuevos; **NO borrar TXT, MX, SPF, DKIM, DMARC u otros registros de correo** si los hay.
- Para dominio raíz también existe opción `ALIAS`/`ANAME` según proveedor; no mezclar indiscriminadamente.
- Propagación DNS puede tardar hasta 24 horas. Tras resolver, comprobar que `https://tappika.es/` y `https://www.tappika.es/` cargan contenido correcto y redirigen al nombre canónico cuando corresponda, y habilitar **Enforce HTTPS** cuando lo permita GitHub.
- De forma opcional / recomendada, verificar el dominio desde la configuración de la cuenta GitHub con un registro TXT concreto **generado por GitHub**, que no se puede inventar antes.
- No anunciar nuevo dominio ni actualizar el enlace en servicios ajenos hasta verificar HTTPS, certificado, rutas legales, navegación móvil y correo.

Fuente técnica: https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site
Verificación de dominio: https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/verifying-your-custom-domain-for-github-pages

## Identidad y legalidad
- **Dominios no son marcas registradas**. Comprobar registrabilidad de `táppika` / `tappika` y denominaciones confundibles ante OEPM/EUIPO y clase relevante antes de grandes inversiones o campañas. Base de datos: https://www.oepm.es/es/herramientas/buscador-base-de-datos/buscador-marcas-y-nombres-comerciales/
- El dominio puede comprarse sin poseer una marca registrada; ello no garantiza ausencia de conflictos.
- El titular legal de la web y de los servicios comerciales debe verificarse antes de publicar el aviso legal y quitar `noindex`.
