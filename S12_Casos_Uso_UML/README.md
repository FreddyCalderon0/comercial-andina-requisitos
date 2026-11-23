# S12_Casos_Uso_UML · Casos de uso UML y escenarios

Comercial Andina S.A.C. · Equipo D · Ingeniería de Requisitos (SI322) · 2026-II · v1.0 · 2026-11-23

Continúa la entrega de la Semana 11 **sin sobrescribirla**. Los catálogos de requisitos de S10 están en `../S10_RF_RNF/`, las historias y criterios de S11 en `../S11_Historias_y_Backlog/` y el BPMN TO-BE de S9 en `../S9_Arquitectura_TOBE/`; los tres se conservan sin cambios como versiones históricas. Los IDs de HU, HUAC, RF/RNF, AC y preguntas son los reales del expediente del equipo; no se renumeró nada.

## Contenido

| Archivo | Para qué sirve |
|---|---|
| `diagramas/S12_EquipoD_Comercial_Andina_CU_Diagrama_v1.0.drawio` | **Fuente editable** del diagrama UML (diagrams.net / draw.io) |
| `diagramas/S12_EquipoD_Comercial_Andina_CU_Diagrama_v1.0.puml` | Misma estructura en PlantUML, como fuente alternativa |
| `diagramas/S12_EquipoD_Comercial_Andina_CU_Diagrama_v1.0.svg` y `.png` | Exportación legible a tamaño de proyector (PNG de 2800 px) |
| `S12_EquipoD_Comercial_Andina_Fichas_CU_v1.0.docx` | Fichas detalladas de `CU-CA-02` y `CU-CA-03` (flujo principal, dos alternos y una excepción por CU) y fichas breves de `CU-CA-01` y `CU-CA-04` |
| `S12_EquipoD_Comercial_Andina_Fichas_CU_v1.0.md` | Copia en Markdown de las fichas, para ver cambios con `git diff` |
| `S12_EquipoD_Comercial_Andina_Matrices_CU_v1.0.xlsx` | Libro con la tabla de origen de los CU, actores, 12 escenarios `ES-CA-12-xx`, trazabilidad en ambos sentidos, candidatos S12, bitácora de elicitación, hallazgos, bitácora de cambios y una hoja `Cobertura` con fórmulas |
| `csv/` | Una copia en CSV (UTF-8) de cada hoja de datos del libro |
| `S12_EquipoD_Comercial_Andina_Casos_Uso_v1.0.pptx` | **Pendiente de agregar**: la presentación de seis láminas no formó parte de esta entrega |

Hojas del libro: `LEEME`, `Casos_de_Uso`, `Actores`, `Escenarios`, `Trazabilidad`, `Traza_Inversa`, `Candidatos_S12`, `Bitacora_Elicitacion`, `Hallazgos`, `Bitacora_Cambios`, `Cobertura`.

## Resumen

- **4 casos de uso** graficados. `CU-CA-01` «Consultar condición previa al picking» (base parcial + candidato), `CU-CA-02` «Consultar disponibilidad reportada» (candidato), `CU-CA-03` «Registrar confirmación humana de despacho» (candidato, sin RF ni HU aprobados) y `CU-CA-04` «Consultar incidente por cambio tardío» (base S10).
- **Actores.** Primarios: Operario de preparación, Almacenero y Coordinador de Despacho. Secundarios: Almacén y Créditos, como fuentes de datos. Ventas y TI son interesados, no actores. Asociaciones simples: no se usó «include» ni «extend» (`Q-CA-S12-10`).
- **12 escenarios** `ES-CA-12-01…12` (4 principales, 5 alternos, 3 excepciones), todos «diseñado, no ejecutado». Los seis de la guía son `01…06`; `07…12` completan el flujo principal de `CU-CA-03` y los casos de apoyo.
- **7 candidatos S12**, ninguno aprobado: `NC-S12-01`, `HU-CA-CAND-S12-01`, `R-CA-F-CAND-S12-01` y `HUAC-CA-CAND-S12-01…04`.
- **11 preguntas de elicitación** (`Q-CA-S12-01…11`), **10 hallazgos** (`H-S12-01…10`) y 10 registros de cambios, decisiones y solicitudes (`CH`, `DM`, `SC`).

## Cambios respecto de S11

