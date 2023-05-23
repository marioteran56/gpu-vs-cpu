# CPU vs GPU (con CUDA)

![CPU vs GPU](https://www.researchgate.net/publication/323281068/figure/fig1/AS:727952463495175@1550568800252/CPU-vs-GPU-architecture-each-blue-square-represents-one-core.ppm)

## Introducción

En este trabajo se busca comparar el rendimiento en cuestiones de tiempo de lo que tarda un modelo de una **CNN** en entrenarse en una **CPU** y en una **GPU**. Para ello se utilizará el dataset de **CIFAR 10**, y se entrenará un modelo de **CNN** para clasificarlos.

## Desarrollo

### Entrenamiento en GPU

El modelo fue entrenado dentro de un **Jupyter Notebook** en **Google Colab**, utilizando una **GPU T4** de **NVIDIA**. Por lo tanto, se aprovechó el uso de **CUDA** para acelerar el entrenamiento en paralelo.

#### Resultados

El modelo fue entrenado durante **5 épocas**, el cual, ignorando la precisión del modelo, tardó **277 segundos** en entrenarse.

En cuanto al tiempo que tardo en evaluar el modelo, fue de **3 segundos**.

### Entrenamiento en CPU

El modelo fue entrenado dentro de un **Jupyter Notebook** en **Google Colab**, utilizando una **CPU**. Por lo tanto, no se aprovechó el uso de **CUDA** para acelerar el entrenamiento en paralelo, sino que se entrenó de manera secuencial.

#### Resultados

El modelo fue entrenado durante **1 sola época**, el cual, ignorando la precisión del modelo, tardó **3521 segundos** en entrenarse, casi **1 hora**.

En cuanto al tiempo que tardo en evaluar el modelo, fue de **40 segundos**, lo que es aproxima a **13 veces más** que en la GPU.

## Conclusión

Como se puede observar, el entrenamiento en **GPU** es mucho más rápido que en **CPU**, ya que en este caso, el entrenamiento en **GPU** fue claramente más rápido que en **CPU**. Esto se debe a que la **GPU** tiene muchos más núcleos que la **CPU**, por lo que puede realizar muchas más operaciones en paralelo que la **CPU**.
