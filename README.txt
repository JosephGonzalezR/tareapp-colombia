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
- Universidades: las de Bogota, en chips de TEXTO (no usamos logos ajenos).
- Precios: /precios/ (matriz de tesis) y /precios-trabajos/.
  Los valores salen del molde chileno x 4,2 (cambio del 2026-08-02) redondeados
  hacia arriba al siguiente $10.000, conservando los mismos saltos porcentuales.
  Para cambiarlos: objeto "bases" en /precios/index.html (un solo lugar) y el
  monto de trabajo corto en /precios-trabajos/index.html.

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
