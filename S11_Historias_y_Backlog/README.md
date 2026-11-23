# S11_Historias_y_Backlog · Historias de usuario y backlog

Comercial Andina S.A.C. · Equipo D · Ingeniería de Requisitos (SI322) · 2026-II · v1.0 · 2026-11-23

Continúa la entrega de la Semana 10 **sin sobrescribirla**. El catálogo RF/RNF de S10 está en `../S10_RF_RNF/` y el BPMN TO-BE de S9 en `../S9_Arquitectura_TOBE/`; ambos se conservan sin cambios como versiones históricas. Los IDs RF/RNF de S10 no se renumeraron y sus enunciados se copiaron del catálogo S10.

## Contenido

| Archivo | Para qué sirve |
|---|---|
| `S11_EquipoD_Comercial_Andina_HU_Backlog_v1.0.xlsx` | Libro con el catálogo de HU, la matriz HUAC, el backlog priorizado, la trazabilidad en ambos sentidos, la bitácora de preguntas, el registro de hallazgos y una hoja `Cobertura` con fórmulas |
| `csv/` | Una copia en CSV (UTF-8) de cada hoja de datos del libro, para ver cambios con `git diff` |

Hojas del libro: `LEEME`, `Datos_D-S11`, `Autoridades_D-S11-02`, `Necesidades_N-CA`, `Epicas`, `BASE_S10_S11`, `Candidatos_RF_S11`, `Catalogo_HU`, `Matriz_HUAC`, `Backlog_S11`, `Trazabilidad`, `Traza_Inversa_HUAC`, `Bitacora_Q_S11`, `Hallazgos`, `Cobertura`.

## Resumen

- **8 historias** (`HU-CA-01…08`): 6 en el incremento propuesto y 2 excluidas (Won't this time: `HU-CA-07` y `HU-CA-08`). Cuatro son del frente Almacén–Operario (`HU-CA-01`, `02`, `03`, `06`) y dos complementarias del flujo, de Ventas (`HU-CA-04`) y Despacho (`HU-CA-05`).
- **14 criterios HUAC** (`HUAC-CA-01…14`): stock suficiente e insuficiente, crédito observado, cambio de versión, ruta cerrada, dato ausente y una prueba de seguridad del RNF `R-CA-Q-01`. Todos están `diseñado / no ejecutado`.
- **Backlog** con 2 épicas (`EP-CA-01`, `EP-CA-02`), MoSCoW, valor, urgencia, esfuerzo, dependencia, orden y razonamiento por historia.
- **4 requisitos candidatos** (`R-CA-F-CAND-S11-01…04`), ninguno aprobado, para lo que S10 no cubre.
- **16 preguntas abiertas** (`Q-CA-S11-01…16`) y **13 hallazgos** (`H-S11-01…13`).

## Cambios respecto de S10

- Nuevos artefactos S11: todo lo listado arriba. No se editó ningún archivo de S9 ni de S10.
- Único archivo previo tocado: el `README.md` de la raíz, con una fila nueva en la tabla de carpetas.
- **BPMN TO-BE: sin cambios.** Las historias solo citan sus elementos; el hallazgo `P-S10-06` (evento «Cambio de pedido recibido») sigue abierto como `Q-CA-S11-14`.

## Límites conocidos

- Los pedidos `P-2101…P-2106` y las reglas `D-S11-01…05` son **datos didácticos sintéticos** de la guía; no son evidencia E33–E42 ni reglas aprobadas.
- Ningún requisito figura como validado. Las pruebas están **diseñadas / no ejecutadas**: no hay software ni datos reales.
- Los puntajes y el MoSCoW son una **propuesta ilustrativa** (`D-S11-04`), no una aprobación de alcance. Un Must sin requisito validado no queda comprometido.
- No hubo una ronda de elicitación real: la bitácora contiene preguntas abiertas y deja una columna para registrar la simulación en clase.
- El BPMN AS-IS (S3–S4) no estaba en el repositorio recibido, y el texto de E39 está por confirmar (según S10).
- Algunos datos de prueba están derivados porque la guía no los trae (ventana, comunicación, cantidad hallada, versión del informe de `P-2104`); están marcados en cada HUAC y en `Hallazgos`.
- `R-CA-F-06` y `N-CA-06` no tienen ninguna historia en el incremento (`H-S11-01`), y `R-CA-Q-03` no tiene HUAC propio (`H-S11-02`).

## Uso de IA y verificación del equipo (completar antes del commit)

El borrador se preparó con apoyo de IA a partir de la guía S11 v1.0 y de los archivos S9 y S10 del equipo. Comprobaciones hechas al generar los archivos:

- [x] Los identificadores de requisitos, AC-CA y escenarios citados existen en el catálogo S10.
- [x] Los elementos BPMN citados existen en el `.bpmn` de S9.
- [x] Las columnas calculadas del libro coinciden con los CSV y las fórmulas se recalcularon sin errores.

Pendiente de revisión humana:

- [ ] Revisión cruzada: otro integrante comprueba historias, criterios negativos y MoSCoW (registrar qué se cambió).
- [ ] Ajustar puntajes y MoSCoW con el criterio del equipo; asignar responsables con nombre.
- [ ] Decidir `H-S11-03` (etiqueta «NO APTO») y la lista de estados (`H-S11-07`).
- Cambios hechos por el equipo tras la revisión: _(completar)_

## Versionado

- S9 y S10 se subieron en commits anteriores, por lo que sus versiones quedan recuperables en el historial.
- Commit de S11 (mensaje sugerido): `S11: historias de usuario y backlog v1.0 (Equipo D)`
- Referencia al commit S11: _(completar con el hash tras crear el commit; no puede conocerse antes de crearlo)_

## Puente a la Semana 12

Las historias, sus actores, objetivos y criterios permiten elegir los casos de uso UML de S12 (flujo principal, alternos y excepciones). No se adelantó ningún diagrama.
