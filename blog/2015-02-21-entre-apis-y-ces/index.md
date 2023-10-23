---
title: "Entre APIs y Ces..."
date: "2015-02-21"
categories: 
  - "chusynth"
  - "tecnologia"
tags: 
  - "fluidsynth-es"
  - "freopen-es"
  - "pyfluidsynth-es"
  - "sf2-es"
  - "soundfont-es"
  - "stdout-es"
---

Sí, la interfaz pyFluidSynth que estoy [forkeando](https://github.com/pakitochus/pyfluidsynth) tiene una función principal: interactuar con la API de fluidsynth, que está escrita en C. Eso lleva a algunos problemas, por ejemplo, en el tipo de datos y estructuras que maneja.

Más o menos podemos decir que la cosa va viento en popa, y he ampliado el número de funciones que la clase `Synth` posee con muchas de las funciones que provee la API, pero hay cosas con las que he tenido que recurrir a magia negra. Para obtener una lista de todos los instrumentos que posee una función he tenido que crear una interfaz para capturar durante unos momentos la salida del shell. En fluidsynth, hay dos opciones de obtener la lista: construir una serie de estructuras horrendas (con las que interactuar en python se puede convertir en un infierno), o capturar la salida del shell con los comandos `inst SF_ID`. Así que opté por esta última.

Tras darle muchísimas vueltas, por fin conseguí hacer una clase, que llamé StdoutHandler, y que llamando `objeto.freopen()` abres un archivo y escribe la salida de la shell en el mismo, y con `objeto.freclose()` se devuelve la salida al stdout del sistema.

Así que esto es lo que he hecho, por si a alguien le hace falta (basado en [este post de StackOverflow](http://stackoverflow.com/questions/26126160/redirecting-standard-out-in-err-back-after-os-dup2)):

\[code lang=python\] class StdoutHandler(object): def \_\_init\_\_(self, f): """Create new stdouthandler, for management of stdin and stdout (some methods of Synth DO need to capture stdout stream). """ self.prevOutFd = os.dup(1) self.prevInFd = os.dup(0) self.prevErrFd = os.dup(2) self.newf = open(f, 'w') self.newfd = self.newf.fileno() # The new file output

def freopen(self): """ Redirects the standard input, output and error stream to the established newfd. :return: """ os.dup2(self.newfd, 0) os.dup2(self.newfd, 1) os.dup2(self.newfd, 2)

def freclose(self): """ Closes the modified input, output and error stream :return: """ self.newf.close() os.dup2(self.prevOutFd, 1) os.close(self.prevOutFd) os.dup2(self.prevInFd, 0) os.close(self.prevInFd) os.dup2(self.prevErrFd,2) os.close(self.prevErrFd) \[/code\]
