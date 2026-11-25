# FORM-IC-01 — Investigación Individual: Arquitecturas Distribuidas en la Industria

## Datos generales de la actividad

- **Actividad:** FORM-IC-01 — Investigación Individual: Arquitecturas Distribuidas en la Industria *(preparatoria para el informe académico individual TA-IND-02 de la semana 6)*
- **Universidad:** Universidad Técnica Estatal de Quevedo (UTEQ)
- **Carrera:** Ingeniería de Software
- **Asignatura:** Aplicaciones Distribuidas
- **Semana:** 5
- **Modalidad:** Individual
- **Estudiante:** Luis Alberto Paca Pilataza
- **Empresa seleccionada:** Datalex
- **Patrón arquitectónico:** API Gateway

---

## Descripción breve del caso y objetivo de la investigación

El caso de estudio analiza la **migración de las API REST de Datalex hacia Amazon API Gateway**, publicada oficialmente por Amazon Web Services en colaboración con ingenieros de Datalex. El objetivo de la investigación es examinar cómo Datalex ejecutó la transición desde su proveedor anterior de API hacia Amazon API Gateway **sin interrupciones del servicio en aproximadamente dos semanas** —mediante importación de claves API, un autorizador personalizado en AWS Lambda, corte DNS por CNAME y posterior optimización con AWS CloudFormation y cabecera nativa `x-api-key`— logrando reducir en **casi un 98 % el costo de operar su solución de API REST** en comparación con el acuerdo contractual del proveedor previo.

Adicionalmente, se fundamenta el patrón **API Gateway** con literatura académica arbitrada reciente verificada por DOI y se plantea un análisis preliminar sobre su aplicabilidad en el proyecto formativo **PFC NEXORA**.

---

## Estructura actual del repositorio

```text
FORM-IC-01-Investigaci-n-Individual-Arquitecturas-Distribuidas-en-la-Industria/
├── docs/
│   ├── main.tex
│   ├── referencias.bib
│   ├── entrega_SGA.tex
│   └── img/
│       └── .gitkeep
├── .gitignore
└── README.md
```

---

## Estado actual de la actividad

- **Fase 1 (completada):**
  - Verificación del repositorio local y remoto.
  - Creación de la estructura inicial de carpetas y archivos (`docs/`, `.gitignore`, `README.md`).
  - Esqueletos iniciales de `docs/main.tex` y `docs/entrega_SGA.tex` configurados con `biblatex` (estilo IEEE, backend Biber).
  - Análisis técnico verificado de la fuente oficial de AWS sobre el caso Datalex.
  - Búsqueda y verificación directa de DOI en páginas oficiales de editoriales para dos referencias académicas recientes, incorporadas junto a la fuente empresarial en `docs/referencias.bib`.
- **Pendiente para fases posteriores:**
  - Lectura, subrayado personal y captura real de evidencias en `docs/img/`.
  - Completar campos institucionales pendientes (facultad, docente, curso/paralelo, fecha de entrega).
  - Redacción definitiva de autoría propia en `docs/main.tex` y `docs/entrega_SGA.tex`, incluida la declaración final de uso de IA.
  - Compilación de los documentos PDF finales y gestión manual de commits/push en Git.

> **Importante:** Los documentos LaTeX (`docs/main.tex` y `docs/entrega_SGA.tex`) se encuentran todavía en preparación estructural y **no han sido compilados** durante esta primera fase.

---

## Instrucciones previstas de compilación (para la fase definitiva)

Cuando el contenido académico esté redactado y revisado, los documentos se compilarán desde la carpeta `docs/` ejecutando:

```bash
pdflatex main.tex
biber main
pdflatex main.tex
pdflatex main.tex
```

