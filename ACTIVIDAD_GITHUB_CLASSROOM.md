### FILE: README.md

[INICIO_ARCHIVO]
# Microproyecto ARM64: Bitácora de Diagnóstico en Terminal

## Contexto
En esta actividad diseñarás y documentarás un microproyecto académico con núcleo en ARM64 Assembly para resolver una necesidad básica de diagnóstico en sistemas locales: capturar, formatear y mostrar información técnica mínima en terminal. El foco está en planear bien antes de codificar.

## Objetivo general
Diseñar, documentar e implementar de forma mínima un microproyecto en ARM64 Assembly (con al menos una macro funcional) que ejecute de 3 a 5 funcionalidades pequeñas, medibles y probables de completar en un entorno con recursos limitados.

## Competencias
- Aplica fundamentos de arquitectura de computadoras en un programa ARM64 pequeño.
- Documenta decisiones técnicas con estructura profesional.
- Define alcance realista y criterios de aceptación verificables.
- Diseña pruebas funcionales simples para validar comportamiento.
- Evalúa críticamente el uso de IA en procesos técnicos.

## Instrucciones rápidas
1. Lee y completa todos los documentos en `docs/`.
2. Define de 3 a 5 funcionalidades pequeñas y evita ampliar el alcance.
3. Implementa núcleo en ARM64 Assembly con al menos 1 macro funcional (ejemplo: macro para impresión en stdout).
4. Verifica manualmente con casos de prueba documentados.
5. Entrega exactamente los 6 archivos solicitados, completos y coherentes entre sí.

## Criterios de entrega
- Se entregan exactamente 6 archivos obligatorios.
- La propuesta respeta restricciones: sin Python, sin stack pesado, sin Docker/Kubernetes, sin cloud adicional ni APIs pagadas.
- Existe coherencia entre problema, arquitectura, casos de uso y plan de pruebas.
- El proyecto está acotado a ~150 líneas funcionales sugeridas.
- Se declara y justifica el uso de IA con validación manual.

## Rúbrica
| Criterio | Excelente (100-90) | Satisfactorio (89-80) | Básico (79-70) | Insuficiente (<70) |
|---|---|---|---|---|
| Documentación técnica | Completa, clara, coherente | Completa con detalles menores faltantes | Parcial o ambigua | Incompleta o incongruente |
| Alcance y factibilidad | Muy bien acotado (3-5 funciones) | Acotado con ligeros excesos | Alcance confuso | Alcance inviable |
| Diseño ARM64 + macro | Núcleo ARM64 y macro clara | ARM64 correcto con macro poco clara | ARM64 parcial | No cumple ARM64/macro |
| Plan de pruebas | Casos medibles y completos | Casos útiles con huecos | Casos limitados | Sin criterios verificables |
| Reflexión de IA e integridad | Crítica, honesta y verificable | Adecuada con poca profundidad | Muy superficial | Ausente o no verificable |
[FIN_ARCHIVO]

### FILE: docs/propuesta.md

[INICIO_ARCHIVO]
# Propuesta técnica del microproyecto

## Problema
En prácticas introductorias de sistemas, el estudiantado suele ejecutar comandos sin comprender cómo se trasladan los datos al nivel de bajo nivel. Hace falta un microproyecto que permita observar flujo básico de entrada/salida y formateo en ARM64 Assembly de forma tangible y corta.

## Justificación
Un proyecto breve con núcleo ARM64 fortalece comprensión de registros, syscalls y estructura del programa. Documentarlo de forma rigurosa desarrolla competencias de ingeniería: planeación, delimitación de alcance, evaluación y trazabilidad de decisiones.

## Alcance y límites
**Alcance (3 a 5 funcionalidades):**
1. Mostrar encabezado del programa en terminal.
2. Capturar un parámetro simple (por ejemplo, etiqueta de ejecución).
3. Imprimir resumen con formato fijo.
4. Reportar código de salida claro (éxito/error básico).

