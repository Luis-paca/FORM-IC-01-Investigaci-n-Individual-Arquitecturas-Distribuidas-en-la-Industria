# FORM-IC-01 — Investigación Individual: Arquitecturas Distribuidas en la Industria

## Datos generales de la actividad

- **Actividad:** FORM-IC-01 — Investigación Individual: Arquitecturas Distribuidas en la Industria
- **Universidad:** Universidad Técnica Estatal de Quevedo (UTEQ)
- **Facultad:** Facultad de Ciencias de la Computación
- **Carrera:** Software (Ingeniería de Software)
- **Asignatura:** Aplicaciones Distribuidas (`ISR-701`)
- **Periodo académico:** Segundo Periodo Académico Ordinario (SPA) 2026–2027
- **Docente:** Gleiston Cicerón Guerrero Ulloa, PhD
- **Nivel / Paralelo:** Séptimo nivel / A
- **Semana / Modalidad:** Semana 5 / Individual
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
- **Pendiente para completar la entrega:**
  - Lectura, subrayado personal y capturas reales de evidencias en `docs/img/`.
  - Redacción definitiva de autoría propia en `docs/main.tex`, incluida la declaración final de uso de IA.
  - Compilación y verificación de `docs/main.pdf` y `docs/entrega_SGA.pdf` (una sola página con la URL completa en una sola línea).
  - Gestión manual de commits progresivos y `push` en Git.

> **Importante:** Los documentos LaTeX (`docs/main.tex` y `docs/entrega_SGA.tex`) aún están en preparación y todavía **no han sido compilados**.

---

## Instrucciones de compilación (Criterio P2)

- **Compilador LaTeX:** `pdflatex` (TeX Live o MiKTeX).
- **Procesador bibliográfico:** `biber` (backend de `biblatex` con estilo `ieee`).
- **Archivo principal del informe:** `docs/main.tex` (bibliografía en `docs/referencias.bib`).
- **Archivo de hoja de entrega para el SGA (1 página):** `docs/entrega_SGA.tex`.
- **Dependencias (paquetes LaTeX requeridos):** `inputenc`, `fontenc`, `babel` (soporte `spanish`), `csquotes`, `geometry`, `graphicx`, `booktabs`, `hyperref`, `biblatex` y `biblatex-ieee`.

### Orden de comandos desde la carpeta `docs/`

Para compilar el informe principal (`main.pdf`):

```bash
pdflatex main.tex
biber main
pdflatex main.tex
pdflatex main.tex
```

Para compilar la hoja de entrega de una sola página para el SGA (`entrega_SGA.pdf`):

```bash
pdflatex entrega_SGA.tex
```

