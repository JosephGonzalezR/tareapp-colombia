Tareapp Colombia (Bogota) — web publica
=======================================

Dominio:  https://tareapp.colombia.ags-ed.com   (GitHub Pages, CNAME en el repo)
Origen:   replica del molde de Chile (E:\tareapp-landing) hecha el 2026-08-02
Receta:   E:\_ESTANDARIZACION_AGS\PROCESO_REPLICACION_WEBS.md
Deploy:   push a main. GitHub Pages tarda 3 a 5 minutos.

Lo que es PROPIO de Colombia (no copiar de otro pais)
-----------------------------------------------------
- WhatsApp: +57 2 620 7344  (wa.me/5726207344). Va en app.js -> CONFIG.
  LEY AGS: cada pais tiene su numero Y su dominio. Nunca los de otro pais.
- Ciudad: Bogota. Moneda: COP (formato es-CO).
- Universidades: las de Bogota, con su LOGO en /assets/logos/ (orden de Joseph
  23-ago-2026, igual que la web de Chile). Fuente: Wikipedia/Wikimedia y el sitio
  oficial (Externado y Central). Se bajan y preparan con
  E:\DevCoordinador\scratch_colombia\logos_co_bajar.py (PNG dentro de 600x165 = 3x
  de la caja CSS .inst-chip img).
- Precios: /precios/ (matriz de tesis) y /precios-trabajos/.
  REGLA (Joseph, 23 y 24-ago-2026): "al tipo de cambio manejaremos mismos
  precios". Colombia paga lo MISMO que Chile, convertido al tipo de cambio REAL,
  redondeado hacia arriba (los saltos porcentuales entre planes se conservan).
  * Trabajo corto $46.000 = los 15 USD del ancla (1 USD = 3.058,67 COP), a la mil.
  * Trabajo de grado = escala chilena x 3,3177 (COP/CLP del 24-ago), al $10.000.
    Antes salia de un x 4,2 inventado el 02-ago: cobraba 26,6% de mas y se
    corrigio el 24-ago (tecnico 630.000 -> 500.000, doctorado Elite
    9.980.000 -> 7.880.000). El calculo y sus 6 verificaciones estan en
    E:\DevCoordinador\scratch_colombia\precios_tesis_co.py
  Para cambiarlos: objeto "bases" en /precios/index.html (un solo lugar) y el
  monto de trabajo corto en /precios-trabajos/index.html. En el Sistema Central
  hay que espejar Config.TIPOS_TRABAJO_PRECIO["CO"] y MONTOS_FRECUENTES["CO"].

Pendientes conocidos (no inventar nada de esto)
-----------------------------------------------
1. DATOS DE PAGO: /pago/ dice que los datos de la cuenta se envian por WhatsApp.
   Cuando haya cuenta colombiana (Nequi / Daviplata / Bancolombia) se reemplaza
   el bloque marcado DATOS-CO con el mismo formato que Chile.
2. REDES SOCIALES: Colombia no tiene cuentas propias todavia. Los enlaces de
   Facebook/TikTok/Instagram estan quitados a proposito (CONFIG los deja en "").
   Cuando existan, se cargan en app.js y en herramientas/geo_webs.py (campo redes).
3. /referencias/ (menu "Respaldo") no lleva comprobantes: los del molde son de
   clientes chilenos con montos en CLP. Se cargan cuando haya comprobantes
   colombianos, con el proceso mensual de E:\_ESTANDARIZACION_AGS\comprobantes_revision.

GEO y medidor
-------------
robots.txt, sitemap.xml, llms.txt, canonical/og:url y JSON-LD los GENERA
E:\DevCoordinador\herramientas\geo_webs.py (sitio "tareapp_co"). No editarlos a
mano. Despues de tocar el HTML:
    python geo_webs.py --sitio tareapp_co
El medidor propio (/assets/ags-analytics.js) reporta a central.ags-ed.com/w/e
con data-sitio="tareapp_co" y se ve en /webstats del Sistema Central.

Estructura
----------
index.html (trabajos) · tesis/ · precios/ · precios-trabajos/ · procedimiento/
faq/ · pago/ (+ pago/problemas/) · referencias/ · nosotros/ · blog/ (5 notas)
privacy/ · terms/ · styles.css · app.js · assets/ · Imagenes/
