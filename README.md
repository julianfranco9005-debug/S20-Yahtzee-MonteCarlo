# Simulación de Monte Carlo aplicada al juego Yahtzee

**S20 – Evidencia de Aprendizaje 1**

| Información | Datos |
|---|---|
| Estudiante | Julian Camilo Franco |
| Programa | Ingeniería de Software y Datos |
| Asignatura | Simulación |
| Docente | Julian Andrés Loaiza |
| Institución | Institución Universitaria Digital de Antioquia |
| Año | 2026 |

---
## 📄 Entregables de la actividad

### 1. Documento técnico – S20

Informe técnico completo de la Evidencia de Aprendizaje 1, que contiene la metodología, implementación, resultados experimentales, análisis y conclusiones del proyecto.

https://docs.google.com/document/d/1fpFtgnnbcCLFlzBRkKFoCCNblL4o2eeFppCCLy19_Ac/edit?usp=sharing


### 2. Video de sustentación

Video explicativo del desarrollo del proyecto, las cuatro fases de la actividad y los resultados obtenidos mediante simulación de Monte Carlo.



---

## 1. Descripción del proyecto

Este proyecto tiene como propósito aplicar el método de Monte Carlo al juego Yahtzee mediante el lenguaje de programación Python.

A partir de un código base, se desarrolla una simulación que permite analizar el comportamiento de cinco dados de seis caras, evaluar alternativas de lanzamiento y conservación, estimar valores esperados y estudiar cómo cambia la probabilidad de obtener un Yahtzee cuando se modifica la distribución de probabilidad de uno de los dados.

El trabajo se desarrolla en Google Colab y se organiza en cuatro fases: USA, MODIFICA, CREA y DEBATE.

## 2. Objetivo general

Aplicar el método de simulación de Monte Carlo al juego Yahtzee para analizar resultados aleatorios, estudiar la convergencia de las estimaciones y evaluar decisiones bajo diferentes condiciones de probabilidad.

## 3. Fases del proyecto

### Fase USA – Análisis del código base

Se estudia y ejecuta el código inicial del juego Yahtzee para comprender su funcionamiento, las reglas de puntuación, la generación de números aleatorios y las decisiones relacionadas con conservar o relanzar dados.

También se analiza el comportamiento de las simulaciones y la variación de los resultados al incrementar el número de iteraciones.

### Fase MODIFICA – Implementación de un dado cargado

Se modifica la distribución de probabilidad de uno de los dados para asignar un 30 % de probabilidad a la cara seis y un 14 % a cada una de las otras cinco caras.

Se realizan 100.000 simulaciones por escenario para comparar la probabilidad de obtener Yahtzee con un dado equilibrado y con uno cargado.

**Resultados obtenidos:**

| Momento de evaluación | Dado equilibrado | Dado cargado |
|---|---:|---:|
| Hasta la tirada 1 | 0,0740 % | 0,2460 % |
| Hasta la tirada 2 | 1,2510 % | 3,2450 % |
| Hasta la tirada 3 | 4,6170 % | 10,0530 % |

Los resultados muestran que aumentar la probabilidad de obtener seis modifica la frecuencia observada de Yahtzee en el experimento.

### Fase CREA – Toma de decisiones

Se evalúan dos alternativas mediante simulación de Monte Carlo, partiendo de los dados `[3, 3, 3, 2, 6]`:

- Conservar los tres dados iguales y relanzar los otros dos.
- Conservar los cinco dados y puntuar.

Se utilizaron 100.000 simulaciones para estimar el valor esperado de cada alternativa.

**Resultados obtenidos:**

- Valor esperado conservando tres dados: 17,2402.
- Valor esperado conservando los cinco dados: 17,0000.

En este escenario, la alternativa de conservar los tres dados iguales presentó un valor esperado superior.

### Fase DEBATE – Monte Carlo y análisis combinatorio

Se analiza si el método de Monte Carlo puede reemplazar el análisis combinatorio.

La conclusión del ejercicio es que ambos métodos se complementan. El análisis combinatorio permite obtener probabilidades exactas cuando es posible calcular todos los casos, mientras que Monte Carlo permite estimar resultados mediante experimentos aleatorios repetidos.

## 4. Convergencia y Ley de los Grandes Números

Se realiza un experimento para observar cómo cambia el valor esperado estimado al incrementar el número de iteraciones.

**Resultados de convergencia:**

| Iteraciones | Valor esperado estimado |
|---:|---:|
| 10 | 14,2000 |
| 100 | 17,6100 |
| 500 | 17,5120 |
| 1.000 | 17,1070 |
| 5.000 | 17,2562 |
| 10.000 | 17,1677 |
| 50.000 | 17,2210 |
| 100.000 | 17,2415 |

Los resultados permiten observar que las estimaciones presentan variaciones cuando se utilizan pocas iteraciones y tienden a estabilizarse al aumentar la cantidad de simulaciones. Este comportamiento se relaciona con la Ley de los Grandes Números.

## 5. Tecnologías y herramientas utilizadas

- **Python:** lenguaje de programación utilizado para desarrollar las simulaciones.
- **Google Colab:** entorno de ejecución del notebook.
- **NumPy:** operaciones y procesamiento numérico.
- **Pandas:** organización de resultados en estructuras de datos.
- **Matplotlib y Seaborn:** generación de gráficas y visualización de resultados.
- **Graphviz:** elaboración del diagrama de flujo.

## 6. Estructura del repositorio

El repositorio contiene los siguientes elementos:

- `S20Yahtzee_Julian_Francob.ipynb`: notebook con el código fuente, las simulaciones, los experimentos y los resultados.
- `README.md`: documentación general del proyecto.

En la entrega final se incorporará el informe técnico en PDF y las evidencias gráficas correspondientes.

## 7. Ejecución del proyecto

Para revisar el proyecto:

1. Abrir el archivo `.ipynb` desde el repositorio.
2. Seleccionar la opción para abrirlo en Google Colab.
3. Ejecutar las celdas en orden.
4. Revisar las salidas, tablas y gráficas generadas.

Los resultados numéricos documentados en este README corresponden a las ejecuciones guardadas en el notebook. Las nuevas ejecuciones pueden presentar pequeñas variaciones debido al componente aleatorio de la simulación.

## 8. Autor

**Julian Camilo Franco**

Estudiante de Ingeniería de Software y Datos.

Institución Universitaria Digital de Antioquia – 2026.