**Límites:**
- Máximo sugerido: ~150 líneas funcionales.
- Sin Python.
- Sin frameworks pesados.
- Sin Docker/Kubernetes.
- Sin cloud ni APIs pagadas.
- Sin base de datos obligatoria.

## Arquitectura (alto nivel)
- **Capa principal obligatoria:** ARM64 Assembly.
- **Macro obligatoria en Assembly:** macro `PRINT` para encapsular syscall de escritura en stdout.
- **Capa opcional mínima (solo si se requiere):** Bash para script de compilación/ejecución local.
- **Artefactos documentales:** `README.md` y archivos en `docs/` como base de evaluación.

## Riesgos y mitigación
1. **Riesgo:** Sobrepasar alcance por agregar funciones.
   - **Mitigación:** Congelar alcance en 4 funciones y registrar cambios.
2. **Riesgo:** Errores de sintaxis Assembly difíciles de depurar.
   - **Mitigación:** Probar por bloques pequeños y validar cada syscall.
3. **Riesgo:** Dependencia excesiva de IA en código.
   - **Mitigación:** Exigir validación manual y bitácora de decisiones.
4. **Riesgo:** Falta de coherencia documental.
   - **Mitigación:** Revisar trazabilidad entre propuesta, caso de uso y pruebas.

## Supuestos
- El entorno académico cuenta con herramientas básicas para ensamblar/ligar ARM64 o emulación equivalente institucional.
- El docente evaluará principalmente documentación, coherencia y calidad de criterios de prueba.
- El microproyecto es individual salvo que la clase indique trabajo en pareja.
[FIN_ARCHIVO]

### FILE: docs/caso_de_uso.md

[INICIO_ARCHIVO]
# Caso de uso principal

## Actor principal
Estudiante de nivel medio superior o superior en asignaturas de arquitectura de computadoras o sistemas embebidos.

## Flujo principal
1. El actor ejecuta el programa en terminal con un parámetro de etiqueta.
2. El programa valida que exista entrada mínima.
3. El programa imprime encabezado usando macro de Assembly.
4. El programa muestra resumen técnico en formato fijo.
5. El programa termina con código de salida de éxito.

## Escenario alterno 1
**Entrada vacía o parámetro ausente**
1. El actor ejecuta sin parámetro.
2. El programa detecta ausencia de entrada.
3. El programa imprime mensaje de uso.
4. El programa termina con código de error controlado.

## Escenario alterno 2
**Entrada con longitud no permitida**
1. El actor envía etiqueta demasiado larga.
2. El programa aplica validación básica de longitud.
3. El programa imprime advertencia y recorte o rechazo (según diseño elegido).
4. El programa finaliza con resultado consistente con política definida.

## Precondiciones
- Entorno con soporte para compilación/ejecución ARM64 definido por la institución.
- Archivos documentales completos y accesibles en el repositorio.
- Alcance funcional congelado (3 a 5 funciones).

## Postcondiciones
- Se imprime salida esperada de forma legible.
- Se registra cumplimiento o falla según criterios de pruebas.
- Queda evidencia de validación manual.

## Criterios de aceptación
- Existe macro funcional de Assembly usada en ejecución real.
- Se cubren al menos 4 casos de prueba funcionales.
- No se usa Python ni stack pesado.
- La documentación y ejecución son coherentes entre sí.
[FIN_ARCHIVO]

### FILE: docs/estructura_repositorio.md

[INICIO_ARCHIVO]
# Estructura del repositorio

## Árbol de carpetas
```text
proyecto-arm64-mini/
├── README.md
└── docs/
    ├── propuesta.md
    ├── caso_de_uso.md
    ├── estructura_repositorio.md
    ├── plan_de_pruebas.md
    └── reflexion_ia.md
```

## Descripción de archivos clave
- `README.md`: guía general, competencias, rúbrica y criterios de entrega.
- `docs/propuesta.md`: definición del problema, arquitectura y límites.
- `docs/caso_de_uso.md`: flujo operativo y escenarios alternos.
- `docs/estructura_repositorio.md`: organización y convenciones.
- `docs/plan_de_pruebas.md`: estrategia y tabla de validación.
- `docs/reflexion_ia.md`: uso responsable de IA e integridad académica.

