# AlmaMovil

Páginas públicas de AlmaMovil, publicadas con GitHub Pages en <https://almamovil.github.io/>.

- `carrito/`: carrito de compras por WhatsApp (<https://almamovil.github.io/carrito/>). El link con la planilla y el
  WhatsApp del comercio lo arma LibreriaLuis (Menu Principal > Link Carrito de compras WhatsApp).
- `app/version.json`: última versión de Alma Móvil (<https://almamovil.github.io/app/version.json>). La app lo consulta
  para avisar que hay una versión nueva. El APK se publica como archivo de una Release de este repo (`v4.10`,
  `AlmaMovil-4.10.apk`) y `url` apunta a esa descarga. `minimaVersionCode`: debajo de ese número el aviso es obligatorio.

Para publicar una versión: crear la Release `vX.YY` con el APK firmado como `AlmaMovil-X.YY.apk`, después actualizar
`versionCode`, `versionName`, `fecha`, `url` y `novedades` en `app/version.json` y hacer push.

`carrito/index.html` no se edita a mano: se genera en LibreriaLuis con
`node Web\CarritoWhatsApp\pagina\armar.js C:\DRRSystemas\almamovil.github.io\carrito` (ver `Web\CarritoWhatsApp\LEEME.md`).
