# webgonia

Colección de páginas HTML estáticas (cada una en un solo archivo, con CSS y JS embebidos, sin build ni dependencias) del prototipo **OpenDirectory**: un directorio abierto de empresas y servicios de Magallanes (Chile), más herramientas de análisis de negocio, economía y finanzas.

## Páginas

| Archivo | Contenido |
|---|---|
| `opendirectory.html` | Página principal: búsqueda y filtros de empresas por categoría y territorio, directorio personal |
| `opendirectory-registro-empresas.html` | Formulario de registro de empresas |
| `opendirectory-punta-arenas-100 1 5.html` | 100 registros de demostración de Punta Arenas |
| `opendirectory-admin-spa 3 6.html` | Panel de administración (SPA) |
| `opendirectory-business-model-canvas.html` | Business Model Canvas |
| `opendirectory-foda-pestel 1 5.html` | Análisis FODA y PESTEL (datos en `foda-pestel.json`, actualmente vacío) |
| `opendirectory-informe-estrategia.html` | Informe: estrategia tradicional vs. startup, tabla resumen, diálogo entre equipos y opciones de versión de escritorio |
| `opendirectory-informe-datos-seo.html` | Informe: base de datos, recolección de datos y analítica SEO |
| `opendirectory-gastronomia-ultima-esperanza.html` | Gastronomía en Última Esperanza y Torres del Paine: calculadora de mesas, monitoreo comercial, pagos, indicadores de precios y ticket digital de bienvenida |
| `opendirectory-fintech-turismo-parques.html` | Leyes e instituciones de fintech, exportaciones y turismo; reglas de conducta en parques de la Patagonia (Torres del Paine) |
| `opendirectory-ciberseguridad-leyes.html` | Ciberseguridad y leyes chilenas de datos e información (19.628, 21.719, 21.663, 21.459) |
| `opendirectory-teoria-juegos.html` | Teoría de juegos y equilibrio de Nash, con calculadora 2×2 (JS inline) |
| `opendirectory-economics-*.html`, `opendirectory-macroeconomia 2 6.html`, `opendirectory-microeconomia 2 6.html` | Laboratorios de economía |
| `opendirectory-finanzas 3 6.html`, `opendirectory-finanzas-chile-2026 2 6.html`, `opendirectory-prevision-remuneraciones-chile 1 6.html` | Finanzas, previsión y remuneraciones en Chile |

## Convenciones

- Los nombres canónicos son estables (`opendirectory.html`, `opendirectory-registro-empresas.html`, `opendirectory-business-model-canvas.html`). Los archivos con nombres versionados antiguos (`opendirectory 1 5.html`, `opendirectory(2).html`, etc.) son redirecciones (`meta refresh`) hacia el canónico.
- Idioma de la interfaz: español; soporta modo claro/oscuro.
- Licencia: MIT propuesta (aún no hay archivo `LICENSE`).

## Uso y publicación

Abrir cualquier `.html` en el navegador. Para publicarlo: GitHub Pages (Settings → Pages → rama `main`, carpeta `/`). No existe `index.html`; hay que añadir uno que redirija a `opendirectory.html` para que la URL raíz funcione.
