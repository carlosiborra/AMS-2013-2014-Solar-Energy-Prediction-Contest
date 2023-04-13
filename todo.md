# TODO

## Lo que se nos pide

1) (0.5 puntos) <del>Preparar un repositorio privado en GitHub para poder hacer los commits semanales de lo realizado en la práctica cada semana. Haciendo al menos un commit cada semana se obtienen 0.5 puntos. Se recomienda que el nombre del repositorio sea vuestro número de grupo de prácticas seguido con el literal “Practica1”. Por ejemplo, si sois el grupo 13 de prácticas, el repositorio se llamará “Grupo13-Practica1”. Enviar el enlace del repositorio al profesor de prácticas por e-mail.</del>
2) <del>Leer los conjuntos de datos. Cada grupo usará una planta solar distinta (punto rojo), sustituyendo xx por el número de grupo</del>
3) (0.25 puntos) <del>Hacer un Análisis Exploratorio de Datos (EDA).</del>
4) <del>Dividir los datos en «train» (los 10 primeros años) y «test» (los 2 últimos). Siguiendo la metodología planteada en la competición, no desordenaremos los datos antes de partir en entrenamiento y test, sino que respetaremos el orden temporal. <mark>Importante: los datos de «test» se reservan para la evaluación final en el apartado 8 de la práctica, no se puede utilizar para tomar decisiones durante el resto de puntos de la práctica (es decir, desde los apartados 4 a 7, habrá que evaluar los distintos métodos sin usar dicho conjunto de test).</mark></del>
5) (1.00 puntos) <del>Métodos básicos: aquí se considerarán los siguientes métodos básicos: KNN, árboles de regresión, regresión lineal. Las métricas de evaluación son RMSE y MAE. Aparte de evaluar las métricas, también se medirá el tiempo que tarda su entrenamiento.</del>
   1) 🚨 Se evaluarán dichos modelos con sus hiperparámetros por omisión.
   2) 🚨 Después, se ajustarán los hiperparámetros más importantes de cada método y se obtendrá su evaluación.
   3) 🚨 Obtener algunas conclusiones, tales como: ¿cuál es el mejor método? ¿Cuál de los métodos básicos de aprendizaje automático es más rápido? ¿Los resultados son mejores que los regresores triviales/naive/baseline? ¿El ajuste de hiperparámetros mejora con respecto a los valores por omisión? ¿Hay algún equilibrio entre tiempo de ejecución y mejora de resultados? Etc.
6) (0.75 puntos) 🚨 ¿Es posible reducir la dimensionalidad del problema? (aquí no tiene por qué utilizarse una técnica estándar, sino algo que se os ocurra para que en los datos haya menos atributos sin empeorar resultados).
7) (0.75 puntos) Métodos avanzados: SVMs, Random Forests.
   1) 🚨 Se evaluarán dichos modelos con sus hiperparámetros por omisión.
   2) 🚨 Después, se ajustarán los hiperparámetros más importantes de cada método y se obtendrá su evaluación.
   3) 🚨 Interpretar la importancia de los atributos según aquellas técnicas que lo permitan.
   4) 🚨 Conclusiones hasta el momento.
8) (0.25 puntos) 🚨 Seleccionar el mejor método, evaluarlo, construir modelo final, hacer predicciones para la competición.
   1) Seleccionar el mejor método de los evaluados en los puntos anteriores.
   2) Usar la partición de test para evaluar ese mejor método. Esta es una estimación de cómo se desempeñaría el modelo en la competición.
   3) Entrenar el modelo final. Guardarlo en un fichero (llamado «modelo_final.pkl»).
   4) Utilizar el modelo final para obtener predicciones para el conjunto de datos de la competición (comp). Guardar estas predicciones en un fichero (llamado «predicciones.csv»)

## Por hacer / completar

- Repasar todos los modelos
- Argumentar el porq se ha usado nMAE como criterion
- Explicar porq se usara el criterion para seleccionar el mejor modelo (al hacerse con validacion)
- Explicar lo de sobreajuste y como se sabe
- Explicacion de que modelo se escoge
- Entrenar previamente el modelo seleccionado con todos los datos antes de pasarlo a formarto pkl
- Explicar porq se usa un scatterplot
- Cambiar tamaño texto de los histogramas con los resultados

## A preguntar

<!-- - Escalado y eliminar param. tanto en por defecto como no -->
<!-- - Seleccion de param, cuando y porq no antes de los sencillos -->
<!-- - Hacer test a parte de train para comparar valores -->
<!-- - Porq con ajuste de hp escalado y tal funciona tan lento -->
- Porq SVM's por omision es una linea recta -> HAY QUE ESCALAR
- Hacer conclusiones y todo eso en español -> REPASAR EL HECHO DE QUE SEA UNA LINEA RECTA
<!-- - Si no se puede comprobar los resultados de test, ¿cómo se puede comprobar que se ha hecho bien?, que decisiones puedo tomar en los apartados 4-7, si no poseo esa información -->
- Que hago para dividir los datos y eliminar variables
- El escalado robusto está bien?
- ¿Qué más podríamos probar/hacer de los modelos?
- ¿Resultados OK?
- GRadient Boosting lo añadimos o no?
- No entiendo porq en SVR si lo cambio de 10 a 15 de budget tarda demasiado
- Se puede utilizar test en el apartado 8 para comparar todos?
- En randForest puedo poner solo log2 ya que es el que mejor funciona?
- Porq NMAE y MAE son distintos, bastatne, y al mae de train detecta el sobreeajuste
- Lo mismo se debe subir el numero de budget para que sea igual en todos y el tiempo sea comparable, o dividir el tiempo entre el número de folds
- El modelo final, tras la seleccion de parametros, hay que seleccionar los atributos?