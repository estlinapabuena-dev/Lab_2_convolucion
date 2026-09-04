# Laboratorio 2 - Convolución, Correlación y Transformada de Fourier
**Universidad Militar Nueva Granada**  
**Asignatura:** Laboratorio de Procesamiento Digital de Señales  
**Estudiantes:** [Lina Marcela Pabuena]    
**Título de la práctica:** Convolución, correlación y transformada de Fourier

## Objetivos
- Comprender la convolución como una operación que permite obtener la respuesta de un sistema discreto ante una entrada determinada.
- Analizar la correlación como medida de similitud entre dos señales.
- Aplicar la Transformada de Fourier como herramienta de análisis en el dominio de la frecuencia.

# PARTE A

## Resumen

Este repositorio documenta la primera fase de un laboratorio enfocado en el procesamiento de señales discretas. El objetivo principal fue calcular la convolución de dos señales, $x[n]$ y $h[n]$, definidas a partir de datos personales (cédula y código estudiantil, respectivamente). El proceso incluyó una **convolución manual**, seguida de una **verificación computacional** utilizando Python.

### 1. Definición de Señales y Convolución Manual

Las señales de entrada, **$x[n]$** y **$h[n]$**, se definieron usando los dígitos de la cédula y el código estudiantil de cada una de las integrantes. La convolución, $y[n] = x[n] * h[n]$, se calculó paso a paso de forma manual, documentando cada operación.

