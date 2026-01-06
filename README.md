# ⛓️ Blockchain C-Implementation

Una implementación educativa y funcional de una **cadena de bloques (blockchain)** desarrollada íntegramente en C. Este proyecto demuestra los conceptos fundamentales detrás de la inmutabilidad de datos y la gestión de transacciones mediante estructuras de datos dinámicas.

---

## 📖 Descripción del Proyecto

Este proyecto simula el comportamiento de una red blockchain básica. Se centra en la integridad de la información mediante el uso de funciones hash y la organización de bloques en una estructura de **lista enlazada**. Es una herramienta ideal para comprender cómo se encadenan los bloques y cómo una pequeña alteración puede invalidar la continuidad de la red.

---

## 🚀 Características Principales

* **Generación de Transacciones**: Sistema automatizado para simular el intercambio de datos entre diferentes "partidos" de forma aleatoria.
* **Integridad mediante Hashing**: Implementación del algoritmo **DJB2**, conocido por su eficiencia y buena distribución de bits para generar firmas digitales de cada bloque.
* **Gestión Dinámica**: Uso avanzado de punteros y listas enlazadas para el almacenamiento escalable de la cadena.
* **Utilidades de Cadena**: Funciones integradas para la inversión de la lista, validación y visualización formateada de los bloques en consola.

---

## 🛠️ Especificaciones Técnicas

### El Algoritmo de Hashing

El proyecto utiliza la función hash **DJB2** para garantizar que cada bloque contenga la huella digital del bloque anterior, asegurando el principio de inmutabilidad:

```c
unsigned long hash(unsigned char *str) {
    unsigned long hash = 5381;
    int c;
    while ((c = *str++))
        hash = ((hash << 5) + hash) + c; /* hash * 33 + c */
    return hash;
}

```

### Estructura del Bloque

Cada nodo de la cadena representa un bloque que contiene:

1. **ID**: Identificador único.
2. **Timestamp**: Registro del momento de creación.
3. **Data**: Información de la transacción.
4. **Hash Anterior**: El vínculo que garantiza la seguridad de la cadena.

---

## ✒️ Autor

Proyecto desarrollado con fines educativos por **Sebastián Fernández Buelvas**.
