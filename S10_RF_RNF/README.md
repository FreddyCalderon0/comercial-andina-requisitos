# S10_RF_RNF · Requisitos funcionales y no funcionales

Comercial Andina S.A.C. · Equipo D · Ingeniería de Requisitos (SI322) · 2026-II · v1.0 · 2026-11-02

Continúa la entrega de la Semana 9 (arquitectura empresarial y proceso TO-BE) **sin sobrescribirla**. Los archivos de S9, incluido el BPMN TO-BE, están en `../S9_Arquitectura_TOBE/` y se conservan sin cambios como versiones históricas.

## Contenido

| Archivo | Para qué sirve |
|---|---|
| `S10_EquipoD_Comercial_Andina_Catalogo_RF_RNF_v1.0.xlsx` | Catálogo (6 RF, 3 RNF), anexos de información, interfaces, reglas y restricciones, plan de medición de RNF, matriz de trazabilidad en ambos sentidos, criterios de aceptación, escenarios, bitácora de elicitación, pendientes, equivalencias S9→S10 y hoja de cobertura con fórmulas |
| `S10_EquipoD_Comercial_Andina_Ficha_Requisitos_v1.0.docx` | Fichas completas de los 20 requisitos (plantilla 11.1 de la guía) y anexos |
| `csv/` | Una copia en CSV (UTF-8) de cada hoja de datos del libro, para ver cambios con `git diff` |
| `prompt_gamma_S10.md` | Prompt para generar la presentación de 6 láminas más portada |
| `S10_EquipoD_Comercial_Andina_RF_RNF_v1.0.pptx` | **Pendiente de agregar**: se genera con el prompt de Gamma y se exporta con este nombre |

## Resumen del catálogo

- 6 RF (`R-CA-F-01…06`), 3 RNF (`R-CA-Q-01…03`), 2 requisitos de información (`R-CA-D-01…02`), 3 interfaces (`R-CA-IF-01…03`), 4 reglas de negocio (`BR-CA-01…04`) y 2 restricciones (`RS-CA-01…02`).
- 16 criterios de aceptación (`AC-CA-…`), 11 escenarios (`ESC-01…11`) y 19 preguntas de bitácora (`Q-CA-S10-01…19`).
- Las seis necesidades N-CA tienen al menos un RF (hoja `Cobertura`).
- Los 20 candidatos de S9 tienen disposición en `Equivalencias_S9_S10`. Los IDs cambiaron porque la guía S10 separa RNF (`Q`), información (`D`), interfaz (`IF`), reglas (`BR`) y restricciones (`RS`).

## Cambios respecto de S9

- Nuevos artefactos S10: todo lo listado arriba. No se editó ningún archivo de S9.
- **BPMN TO-BE: sin cambios.** La revisión frente a la especificación dejó un hallazgo (`P-S10-06` en `Pendientes`): el cambio del pedido se verifica solo en la compuerta 3 y en el cierre de ruta; un cambio entre ambos puntos lo cubre únicamente el aviso asíncrono de `R-CA-F-04`. Si el equipo decide modelar el evento «Cambio de pedido recibido», será un `.bpmn` v2 nuevo, sin tocar el de S9.

## Límites conocidos

- Ningún requisito figura como validado: no hubo elicitación real. Estado máximo: «propuesto · por validar».
- La bitácora usa solo evidencia E33–E42, S6 y S9. Donde no consta una respuesta, la pregunta queda abierta.
- Las cifras de los RNF (3 s, percentil 95, 10 usuarios, 100 %) son **supuestos académicos por validar**.
- Los escenarios están **diseñados / no ejecutados**. No se informa ninguna prueba como aprobada.
- No se dispuso del BPMN AS-IS (S3–S4), del árbol/Ishikawa de S5 ni de los textos de R1, R3, R5 y RES-01…03 del Word de S6; E37 no está descrita. Conviene alinear nombres con esos artefactos.
- La asignación de roles de la portada de la presentación es una propuesta; ajustarla si el equipo asignó otra.

## Uso de IA y verificación del equipo (completar antes del commit)

El borrador se preparó con apoyo de IA a partir de los archivos S6 y S9 del equipo. Según la guía, el equipo indica qué verificó:

- [ ] Se contrastaron las cifras de E33 y E34 con la presentación de S6.
- [ ] Se revisó que cada enunciado respete la frontera del SoI (no aprueba crédito, no certifica stock, no cierra rutas).
- [ ] Se revisaron los IDs y la hoja `Equivalencias_S9_S10`.
- [ ] Se revisó que las cifras de los RNF estén rotuladas como supuesto académico.
- [ ] Revisión cruzada: otro integrante señaló al menos una ambigüedad, un caso negativo ausente o una posible invasión de autoridad (registrar cuál y qué se cambió).
- Cambios hechos por el equipo tras la revisión: _(completar)_

## Versionado

- S9 se subió en un commit anterior (`S9: entrega Semana 9 (Equipo D)`), por lo que la versión previa queda recuperable en el historial del repositorio.
- Commit de S10: `S10: catálogo RF/RNF v1.0 (Equipo D)`
- Referencia al commit: _(completar con el hash tras el push)_

## Puente a la Semana 11

Los RF/RNF y sus AC son la base para interacción, historias de usuario / casos de uso y validación. No se adelantó ninguno de esos artefactos.
