# webgonia

Colección de **26 archivos HTML estáticos** (CSS y JS embebidos, sin build, sin dependencias, sin `package.json`) que forman el prototipo **OpenDirectory**: un directorio abierto de empresas y servicios de Magallanes (Chile), con laboratorios de economía y finanzas e informes sobre turismo en la Patagonia.

> Los informes de este repositorio son material educativo y de diseño de investigación. **No contienen datos verificados** (visitantes, precios, multas); donde falta un dato lo dicen y señalan la fuente. Verifique siempre en las fuentes oficiales.

## Estructura del directorio

```
webgonia/
├── README.md
├── foda-pestel.json          # datos FODA/PESTEL; hoy contiene solo {}
├── docs/
│   └── agente-marketing.md   # borrador de diseño de un agente de marketing
├── .github/                  # configuración de agentes de GitHub
└── *.html                    # páginas (tabla siguiente)
```

### Archivos HTML (generado a partir del contenido real)

| Archivo | Tipo | Bytes | Líneas | Título |
|---|---|---|---|---|
| `opendirectory 1 5.html` | redirección | 440 | 16 | Redirigiendo… |
| `opendirectory(2).html` | redirección | 440 | 16 | Redirigiendo… |
| `opendirectory(3).html` | redirección | 440 | 16 | Redirigiendo… |
| `opendirectory-admin-spa 3 6.html` | página | 29.710 | 80 | OpenDirectory Admin |
| `opendirectory-business-model-canvas 1 5.html` | redirección | 514 | 16 | Redirigiendo… |
| `opendirectory-business-model-canvas.html` | página | 22.976 | 48 | Business Model Canvas · OpenDirectory Business Lab |
| `opendirectory-ciberseguridad-leyes.html` | página | 9.096 | 71 | Ciberseguridad y leyes de datos en Chile · OpenDirectory |
| `opendirectory-economics-lab-spa 1 5.html` | página | 21.854 | 38 | OpenDirectory Economics Lab |
| `opendirectory-economics-spa 1 2 1.html` | página | 22.785 | 35 | OpenDirectory Economics Lab |
| `opendirectory-economics-spa 1 6.html` | página | 22.785 | 35 | OpenDirectory Economics Lab |
| `opendirectory-finanzas 3 6.html` | página | 29.385 | 31 | OpenFinance Chile · OpenDirectory |
| `opendirectory-finanzas-chile-2026 2 6.html` | página | 39.711 | 47 | Finanzas Chile 2026 · OpenDirectory Business Lab |
| `opendirectory-fintech-turismo-parques.html` | página | 14.135 | 95 | Fintech, exportaciones, turismo y parques de la Patagonia · OpenDirectory |
| `opendirectory-foda-pestel 1 5.html` | página | 5.345 | 77 | OpenDirectory Business Lab · FODA y PESTEL |
| `opendirectory-gastronomia-ultima-esperanza.html` | página | 24.055 | 194 | Gastronomía en Última Esperanza: diseño de investigación · OpenDirectory |
| `opendirectory-informe-datos-seo.html` | página | 9.846 | 87 | Informe · Base de datos, recolección y analítica SEO · OpenDirectory |
| `opendirectory-informe-estrategia.html` | página | 9.835 | 39 | Informe · Estrategia tradicional vs startup en OpenDirectory |
| `opendirectory-macroeconomia 2 6.html` | página | 17.925 | 22 | OpenEconomics · OpenDirectory |
| `opendirectory-microeconomia 2 6.html` | página | 18.634 | 23 | OpenMicroeconomics · OpenDirectory |
| `opendirectory-patagonia-economia-marketing.html` | página | 13.472 | 96 | Economía y marketing de la Patagonia · OpenDirectory |
| `opendirectory-prevision-remuneraciones-chile 1 6.html` | página | 26.317 | 30 | Previsión y Remuneraciones Chile · OpenDirectory |
| `opendirectory-punta-arenas-100 1 5.html` | página | 19.341 | 44 | OpenDirectory Punta Arenas · 100 registros de demostración |
| `opendirectory-registro-empresas 3 6.html` | redirección | 501 | 16 | Redirigiendo… |
| `opendirectory-registro-empresas.html` | página | 20.889 | 73 | Registrar empresa · OpenDirectory |
| `opendirectory-teoria-juegos.html` | página | 4.393 | 60 | Teoría de juegos y equilibrio de Nash · OpenDirectory |
| `opendirectory.html` | página | 17.452 | 114 | OpenDirectory · Empresas y servicios de Magallanes |