- **Señal $y[n]$**: María José
  ![conv majo](https://github.com/user-attachments/assets/a3fb18ed-6df5-4a69-818a-dac87e23b746)

- **Señal $y[n]$**: Valentina
 ![conv vale](https://github.com/user-attachments/assets/23e43f71-4eb9-49c3-9fa7-58743fa4ac29)

- **Señal $y[n]$**: Lina
  ![conv lina](https://github.com/user-attachments/assets/153582a5-05e7-4d07-b0c3-720d2b422c82)


### 2. Representación Gráfica y Secuencial

Se generaron las representaciones gráficas y secuenciales de las señales originales ($x[n]$, $h[n]$) y de la señal resultante ($y[n]$). Este paso se realizó a mano para visualizar el desplazamiento y la superposición de las señales.

- **Gráfica señal $y[n]$**: María José
  ![conv majo a mano](https://github.com/user-attachments/assets/3b62d600-5d17-4355-b457-d766a14de749)

- **Gráfica señal $y[n]$**: Valentina
  ![conv vale a mano](https://github.com/user-attachments/assets/fce6176d-1b8e-49ad-932e-ab8a7b29ed86)

- **Gráfica señal $y[n]$**: Lina
  ![conv lina a mano](https://github.com/user-attachments/assets/514129b4-bbf1-4e4d-9e9f-46781c67801a)


### 3. Verificación Computacional con Python

Para validar los resultados manuales, se implementó el cálculo de la convolución en Python. Se utilizó la librería **NumPy** para manipular las señales como arreglos y verificar la precisión del cálculo.

<pre>
  # Datos Majo
x = np.array([1,0,1,1,0,8,5,6,7,9])   # cédula
h = np.array([5,6,0,0,8,7,6])         # código estudiantil

# Gráfica de h[n]
t = np.arange(len(h))
plt.figure(figsize=(8, 4))
plt.stem(t, h)
plt.xlabel('n')
plt.ylabel('h [n]')
plt.title('h [n] María José')
plt.grid()
plt.show()

# Gráfica de x[n]
t = np.arange(len(x))
plt.figure(figsize=(8, 4))
plt.stem(t, x)
plt.xlabel('n')
plt.ylabel('x [n]')
plt.title('x [n] María José')
plt.grid()
plt.show()

# Convolución
y = np.convolve(x, h, mode='full')
print("Señal convolución entre h [n] y x [n], María José:")
print(y)

# Gráfica de y[n]
t = np.arange(len(y))
plt.figure(figsize=(10, 4))
plt.stem(t, y)
plt.xlabel('n')
plt.ylabel('y [n]')
plt.title('Convolución y [n] = x [n] * h [n]')
plt.grid()
plt.show()
</pre> 

## Gráfica Código Estudiantil María José
<img width="678" height="394" alt="Grafica Codigo estudiantil majo" src="https://github.com/user-attachments/assets/1aaf8e9b-b287-4250-b6c0-6ca1ea3164a4" />

## Gráfica Cédula María José
<img width="678" height="394" alt="Grafica cedula majo" src="https://github.com/user-attachments/assets/6bef032c-da47-4662-96d0-f239514e7249" />

## Gráfica Convolución María José
<img width="850" height="394" alt="convolución Majo" src="https://github.com/user-attachments/assets/7a8b5d55-60a3-4030-b6a4-b4961f4605ad" />

<pre>
# Datos de Valentina
x = np.array([1,0,2,3,3,7,1,2,5,9])   # cédula
h = np.array([5,6,0,0,8,1,7])         # código estudiantil

# Gráfica de h[n]
t = np.arange(len(h))
plt.figure(figsize=(8, 4))
plt.stem(t, h)
plt.xlabel('n')
plt.ylabel('h[n]')
plt.title('h[n] Valentina')
plt.grid()
plt.show()

# Gráfica de x[n]
t = np.arange(len(x))
plt.figure(figsize=(8, 4))
plt.stem(t, x)
plt.xlabel('n')
plt.ylabel('x[n]')
plt.title('x[n] Valentina')
plt.grid()
plt.show()

# Convolución
y = np.convolve(x, h, mode='full')
print("Señal convolución entre h[n] y x[n], Valentina:")
print(y)

# Gráfica de y[n]
t = np.arange(len(y))
plt.figure(figsize=(10, 4))
plt.stem(t, y)
plt.xlabel('n')
plt.ylabel('y[n]')
plt.title('Convolución y[n] = x[n] * h[n]')
plt.grid()
plt.show()
</pre> 
## Gráfica Código Estudiantil Valentina
<img width="678" height="393" alt="Grafica Codigo estudiantil Vale" src="https://github.com/user-attachments/assets/8b83cab4-9bdc-4b25-9e0c-d32b3719cae3" />

## Gráfica Cédula Valentina
<img width="678" height="393" alt="Grafica cedula vale" src="https://github.com/user-attachments/assets/e2d26cb3-f49a-40fb-ac49-1b276941aa10" />

## Gráfica Convolución Valentina
<img width="850" height="394" alt="convolución Vale" src="https://github.com/user-attachments/assets/59ea24ef-ce9b-40b7-a16b-fa83f87d4260" />

<pre>
# Datos de Lina
x = np.array([1,0,1,1,0,8,2,1,5,0])   # cédula
h = np.array([5,6,0,0,8,2,2])         # código estudiantil

# Gráfica de h[n]
t = np.arange(len(h))
plt.figure(figsize=(8, 4))
plt.stem(t, h)
plt.xlabel('n')
plt.ylabel('h[n]')
plt.title('h[n] Lina')
plt.grid()
plt.show()

# Gráfica de x[n]
t = np.arange(len(x))
plt.figure(figsize=(8, 4))
plt.stem(t, x)
plt.xlabel('n')
plt.ylabel('x[n]')
plt.title('x[n] Lina')
plt.grid()
plt.show()

# Convolución
y = np.convolve(x, h, mode='full')
print("Señal convolución entre h[n] y x[n], Lina:")
print(y)

# Gráfica de y[n]
t = np.arange(len(y))
plt.figure(figsize=(10, 4))
plt.stem(t, y)
plt.xlabel('n')
plt.ylabel('y[n]')
plt.title('Convolución y[n] = x[n] * h[n]')
plt.grid()
plt.show()
</pre> 
## Gráfica Código Estudiantil Lina
<img width="678" height="393" alt="Grafica Codigo estudiantil Lina" src="https://github.com/user-attachments/assets/6fbecc7b-b591-4250-8839-b40a92d5a6e7" />

## Gráfica Cédula Lina
<img width="678" height="393" alt="Grafica cedula lina" src="https://github.com/user-attachments/assets/d56ceb1a-93f1-49ea-afb2-bd100345d890" />

## Gráfica Convolución Lina
<img width="850" height="394" alt="convolución Lina" src="https://github.com/user-attachments/assets/fbcbcc0f-cf23-4089-8a8a-2a91edeaf5a6" />

# PARTE B

##  Resumen

Esta sección del laboratorio se centra en la aplicación de la **correlación cruzada** entre dos señales discretas, **$x[n]$** y **$h[n]$**. El objetivo es determinar la similitud entre ambas señales en función de un desplazamiento temporal. El proceso incluye el cálculo, la representación gráfica del resultado y una discusión sobre la utilidad de esta técnica en el procesamiento digital de señales.

### 1. Definición de Señales


- Señal Cosenoidal
  x1[nTs] = cos(2π * 100 * nTs) = cos(n * π/4)  
- Señal Senoidal
  x2[nTs] = sin(2π * 100 * nTs) = sin(n * π/4)

### 2. Correlación Cruzada
### 3. ¿En qué situaciones resulta útil aplicar la correlación cruzada en el procesamiento digital de señales?

# Parte C
## Resumen 
Esta sección del laboratorio se centra en la **convolución** y la **correlación cruzada**, específicamente su relación con la simetría de las señales. Se examina cómo el orden de las señales afecta los resultados de la convolución y cómo la correlación cruzada está intrínsecamente ligada a la convolución de una señal invertida en el tiempo. El objetivo principal es validar la **propiedad conmutativa de la convolución** y demostrar la conexión entre ambas operaciones.

