# Tarea 4 - Modelos de aprendizaje supervisado y no supervisado
**Introducción a la Ciencia de Datos para Economía**
*A01595260 - Miguel Ángel López Ramírez*
*A01377310 - Jesús Iván Negrete Vázquez*

## Objetivo del proyecto
**Objetivo General:** Aplicar modelos de aprendizaje supervisado y no supervisado sobre base de incidentes viales reportados al C5 de la CDMX, que lleva el nombre *db_falsas_alarmas*, disponible en [Incidentes viales reportados por C5](https://datos.cdmx.gob.mx/dataset/incidentes-viales-c5). Lo anterior con la finalidad de identificar patrones de predicción sobre Falsas Alarmas así como elementos de agrupación geográfica.

**Objetivos particulares**
1. Aplicar modelos supervisados para encontrar patrones que puedan predecir las falsas alarmas.
2. Utilizar métricas de evaluación para decidir sobre el modelo más apto para la predicción.
3. Encontrar a través de aprendizaje no supervisado agrupaciones geográficas.
4. Encontrar y transparentar limitaciones sobre la aplicación de los modelos.

### Funcionamiento de uv

Para agregar paquetes a uv
```
uv add paquete
```

Para agregar paquetes en grupos
```
uv add --group nombre_del_grupo paquete
```

Para actualizar grupos
```
uv sync --groups nombre_del_grupo
```

Para actualizar grupos
```
uv sync --groups nombre_del_grupo
```

Para actualizar todos los grupos
```
uv sync --all-groups
```

## Elementos colaborativos
Dentro del proyecto, se trabajan 4 notebooks con diferentes análisis, de los cuales 2 son los notebooks de interés.
- El notebook 03, de nombre `nb03_supervisado_c5.ipynb` establece la parte de aprendizaje supervisado y el desarrollo de modelos predictivos. 
- El notebook 04, de nombre `nb04_no_supervisado_c5.ipynb` aplica aprendizaje no supervisado para encontrar agrupaciones geográficas en la data.

El orden de ejecución de los notebooks es:
1. `nb03_supervisado_c5.ipynb`
2. `nb04_no_supervisado_c5.ipynb`