## Datos concretos del código

- **Arquitectura:** cada página es independiente; no comparten CSS ni JS. Los datos de empresas están en arreglos JS embebidos y se duplican entre páginas.
- **Persistencia:** solo `localStorage` del navegador (claves vistas: `od-admin-state`, `od-business-requests`, `od-canvas-state`, `od-ticket-secret`, `od-ticket-used`). No hay backend ni base de datos.
- **Seguridad:** no existe autenticación real; el panel admin y el ticket de bienvenida son **prototipos** (la clave de firma está en el navegador).
- **Tema:** respeta `prefers-color-scheme` (claro/oscuro). Idioma: español.
- **Redirecciones:** los nombres versionados antiguos (`opendirectory 1 5.html`, `opendirectory(2).html`, `opendirectory(3).html`, `opendirectory-business-model-canvas 1 5.html`, `opendirectory-registro-empresas 3 6.html`) son `meta refresh` hacia el nombre canónico. Los demás archivos con sufijos numéricos (p. ej. `... 3 6.html`) **no** son redirecciones y mantienen su nombre antiguo; renombrarlos es un trabajo pendiente.
- **Faltan:** `index.html`, `LICENSE`, `sitemap.xml`, `robots.txt`, pruebas automatizadas, CI.

## Páginas por tema

| Tema | Archivos |
|---|---|
| Directorio | `opendirectory.html`, `opendirectory-registro-empresas.html`, `opendirectory-punta-arenas-100 1 5.html`, `opendirectory-admin-spa 3 6.html` |
| Estrategia y negocio | `opendirectory-business-model-canvas.html`, `opendirectory-foda-pestel 1 5.html`, `opendirectory-informe-estrategia.html`, `opendirectory-teoria-juegos.html` |
| Economía y finanzas | `opendirectory-economics-*`, `opendirectory-macroeconomia 2 6.html`, `opendirectory-microeconomia 2 6.html`, `opendirectory-finanzas*`, `opendirectory-prevision-remuneraciones-chile 1 6.html` |
| Datos, SEO y legal | `opendirectory-informe-datos-seo.html`, `opendirectory-ciberseguridad-leyes.html`, `opendirectory-fintech-turismo-parques.html` |
| Turismo y Patagonia | `opendirectory-gastronomia-ultima-esperanza.html`, `opendirectory-patagonia-economia-marketing.html` |

## Cómo contribuir (dónde va cada cosa)

- Texto, teoría o calculadoras: una página nueva `opendirectory-<tema>.html` en la raíz, con la misma estética (claro/oscuro, español).
- Lógica reutilizable o pesada: `js/` (módulos ES) o un crate Rust compilado a WebAssembly en `rust/`.
- Datos (noticias, empresas): `data/*.json` con esquema fijo, cargados con `fetch` (requiere servidor local: `python -m http.server`).
- Marketing/SEO: ver `opendirectory-patagonia-economia-marketing.html` y `docs/agente-marketing.md`.
- Añada cada página nueva a esta tabla y no cree nombres versionados.

## Publicación

GitHub Pages: Settings → Pages → rama `main`, carpeta `/`. Falta `index.html`; sin él la URL raíz devuelve 404.

## Preguntas abiertas

1. ¿Cuál es la meta de la página: catálogo confiable o experimento de demanda? (`verified:false` convive con el texto «información verificada».)
2. ¿Qué fuente única de datos reemplaza los arreglos JS duplicados?
3. ¿Qué licencia: MIT es solo propuesta; ¿también para los datos?
4. ¿Cuándo se renombran los archivos con sufijos numéricos y se dejan redirecciones?
5. ¿Quién revisa y actualiza las páginas legales y de parques, y con qué fecha de última revisión?
6. ¿Qué métrica decide continuar o pivotar el proyecto?
7. ¿Qué datos personales se almacenarán y bajo qué base legal (Ley 21.719)?
8. ¿Qué parte del agente de marketing se construirá y con qué proveedor de modelo?
