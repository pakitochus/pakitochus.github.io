---
title: "FluidSynth superado. Ahora empieza lo bueno."
date: "2015-08-26"
categories: 
  - "tecnologia"
tags: 
  - "chusocol-es"
  - "chusynth-es"
  - "fluidsynth-es"
  - "linux-es"
  - "pyfluidsynth-es"
  - "python-es"
  - "raspberry-pi-es"
  - "sintetizador-es"
  - "synthesizer-es"
---

Por fin puedo decir que he echado un pulso a **fluidsynth**, sus python bindings (**pyFluidSynth**, see [original project](https://github.com/nwhitehead/pyfluidsynth) and my personal [fork](https://github.com/pakitochus/pyfluidsynth)) y a todas las dificultades que un proyecto de estas características te pone delante. Pero lo primero es lo primero, así que aquí tenéis una Demo de como funciona fluidsynth en una **Raspberry Pi 2 B+** (Raspbian), haciendo llamadas mediante los python bindings de fluidsynth:

https://www.youtube.com/watch?v=DEsfSsX-g4g

Y ahora vamos con los detalles. El video muestra simplemente una llamada a liveDemo.py, un script que he preparado para probar 20 segundos del programa 0 y 20 segundos del programa 50 de cualquier soundfont que tengamos (por defecto carga /usr/share/sounds/sf2/FluidR3\_GM). Así que los pasos para probarlo, desde una Raspberry Pi conectada a internet con Raspbian son los siguientes.

En primer lugar, nos aseguramos de tener instalado FluidR3\_GM y las librerías de python de ALSA:

`sudo apt-get install fluid-soundfont-gm python-pyalsa`

Posteriormente, hacemos un clone de pyFluidSynth, con el código:

`git clone https://github.com/pakitochus/pyfluidsynth.git`

Navegamos hasta el lugar donde está la instalación y ejecutamos:

`cd pyfluidsynth sudo python setup.py install`

Y en principio, ya podríamos ejecutar el test con:

`cd test python liveDemo.py`

Por supuesto, hace falta tener un teclado midi conectado a la raspberry, yo sugiero MIDI USB. En el script, se presupone que el puerto en el que está conectado es el 20,0, pero esto no tiene por qué ser así. La forma correcta de saber cual es el dispositivo que tenemos completado es mediante el comando:

`aconnect -i`

que listará algo así como:

\[code lang=text\] cliente 0: 'System' \[tipo=kernel\] 0 'Timer ' 1 'Announce ' cliente 14: 'Midi Through' \[tipo=kernel\] 0 'Midi Through Port-0' cliente 23: 'MIDI KEYBOARD' \[tipo=kernel\] 0 'MIDI KEYBOARD MIDI 1' \[/code\]

Suponiendo esos datos, para cambiar el que está por defecto, editamos el archivo liveDemo.py, y en la línea 29, donde aparece

\[code lang=text\] sender = (20, 0) # Modify according to the current port of the USB MIDI input \[/code\]

cambiamos por

\[code lang=text\] sender = (29, 0) \[/code\]

De igual modo, para cambiar la soundfont a utilizar o modificar la ruta, vamos a la línea 22 del archivo, y sustituimos la línea

\[code lang=text\] sfid = fs.sfload("/usr/share/sounds/sf2/FluidR3\_GM.sf2") \[/code\]

por la ruta hasta el archivo de soundfont que queramos. En el video, he utilizado una colección que he recopilado y creado -a partes iguales- llamada **ChusoCol**, que podéis encontrar en [Sourceforge](http://chusocol.sourceforge.net) (pronto subiré la ChusoCol 2, la del video).

Y eso es todo. No deja de ser una demostración de como funciona el fork de pyFluidSynth. Ahora es cuando viene lo bueno: **convertir la RPi2 en un _single-purpose_ computer** y añadir todos los controles para usar el **PiFace Control and Display** module.

Esto no ha hecho más que empezar. Pero ya hay un paso menos que dar.
