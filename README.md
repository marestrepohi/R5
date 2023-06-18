# MLOPS R5

Contando con que los recursos son ilimitados escogería trabajar con Amazon SageMaker ya que es un servicio dedicado a automatizar y estandarizar procesos en todo el ciclo desarrollo y producción de Machine Learning, este servicio puede entrenar, probar, solucionar, desplegar y gestionar modelos de ML a escala de forma sencilla.

Antes de llevar a producción cualquier proyecto de ML debemos tener en cuenta los siguientes pasos. 

![](images/ml-lifecycle-phases.png)



*__Identificacion de problema de negocio:__* es la fase más importante de un proyecto de ML. En esta fase, debe definir claramente el problema que está tratando de resolver y el valor comercial que se espera lograr ademas se debe determinar si ML es el enfoque correcto para su problema y si tiene suficientes datos para entrenar un modelo preciso.

*__Enmarcado del problema:__*  En esta fase se define la metodología con la cual se va abordar el problema de negocio mediante técnicas de ML. También se determina qué observar y qué se debe predecir (variable objetivo). Además, se Identifican qué predecir y cómo optimizar el rendimiento con diferentes métricas de rendimiento.

*__Procesamiento y preparación de datos:__* En este paso, los científicos de datos/ingenieros de datos recopilan datos, los integran con diferentes fuentes y los limpian y transforman para que estén listos para su consumo. Los ingenieros/científicos de datos también pueden dividir los datos en tres conjuntos: entrenamiento, validación y prueba. Los conjuntos de entrenamiento se utilizan directamente para entrenar el modelo, los conjuntos de validación son ejemplos no vistos que se utilizan para evaluar el rendimiento del modelo, y los conjuntos de prueba son otro conjunto de registros no vistos que se utilizan para verificar el rendimiento del modelo en situaciones reales.

*__Entramiento y tuneo del modelo:__* En esta fase, seleccionas un algoritmo adecuado para el problema y luego se entrenas el modelo con datos de entrenamiento, se establece una métrica objetivo para el modelo, con el fin de  optimizar y configurar los hiperparámetros para obtener el mejor rendimiento del modelo y evitar problemas como el sobre ajuste.

*__Evaluación del modelo:__* Una vez que se haya completado el entrenamiento del modelo, es necesario evaluar su rendimiento y precisión. Es recomendable generar varios modelos utilizando diferentes métodos y luego evaluar la efectividad de cada uno. El modelo entrenado se evalúa utilizando una porción del conjunto de datos que se ha reservado como conjunto de validación. En función de los resultados de la evaluación, es posible realizar ajustes en los datos, el algoritmo o en ambos aspectos.

*__Implementación y monitoreo:__* Después de entrenar, ajustar y evaluar su modelo, puede implementarlo en producción y realizar predicciones e inferencias. En la implementación del modelo de ML se definen los activos de ML, como el modelo, sus parámetros e hiperparámetros, los scripts de entrenamiento y los datos de entrenamiento y prueba. Se presta especial atención a la identidad, los componentes, el control de versiones y las dependencias de estos artefactos de ML. El objetivo final es desplegar estos artefactos en forma de servicios o componentes de infraestructura.
En este paso se deben abarcar prácticas como la integración continua (CI) para agregar datos y modelos de prueba y validación, la entrega continua (CD) para automatizar la implementación de modelos en servicios de predicción, la capacitación continua (CT) que permite el reentrenamiento automático de los modelos y la monitorización continua (CM) para supervisar los datos de producción y las métricas de rendimiento del modelo.
Una vez implementado el modelo de ML, es crucial monitorear su rendimiento para asegurar su comportamiento esperado. Esto implica supervisar los cambios de dependencia, datos, y la estabilidad numérica del modelo. También se debe monitorear el rendimiento computacional del sistema de ML, los procesos de generación de características y la degradación de la calidad predictiva en los datos. 


__Posible sistema para poner en producción y monitorear los diferentes modelos__

![](images/mlops-continuous-delivery-and-automation-pipelines-in-machine-learning-4-ml-automation-ci-cd.svg)


como se aprecia en la imagen un sistema de MLOPS consta de varios pasos, comenzando con la recopilación de datos de diversas fuentes, seguida de la preparación de los datos para su uso en el entrenamiento del modelo. Una vez preparados, se procede al entrenamiento del modelo utilizando algoritmos que aprenden de los datos y generan un modelo. Después, se evalúa el rendimiento del modelo utilizando nuevos datos para comprobar su capacidad de predicción. Una vez que el modelo ha sido evaluado, se implementa para su uso en producción, lo que implica empaquetarlo y hacerlo accesible a los usuarios. Este proceso puede estar propenso a errores. Sin embargo, la entrega continua y la automatización pueden mejorar este proceso al automatizar los pasos de todo el sistema, permitiendo una implementación más rápida y confiable de nuevos modelos. Esto ayuda a reducir errores y mejorar la eficiencia general del sistema de ML.