# Guía de contribución

Las contribuciones deben preservar el carácter académico, reproducible y verificable del repositorio.

## Requisitos mínimos

1. Explique el problema matemático, los supuestos y el dominio de validez.
2. Identifique el método, su criterio de parada y su costo esperado.
3. Incluya al menos un caso con solución conocida o una referencia independiente.
4. Reporte residuo y error; no los trate como cantidades equivalentes.
5. Discuta estabilidad y condicionamiento cuando sean relevantes.
6. Fije la semilla de experimentos aleatorios.
7. Evite rutas absolutas y dependencias locales no documentadas.
8. Limpie datos sensibles, checkpoints y salidas innecesariamente voluminosas.

## Convención de nombres

- Carpetas y archivos en minúsculas y `snake_case`.
- Prefijo numérico para conservar el orden temático.
- Sufijo de lenguaje cuando existan implementaciones paralelas: `_python`, `_julia` o `_pluto`.
- Las variantes históricas deben indicar fecha, contenido y número de versión.

## Verificación sugerida

- Ejecute el cuaderno completo desde un entorno limpio.
- Compruebe que no quedan celdas con error.
- Compare el resultado con un caso límite o una solución de referencia.
- Registre tolerancia, precisión, iteraciones y versión de las bibliotecas.
- Revise que gráficas y tablas incluyan variables, unidades y leyendas.

