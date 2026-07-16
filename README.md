# Sistema de Recomendación de Productos en Transacciones Retail

Sistema de recomendación de productos construido sobre datos de transacciones
retail usando market basket analysis, identificando qué productos se compran
frecuentemente juntos y generando recomendaciones ordenadas por relevancia
para cualquier producto dado.

## Problema

Los retailers pierden oportunidades de aumentar el ticket de compra al no
sugerir productos relevantes en el momento oportuno. Este proyecto responde
una pregunta práctica: **dado un producto que compra un cliente, ¿qué otros
productos se le deberían recomendar?**

## Metodología

1. Limpieza de datos y preparación a nivel transacción
2. Análisis exploratorio del tamaño de canasta y frecuencia de productos
3. Market basket analysis con el algoritmo Apriori
4. Minería de reglas de asociación (soporte, confianza, lift)
5. Validación de estabilidad de reglas en múltiples muestras aleatorias
6. Función de recomendación: dado un producto, retorna los artículos más relacionados

## Hallazgos principales

- **Estructura de co-compra limitada:** las frecuencias de productos son casi
  uniformes en todo el catálogo (~36,000–37,000 ocurrencias cada uno), y las
  reglas de asociación más fuertes encontradas tuvieron un lift de solo ~1.16 —
  cercano al umbral que indica ausencia de relación real.
- **Patrones estables aunque débiles:** repetir el análisis sobre 5 muestras
  aleatorias independientes produjo en gran medida las mismas reglas, confirmando
  que las relaciones son consistentes y no producto del azar.
- **Metodología sólida y transferible:** la función de recomendación funciona
  correctamente. En un entorno con patrones reales de co-compra, este mismo
  pipeline generaría recomendaciones significativamente más fuertes y accionables.

## Herramientas

Python · pandas · mlxtend · scikit-learn · matplotlib · seaborn

## Notebook

[Ver notebook completo →](https://github.com/claudiogaytan28/product-recommendation-system/blob/main/03_product_recommendation_system.ipynb)