- Nuevos artefactos S12: todo lo listado arriba. No se editó ningún archivo de S9, S10 ni S11.
- Único archivo previo tocado: el `README.md` de la raíz, con una fila nueva en la tabla de carpetas y la convención de commit `S12: …`.
- **Diferencias entre la guía y el expediente real** (hallazgo `H-S12-04`). La guía habla de `HU-CA-01…05` y `HUAC-CA-01…10`, y usa `R-CA-F-CAND-S11-01` como candidato de la consulta de stock. El catálogo del equipo tiene `HU-CA-01…08`, `HUAC-CA-01…14`, y el candidato de disponibilidad es `R-CA-F-CAND-S11-02`. Se conservaron los IDs reales.

## Límites conocidos

- Los pedidos `P-2101…P-2106` y los datos `D-S11` y `D-S12` son **datos didácticos sintéticos**; no son evidencia E33–E42 ni reglas aprobadas.
- Ningún requisito, historia ni criterio candidato figura como aprobado. Las pruebas están **diseñadas / no ejecutadas**: no hay software ni datos reales.
- «Confirmar despacho» no está definido (`Q-CA-S12-01`). `CU-CA-03` se apoya en una historia y un requisito candidatos; `HU-CA-05` solo cubre detectar cambios tardíos.
- `R-CA-Q-01` hoy se limita al «registro de la habilitación»; ampliarlo a la confirmación de despacho es una solicitud de cambio (`SC-S12-03`), no un hecho.
- `ES-CA-12-03` tiene dos resultados posibles según a qué versión corresponden las 9 unidades de `P-2104` (`Q-CA-S11-09`, `H-S12-06`).
- `D-S12` no trae las direcciones anterior y nueva de `P-2105` ni el pedido de `ES-CA-12-06`; los escenarios no inventan esos valores (`H-S12-10`).
- `HU-CA-03`, `HU-CA-04` y `HU-CA-06` no tienen caso de uso en esta entrega (`H-S12-08`).
- Las fichas de `CU-CA-01` y `CU-CA-04` son breves: flujo principal y una variante.
- Las fechas de revisión propuestas (2026-11-30) son una sugerencia del equipo.
- El `.drawio` se generó como XML estándar de mxGraph y el `.puml` como texto PlantUML; **no se abrieron en diagrams.net ni se renderizaron con PlantUML** en la sesión donde se prepararon. El SVG y el PNG sí se renderizaron y revisaron. Conviene abrir el `.drawio` y el `.puml` una vez antes del commit.

## Uso de IA y verificación del equipo (completar antes del commit)

El borrador se preparó con apoyo de IA a partir de la guía S12 v1.0 y de los archivos S9, S10 y S11 del equipo. Comprobaciones hechas al generar los archivos:

- [x] Cada ID de HU, HUAC, RF/RNF, AC, N-CA y pregunta citado existe en los catálogos S10 y S11 (comprobado por script).
- [x] Cada escenario cita solo requisitos, HUAC y AC que figuran en la lista de su caso de uso, y cada flujo de las fichas tiene su escenario.
- [x] Las fórmulas de la hoja `Cobertura` se recalcularon sin errores.
- [x] El Word se convirtió a PDF y se revisó página por página; el diagrama se revisó en PNG.
- [x] S9, S10 y S11 son idénticos byte a byte a la entrega recibida.

Pendiente de revisión humana:

- [ ] Revisión cruzada: un integrante que no dibujó el diagrama comprueba actores, límite, nombres, lectura e identificadores; otro revisa alternos, permisos y fuentes (registrar qué se cambió).
- [ ] Abrir `.drawio` y `.puml` y confirmar que se ven como el PNG.
- [ ] Asignar responsables con nombre en las fichas y confirmar las fechas de revisión propuestas.
- [ ] Decidir `SC-S12-01…04` (solicitudes de cambio) y el vocabulario de estados (`H-S12-05`).
- Cambios hechos por el equipo tras la revisión: _(completar)_

## Versionado

- S9, S10 y S11 se subieron en commits anteriores, por lo que sus versiones quedan recuperables en el historial. Commit de S11: `130c87b7b6693e048255c5d543db7595b057ff78`.
- Commit de S12 (mensaje sugerido): `S12: casos de uso UML y escenarios v1.0 (Equipo D)`
- Referencia al commit S12: f52812778d8951ea47943d9bbe3aa20497d27dc6

## Puente a la Semana 13

Las fichas CU y el diagrama son insumos de la ERS preliminar (PC3). Queda decidir allí si `HU-CA-03`, `HU-CA-04` y `HU-CA-06` derivan casos de uso adicionales y completar los alternos de `CU-CA-01` y `CU-CA-04`. No se adelantó ningún diagrama de flujo de datos.
