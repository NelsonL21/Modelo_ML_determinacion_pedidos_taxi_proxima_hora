# Modelo_ML_determinacion_pedidos_taxi_proxima_hora
La compañía Sweet Lift Taxi ha recopilado datos históricos sobre pedidos de taxis en los aeropuertos. Para atraer a más conductores durante las horas pico, necesitamos predecir la cantidad de pedidos de taxis para la próxima hora. Construye un modelo para dicha predicción.

La métrica RECM en el conjunto de prueba no debe ser superior a 48.

## Conclusión general 

Se evidencia que los datos pudieron ser ordenados con éxito, se puedo pasar al tipo datetime[64] haciendo más sencilla la tarea del análisis de la serie temporal.

Se observa un dataframe ocmpleto son valores nulos.

Se evidencia una desviación estandar de 9 ordenes de viaje, con una data de más de 26.000 entradas, vemos que lo más común es tener un aproximado de entre 8 y 19  ordenes de taxi cada 10 min.

Observamos que hay moemntos donde no se tiene pedidos, y otros donde le máximo fue de 119 ordenes en 10min.

La media de viajes cada 10min en una jornada es de 14.

Se observa un claro aumento en la pendiente de la recta que describe el número de ordenes en el tiempo a partir del més de junio, (Figura 1)  lo cual puede indicar que al llegar la época de verano aumenta el empleo de taxis como medio de transporte, siendo esta una muy buena oportunidad para potenciación de las ventas para la empresa.

![Imagen](https://github.com/NelsonL21/Modelo_ML_determinacion_pedidos_taxi_proxima_hora/blob/main/Serie%20temporal.png)

**Figura 1:** gráficas del comportamiento de la serie temporal en el tiempo, desglozada en tendencia, estaconalidad y residuales.

Se evidencia que es una serie de tiempo estocástica no estacionaria, ya que el valor medio cambia con el tiempo.

Así mismo, se evidencia presencia de picos en agosto, en los días 13, 20 y 27, claramente diferencaidos del resto, se recomienda estudiar que sucedió dichos días, para detemrinar futuras oportunidades de negocio, y potencias capañas de marketing dichos días.

Se evidencia una clara y marcada tendencia a la alza a lo largo de todo el periodo de estudio, indicando que todo va en excelente camino.

Se implementaron 3 modelos, Regresión lineal, arbol de desición aleatorio y Potenciación de gradiente.

Como era de esperarse, el modelo que mejor dió resultado fué la regresión lineal con un RMSE = 31.03% superando en 17.23% las expectativas del cliente, el cual requeria de un medelo de máximo RMSE = 48% tal como se evidencia en la siguiente tabla (Tabla 1):

![Imagen2](https://github.com/NelsonL21/Modelo_ML_determinacion_pedidos_taxi_proxima_hora/blob/main/Tabla%20RMSE%20obtenidos%20por%20diferente%20modelos.png)

**Tabla 1:** Resultado de modelos de machine learning.

