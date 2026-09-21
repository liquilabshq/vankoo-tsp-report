# Guía de uso de la carpeta `assets`

Todas las imágenes, capturas y diagramas del informe se almacenan aquí. **No se suben
imágenes a la raíz del repositorio** ni se pegan enlaces externos (Google Drive, Imgur,
etc.): el informe debe exportarse a PDF sin depender de internet.

## Convención de nombres

```
<seccion>-<descripcion-corta>-<vN>.<ext>
```

- Todo en **minúsculas**, separado por guiones (`-`), **sin espacios ni tildes**.
- `vN` solo si se reemplaza una versión anterior del mismo artefacto (`v2`, `v3`, ...).
- Formatos: `.png` para capturas y diagramas, `.jpg`/`.jpeg` para fotos de perfil,
  `.svg` para diagramas vectoriales exportados.
- Ancho recomendado: **1600 px máximo** (el PDF es A4 con márgenes de 25 mm).

Ejemplos:

```
assets/cap2-requirements-elicitation/user-personas/user-persona-mype.png
assets/cap4-product-design/web-app/wireframes/wireframe-web-dashboard.png
assets/profiles/perfil-apellido-nombre.jpeg
```

## Diagramas: `src/` y `out/`

Las carpetas de diagramas generados (arquitectura C4, diagramas de clases, base de datos)
se dividen en dos:

- `src/` — el archivo fuente editable: `.puml` (PlantUML), `.dsl` (Structurizr), `.sql`.
- `out/` — el `.png` exportado, que es el que se referencia desde el `README.md`.

Ambos se versionan. Si alguien necesita corregir un diagrama, edita el fuente y vuelve a
exportar; no se reemplaza solo la imagen.

## Cómo referenciar una imagen desde el README

Siempre con **ruta relativa** iniciando en `./assets/`:

```markdown
![User Persona - Dueño de MYPE](./assets/cap2-requirements-elicitation/user-personas/user-persona-mype.png)
```

## Mapa de carpetas → sección del informe

| Carpeta | Sección del informe |
|---|---|
| `logos/` | Carátula (logo UPC, logo de LiquiLabs y de Vankoo) |
| `profiles/` | 1.1.2. Perfiles de integrantes del equipo |
| `cap1-introduccion/lean-ux-canvas/` | 1.2.2.4. Lean UX Canvas |
| `cap1-introduccion/segmentos-objetivo/` | 1.3. Segmentos objetivo (gráficos e información estadística) |
| `cap2-requirements-elicitation/competidores/` | 2.1. Competidores (logos y Competitive Analysis Landscape) |
| `cap2-requirements-elicitation/entrevistas/` | 2.2.2. Registro de entrevistas (screenshots del video) |
| `cap2-requirements-elicitation/user-personas/` | 2.3.1. User Personas (UXPressia) |
| `cap2-requirements-elicitation/user-task-matrix/` | 2.3.2. User Task Matrix |
| `cap2-requirements-elicitation/user-journey-mapping/` | 2.3.3. User Journey Mapping (UXPressia) |
| `cap2-requirements-elicitation/empathy-mapping/` | 2.3.4. Empathy Mapping (UXPressia) |
| `cap2-requirements-elicitation/as-is-scenario-mapping/` | 2.3.5. As-is Scenario Mapping (LucidChart / Miro) |
| `cap3-requirements-specification/to-be-scenario-mapping/` | 3.1. To-Be Scenario Mapping |
| `cap3-requirements-specification/impact-mapping/` | 3.3. Impact Mapping (UXPressia) |
| `cap3-requirements-specification/product-backlog/` | 3.4. Product Backlog (captura de la herramienta) |
| `cap4-product-design/style-guidelines/` | 4.1. Style Guidelines |
| `cap4-product-design/information-architecture/` | 4.2. Information Architecture |
| `cap4-product-design/landing-page/wireframes/` | 4.3.1. Landing Page Wireframe |
| `cap4-product-design/landing-page/mockups/` | 4.3.2. Landing Page Mock-up |
| `cap4-product-design/web-app/wireframes/` | 4.4.1. Web Applications Wireframes |
| `cap4-product-design/web-app/wireflow-diagrams/` | 4.4.2. Web Applications Wireflow Diagrams |
| `cap4-product-design/web-app/mockups/` | 4.4.3. Web Applications Mock-ups |
| `cap4-product-design/web-app/user-flow-diagrams/` | 4.4.4. Web Applications User Flow Diagrams |
| `cap4-product-design/web-app/prototyping/` | 4.5. Web Applications Prototyping (screenshot del video) |
| `cap4-product-design/software-architecture/context-diagram/` | 4.6.1. Software Architecture Context Diagram |
| `cap4-product-design/software-architecture/container-diagrams/` | 4.6.2. Software Architecture Container Diagrams |
| `cap4-product-design/software-architecture/components-diagrams/` | 4.6.3. Software Architecture Components Diagrams |
| `cap4-product-design/class-diagrams/` | 4.7.1. Class Diagrams |
| `cap4-product-design/database-design/` | 4.8.1. Database Diagram |
| `cap5-product-implementation/configuration-management/` | 5.1. Software Configuration Management |
| `cap5-product-implementation/sprint-1/sprint-backlog/` | 5.2.1.2. Sprint Backlog 1 (captura del board) |
| `cap5-product-implementation/sprint-1/development-evidence/` | 5.2.1.3. Development Evidence for Sprint Review |
| `cap5-product-implementation/sprint-1/testing-evidence/` | 5.2.1.4. Testing Suite Evidence for Sprint Review |
| `cap5-product-implementation/sprint-1/execution-evidence/` | 5.2.1.5. Execution Evidence for Sprint Review |
| `cap5-product-implementation/sprint-1/services-documentation/` | 5.2.1.6. Services Documentation Evidence for Sprint Review |
| `cap5-product-implementation/sprint-1/deployment-evidence/` | 5.2.1.7. Software Deployment Evidence for Sprint Review |
| `cap5-product-implementation/sprint-1/collaboration-insights/` | 5.2.1.8. Team Collaboration Insights during Sprint |
| `cap5-product-implementation/sprint-1/actas-reunion/` | 5.2.1.9. Actas de reunión |
| `anexos/` | Anexos |

Los sprints siguientes se agregan como `cap5-product-implementation/sprint-2/`,
`sprint-3/`, etc., replicando las mismas subcarpetas.

## Reglas de trabajo

1. Cada integrante trabaja en su rama y sube **solo** los assets de las secciones que le
   corresponden.
2. No borrar los archivos `.gitkeep`; mantienen las carpetas vacías versionadas.
3. No subir archivos `.mp4`, `.psd`, `.fig` ni ZIP al repositorio (van a Blackboard y al
   aula virtual). En el informe se enlaza el video de Microsoft Stream.
4. Antes de exportar a PDF, verificar que **todas** las imágenes se rendericen en la vista
   previa de Markdown.
