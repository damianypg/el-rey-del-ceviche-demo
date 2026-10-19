# El Rey del Ceviche: landing (demo)

Landing de El Rey del Ceviche, cevichería en Riobamba. Página estática de un solo archivo (`index.html` autocontenido: HTML, CSS y JS vanilla, con fuentes e imágenes incrustadas).

**Demo para el cliente:** https://damianypg.github.io/el-rey-del-ceviche-demo/

## Archivos publicados

| Archivo | Qué es |
|---|---|
| `index.html` | La landing completa |
| `og.jpg` | Imagen para compartir (1200×630) |
| `robots.txt` | Permite el rastreo; la página lleva `noindex` mientras sea demo |

`index.html` es un archivo generado: no se edita aquí a mano.

## Despliegue

Cada push a `main` publica `index.html`, `og.jpg` y `robots.txt` en GitHub Pages mediante `.github/workflows/deploy.yml` (`actions/upload-pages-artifact` + `actions/deploy-pages`).

## Al lanzar con el dominio definitivo (pendiente)

1. **Quitar** `<meta name="robots" content="noindex, nofollow">` de `index.html`: solo existe para que Google no indexe la demo.
2. Cambiar `canonical`, `og:url` y `og:image` al dominio definitivo.
3. En el hosting definitivo, configurar las cabeceras CSP, HSTS, `X-Content-Type-Options`, `Referrer-Policy` y `frame-ancestors`, que GitHub Pages no permite.
4. Confirmar con el negocio los precios, el horario y las promos vigentes.
