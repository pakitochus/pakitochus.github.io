---
title: "¡Comienza la Aventura!"
date: "2015-02-18"
categories: 
  - "chusynth"
  - "tecnologia"
---

Por fin empieza esta aventura: hacer un dispositivo monotarea que se comporte como un sampler basado en SoundFonts, o lo que es lo mismo, mi **ChuSynth**. Mi plan es utilizar [fluidsynth](http://www.fluidsynth.org) como una librería cargada desde python, utilizando [pyFluidSynth](https://github.com/nwhitehead/pyfluidsynth) (que estoy [forkeando](https://github.com/pakitochus/pyfluidsynth) para añadir funcionalidades que necesito) desde donde se puedan realizar tareas básicas como cargar soundfonts, cambiar presets, etc, y que de los mensajes midi se ocupe fluidsynth.

[![Sin nombre](https://fjesusmartinez.files.wordpress.com/2015/02/sin-nombre.png?w=300)](https://fjesusmartinez.files.wordpress.com/2015/02/sin-nombre.png)

Las anteriores pruebas con la Raspberry Pi B+ habían sido un poco fiasco (temas de velocidad de CPU), pero por fin, con la salida de las **Raspberry Pi 2 B**, todo ha cambiado. He hecho las primeras pruebas de utilizar fluidsynth incluso con soundfonts grandes, y apenas hay problemas de polifonía.

Así pues el proyecto (en principio) se dividirá en las siguientes partes:

1. Dotar a pyFluidSynth de las funciones que necesito para implementar la aplicación (interacción con C++ mediante ctypes):
    - Listar y cambiar los presets
    - Establecer opciones límites de polifonía
2. Crear el resto de programas de python que corresponden con la interfaz con PiFace y la interfaz de usuario.
3. Montarlo todo en la Raspberry Pi y optimizar Raspbian para un single-purpose computer.