## Convenciones de nombres
- Archivos en minúsculas y con guion bajo.
- Encabezados claros por sección en Markdown.
- Identificadores de pruebas con prefijo `CP-`.
- Versiones de entrega con etiquetas simples tipo `v0.1-docs`, `v0.2-validacion`.

## Versionado simple
- `v0.1`: documentos iniciales completos.
- `v0.2`: ajustes por retroalimentación docente.
- `v1.0`: versión final validada contra plan de pruebas.
- Cada cambio debe dejar nota breve del motivo en el commit.
[FIN_ARCHIVO]

### FILE: docs/plan_de_pruebas.md

[INICIO_ARCHIVO]
# Plan de pruebas

## Estrategia de pruebas
Se aplicarán pruebas manuales funcionales en terminal, enfocadas en validar entradas válidas, entradas inválidas y consistencia de salida. La prioridad es comprobar comportamiento observable y cumplimiento del alcance definido.

## Casos de prueba
| ID | Entrada | Resultado esperado | Criterio de éxito |
|---|---|---|---|
| CP-01 | Ejecutar con parámetro válido corto | Muestra encabezado y resumen técnico | Salida legible + código de éxito |
| CP-02 | Ejecutar sin parámetro | Mensaje de uso o error controlado | Código de error documentado |
| CP-03 | Parámetro con longitud límite | Procesa sin romper formato | Salida completa sin corrupción |
| CP-04 | Parámetro demasiado largo | Rechazo o recorte según diseño | Comportamiento coincide con especificación |
| CP-05 | Varias ejecuciones consecutivas | Resultados consistentes | Misma lógica en cada corrida |

## Cobertura mínima
- 100% de funcionalidades definidas en alcance (3 a 5) con al menos un caso cada una.
- Al menos 2 pruebas de manejo de error.
- Verificación explícita de uso de macro Assembly en ejecución.

## Criterios de aprobación
- Se aprueba cuando al menos 4/5 casos pasan y ningún fallo contradice requisitos críticos.
- Si falla un criterio crítico (macro no funcional, uso de Python, alcance excesivo), la entrega requiere corrección antes de acreditarse.
- La evidencia de pruebas debe ser trazable y coherente con documentación.
[FIN_ARCHIVO]

### FILE: docs/reflexion_ia.md

[INICIO_ARCHIVO]
# Reflexión sobre uso de IA

## Uso de IA
La IA se utilizó como apoyo para:
- Proponer estructura inicial de documentación.
- Sugerir redacción técnica clara.
- Revisar consistencia entre objetivos, casos de uso y pruebas.

## Validación manual
- Se revisó cada sección para asegurar viabilidad técnica real.
- Se ajustaron alcances para mantener proyecto pequeño.
- Se contrastó que la propuesta cumpla ARM64 Assembly y macro obligatoria.

## Riesgos de IA
- Generar soluciones demasiado grandes o fuera del contexto de la clase.
- Producir instrucciones no compatibles con el entorno local.
- Introducir errores conceptuales si no se valida de forma crítica.

## Aprendizajes
- La IA acelera borradores, pero no sustituye criterio técnico.
- La calidad depende de validar manualmente cada decisión.
- La documentación clara evita retrabajo en implementación.

## Declaración de integridad académica
Declaro que esta propuesta fue revisada y comprendida por mí. Cualquier apoyo de IA se usó como herramienta de asistencia, no como sustituto de mi análisis. Me hago responsable de la coherencia técnica y de la autenticidad de la entrega.
[FIN_ARCHIVO]

## Checklist final

- ✅ README.md
- ✅ docs/propuesta.md
- ✅ docs/caso_de_uso.md
- ✅ docs/estructura_repositorio.md
- ✅ docs/plan_de_pruebas.md
- ✅ docs/reflexion_ia.md
