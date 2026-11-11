# Password Generator (2022)

Proyecto de **aprendizaje con Python y Tkinter**: una interfaz sencilla que recibe un nombre de usuario, genera una contraseña de 12 caracteres y registra ambos datos en un archivo local.

> **Aviso importante:** este es un ejercicio antiguo, **no un gestor de contraseñas seguro**. El programa utiliza `random.sample` en lugar de un generador criptográfico y guarda las credenciales **en texto plano** dentro de `data.txt`. No lo uses con cuentas ni contraseñas reales.

## Cómo funciona

1. La interfaz solicita un nombre de usuario.
2. Al pulsar **Generar contraseña**, el programa crea una cadena de 12 caracteres.
3. Añade el nombre de usuario y la contraseña al archivo `data.txt`.
4. Muestra un mensaje cuando se completa el registro.

## Código fuente

El código del prototipo está conservado en [CODE.md](CODE.md), junto a texto explicativo. Para ejecutarlo con Python, copia **solo el bloque de código**, que comienza por `from tkinter import *`, en un archivo con extensión `.py`. Necesitarás una instalación de Python con Tkinter disponible.

El repositorio incluye también un ejecutable antiguo para Windows que **no se ha verificado recientemente**.

## Limitaciones conocidas

- No cifra las contraseñas ni protege el archivo de salida.
- No usa `secrets` ni un generador criptográficamente seguro.
- No permite configurar políticas de longitud o complejidad.
- Es un prototipo educativo, no una aplicación mantenida para producción.

Este repositorio se conserva como parte del aprendizaje y de la evolución de mis proyectos.
