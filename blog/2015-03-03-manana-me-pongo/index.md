---
title: "Mañana me pongo"
date: "2015-03-03"
categories: 
  - "ciencia"
  - "tecnologia"
tags: 
  - "ciencia-es"
  - "data-science-es"
  - "julia-es"
  - "julialang-es"
  - "jupyter-es"
  - "matlab-es"
  - "open-source-es"
  - "programacion-es"
  - "python-es"
  - "razones-es"
  - "scipy-es"
---

Pero de verdad. Mañana empiezo el curso de [Edx](http://www.edx.org) llamado 6.00.2x **Introduction to Computational Thinking and Data Science**. Otro MOOC más que espero que me de buenas bases para migrar decididamente desde el malvado y pesado, pero cómodo, **Matlab** a **Python**, que es Open Source (vaya, de lo mío).

Es un paso importante, porque además de seguir a la peña científica que generalmente [están migrando a Python desde plataformas como R o Matlab](http://www.nature.com/news/my-digital-toolbox-climate-scientist-damien-irving-on-python-libraries-1.16805) con proyectos como [SciPy](http://scipy.org), apoyo a proyectos que me resultan extremadamente atractivos, como [Jupyter](http://jupyter.org), una especie de [IPython](http://www.ipython.org) evolucionado para ser _language-agnostic_ y poder trabajar a la vez con Python, R, y [Julia](http://www.julialang.org).

El mundo del software evoluciona muy rápidamente, y si hasta ahora Matlab tenía el beneficio de la comodidad, multitud de extensiones y paquetes para trabajar en casi cualquier cosa, parece que cada vez Python se yergue como un potente rival. Una listilla con mis razones para hacer el cambio podría ser esta:

|  | Matlab | Python |
| --- | --- | --- |
| Librerías third-party | Sí | Sí |
| Diseño de Aplicaciones | Horrendo[1](#fn-164-1) | Fácil |
| Multi-purpose | No | Sí |
| Gráficos | Propia[2](#fn-164-2) | [MatPlotLib](http://matplotlib.org) |
| Open Source | No | Sí |
| Eficiencia Computacional | Baja | Baja |
| Integración con otros lenguajes | Difícil[3](#fn-164-3) | Buena |
| Shell interactivo | Sí | IPython |
| Multitud de IDEs | No | Sí |

* * *

2. Matlab contiene utilidades para crear interfaces gráficas y programas empaquetados, pero su uso es muy difícil, ineficiente y depende de una instalación de Matlab en el ordenador en el que se ejecute. [↩](#fnref-164-1)

4. La librería de plots de Matlab es muy variada y los resultados son bastante visuales, pero ha sido superada por `ggplot2` y `matplotlib` hace tiempo. [↩](#fnref-164-2)

6. Existen formas de interactuar con C, C++ y Java desde Matlab, pero de forma un poco limitada. La capacidad de extensión de Python con otros lenguajes lo supera con diferencia. [↩](#fnref-164-3)
