# Proyecto-Sprint-1-SegmentIQ-
Este proyecto representa la fase inicial (Sprint 1) de una iniciativa de análisis de datos para la empresa "Store 1". El objetivo principal fue realizar un diagnóstico y limpieza profunda de una muestra de datos de clientes para garantizar que la información sea íntegra, coherente y esté lista para modelos analíticos o de negocio posteriores
📝 Descripción Técnica
1. El Conjunto de Datos
La muestra consistió en registros de usuarios con las siguientes dimensiones:

Identificadores: user_id (tratado como cadena para preservar integridad).

Información Demográfica: Nombre del usuario (user_name) y edad (user_age).

Comportamiento de Consumo: Categorías favoritas (fav_categories) y una lista de gastos asociados (total_spendings).

2. Problemas Críticos Identificados
Antes de la intervención, los datos presentaban "ruido" que impediría un análisis preciso:

Inconsistencias de Formato: Nombres con espacios redundantes y guiones bajos en lugar de espacios.

Tipado Incorrecto: Edades almacenadas como números de punto flotante (float), lo cual es semánticamente incorrecto para esta variable.

Falta de Estructura: Nombres y apellidos agrupados en una sola cadena, dificultando el análisis granular.

3. Metodología de Limpieza y Transformación
El proceso se dividió en etapas lógicas de procesamiento de datos utilizando Python:

Normalización de Texto: Se implementaron métodos como .strip() y .replace() para limpiar los nombres, seguidos de .split() para estructurarlos en sublistas de [Nombre, Apellido].

Casting de Datos y Robustez: Se realizó la conversión de edades a enteros (int). Se añadió un bloque de manejo de excepciones (try-except) para gestionar errores de conversión en caso de datos no numéricos, asegurando que el script no se detenga ante valores inesperados.

Enriquecimiento y Agregación: Se calcularon métricas de valor por usuario, como el gasto total, sumando las listas de transacciones individuales.

Optimización de Flujo: Se desarrolló una solución escalable mediante bucles (for) para procesar múltiples registros de manera automatizada, permitiendo que el código sea reutilizable para volúmenes de datos mayores.

✅ Conclusiones y Resultados
El resultado final es una estructura de datos denominada users_clean, que presenta las siguientes mejoras:

Datos Atómicos: Nombres y apellidos separados y normalizados.

Integridad de Tipos: Edades consistentes y IDs ordenados ascendentemente para facilitar búsquedas.

Visibilidad Financiera: Resúmenes claros que vinculan al usuario con su capacidad de gasto total.
