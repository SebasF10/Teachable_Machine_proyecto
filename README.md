# Reconocimiento de Gestos con Redes Neuronales usando Teachable Machine

## Integrantes

- Sebastian Feo Murillo
- Oscar Julian Uribe Pinto

--- 

# Descripción del proyecto

Este proyecto consiste en desarrollar un sistema de Inteligencia Artificial capaz de reconocer diferentes gestos de la mano mediante una cámara web utilizando Teachable Machine.

El objetivo del proyecto es comprender cómo una red neuronal aprende patrones visuales y clasifica imágenes en tiempo real. El modelo fue entrenado para identificar cinco gestos diferentes de la mano y realizar una predicción automática utilizando una cámara web.

Este tipo de tecnología puede aplicarse en sistemas de control sin contacto, accesibilidad, automatización, videojuegos e interfaces gestuales.

---

# Problema a resolver

Actualmente muchas aplicaciones requieren el uso de teclado o mouse para interactuar con un sistema. Sin embargo, existen situaciones donde es más práctico utilizar únicamente una cámara para reconocer gestos.

Para solucionar este problema se desarrolló un modelo de Inteligencia Artificial capaz de identificar automáticamente distintos gestos de la mano utilizando una cámara web.

---

# Clases utilizadas

El modelo fue entrenado para reconocer las siguientes clases:

- Mano abierta
- Pulgar arriba
- Pulgar abajo
- Señal de alto
- Señal de paz

Cada una representa un gesto diferente para que la red neuronal aprenda a distinguir sus características visuales.

Cada clase fue entrenada con 50 imagenes

---

# Dataset utilizado

Las imágenes fueron capturadas utilizando la cámara web integrada de Teachable Machine.

Para mejorar el entrenamiento se tomaron imágenes variando:

- Distancia de la mano.
- Posición.
- Inclinación.
- Iluminación.
- Fondo.
- Orientación.

De esta manera el modelo aprende a reconocer los gestos en diferentes condiciones y no únicamente en una posición específica.

---


# Funcionamiento del modelo

El modelo fue desarrollado utilizando Teachable Machine, el cual emplea una red neuronal mediante la técnica de Transfer Learning.

Cuando la cámara captura una imagen ocurre el siguiente proceso:

1. La imagen es convertida en una matriz de píxeles.
2. Cada píxel contiene valores numéricos que representan colores.
3. La red neuronal analiza esos valores para encontrar patrones.
4. La información atraviesa todas las capas de la red mediante el proceso conocido como **Forward Pass**.
5. Cada neurona realiza operaciones matemáticas utilizando los pesos aprendidos durante el entrenamiento.
6. Finalmente, la red genera una predicción indicando cuál de las clases aprendidas es la más probable.

---

# ¿Qué ve realmente la IA?

La Inteligencia Artificial no reconoce una mano como lo hace una persona.

Lo que realmente recibe es una imagen formada por miles de píxeles.

Cada píxel contiene números que representan colores e intensidad.

La red neuronal analiza únicamente esos valores numéricos y encuentra relaciones matemáticas entre ellos para identificar patrones similares a los observados durante el entrenamiento.

Por ello la IA trabaja con:

- Píxeles.
- Valores numéricos.
- Patrones.
- Relaciones matemáticas.
- Pesos neuronales.

La IA no comprende el significado de los gestos; simplemente compara los patrones visuales de la imagen con los aprendidos durante el entrenamiento.

---

# Relación con los conceptos vistos en clase

## Redes neuronales

La red neuronal aprende automáticamente las características presentes en las imágenes para poder diferenciarlas.

## Clasificación

El modelo clasifica cada imagen dentro de una de las cinco categorías entrenadas.

## Reconocimiento de patrones

Durante el entrenamiento la IA aprende qué características visuales identifican cada gesto.

## Pesos neuronales

Cada conexión de la red posee un peso.

