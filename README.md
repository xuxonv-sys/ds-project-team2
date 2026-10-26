# Tarea 3 - Exploración de la base de incidentes viales de la CDMX
**Introducción a la Ciencia de Datos para Economía**
*A01595260 - Miguel Ángel López Ramírez*
*A01377310 - Jesús Iván Negrete Vázquez*

## Objetivo del proyecto
**Objetivo General:** Explorar y entender la base de incidentes viales reportados al C5 de la CDMX, que lleva el nombre *db_falsas_alarmas*, disponible en [Incidentes viales reportados por C5](https://datos.cdmx.gob.mx/dataset/incidentes-viales-c5).

**Objetivos particulares**
1. Entender la base: qué registra y qué significa cada fila.
2. Revisar su calidad: tipos de datos, variables faltantes, registros duplicados.
3. Perfilar las variables que se encuentran en la base.
4. Formular preguntas sobre la información y responderlas con gráficas.

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
Dentro del proyecto, se trabajan 2 notebooks con diferentes análisis.
- El notebook 01, de nombre `nb01_estructura_perfilado.ipynb` establece el contexto, explica qué información se encuentra dentro de la base, evalua su calidad y presenta los hallazgos iniciales. 
- El notebook 02, de nombre `nb02_preguntas_visualizaciones.ipynb` retoma los hallazgos  para formular preguntas, profundiza el análisis apoyándose de gráficas y presenta conclusiones.

El orden de ejecución de los notebooks es:
1. `nb01_estructura_perfilado.ipynb`
2. `nb02_preguntas_visualizaciones.ipynb`
