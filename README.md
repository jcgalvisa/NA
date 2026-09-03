# Análisis Numérico

Cuadernos computacionales y material académico para el estudio riguroso del análisis numérico. El repositorio combina formulación matemática, análisis de error y experimentación reproducible en **Julia**, **Python**, **Jupyter/Colab** y **Pluto.jl**.

Autor y docente: [Juan Galvis](https://scholar.google.com/citations?user=lbfc2joAAAAJ&hl=en), Universidad Nacional de Colombia.

> Un resultado numérico no se considera completo sin discutir el error, el condicionamiento del problema, la estabilidad del algoritmo y el costo computacional.

## Portada interactiva

La [Introducción interactiva al Análisis Numérico](https://jcgalvisa.github.io/NA/) presenta los objetivos del curso, las familias de problemas, las fuentes de error y el papel del cómputo científico. La publicación se actualiza automáticamente desde `docs/` mediante GitHub Pages.

## Ruta de estudio

| Unidad | Pregunta central | Contenido computacional |
|---|---|---|
| [00 · Fundamentos](00_fundamentos/) | ¿Cómo se mide y compara la convergencia? | Notación asintótica, tasas y repaso matemático |
| [01 · Aritmética finita](01_aritmetica_punto_flotante/) | ¿Qué números puede representar una máquina? | IEEE 754, redondeo, épsilon de máquina y propagación del error |
| [02 · Ecuaciones no lineales](02_ecuaciones_no_lineales/) | ¿Cómo se aproxima una raíz con garantías? | Bisección, Newton, punto fijo, criterios de parada y convergencia |
| [03 · Sistemas lineales](03_sistemas_lineales/) | ¿Cuándo una solución calculada es confiable? | Normas, PLU, Cholesky, condicionamiento y residuo |
| [04 · Interpolación](04_interpolacion_aproximacion/) | ¿Cómo aproximar una función a partir de datos? | Interpolación polinomial, splines y ejemplos geométricos |
| [05 · Ajuste de parámetros](05_ajuste_parametros/) | ¿Cómo identificar modelos a partir de observaciones? | Mínimos cuadrados, optimización y modelos de crecimiento |
| [06 · Ecuaciones diferenciales](06_ecuaciones_diferenciales_ordinarias/) | ¿Cómo evoluciona el error al integrar una dinámica? | Solución numérica de problemas de valor inicial |
| [07 · Métodos avanzados](material_classroom/07_metodos_avanzados/) | ¿Cómo explorar distribuciones difíciles de muestrear? | Introducción a Metropolis-Hastings en Pluto |

## Lenguajes y formatos

- **Python:** NumPy, SciPy, Matplotlib e ipywidgets.
- **Julia:** `LinearAlgebra`, ecosistema científico y cuadernos Jupyter.
- **Pluto.jl:** documentos reactivos autocontenidos con entorno reproducible.
- **Google Colab:** ejecución en navegador de los archivos `.ipynb`.

## Criterios de rigor

Cada método debe evaluarse desde cinco perspectivas:

1. **Consistencia:** relación entre el problema exacto y su discretización.
2. **Convergencia:** comportamiento del error cuando mejora la resolución o aumentan las iteraciones.
3. **Estabilidad:** amplificación de errores de redondeo, perturbaciones y datos inexactos.
4. **Condicionamiento:** sensibilidad inherente del problema, independiente del algoritmo.
5. **Complejidad:** memoria, operaciones y escalabilidad necesarias para una tolerancia dada.

En los experimentos se recomienda reportar error absoluto y relativo, residuo, tolerancia, número de iteraciones, tiempo de ejecución y precisión utilizada.

## Ejecución

Los archivos `.ipynb` se abren con JupyterLab, VS Code o Google Colab. Ejecute las celdas en orden y revise primero los prerrequisitos del cuaderno.

Para usar Pluto.jl:

```julia
import Pkg
Pkg.add("Pluto")
using Pluto
Pluto.run()
```

## Material del Classroom

La carpeta [`material_classroom/`](material_classroom/) contiene únicamente variantes o recursos que complementan los cuadernos principales. El [catálogo del Classroom](material_classroom/README.md) enlaza las notas, evaluaciones, rúbricas, proyectos y grabaciones que permanecen en Google Drive para evitar duplicación y crecimiento innecesario.

## Organización

```text
NA/
├── 00_fundamentos/
├── 01_aritmetica_punto_flotante/
├── 02_ecuaciones_no_lineales/
├── 03_sistemas_lineales/
├── 04_interpolacion_aproximacion/
├── 05_ajuste_parametros/
├── 06_ecuaciones_diferenciales_ordinarias/
├── material_classroom/
├── archivo_versiones/
└── docs/
```

`archivo_versiones/` conserva copias históricas o checkpoints claramente identificados; no deben usarse como punto de partida para nuevos desarrollos.

## Reproducibilidad y contribuciones

- No sobrescriba resultados sin conservar los parámetros del experimento.
- Fije semillas aleatorias cuando la comparación dependa de simulaciones.
- Distinga siempre error hacia adelante, error hacia atrás y residuo.
- Documente las versiones de paquetes cuando un resultado dependa de ellas.
- Use nombres descriptivos en español, minúsculas y `snake_case`.
- Evite incluir salidas voluminosas, checkpoints o datos generados automáticamente.

## Licencia

El contenido se distribuye bajo la [GNU General Public License v3.0](LICENSE).