Durante el entrenamiento esos pesos cambian constantemente para reducir el error y mejorar las predicciones.

## Forward Pass

Cuando una imagen entra al modelo, la información pasa por todas las capas de la red neuronal.

Cada neurona realiza operaciones matemáticas utilizando los pesos aprendidos hasta obtener la predicción final.

---

# Casos donde funciona correctamente

El modelo obtiene buenos resultados cuando:

- Existe buena iluminación.
- La mano está completamente visible.
- El gesto es similar a los utilizados durante el entrenamiento.
- La cámara está enfocada.
- El fondo no presenta demasiados objetos.

En la siguiente imagen se observa un caso donde el modelo reconoce correctamente el gesto realizado.

![Caso de éxito](Imagenes\exito.png)

En este ejemplo el modelo identifica correctamente el gesto mostrado, demostrando que aprendió correctamente los patrones presentes en esa clase.

---

# Casos donde falla

Durante las pruebas también se observaron errores de clasificación.

Uno de los casos ocurrió al mostrar la señal de paz. En lugar de reconocer correctamente el gesto, el modelo asignó una mayor probabilidad a otras clases y produjo una predicción incorrecta.

Las principales causas de este error pueden ser:

- Cantidad insuficiente de imágenes para algunas clases.
- Gestos visualmente similares.
- Diferencias en la posición de la mano.
- Variaciones de iluminación.
- Ruido en el fondo.
- Sobreajuste del modelo.

La siguiente imagen muestra un ejemplo del error de clasificación.

![Caso de error](Imagenes\error.png)

Este tipo de errores demuestra que el rendimiento de una red neuronal depende directamente de la calidad, cantidad y variedad del conjunto de datos utilizado durante el entrenamiento.

---

# Análisis de resultados

En las pruebas realizadas el modelo logró reconocer correctamente la mayoría de los gestos cuando las condiciones eran similares a las utilizadas durante el entrenamiento.

Los errores aparecieron principalmente cuando algunos gestos presentaban características visuales parecidas o cuando las imágenes tenían posiciones, iluminación o ángulos diferentes.

Esto evidencia la importancia de construir un conjunto de datos amplio y variado para mejorar la capacidad de generalización del modelo.

---

# Reflexión crítica

Este proyecto permitió comprender que una red neuronal puede aprender a clasificar imágenes mediante ejemplos previamente etiquetados.

También se comprobó que el desempeño del modelo depende en gran medida de la calidad del conjunto de datos. Mientras más variadas sean las imágenes utilizadas durante el entrenamiento, mayor será la capacidad del modelo para reconocer nuevos ejemplos y menor será la probabilidad de cometer errores.

---

# ¿La IA realmente entiende lo que ve?

No.

La Inteligencia Artificial no entiende el significado de los gestos como lo hace un ser humano.

No sabe que un pulgar arriba representa aprobación o que una señal de paz representa un saludo.

Lo único que hace es analizar miles de píxeles, encontrar patrones matemáticos y compararlos con los aprendidos durante el entrenamiento para determinar cuál de las clases conocidas es la más parecida a la imagen capturada.

---

# Tecnologías utilizadas

- Teachable Machine
- TensorFlow.js
- HTML
- JavaScript
- GitHub

---

# Estructura del repositorio

```
Proyecto/
│
├── modelo-IA/
│   ├── model.json
│   ├── metadata.json
│   └── weights.bin
│
├── imagenes/
│   ├── exito.png
│   └── error.png
│
└── README.md
```

---

# Conclusión

Este proyecto permitió comprender el funcionamiento básico de una red neuronal aplicada al reconocimiento de imágenes mediante Teachable Machine.

A través del entrenamiento del modelo fue posible observar cómo la Inteligencia Artificial aprende patrones visuales, clasifica imágenes y genera predicciones en tiempo real. Además, se comprobó que la calidad y variedad del conjunto de datos es uno de los factores más importantes para obtener un modelo preciso y confiable.