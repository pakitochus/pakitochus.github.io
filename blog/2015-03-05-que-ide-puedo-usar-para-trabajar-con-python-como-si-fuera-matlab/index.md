---
title: "¿Qué IDE puedo usar para trabajar con Python como si fuera Matlab?"
date: "2015-03-05"
categories: 
  - "ciencia"
  - "tecnologia"
tags: 
  - "canopy-es"
  - "data-science-es"
  - "eip-es"
  - "ide-es"
  - "matlab-es"
  - "python-es"
  - "science-es"
  - "scipy-es"
  - "spyder-es"
---

Esta es la primera pregunta que me hice a la hora de pasarme a **Python**. Y no es una respuesta fácil. Si dejamos de lado diferencias tan sustanciales como que Python es orientado a objetos y Matlab no, y las diferencias a la hora de trabajar con uno y otro, habría que atender a varias circunstancias. Para mi, un IDE que funcione bien tiene que tener al menos:

- Editor integrado (si puede ser con sugerencias)
- Ventana de comandos (IPython a ser posible)
- Visor de variables
- Posibilidad de salvar un workspace

Prácticamente todos los IDEs cumplen estas características. Después de mucho navegar por la web me encontré los más parecidos a Matlab que me podía tirar a la cabeza: [Spyder](https://code.google.com/p/spyderlib/) y [IEP](http://www.iep-project.org). Ambos cumplen exactamente lo que prometen: un IDE para trabajar con [SciPy](http://www.scipy.org) (con todo lo que ello conlleva: numpy, matplotlib, scipy, sklearn).

[![Spyder UI](https://fjesusmartinez.files.wordpress.com/2015/03/spyder.jpg?w=300)](https://fjesusmartinez.files.wordpress.com/2015/03/spyder.jpg)

El primero que probé era **Spyder**, bastante consolidado ya en el mundillo, y que cumple todo lo anteriormente dicho. Es bueno, fiable y permite guardar el workspace en un único fichero (pero esto también puede ser un problema, porque es un fichero propio de spyder). Tiene un autodetector de las funciones que se están usando, que muestra la ayuda de dicha función en una pestaña (si la tenemos visible). En su contra diré que es más bien feo (tanto la UI como el icono) y que no tiene sugerencias instantáneas.

[![EIP UI](https://fjesusmartinez.files.wordpress.com/2015/03/eip.jpg?w=300)](https://fjesusmartinez.files.wordpress.com/2015/03/eip.jpg)

Por otra parte, conocí **EIP**, que por el momento me gusta más. Está en un desarrollo un poco más activo, aunque menos maduro que Spyder, con todo lo que ello conlleva. La principal diferencia es que no tiene un asistente para guardar workspace (se puede hacer desde código), pero en contrapartida posee sugerencias _live_ de funciones, objetos y demás que estén en el workspace, lo que es muy conveniente cuando uno está empezando. También en el apartado estético gana por su limpieza e integración con el sistema operativo. Todavía es pronto para hacer un diagnóstico y me quedan muchas horas que trabajar con alguno de ellos, pero por lo pronto, yo me quedo con **EIP**, por las sugerencias y por su interfaz más pulida. Quizá en algún momento necesite guardar variables del workspace, en ese momento me plantearé que opción es más buena.

**Editado**: Una tercera opción que se me olvidó citar al ser de pago (aunque tienen una versión gratuita) es [Canopy](https://www.enthought.com/products/canopy/). Quizá es la que más se parezca a Matlab y viene perfecamente equipado con todo lo necesario para trabajar. Lo que es más, está disponible tanto para Windows como para Mac y Linux, lo que lo hace una opción muy buena a tener en cuenta si no importa el hecho de que no sea open source.
