# Story_user3
# 📦 Sistema de Gestión de Inventario (CRUD + CSV)

## 📌 Descripción

Este proyecto es un **sistema de gestión de inventario en consola** desarrollado en Python.
Permite administrar productos mediante operaciones CRUD y guardar/cargar la información usando archivos CSV.

---

## 🚀 Funcionalidades

* Agregar productos
* Mostrar inventario
* Buscar productos
* Actualizar productos
* Eliminar productos
* Calcular estadísticas
* Guardar inventario en CSV
* Cargar inventario desde CSV (sobrescribir o fusionar)

---

## 🧩 Estructura del Proyecto

```
inventory_app/
│
├── app.py          # Archivo principal (menú y ejecución)
├── servicios.py    # Lógica del sistema (CRUD + estadísticas)
├── archivos.py     # Manejo de archivos CSV
└── README.md
```

---

## 🛠️ Tecnologías utilizadas

* Python 3
* Módulo `csv` (librería estándar)

---

## ▶️ Cómo ejecutar

1. Descarga o clona el proyecto
2. Abre la carpeta en tu editor o terminal
3. Ejecuta el programa:

```
python app.py
```

---

## 📋 Opciones del menú

```
1. Agregar producto
2. Mostrar inventario
3. Buscar producto
4. Actualizar producto
5. Eliminar producto
6. Estadísticas
7. Guardar CSV
8. Cargar CSV
9. Salir
```

---

## 📊 Estructura de datos

Cada producto se almacena como un diccionario:

```
{
  "nombre": str,
  "precio": float,
  "cantidad": int
}
```

El inventario es una lista de estos diccionarios.

---

## 📈 Estadísticas

El sistema calcula:

* Total de unidades
* Valor total del inventario
* Producto más caro
* Producto con mayor stock

---

## 💾 Formato del archivo CSV

El archivo debe tener esta estructura:

```
nombre,precio,cantidad
Laptop,2500,5
Mouse,50,10
```

---

## ⚠️ Validaciones

* El precio debe ser numérico y no negativo
* La cantidad debe ser un número entero no negativo
* El archivo CSV se valida antes de cargar
* Las filas inválidas se omiten y se reportan

---

## 🔄 Comportamiento al cargar CSV

Al cargar un archivo:

* **Sobrescribir (S):** reemplaza todo el inventario actual
* **Fusionar (N):**

  * Si el producto existe → suma la cantidad
  * Si el precio cambia → se actualiza al nuevo

---

## 🧠 Manejo de errores

El sistema maneja errores como:

* Entradas inválidas del usuario
* Archivo no encontrado
* Errores de codificación
* Formato CSV incorrecto

El programa **no se cierra por errores**, siempre regresa al menú.

---
