Crea una presentación de EXACTAMENTE 7 láminas en español: una portada y 6 láminas de contenido, en este orden. Es un entregable académico de Ingeniería de Requisitos (UNI, SI322, 2026-II) sobre el caso Comercial Andina S.A.C.

REGLAS GENERALES
- No agregues láminas, imágenes de stock ni datos que no estén en este texto. Respeta todas las cifras, IDs y nombres tal como aparecen.
- Estilo académico sobrio: fondo gris claro (#EEEEEE), azul marino (#2B3067) como color principal, texto oscuro. Usa el ámbar (#F4B400) solo para marcar lo «por validar». Tipografía sans-serif (Arial o similar).
- Usa tablas compactas, tarjetas y diagramas simples. Máximo ~90 palabras por lámina de contenido salvo las tablas; letra legible (mínimo 12 pt). Mantén todos los IDs (R-CA-F-01, AC-CA-01…) en negrita.
- En cada lámina, abajo a la derecha, una línea pequeña: «Equipo D · S10 · Comercial Andina S.A.C.».
- Agrega las notas del expositor de cada lámina en las notas de la diapositiva.

LÁMINA 0 · PORTADA (réplica del estilo de la portada de la Semana 6)
Fondo gris claro; barra vertical azul marino a la izquierda con tres puntos blancos; arriba el texto pequeño «Presentado por el GRUPO D»; título enmarcado con borde azul marino y un cuadrado azul en la esquina superior derecha: «REQUISITOS FUNCIONALES Y NO FUNCIONALES». Debajo del título, una línea: «De las necesidades y el proceso TO-BE a un catálogo verificable».
Panel azul marino a la izquierda con texto blanco: «Caso de negocio» / «Comercial Andina S.A.C.» / «Ingeniería de Requisitos | SI322W» / «Semestre Académico 2026-II» / «Docente» / «Tobías Aliaga Vílchez» / «Semana 10 · Guía práctica».
A la derecha, el título «Integrantes y roles» y esta lista (nombre y código en negrita, rol normal):
- Espinoza Ponte, Joseph Javier 20240096G: Analista de negocio (líder)
- Torres Julca, Enrique 20242074K: Analista SoI / TI
- Calderón Ollero, Freddy Jerry 20244106G: Representante de Ventas
- Torres Oscanoa, Anthony Bryan 20242077J: Representante de Crédito
- Julian Merino Joao Fabrizzio David 20244622E: QA / relator (trazabilidad)
- Canchanya Tito Diego Alonso 20241061B: Representante de Almacén
- Chana Chura, Frank Anthony 20244149H: Representante de Despacho
- Achata Quijaite, Cesar Jared: Apoyo rotativo (Cliente / Atención)

LÁMINA 1 · PROBLEMA, KPI Y EVIDENCIAS
Título: «De 72 % a ≥ 95 %: qué problema resuelven los requisitos».
Tres cifras grandes: «72 %» (144 de 200 pedidos entregados en la ventana comprometida) · «≥ 95 %» (meta didáctica = 190 de 200) · «23 p.p.» de brecha. Debajo, una cadena en flechas: Objetivo (entregar en la ventana comprometida) → KPI → Problema (56 de 200 fuera de ventana) → Causa → Evidencia → Necesidad → Brecha → Cambio TO-BE → Requisito.
Tabla «Señales observadas en la muestra E33 (200 pedidos)»: picking antes del registro final 22 · diferencia de stock o sustitución 19 · crédito posterior al picking 15 · rutas reabiertas 13 · direcciones corregidas 11 · pedidos con dos versiones 8. Nota obligatoria en la tabla: «Las señales pueden coincidir en un mismo pedido: no son causas independientes ni sumables».
Tabla «Brechas seleccionadas» (G-CA → evidencia → tipo de afirmación): G-CA-N-01 picking y crédito sin hito explícito (E33, E34, E35, E38 · observado/interpretado); G-CA-N-02 estados distintos según el actor (E36, E40 · observado); G-CA-N-03 cierre de ruta 13:40–13:45 y cambios tardíos (E33, E38 · observado; causa en hipótesis); G-CA-D-01 versiones fuera de Andina360 (E33, E41 · observado); G-CA-D-02 ventana y hora real sin definición oficial (E34, E36 · observado); G-CA-T-01 integración y disponibilidad (E41, E42 · HIPÓTESIS, en ámbar).
Franja inferior «Lo que no se afirma»: P-1084 y P-1093 salieron tarde con secuencia ordenada (E34, n = 6: asociaciones, no causas) · la causa «caídas de Andina360» fue rechazada en S6 (H-TI) · 95 % de 200 = 190; la brecha de 46 pedidos en la muestra no se atribuye al sistema propuesto.
Notas del expositor (~30 s): «Partimos del mismo caso de S6 y S9. Las seis señales conviven en los pedidos; por eso trabajamos necesidades y brechas, no una causa única.»

LÁMINA 2 · NECESIDADES Y RELACIÓN CON LOS BPMN AS-IS Y TO-BE
Título: «Seis necesidades N-CA y su ruta en el proceso».
Tabla de 6 filas (N-CA · necesidad · estado en S9): N-CA-01 versión vigente y estable del pedido · Validada, condicionada (R4) | N-CA-02 existencias utilizables y separaciones antes de comprometer · Reformulada (U-02) | N-CA-03 estado de crédito y quién autoriza excepciones antes de habilitar despacho · Reformulada (U-03, R2b) | N-CA-04 Despacho con datos completos antes del cierre y criterio de replanificación · Reformulada; R6 validada | N-CA-05 estado y ventana coherentes con aviso de cambios · Validada (confianza media) | N-CA-06 definición y evidencia confiables de «entrega a tiempo» · Validada; R1 pendiente.
A la derecha, dos diagramas simples de flujo, uno encima del otro.
(a) «AS-IS (según S6/S9)»: Pedido informal por WhatsApp o teléfono (~65 %) → Picking anticipado → Crédito tardío → Planilla de rutas aislada → Entrega. Rotúlalo «descrito en S6/S9; alinear con el BPMN AS-IS del equipo».
(b) «TO-BE (BPMN de S9)»: Solicitud recibida → Registrar pedido y crear versión vigente → en paralelo [¿Stock utilizable confirmado?] y [¿Crédito conforme? → excepción de Jefatura] → HITO «Picking habilitado con versión vigente del pedido» → Preparar → ¿Cliente o Ventas cambiaron el pedido? (Sí: nueva versión y reevaluar) → Notificar estado y ventana → ¿Dirección y pedido estables antes del corte 13:40–13:45? (No: replanificar y recalcular ventana) → Entregar → Verificar. Deja un recuadro vacío con la leyenda «Insertar captura del BPMN exportada desde Camunda».
Notas del expositor (~30 s): «Cada necesidad tiene su punto en el TO-BE: versión y hito, stock, crédito, cierre de ruta, aviso al cliente y resultado.»

LÁMINA 3 · CATÁLOGO DE REQUISITOS FUNCIONALES
Título: «Catálogo de RF: el SoI consulta, registra y advierte».
Cuatro tarjetas con ID y enunciado completo, más dos filas resumidas. Texto exacto:
R-CA-F-01 (N-CA-01 · G-CA-D-01 · E33, E34, E36, E38, E40): «El SoI deberá registrar el identificador y la versión vigente del pedido utilizados al emitir la condición de aptitud para preparación, junto con la fecha, la hora, la fuente de confirmación y el estado de verificación de stock y de crédito informado por Almacén y Créditos.»
R-CA-F-02 (N-CA-01, N-CA-05 · E34, E36, E38, E40): «El SoI deberá mostrar a un usuario autorizado de Ventas, Almacén o Despacho, cuando consulte un pedido, la versión vigente, el estado oficial y la fecha-hora y la fuente de cada dato mostrado, identificando las versiones anuladas.»
R-CA-F-03 (N-CA-02 · E33, E35, E36, E41): «El SoI deberá mostrar a Ventas, antes de que confirme un compromiso de entrega, la disponibilidad utilizable y las separaciones pendientes de cada ítem del pedido tal como las informa Almacén, con su fecha-hora y fuente.»
R-CA-F-04 (N-CA-01, 03, 04 · E33, E34, E38, E41): «El SoI deberá advertir a Ventas, Almacén, Créditos y Despacho, cuando se registre una nueva versión del pedido o un cambio de cantidad o dirección, qué verificaciones previas (stock, crédito, aptitud para preparación, ruta) quedan sin vigencia y qué versión las originó, y registrar el aviso.»
Filas resumidas: R-CA-F-05 (N-CA-05) registrar lo comunicado al cliente y marcarlo desactualizado cuando una versión posterior cambie estado o ventana · R-CA-F-06 (N-CA-06) registrar una incidencia de definición cuando falte la ventana prometida o la hora real de entrega.
Pie de lámina: «Cada RF: un solo comportamiento observable; el SoI no decide, solo consulta, consolida, advierte y registra. Estado: propuesto · por validar (ámbar).»
Notas del expositor (~40 s): «Cada requisito nace de una necesidad y de un punto del TO-BE. Ninguno aprueba crédito, certifica stock ni cierra rutas.»

LÁMINA 4 · CATÁLOGO DE REQUISITOS NO FUNCIONALES
Título: «Catálogo de RNF con métrica y validaciones pendientes».
Tres tarjetas con ID, enunciado resumido (conserva las cifras) y una mini tabla propiedad / medida / valor objetivo / método:
R-CA-Q-01 Seguridad (control de acceso): «El SoI deberá aceptar el registro de la autorización de habilitación únicamente cuando el usuario posea un rol vigente reconocido por la autoridad correspondiente, y deberá denegar y auditar toda solicitud de un usuario sin ese rol.» Medida: % de solicitudes sin permiso denegadas y auditadas · Objetivo: 100 % (supuesto académico) · Método: prueba negativa; un rol lector invoca la operación de forma directa (no basta ocultar el botón).
R-CA-Q-02 Auditabilidad e integridad de trazas: «El SoI deberá conservar, para cada registro de versión, aptitud, advertencia, comunicación e incidencia, el autor, la fecha-hora, el motivo (cuando aplique) y la versión del pedido, e impedir que un registro existente se modifique o elimine sin dejar una nueva entrada que lo corrija y lo enlace.» Medida: % de registros completos y registros alterables sin traza · Objetivo: 100 % y 0 (supuesto académico) · Método: inspección de muestra y prueba de alteración.
R-CA-Q-03 Desempeño de consulta: «El SoI deberá responder a la consulta de versión y estado vigentes en no más de 3 segundos para el 95 % de las consultas, con hasta 10 usuarios concurrentes, y si una fuente no responde indicará «dato no disponible» en lugar de mostrar el último dato como actual.» Método: prueba de carga simulada, percentil 95.
Franja ámbar: «Todas las cifras son SUPUESTOS ACADÉMICOS POR VALIDAR; no son datos del caso. Por elicitar con TI: horario de operación, volumen concurrente, fuentes y exclusiones; roles reales y autoridad que los reconoce; período de conservación de registros.»
Notas del expositor (~40 s): «Dejamos las cifras rotuladas como supuesto. Lo que sí es firme es la prueba negativa de seguridad.»

LÁMINA 5 · INFORMACIÓN, INTERFAZ, REGLAS, RESTRICCIONES Y FRONTERA
Título: «Datos, interfaces, reglas y restricciones: quién decide qué».
Izquierda, diagrama de frontera: un recuadro central «SoI: Coordinación y trazabilidad del pedido» con cuatro verbos (consulta · consolida · advierte · registra). Alrededor, cuatro recuadros de autoridad con flechas bidireccionales: Ventas (versión y compromiso) · Almacén (stock físico y sustituciones) · Créditos / jefatura (aprobación y excepciones) · Despacho (cierre y replanificación de rutas). Leyenda: «El SoI NO autoriza crédito, NO certifica ni libera stock físico, NO cierra ni replanifica rutas (RS-CA-01)».
Derecha, tres bloques compactos:
1) Información: R-CA-D-01 historial de versiones y cambios (ID, versión, estado, fecha-hora, autor, motivo, tipo de cambio, fuente, momento respecto del cierre) · R-CA-D-02 ventana prometida y fecha-hora real de entrega.
2) Interfaces conceptuales (emisor → receptor · correlación ID de pedido + versión): R-CA-IF-01 Almacén → SoI · R-CA-IF-02 Créditos → SoI · R-CA-IF-03 SoI ↔ Despacho. «Mecanismo por validar; no se asume ninguna API (RS-CA-02)».
3) Reglas de negocio con autoridad: BR-CA-01 hito «pedido apto para preparación» (Ventas, Almacén, Créditos; R2b pendiente) · BR-CA-02 crédito conforme o excepción, CR-01 (Créditos / jefatura) · BR-CA-03 estabilidad antes del cierre 13:40–13:45 (Despacho; vigencia por confirmar, R6) · BR-CA-04 promesa preliminar frente a compromiso confirmado (Ventas, Almacén).
Notas del expositor (~40 s): «Lo más importante de esta lámina es la frontera: cada decisión conserva su dueño.»

