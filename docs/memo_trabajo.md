# Tarea 4. Modelos de aprendizaje supervisado y no supervisado
## **Introducción a Ciencia de Datos para Economía** - Equipo 2

### ¿Cuál es el modelo supervisado que se recomienda?

### ¿Cuál es el principal hallazgo geográfico y cómo complementa al supervisado
Los reportes al C5 se concentran en el centro de la CDMX y a lo principalmente en avenidas y vialidades centrales, las cuales se cruzan en dicha zona centro. Conforme nos alejamos hacia la periferia, hay menos reportes dentro de la base de datos, y DBSCAN los cataloga como ruido, es decir, reportes que no forman parte de ninguna zona de interés. Con la configuración elegida (eps=0.25 km y min_samples=100), se forman 198 zonas que agrupan al 51.9% de los reportes (64,486). El otro 48.1% queda fuera.
Las zonas de interés o clusters más grandes se encuentran sobre todo en las alcaldías Cuauhtémoc y Venustiano Carranza, que son más céntricas y en las que se encuentran vialidades principales que cruzan entre sí, como son los ejes viales. El cluster más grande tiene 4,674 reportes al C5 de la CDMX, y su centro se encuentra en la Colonia Roma Norte, cerca de vialidades como Insurgentes, Reforma, Cuauhtémoc y el Circuito Interior. La proporción de reportes que potencialmente se pueden catalogar como ruido cambia también según la alcaldía; con valores de 12.9% en Cuauhtémoc y 20.8% en Venustiano Carranza, a 100% en Cuajimalpa y Milpa Alta, lo que nos da una disparidad en la forma que se catalogan y centralizan los reportes en estas alcaldías.

### Limitaciones

En la parte no supervisada, destacamos que el que haya más reportes en la Zona Centro no significa que ahí haya más falsas alarmas. Los reportes catalogados como 'F' solo el 20.2% de los reportes cae dentro de los clusters y 20.4% cae fuera. En este sentido, DBSCAN y el aprendizaje no supervisado solo nos dice dónde se acumulan los reportes, no dónde es más probable que una alerta sea falsa. Además, eps y min_samples los elige el analista, y no existe una etiqueta con la que contrastar si la elección está bien hecha. 

### Recomendaciones para el futuro

Algunas recomendaciones que nosotros tendríamos antes de una implementación operativa son:
1. Definir bien qué constituye una "falsa alarma", documentando cómo se asigna la etiqueta F, quién la asigna y con qué criterio; esto para evitar que el modelo infiera patrones que solamente están relacionados con la subjetividad humana.
2. Realizar una evaluación por alcaldía y por nivel de densidad. Un promedio entre todas las alcaldías sin considerar su tamaño y su densidad poblacional puede esconder un mal desempeño en zonas con pocos datos, como Cuajimalpa o Milpa Alta, y sobrestimar zonas densamente pobladas como Cuauhtémoc o Iztapalapa.