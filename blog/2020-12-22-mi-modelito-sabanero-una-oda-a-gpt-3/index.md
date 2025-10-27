---
title: "Mi Modelito Sabanero: Una oda a GPT-3"
date: "2020-12-22"
categories: 
  - "ciencia"
  - "divulgacion"
  - "humor"
  - "musica"
tags: 
  - "inteligencia-artificial"
  - "lenguaje"
  - "lenguaje-natural"
  - "musica"
  - "musical-es"
  - "transformer"
  - "villancico"
title-block-banner: url(images/PORTADA_MODELITO.jpg) 50% 50% 
image: images/PORTADA_MODELITO.jpg
---

Ayer fue [#CienciaPasión2020](https://twitter.com/hashtag/CienciaPasi%C3%B3n2020?src=hashtag_click). Como [#CienciaVisión](https://twitter.com/hashtag/CienciaVisi%C3%B3n?src=hashtag_click), un escaparate del humor, la música y el amor por la ciencia a todos los niveles, a los que [@InmaPToro](https://twitter.com/InmaPToro) y un servidor tuvieron a bien invitarnos. El objetivo: cantar una noticia del año. La nuestra: GPT-3

{{< video https://www.youtube.com/watch?v=1i-gkm9Xt6Q >}}

Pero antes, queremos agradecer de CORAZÓN a la peñita maravillosa que organizan todas estas MARAVILLAS de iniciativas y que nos llaman pa mamarrachear al compás: [@bynzelman](https://twitter.com/bynzelman)[@maitecicleta](https://twitter.com/maitecicleta)[@hayquehacerla](https://twitter.com/hayquehacerla)[@PutoMikel](https://twitter.com/PutoMikel)[@Nebesu\_](https://twitter.com/Nebesu_)[@ConchiLillo](https://twitter.com/ConchiLillo)[@manolux4444](https://twitter.com/manolux4444)[@sassyscience\_](https://twitter.com/sassyscience_)[@garirius](https://twitter.com/garirius)[@Victagua](https://twitter.com/Victagua) (fijo que me dejo alguien)

Y ahora paso a comentar algo que me han preguntado en varias ocasiones: ¿De qué co\*\*es va la letra de la canción? Este "modelito" sabanero no es otro que GPT-3, un modelo de deep learning para el lenguaje natural que desde su publicación ha revolucionado el campo. ¡Vamos por frases!

_"Con mi burrito sabanero voy entrenando mi modelo,  
red neuronal del lenguaje natural"._

Son redes neuronales (una de las bases de la inteligencia artificial) especializadas en comprender y entender el lenguaje de los seres humanos -> el "lenguaje natural".

_"Con tensorflow voy programando, el modelo voy compilando,_  
_capa tras capa vi’apilando, el modelo voy compilando_  
_GPT, GPT, se llama GPT-3"_

Tensorflow es la librería más usada para programar redes neuronales. Aunque yo soy más de PyTorch. Pero a día de hoy es el estándar de programación y en producción. Casi todos los grandes avances se pueden encontrar preparados para Tensorflow.

En estos modelos de deep learning, las neuronas se estructuran por "capas", grupos de neuronas que se conectan con otras capas. En nuestro caso, palabras. Si las neuronas fueran alumnos que aprenden, las capas serían filas, como [comentaba en Famelab](https://www.youtube.com/watch?v=4xaPxNPr43w).

Y GPT-3 es el sucesor de GPT-2 y 1, modelos de redes neuronales creados para modelar el lenguaje natural, basados en una arquitectura llamada "transformer". Y que fueron un bombazo por [artículos como este](https://www.theguardian.com/commentisfree/2020/sep/08/robot-wrote-this-article-gpt-3), completamente escritos por una Int. Artificial.

_"Libro tras libro descargando, la wikipedia escrapeando,_  
_todas las palabras en vectores a la entrada y a la salida"_

GPT-3 se entrenó utilizando millones de libros de dominio público, artículos científicos y la wikipedia al completo. Referencias: [https://arxiv.org/abs/2005.14165](https://t.co/fWJhUhbyH8?amp=1)

_"Atención, atención, mecanismo de atención"_

![Imagen](https://pbs.twimg.com/media/EptGIRdXIAYGzoC?format=jpg&name=medium)

La gran innovación de los transformers es el "mecanismo de atención", una herramienta que se construye en las redes neuronales, que permite a la red centrarse en unas entradas más que en otras, les presta más "atención".

El mecanismo de auto-atención (self-attention) se presentó en el paper "Attention is all you need", en el NeurIPS 2017, paper que, por cierto, también aparece en el vídeo: [https://proceedings.neurips.cc/paper/2017/hash/3f5ee243547dee91fbd053c1c4a845aa-Abstract.html](https://proceedings.neurips.cc/paper/2017/hash/3f5ee243547dee91fbd053c1c4a845aa-Abstract.html)

_"Tuki tuki tuki tuki,_  
_tuki tuki tuki ta_  
_ajusta bien el modelo que lo vamos a entrenar"_

Tremendo cumbión. Pues eso, a preparar un modelo de red "tó polluo", que si no, no funciona.

_"Tuki tuki tuki tuki,_  
_tuki tuki tuki ta,_  
_a ver si pasa el test de Turing, que lo vamos a petar"_

El test de Turing es un test diseñado por Alan Turing, que permitiría decir cuando una máquina es inteligente. Esto sucedía en un entorno experimental en el que humanos interactuaban vía texto en conversación con otros humanos, o podría ser con máquinas. Si un ser humano era incapaz de discernir si estaba hablando con una máquina o con otro ser humano, se dice que ese algoritmo ha pasado el Test de Turing.

_"Con mi burrito sabanero vi’entrenando mi transformer  
En arXiv, en arXiv, puedes encontrarme allí  
en github, en github puedes encontrarme allá"_

[http://arXiv.org](https://t.co/noAoIn8XwD?amp=1) es una web donde muchos científicos publican sus avances antes de enviarlos a revistas. Son conocidos como pre-prints, y aunque todavía no han pasado el proceso de revisión, es una forma muy rápida (y gratuita) de acceder al conocimiento que se está produciendo.

Y Github, pues eso.. [@github](https://twitter.com/github) Un servidor de Git, un sistema de control de versiones donde los desarrolladores de software centralizar el control de los cambios que hacen a su código. Allí están centralizados en "repositorios", lugares desde donde después se puede distribuir el código y contribuir a una ciencia más abierta.

_"Muy pronto los veremos integraos en una aplicación_  
_dentro del Office generando textos con gran precisión_  
_y en robots, en robots, robots de conversación"_

La aplicación directa: integrar los modelos para generar, aumentar productividad e interactúar con humanos. Ya hay modelos similares que se están implementando en aplicaciones como Photoshop para ayudar en la productividad de imagen. Y para el lenguaje natural, herramientas como DeepL translate ya tienen una gran difusión para traducir textos. Es sólo cuestión de tiempo que se integren en los paquetes de software más usados.

_"Y con lo caro que se ha puesto el precio del kilovatio_  
_y lo que gasta en entrenarlo, Endesa se está forrando._  
_GPU, GPU, la factura de la luz"_

El consumo energético: ésta es la cara B de todo el _boom_ del Deep Learning. El consumo de las GPU, o las unidades de procesamiento gráfico que se utilizan en redes neuronales es mucho más elevado que el de los procesadores normales. Se dice que [entrenar GPT-3 consumió tanto como conducir un coche de la tierra a la luna, y volver](https://www.theregister.com/2020/11/04/gpt3_carbon_footprint_estimate/).

_"Perrea con Ada Lovelace, lo baila Alan Turing,_  
_lo está bailando Hinton perreando a LeCun._  
_Perreamos tan a ritmo nos cargamos la ley de Moore"_

Ada Lovelace (1815-1852) se considera la primera programadora de la historia. Fue hija del poeta inglés Lord Byron, y de la también matemática y activista social Anna Isabella Byron. Fue educada, entre otras, por la matemática Mary Somerville. Tuvo una buena relación con Charles Babbage, a quien ayudó a diseñar el funcionamiento teórico de la "máquina diferencial", describiendo en sus "Notas" con un lenguaje muy técnico cómo funcionaría esta máquina, distinguiendo con claridad los conceptos de datos y procesamiento. Pero para más datos, este hilo es genial:

{{< tweet AUEmmyNoether 1340394678278119437 >}}

De [Alan Turing](https://es.wikipedia.org/wiki/Alan_Turing), poco se puede decir que no se haya dicho ya. Padre de la Inteligencia Artificial, descifró Enigma (la máquina de los Nazis) y fue condenado al ostracismo por su propio gobierno al descubrir su homosexualidad. Acabó suicidándose.

Por último, [Hinton y LeCun](https://www.zdnet.com/article/deep-learning-godfathers-bengio-hinton-and-lecun-say-the-field-can-fix-its-flaws/) son considerados "padres" de la explosión del deep learning.

Con esto, y un bizcocho... ¡A PERREAR, PERREAR LA INTELIGENCIA ARTIFICIAL!

Gracias a los que habéis llegado hasta aquí, y a los que habéis hecho posible esta canción, este hilo y esta alegría que llevo dentro desde [#cienciapasion2020](https://twitter.com/hashtag/cienciapasion2020?src=hashtag_click) !!!