LÁMINA 6 · ACEPTACIÓN, TRAZABILIDAD Y PENDIENTES
Título: «Cómo se comprobará y qué falta decidir».
Izquierda, ejemplo de AC con formato Dado / Cuando / Entonces:
AC-CA-01 (R-CA-F-01) — Dado un pedido P con versión V2 confirmada, con stock verificado y crédito conforme; Cuando Ventas emite la condición de aptitud; Entonces el SoI conserva P, V2, fecha-hora, fuente y estado de verificación. Caso negativo: si luego llega V3, la condición con V2 queda identificable y no se reutiliza sin una nueva emisión.
AC-CA-Q-01 (R-CA-Q-01) — Caso negativo: un rol lector invoca directamente la operación protegida; la solicitud se deniega y se audita.
Centro, cadena de trazabilidad de ejemplo en flechas: E38 / E41 → N-CA-01 → G-CA-D-01 → C-01 y C-05 (TO-BE) → R-CA-F-01 → AC-CA-01. Debajo, tres indicadores: «6 de 6 necesidades con RF» · «20 requisitos · 16 AC · 11 escenarios» · «Estado de los 11 escenarios: diseñado / no ejecutado».
Derecha, «Decisiones pendientes» (ámbar): R4 quién fija la versión oficial · U-02 definición de «stock disponible» · U-03 / R2b autoridad de excepciones y preparar antes del crédito · U-04 y R6 cambios tras el cierre y vigencia 13:40–13:45 · Q-CA-01 / R1 timestamp oficial y dueño del KPI · G-CA-T-01 validación técnica de fuentes · Decisión del equipo sobre un BPMN v2 (evento «Cambio de pedido recibido»).
Cierre: «Ninguna prueba se informa como aprobada: no hay software ni datos reales. Siguiente paso (S11): interacción, historias de usuario y casos de uso sobre estos requisitos.»
Notas del expositor (~50 s): «Si nos piden defender una cadena: E38 y E41 llevan a N-CA-01, a la brecha de versión y a R-CA-F-01; su criterio negativo es que V2 no se reutiliza cuando llega V3.»
