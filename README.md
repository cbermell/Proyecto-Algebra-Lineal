# 📐 Proyecto: Gráficos por Computadora 2D y Transformaciones Lineales

![Python](https://img.shields.io/badge/Python-3.14%2B-blue)
![NumPy](https://img.shields.io/badge/Library-NumPy-orange)
![Matplotlib](https://img.shields.io/badge/Library-Matplotlib-green)
![Status](https://img.shields.io/badge/Status-Completado-brightgreen)

> **Resumen:** Implementación práctica de conceptos de Álgebra Lineal aplicados a gráficos por computadora. Este proyecto demuestra cómo manipular objetos geométricos en 2D utilizando matrices de transformación y coordenadas homogéneas.

---

## 📋 Tabla de Contenidos
1. [Descripción del Proyecto](#-descripción-del-proyecto)
2. [Fundamento Matemático](#-fundamento-matemático)
3. [Resultados Visuales](#-resultados-visuales)
4. [Estructura del Código](#-estructura-del-código)
5. [Instalación y Uso](#-instalación-y-uso)

---

## 📝 Descripción del Proyecto

El objetivo principal de este proyecto es desmitificar cómo funcionan los motores gráficos "bajo el capó". Utilizando **Python**, creamos un motor de renderizado 2D simple que permite:

* Definir objetos geométricos mediante vértices.
* Aplicar transformaciones afines (Rotación, Escala, Traslación, Corte).
* Visualizar en tiempo real el efecto de las operaciones matriciales.
* Demostrar propiedades matemáticas clave, como la **no conmutatividad** de las matrices.

---

## 🧠 Fundamento Matemático

El núcleo del proyecto se basa en el uso de **Coordenadas Homogéneas**. 
Para permitir que la traslación sea una operación lineal (multiplicación de matrices) y no una suma vectorial, proyectamos nuestros vectores 2D $(x, y)$ al espacio 3D $(x, y, 1)$.

Esto nos permite usar matrices de $3 \times 3$ para todas las operaciones:

$$
P' = T \cdot P
$$

Donde:
* $P$: Matriz de vértices del objeto.
* $T$: Matriz de Transformación unificada.

---

## 🎨 Resultados Visuales

### 1. Galería de Transformaciones
Visualización de las operaciones fundamentales aplicadas al objeto base ("La Casa").

| Rotación (45°) | Escalamiento | Corte (Shear) | Traslación |
|:---:|:---:|:---:|:---:|
| *(Gira sobre el origen)* | *(Deforma ejes X/Y)* | *(Inclina la figura)* | *(Desplaza posición)* |

> *Nota: Puedes ver las gráficas generadas ejecutando el Notebook.*

### 2. La Importancia del Orden (No Conmutatividad)
Demostración de que $A \cdot B \neq B \cdot A$.
* **Secuencia 1:** Rotar $\to$ Escalar $\to$ Trasladar.
* **Secuencia 2:** Trasladar $\to$ Escalar $\to$ Rotar.

El resultado geométrico final es drásticamente diferente, validando la teoría matricial.

---

## 📂 Estructura del Código

El *Notebook* está organizado de forma secuencial:

1.  **Introducción Teórica:** Definición de espacios vectoriales y el problema de la traslación.
2.  **Definición del Objeto:** Creación de la matriz de vértices de una figura asimétrica (Casa).
3.  **Funciones de Transformación:** Implementación en `NumPy` de:
    * `obtener_matriz_rotacion(grados)`
    * `obtener_matriz_traslacion(dx, dy)`
    * `obtener_matriz_escalado(sx, sy)`
    * `obtener_matriz_corte(kx, ky)`
4.  **Visualización:** Uso de `Matplotlib` para graficar el "Antes" (Gris) y el "Después" (Color).
5.  **Composición:** Multiplicación de múltiples matrices para generar movimientos complejos.

---

## 🚀 Instalación y Uso

Puedes ejecutar este proyecto directamente en Google Colab o localmente.

### Requisitos Previos
* Python 3.x
* Librerías: `numpy`, `matplotlib`

### Ejecución Local
```bash
# Clonar el repositorio
git clone [https://github.com/cbermell/Proyecto-Algebra-Lineal.git](https://github.com/cbermell/Proyecto-Algebra-Lineal.git)
cd Proyecto-Algebra-Lineal

# Instalar dependencias
pip install numpy matplotlib

# Ejecutar Jupyter Notebook
jupyter notebook
```

---

## 👨‍💻 Autor

**Carlos Bermello**
*Estudiante de Ingeniería / Ciencias de la Computación*

* **Institución:** [Universidad Católica de Santiago de Guayaquil](https://www.ucsg.edu.ec/)
* **Materia:** Álgebra Lineal
* **GitHub:** [@cbermell](https://github.com/cbermell)
* **Repositorio:** [Proyecto-Algebra-Lineal](https://github.com/cbermell/Proyecto-Algebra-Lineal)

---

> **Nota:** Este proyecto fue desarrollado con fines académicos para demostrar la aplicación práctica de matrices y espacios vectoriales en la computación gráfica.
