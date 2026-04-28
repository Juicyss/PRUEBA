# Propuesta de Práctica Temática (Enfoque en Documentación)

## 1) Título de la actividad
**Diseño de Mini Proyecto Temático: Documentación Primero**

> Ejemplos de temas válidos:
> - **Mini Toolkit en ARM64**
> - **Asistente de Estudio en Terminal**
> - **Reporteador de Información del Sistema**
> - **Organizador de Archivos**
> - **Juego de Aprendizaje en Línea de Comandos**

---

## 2) Descripción general
En esta actividad vas a **diseñar la propuesta de un proyecto pequeño** orientado a terminal, con énfasis en la **planeación, documentación y justificación técnica** antes de escribir código.

Debes seleccionar **un lenguaje principal** para tu propuesta:
- ARM64 Assembly
- C
- Python
- Bash

> **Nota importante:** Si eliges **ARM64 Assembly**, limita tu alcance a un programa **muy pequeño** (por ejemplo: operaciones básicas, parsing mínimo de argumentos o utilerías simples), ya que el objetivo principal es documentar bien la idea.

### Propósito académico
- Practicar cómo aterrizar una idea técnica en documentos claros.
- Definir un alcance realista para un proyecto breve.
- Justificar decisiones de diseño y estructura de repositorio.
- Preparar una base sólida para implementación posterior.

### Restricciones del proyecto
Para mantener el proyecto viable con herramientas gratuitas y tiempo limitado:
- Debe ser un proyecto **pequeño y acotado**.
- Evita frameworks grandes.
- No uses APIs pagadas.
- No incluyas bases de datos complejas.
- No uses servicios en la nube.
- No uses contenedores.
- Evita dependencias difíciles de instalar.

---

## 3) Entregables del estudiante
Tu repositorio debe incluir, como mínimo, los siguientes archivos:

- `README.md`
- `docs/propuesta.md`
- `docs/caso_de_uso.md`
- `docs/estructura_repositorio.md`
- `docs/plan_de_pruebas.md`

Opcional (si ya tienes un avance inicial):
- `src/`
- `scripts/`
- `tests/`

### Contenido esperado por archivo

#### `README.md`
Incluye:
1. Nombre del proyecto.
2. Tema elegido y problema que resuelve.
3. Lenguaje principal (ARM64 Assembly, C, Python o Bash).
4. Alcance breve (qué sí hará y qué no hará).
5. Instrucciones mínimas para ejecutar (si hay código).

#### `docs/propuesta.md`
Incluye:
1. Objetivo general del proyecto.
2. Objetivos específicos (3 a 5).
3. Justificación técnica y académica.
4. Alcance delimitado (entregable pequeño).
5. Lista de funcionalidades prioritarias (MVP).

#### `docs/caso_de_uso.md`
Incluye:
1. Perfil de usuario (quién lo usaría).
2. Escenario principal de uso.
3. Entradas esperadas.
4. Proceso general.
5. Salidas esperadas.
6. Ejemplo narrado de uso paso a paso.

#### `docs/estructura_repositorio.md`
Incluye:
1. Árbol del repositorio.
2. Propósito de cada carpeta/archivo.
3. Convenciones de nombres.
4. Flujo de trabajo propuesto (cómo crecería el proyecto sin perder orden).

#### `docs/plan_de_pruebas.md`
Incluye:
1. Estrategia de pruebas manuales mínimas.
2. Casos de prueba funcionales (tabla).
3. Casos límite (errores, entradas vacías, parámetros inválidos).
4. Criterios de aceptación.

Formato sugerido para tabla de pruebas:

| ID | Escenario | Entrada | Resultado esperado | Estado |
|----|-----------|---------|--------------------|--------|
| CP-01 | Ejecución básica | `...` | `...` | Pendiente |
| CP-02 | Entrada inválida | `...` | Mensaje de error claro | Pendiente |

---

## 4) Estructura recomendada del repositorio
Usa esta estructura mínima como base:

```text
nombre-del-proyecto/
├── README.md
├── docs/
│   ├── propuesta.md
│   ├── caso_de_uso.md
│   ├── estructura_repositorio.md
│   └── plan_de_pruebas.md
├── src/
│   └── main.<ext>
├── scripts/
│   └── run.sh
└── tests/
    └── test_plan.md
```

> `main.<ext>` depende del lenguaje elegido (`.s`, `.c`, `.py`, `.sh`).

---

## 5) Criterios de evaluación sugeridos
Puntaje total sugerido: **100 puntos**

1. **Claridad de la propuesta (25 pts)**
   - Objetivo bien definido.
   - Problema y solución redactados con precisión.

2. **Delimitación del alcance (20 pts)**
   - Proyecto pequeño y realista.
   - Funcionalidades priorizadas correctamente.

3. **Calidad de documentación (30 pts)**
   - Estructura completa.
   - Redacción técnica clara.
   - Coherencia entre archivos.

4. **Diseño de estructura del repositorio (15 pts)**
   - Organización lógica.
   - Nombres claros y consistentes.

5. **Plan de pruebas (10 pts)**
   - Casos de prueba relevantes y verificables.

---

## 6) Recomendaciones prácticas para el estudiante
- Empieza por redactar el caso de uso antes de codificar.
- Si tienes duda entre dos ideas, elige la más pequeña.
- Prioriza una sola funcionalidad central bien explicada.
- Si usas IA de apoyo, úsala para iterar borradores, no para inflar alcance.
- Evita “feature creep”: documenta primero, implementa después.

---

## 7) Entrega en GitHub Classroom
- Sube tu repositorio con la estructura solicitada.
- Asegúrate de que los archivos de `docs/` sean legibles en Markdown.
- Verifica que tu propuesta se pueda entender sin explicación oral adicional.

**Resultado esperado:** una propuesta técnica breve, coherente y lista para convertirse en una práctica implementable.
