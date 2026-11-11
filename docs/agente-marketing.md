# Borrador: agente de marketing online para OpenDirectory

Estado: **borrador de diseño**. No hay código del agente en este repositorio.

## Propósito
Ayudar a las empresas de Magallanes a mejorar su presencia online (SEO local, contenido, reseñas) **sin automatizar nada que engañe** a clientes o buscadores.

## Alcance
| Hace | No hace |
|---|---|
| Auditar una ficha (título, descripción, datos estructurados, enlaces) | Publicar reseñas ni enlaces comprados |
| Sugerir palabras clave a partir de datos de Search Console aportados | Prometer posiciones en buscadores |
| Redactar borradores de textos en ES/EN para revisión humana | Enviar mensajes comerciales sin consentimiento |
| Generar informes mensuales de métricas | Guardar datos personales innecesarios |

## Entradas
- Ficha de la empresa (campos del formulario de registro).
- Exportaciones propias: Search Console, analítica, reseñas.
- Precios y reglas del parque desde las páginas del repositorio (con fecha de revisión).

## Salidas
Informe de auditoría, lista priorizada de mejoras, borradores de contenido marcados «generado por IA, pendiente de revisión».

## Reglas (guardrails)
1. Toda afirmación factual cita su fuente y fecha; si no la hay, dice «sin dato».
2. Un humano aprueba antes de publicar.
3. Cumple las prácticas éticas de la página `opendirectory-patagonia-economia-marketing.html` y la ley de datos de `opendirectory-ciberseguridad-leyes.html`.
4. No almacena secretos en el repositorio.

## Arquitectura propuesta
Interfaz web estática → API (TypeScript/Node o Python) → modelo de lenguaje → base de datos (ver `opendirectory-informe-datos-seo.html`). Registro de cada acción para auditoría.

## Evaluación
- Conjunto de fichas de prueba con auditorías hechas por una persona experta; medir coincidencia.
- Revisión de errores factuales (tasa de afirmaciones sin fuente).
- Prueba A/B de los textos generados frente a los escritos a mano, con métrica pre-registrada.

## Preguntas abiertas
- ¿Quién es responsable de aprobar el contenido?
- ¿Qué modelo y proveedor, y qué datos se pueden enviar a terceros (Ley 21.719)?
- ¿Cómo se mide el beneficio real para las empresas?
